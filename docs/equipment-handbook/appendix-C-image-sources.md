# 부록 C. 사진·영상·자료 출처 — 실물을 합법적으로 보는 방법

> **왜 이 문서가 필요한가**: 이 총서는 장비 사진 파일을 저장소에 포함하지 않습니다.
> 장비 사진은 대부분 장비사의 저작물이고, 무단 복제·재배포가 어렵습니다.
> 대신 **"어디에서 어떤 검색어로 보면 되는가"** 를 정리했습니다. 실무자들이 실제로 쓰는 경로 그대로입니다.

---

## C-0. 먼저 — 무엇을 봐야 공부가 되는가 (우선순위)

입문자가 장비 외관 사진을 100장 봐도 얻는 게 적습니다. 다음 순서로 보세요.

| 우선순위 | 볼 것 | 이유 |
|----------|-------|------|
| **1위** | **챔버 단면도 / 컷어웨이(cutaway) 도해** | 부품 배치와 흐름이 보임. 이 총서의 도해 + 특허 도면이 최고의 교재 |
| **2위** | **소모성 부품 실물 사진** (포커스 링, 샤워헤드, 타겟, 패드, 블레이드, 캐필러리) | 현장에서 매일 만지는 물건. 손에 잡히는 감각이 생김 |
| **3위** | **PM 작업 영상 / 부품 교체 영상** | 실제 업무 흐름 이해 |
| **4위** | **결함 SEM 이미지** (패턴 붕괴, 보잉, 디싱, 보이드, 칩핑) | 증상-원인 연결 학습에 직결 |
| 5위 | 장비 외관 사진 | 크기·풋프린트 감각 정도 |

---

## C-1. 최고의 무료 자료 — 특허 도면

**실무자들이 장비 내부 구조를 공부할 때 가장 많이 쓰는 방법입니다.** 무료이고, 합법이며, 도면이 정확합니다.

| 사이트 | 사용법 |
|--------|--------|
| **Google Patents** (patents.google.com) | `assignee:"Applied Materials" showerhead` / `assignee:"Lam Research" edge ring` / `assignee:"ASML" immersion hood` 처럼 **양수인(회사) + 부품명**으로 검색 |
| **KIPRIS** (한국특허정보원) | 한국어 검색. 국내 출원 장비 특허 |
| **USPTO / Espacenet** | 미국·유럽 원문 |

**추천 검색 조합 예시**

```
 assignee:"Applied Materials" AND (showerhead OR "process kit" OR "electrostatic chuck")
 assignee:"Lam Research"     AND ("edge ring" OR "focus ring" OR "plasma etch chamber")
 assignee:"Tokyo Electron"   AND (coater OR developer OR "substrate processing")
 assignee:"ASML"             AND ("immersion" OR "EUV source" OR "wafer stage")
 assignee:"Ebara"            AND ("polishing" OR "dry pump")
 assignee:"DISCO"            AND (dicing OR grinding)
 assignee:"BESI" OR assignee:"ASM Pacific" AND ("hybrid bonding" OR "die bonding")
```

> **팁**: 특허의 "도면 설명(Brief Description of Drawings)" 부분을 읽으면 각 부품 번호가 무엇인지 나옵니다.
> 챔버 도면 + 부품 번호 설명 = 사실상 장비 교재입니다.

---

## C-2. 장비사 공식 사이트 (제품 페이지·뉴스룸)

각 사 공식 페이지에는 제품 외관 사진, 일부 구조 설명, 기술 백서가 공개되어 있습니다.
**열람은 자유롭지만, 이미지 재배포는 각 사 정책을 따라야 합니다.**

