# 반도체 R&D 기술 동향 분석 자동화 파이프라인

## Overview

- **Objective** : 반도체 핵심 기술 도메인(HBM/DRAM, 파운드리 공정, AI 가속기, 전력반도체 등)에 대한 경쟁사 기술 성숙도 및 R&D 동향을 자동 분석하고, 전략 보고서(PDF)를 생성하는 멀티 에이전트 파이프라인
- **Method** : LangGraph Supervisor 패턴 기반 멀티 에이전트 협업 — 웹 검색 → RAG 검색 → 기술 분석 → 보고서 작성 → PDF 포매팅 순서로 자동 순환 실행
- **Tools** : LangGraph, LangChain, ChromaDB, HuggingFace (BAAI/bge-m3), OpenAI GPT-4o, Tavily Search, ReportLab

## Features

- **PDF 자료 기반 RAG** : `data/manual_reports/` 에 업로드한 arXiv 논문 및 ETRI/KISTEP 동향보고서를 자동 분류·청킹하여 ChromaDB 벡터 DB 구축
- **도메인 인식 경쟁사 선정** : 쿼리 기술 도메인에 따라 경쟁사를 자동 분류 (메모리 → Samsung/Micron, 파운드리 → TSMC/Intel Foundry/Rapidus 등)
- **TRL 기반 기술 성숙도 분석** : 특허 출원 패턴·학회 발표 빈도·채용공고 키워드 등 간접 지표를 근거로 TRL 1–9 추정, 한계(불확실성) 명시
- **구조화된 5섹션 보고서 자동 생성** : Executive Summary / R&D 동향 / 경쟁사 위협 분석 / 전략적 대응 / Reference
- **확증 편향 방지 전략** : 웹 검색 시 긍정(Pros)/부정(Cons) 다면 검색 강제 적용, TRL 추정 근거의 한계 고지 박스를 보고서에 고정 출력
- **한글 PDF 생성** : ReportLab + NanumGothic 폰트 기반으로 한글 표·수식 정상 렌더링

## Tech Stack

| Category | Details |
|----------|---------|
| Framework | LangGraph, LangChain, Python 3.11 |
| LLM | GPT-4o via OpenAI API |
| Retrieval | ChromaDB (Hit Rate@K, MRR) |
| Embedding | BAAI/bge-m3 (HuggingFace, 로컬 실행) |
| Web Search | Tavily Search API |
| PDF 생성 | ReportLab + NanumGothic TTF |
| 패키지 관리 | uv (pyproject.toml) |

## Agents

| Agent | 역할 |
|-------|------|
| **Supervisor** | 작업 흐름 관리, 각 에이전트 순차 라우팅 (Star 구조) |
| **Web Search Agent** | Tavily로 최신 시장 동향·특허·뉴스 수집, Pros/Cons 다면 검색 |
| **RAG Agent** | ChromaDB에서 관련 논문·보고서 검색, Hit Rate@K·MRR 측정 |
| **Tech Analyst Agent** | 도메인 인식 경쟁사 선정 + TRL 기반 기술 성숙도 분석 |
| **Report Writer Agent** | 5섹션 구조화 보고서 생성, LLM 기반 제목 자동 생성 |
| **Formatting Node** | 마크다운 → ReportLab PDF 변환, 날짜 기반 파일명 저장 |

## Architecture

```
START
  │
  ▼
Supervisor ──→ Web Search Agent ──┐
  ▲                               │
  │◄──────────────────────────────┘
  │
  ├──→ RAG Agent ──────────────────┐
  ▲                                │
  │◄───────────────────────────────┘
  │
  ├──→ Tech Analyst Agent ─────────┐
  ▲                                │
  │◄───────────────────────────────┘
  │
  ├──→ Report Writer Agent ────────┐
  ▲                                │
  │◄───────────────────────────────┘
  │
  └──→ Formatting Node ──→ END (PDF 저장)
```

## Directory Structure

```
.
├── agent.ipynb              # 메인 멀티 에이전트 파이프라인
├── data.ipynb               # RAG 데이터 준비 (PDF 청킹 → ChromaDB 구축)
├── pyproject.toml           # 의존성 관리 (uv)
├── uv.lock                  # 재현 가능한 패키지 버전 고정
├── font/                    # NanumGothic TTF (한글 PDF 렌더링용)
├── data/
│   └── manual_reports/      # 수동 업로드 PDF (arXiv 논문 + 동향보고서) ← git 제외
└── chroma_db/               # ChromaDB 벡터 DB (data.ipynb 실행 시 자동 생성) ← git 제외
```

## Getting Started

```bash
# 1. 패키지 설치
uv sync

# 2. 환경변수 설정
cp .env.example .env
# .env 에 OPENAI_API_KEY, TAVILY_API_KEY 입력

# 3. PDF 업로드
# data/manual_reports/ 폴더에 분석할 PDF 파일 추가 (arXiv 논문, 산업 보고서 등)

# 4. 벡터 DB 구축  →  data.ipynb 순서대로 실행
#    Cell 0 (환경설정) → Cell 6 (인벤토리 확인) → Cell 8 (함수 정의) → Cell 9 (ChromaDB 재구축)

# 5. 분석 실행  →  agent.ipynb 순서대로 실행
#    마지막 셀에서 분석 쿼리 선택 후 실행 → semiconductor_analysis_YYYYMMDD.pdf 생성
```

## Contributors

- 김가은 : Workflow 정의, RAG Agent, Supervisor, agent 통합
- 송윤아 : VectorDB 구축, WebSearch Agent
- 채희지 : Tech Analyst agent, Report Writer Agent