| 회사 | 도메인 | 볼 것 |
|------|--------|-------|
| ASML | asml.com | EUV·DUV 시스템 페이지, 기술 설명 영상("How does EUV work" 류), 연례 리포트 |
| Applied Materials | appliedmaterials.com | 제품 카탈로그(식각/증착/PVD/CMP/임플란트), 블로그 |
| Lam Research | lamresearch.com | 식각·증착·도금 제품, **교육 콘텐츠가 비교적 풍부** |
| Tokyo Electron | tel.com | 트랙·식각·세정·프로버, 기술 소개 페이지 |
| KLA | kla.com | 검사·계측 원리 설명 자료 |
| ASM International | asm.com | ALD 기술 설명 |
| Ebara | ebara.com | CMP·드라이 펌프 |
| DISCO | disco.co.jp | 다이싱·그라인딩, **소모품(블레이드/휠) 카탈로그가 매우 유용** |
| EV Group | evgroup.com | 웨이퍼 본딩·하이브리드 본딩 |
| SUSS MicroTec | suss.com | 본딩·코팅·노광 |
| Advantest / Teradyne | advantest.com / teradyne.com | 테스터·핸들러 |
| Axcelis | axcelis.com | 이온주입 |
| Edwards Vacuum | edwardsvacuum.com | **진공 펌프 원리 설명 자료가 교육용으로 좋음** |
| MKS Instruments | mks.com | MFC·게이지·RF 전원. **"기술 노트"가 기초 학습에 훌륭함** |

> **특히 추천**: MKS와 Edwards의 기술 자료는 진공·유량·압력·RF 기초를 **교과서 수준으로 무료 공개**합니다.
> [0-2장](00-2-vacuum.md), [0-3장](00-3-gas-and-fluids.md)을 보강하려면 여기부터 보세요.

---

## C-3. 자유롭게 쓸 수 있는 이미지 (라이선스 확인 필수)

| 소스 | 특징 | 주의 |
|------|------|------|
| **Wikimedia Commons** (commons.wikimedia.org) | CC 라이선스 이미지. `semiconductor`, `cleanroom`, `wafer`, `sputtering`, `Czochralski` 등 검색 | 라이선스 종류(CC-BY, CC0 등)와 저작자 표기 요구 확인 |
| **Wikipedia 문서 내 도해** | 원리 도해가 잘 정리된 경우가 많음 | 상동 |
| **각국 연구기관 공개자료** (NIST, Sandia, imec 등) | 공정·장비 도해 | 기관별 이용 조건 확인 |
| **대학 강의자료(공개)** | 예: 반도체 공정 강의 슬라이드 | 재배포 조건 확인 |
| **논문 도면** | 원리 도식이 정확 | 저널 저작권. 개인 학습용 열람만 |

---

## C-4. 영상 — 원리 이해에 가장 빠른 매체

| 종류 | 검색어 예 | 비고 |
|------|-----------|------|
| **EUV 원리** | `ASML EUV how it works`, `EUV light source tin droplet` | 공식 채널 애니메이션이 매우 좋음 |
| **팹 투어** | `semiconductor fab tour cleanroom`, `300mm fab OHT` | 반송·클린룸 감각 |
| **플라즈마 식각** | `plasma etching explained`, `reactive ion etching animation` | |
| **CMP** | `chemical mechanical polishing CMP how it works` | |
| **와이어 본딩** | `wire bonding process slow motion`, `ball bonding capillary` | 고속 카메라 영상이 인상적 |
| **다이싱** | `wafer dicing saw`, `stealth dicing process` | |
| **하이브리드 본딩** | `hybrid bonding wafer to wafer animation` | |
| **진공 펌프** | `turbomolecular pump how it works`, `cryopump regeneration` | |
| **CZ 성장** | `silicon ingot growth Czochralski timelapse` | 결정이 자라는 장면 |

> 공식 채널(장비사·학회·연구기관)과 교육 채널을 우선하세요. 개인 채널은 부정확한 설명이 섞일 수 있습니다.

---

## C-5. 학회·기술 문헌 (가장 정확한 기술 정보)

| 소스 | 내용 |
|------|------|
| **SPIE Advanced Lithography** | 리소·EUV·마스크·계측의 1차 자료. 초록은 무료로 읽히는 경우가 많음 |
| **IEEE IEDM / VLSI Symposium** | 소자·공정 최신 결과 |
| **IEEE ECTC / IMAPS** | **패키징 장비·기술의 핵심 학회** |
| **ALD/ALE Conference** | ALD·ALE 전문 |
| **SEMICON (Korea/West/Taiwan 등) 발표자료** | 장비·시장·기술 동향, 비교적 접근 용이 |
| **AVS (진공학회)** | 진공·플라즈마 기초 |
| **SEMI 표준 문서** | E10(가동률), E30(GEM), E84, S2/S8(안전) 등. 요약은 SEMI 사이트에서 확인 |
| **arXiv (cond-mat 등)** | 일부 공정·플라즈마 시뮬레이션 논문 무료 |

---

## C-6. 교과서 (한 권씩 붙잡을 만한 것)

| 주제 | 성격 |
|------|------|
| 반도체 공정 개론 | Campbell, *Fabrication Engineering at the Micro- and Nanoscale* / Quirk & Serda, *Semiconductor Manufacturing Technology* — 장비 서술이 비교적 친절 |
| 플라즈마 | Lieberman & Lichtenberg, *Principles of Plasma Discharges and Materials Processing* — 플라즈마 장비의 정석(난이도 높음) |
| 진공 기술 | 진공공학 개론서 또는 Edwards/MKS 기술 자료 |
| 리소그래피 | Mack, *Fundamental Principles of Optical Lithography* |
| CMP | CMP 전문 단행본(핸드북류) |
| ALD | ALD 리뷰 논문(Chemical Reviews 등)이 교과서보다 최신 |
| 패키징 | Tummala, *Fundamentals of Microsystems Packaging* / ECTC 튜토리얼 자료 |

---

## C-7. 장별 검색어 인덱스 (복사해서 쓰세요)

### Part 0 공통 기초
```
turbomolecular pump cutaway / cryopump cross section / dry pump multistage roots
capacitance manometer diaphragm gauge / Bayard-Alpert ion gauge / RGA spectrum leak
slit valve semiconductor / pendulum throttle valve APC / ConFlat copper gasket
mass flow controller thermal cutaway / gas box gas stick VCR
showerhead CVD dual channel / clogged showerhead
precursor ampoule ALD bubbler / solid precursor sublimation / DLI vaporizer
capacitively coupled plasma reactor / inductively coupled plasma TCP coil
RF matching network variable capacitor / plasma sheath ion energy
electrostatic chuck cross section / helium backside cooling wafer
multi zone heater chuck / lift pin / edge ring erosion
FOUP 300mm / OHT overhead hoist transport / EFEM SCARA robot
vacuum transfer chamber frog leg robot / wafer aligner notch
FFU laminar flow cleanroom / ionizer wafer ESD
FDC trace semiconductor / run to run EWMA / chamber matching
yttria coating plasma resistant parts / thermal spray Y2O3
```

### Part 1 전공정
```
Czochralski crystal puller / hot zone / MCZ magnetic field / Dash necking
multi wire saw diamond wire / double side polishing wafer carrier
epitaxial reactor susceptor lamp heated / float zone RF coil
vertical furnace quartz tube boat elevator / LPCVD injector nozzle
RTP lamp array pyrometer / spike anneal profile / flash lamp anneal / laser spike anneal
EUV lithography scanner cutaway / EUV LPP tin droplet CO2 laser / EUV collector mirror
Mo/Si multilayer mirror / EUV reflective mask TaBN / EUV pellicle
immersion lithography water hood / immersion bubble watermark defect
coater developer track module stack / spin coating dispense nozzle / hot plate chill plate
SADP spacer double patterning / OPC mask / Bossung curve focus exposure matrix
resist pattern collapse SEM / T-top resist / standing wave BARC
CCP dielectric etch chamber / ICP conductor etch chamber
focus ring edge ring consumable / high aspect ratio etch 3D NAND SEM
bowing twisting HAR / atomic layer etching cycle / cryogenic etch
downstream asher remote plasma / bevel edge etch
PECVD showerhead susceptor / multi station PECVD / HDP-CVD gap fill / flowable CVD
ALD cycle purge schematic / spatial ALD rotary / batch ALD furnace
low-k SiCOH UV cure / film stress wafer bow
magnetron sputtering rotating magnet / sputter target erosion nodules
IMP PVD / HiPIMS / collimator PVD / PVD cluster degas preclean
electroplating ECP contact ring anode / bottom up superfill additives
dual damascene copper flow / tungsten CVD volcano defect / ALD tungsten low fluorine
NiSi salicide RTA / TaN barrier ALD copper / molybdenum word line precursor
ion implanter beamline analyzer magnet / Bernas IHC ion source
electrostatic scanner parallelizing lens / Faraday cup dose / plasma flood gun
energy contamination decel / ion channeling tilt twist / plasma doping PLAD
CMP polisher platen carrier head / multi zone carrier head membrane
CMP pad grooves / conditioner diamond disk / retaining ring wear
copper CMP dishing erosion SEM / eddy current endpoint CMP / post CMP PVA brush
single wafer spin cleaner nozzle arm / wet bench chemical tanks
megasonic cleaning pattern damage / pattern collapse capillary SEM
supercritical CO2 drying semiconductor / Marangoni IPA drying / vapor HF COR
spectroscopic ellipsometer / OCD scatterometry / CD-SEM measurement
diffraction based overlay target / bright dark field wafer inspection
e-beam inspection voltage contrast / review SEM EDX defect / wafer defect map signature
wafer prober probe card MEMS / ATE test head wafer sort
```

### Part 2 후공정
```
wafer backgrinding infeed spindle / stress relief die strength
blade dicing saw / stealth dicing laser modified layer / plasma dicing
die bonder ejector pin DAF / wire bonder capillary ball bond ultrasonic
wire sweep molding defect / thermocompression bonding TCB HBM stacking
TC-NCF non conductive film / MR-MUF molded underfill
hybrid bonding copper to copper wafer to wafer / hybrid bonding die to wafer
TSV etch plating CMP / temporary bonding debonding laser carrier
transfer molding compression molding package / solder ball mount reflow profile
fan out wafer level packaging RDL / panel level packaging die shift
X-ray inspection solder void AXI / scanning acoustic tomography delamination
test handler socket / burn in board
```

---

## C-8. 저작권·활용 가이드 (실무에서 중요)

| 상황 | 권장 |
|------|------|
| 개인 학습용으로 사진을 보고 이해 | 자유 |
| 사내 교육자료에 장비사 사진 사용 | **출처 표기 + 가능하면 장비사 허가 확인**. 장비사는 협력 고객에게 자료를 제공하는 경우가 많으니 **정식으로 요청**하는 것이 가장 안전 |
| 블로그·논문·발표에 사진 사용 | 라이선스 확인(Wikimedia CC 등) 또는 직접 그린 도해 사용 |
| 공개 저장소(GitHub 등)에 이미지 포함 | **권리 확인된 것만.** 불확실하면 도해로 대체 (이 총서의 방식) |
| 사내 장비 실물 촬영 | **대부분의 팹에서 금지**(보안). 반드시 사내 규정 확인 |

> 마지막 조언: 현장에 들어가면 **실물이 최고의 교재**입니다. PM에 입회할 기회가 생기면
> 교체되는 부품을 직접 손에 들고, 마모 흔적을 보고, 사수에게 "이게 왜 이렇게 닳았나요?"를 물어보세요.
> 이 총서의 모든 내용이 그 순간에 연결됩니다.

> 다음: [부록 D. 트러블슈팅 치트시트](appendix-D-troubleshooting.md)
</content>
