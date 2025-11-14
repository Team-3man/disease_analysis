# 🚑 연령·체중·수면·생활습관에 따른 주요 질병 발생 비율 분석

# 🎯 프로젝트 개요
현대인의 건강은 단순히 체중이나 운동 여부만으로 결정되지 않는다.  
**BMI(체질량지수), 신체활동, 수면시간, 음주·흡연 습관, 정신건강 등 다양한 요인이 복합적으로 작용**하며 질병의 발생 위험을 좌우한다.

하지만 실제로 어떤 요인이 어떤 질병과 가장 강하게 연결되는지,  
어떤 패턴이 존재하는지 직접적인 데이터 없이 파악하기는 어렵다.

본 프로젝트는 **Indicators of Heart Disease 2022 데이터**를 기반으로,  
다양한 생활요인들이 주요 질병에 어떤 영향을 미치는지 시각적으로 분석하는 것을 목표로 한다.

---

## 👨‍👨‍👦 팀원소개
- 김승주 : 우울장애·당뇨 등과 수면·정신건강지표·생활습관 요소 분석
- 이규식 : 심근경색·협심증·뇌졸중 등 심혈관계 질환과 연령·BMI·생활습관의 관계 분석
- 양희준 : 천식·COPD 중심으로 비만, 흡연, 활동량, 코로나 등과의 연관성 탐구

## 🛒 시장 조사
### ❤️ 심혈관 질환(CVD)의 문제 규모

심혈관 질환은 전 세계 사망 원인 1위이자 가장 부담이 큰 질환군이다.  
2023년 기준 CVD로 인한 손실 장애보정생존년(DALYs)은 **4억 3,700만 명-년**으로  
1990년(3억 2,000만) 대비 **약 1.4배 증가**했다.

- **2023년 CVD 사망자:** 약 **1,920만 명**
- **주요 원인 질환**
  - 허혈성 심질환: **약 891만 명**
  - 뇌졸중: **약 679만 명**
  
전 세계적으로 여전히 증가 추세이며, 의료·경제적 부담도 커지고 있다.

---

### 📈 심혈관 질환 증가의 주요 원인

심혈관 질환 부담의 **약 80%**는 수정 가능한 위험요인(modifiable risk factors)으로 설명된다.

### 주요 위험 요인
- **고혈압** (가장 큰 기여 요인)
- **비만 증가**
- **당뇨 및 고혈당**
- **고LDL 수치**
- **흡연·음주**
- **대기오염, 수면 부족, 스트레스**

### 증가 배경
- **고령화**로 위험군 인구 확대
- **비만·당뇨 증가**로 대사질환 기반 위험군 확대
- **신체활동 감소 및 좌식 생활 증가**
- **식습관 서구화·고열량 식사 패턴 확산**
- 만성질환 관리의 **지역·계층적 격차**


### 우울증 환자의 지속적인 증가
지난해 우울증으로 병원 진료를 받은 환자가 100만명을 넘은 것으로 나타났다. 특히 20대 여성 환자 비중이 가장 컸다.

국회 보건복지위원회 소속 남인순 더불어민주당 의원실이 국민건강보험공단에서 받은 ‘최근 5년간(2018∼2022년) 우울증 진료 인원 현황’을 3일 보면, 지난해 우울증 증상(질병코드 F32, F33)으로 병원을 찾은 이들은 100만744명이었다. 2018년 같은 증상으로 진료를 받은 환자 75만2976명과 비교하면 32.9% 증가한 수치다.

우울증 진료를 받은 환자는 2019년 79만911명, 2020년 83만2378명, 2021년 91만5298명 등 해마다 늘어 지난해 처음 100만 명을 넘어섰다.

출처 - https://www.hani.co.kr/arti/society/health/1110654.html
---

## 🧭 기대 효과
- 내가 어느 구간에 속할 때 어떤 질병 위험이 높아지는지”를 데이터로 명확하게 보여주는 것을 목표로 한다.
- 연령·BMI·수면·생활습관이 실제 질병으로 어떻게 연결되는지를 직관적으로 이해할 수 있다.
- 개인별로 어떤 요소를 우선 관리해야 하는지, 위험 요인의 우선순위를 설정하는 데 도움이 된다.

---

# 📊 데이터 소개
- 데이터 출처 :[Kaggle - 2022 Heart Disease](https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease)
- 데이터 구성 : 40개의 컬럼, 데이터 수 약 44만개

---

# 🔎 데이터 정보

### 1️⃣ 기본 인구통계 정보
- 주(State), 성별(Sex), 인종(RaceEthnicityCategory), 연령대(AgeCategory)

### 2️⃣ 신체 데이터
- 키(HeightInMeters), 체중(WeightInKilograms), BMI

### 3️⃣ 생활습관 관련 변수
- 수면시간(SleepHours)  
- 흡연상태(SmokerStatus), 전자담배(ECigaretteUsage)  
- 음주여부(AlcoholDrinkers)  
- 신체활동(PhysicalActivities)  

### 4️⃣ 건강상태 및 질환 정보
- 심근경색(HadHeartAttack)  
- 협심증(HadAngina)  
- 뇌졸중(HadStroke)  
- 천식(HadAsthma)  
- COPD(HadCOPD)  
- 우울장애(HadDepressiveDisorder)  
- 신장질환(HadKidneyDisease)  
- 당뇨병(HadDiabetes)
- 코로나(CovidPos)

### 5️⃣ 검사·예방접종 정보
- HIVTesting  
- FluVaxLast12  
- PneumoVaxEver  
- TetanusLast10Tdap  

### 6️⃣ 생활불편·정신건강 관련
- PhysicalHealthDays  
- MentalHealthDays  
- GeneralHealth  

---

## 🔍 본 프로젝트에서 주요하게 사용하는 핵심 변수

프로젝트 목적이 “생활습관 → 질병 비율/위험 패턴 분석”이므로  
40개 중 아래 변수만 핵심 분석 대상으로 사용

- **BMI(체중상태)**
- **Sex(성별)**
- **AgeCategory(연령대)**
- **SleepHours(수면시간)**
- **SmokerStatus(흡연여부)**
- **AlcoholDrinkers(음주여부)**
- **PhysicalActivities(운동 여부)**
- **8개 주요 질병 변숫값**
  - HadHeartAttack, HadAngina, HadStroke  
  - HadAsthma, HadCOPD  
  - HadDepressiveDisorder, HadKidneyDisease  
  - HadDiabetes
  - CovidPos

---

## 1. 데이터 수집 및 로드
| index | State   | Sex    | GeneralHealth | PhysicalHealthDays | MentalHealthDays | LastCheckupTime                                   | PhysicalActivities | SleepHours | HadHeartAttack | HeightInMeters | WeightInKilograms | BMI   | AlcoholDrinkers | HIVTesting | FluVaxLast12 | PneumoVaxEver | TetanusLast10Tdap                                         | HighRiskLastYear | CovidPos |
|------:|---------|--------|---------------|---------------------|------------------|----------------------------------------------------|--------------------|------------|----------------|----------------|--------------------|-------|------------------|------------|--------------|----------------|-------------------------------------------------------------|-------------------|----------|
| 0     | Alabama | Female | Very good     | 0.0                 | 0.0              | Within past year (less than 12 months)            | No                 | 8.0        | No             | NaN            | NaN                | NaN   | No               | No         | Yes          | No             | Yes, received tetanus shot but not sure what type          | No                | No       |
| 1     | Alabama | Female | Excellent     | 0.0                 | 0.0              | NaN                                                | No                 | 6.0        | No             | 1.60           | 68.04              | 26.57 | No               | No         | No           | No             | No, did not receive any tetanus shot in the past 10 years  | No                | No       |
| 2     | Alabama | Female | Very good     | 2.0                 | 3.0              | Within past year (less than 12 months)            | Yes                | 5.0        | No             | 1.57           | 63.50              | 25.61 | No               | No         | No           | No             | NaN                                                         | No                | Yes      |
| 3     | Alabama | Female | Excellent     | 0.0                 | 0.0              | Within past year (less than 12 months)            | Yes                | 7.0        | No             | 1.65           | 63.50              | 23.30 | No               | No         | Yes          | Yes            | No, did not receive any tetanus shot in the past 10 years  | No                | No       |
| 4     | Alabama | Female | Fair          | 2.0                 | 0.0              | Within past year (less than 12 months)            | Yes                | 9.0        | No             | 1.57           | 53.98              | 21.77 | Yes              | No         | No           | Yes            | No, did not receive any tetanus shot in the past 10 years  | No                | No       |


## 2. 데이터구조
### 수치형 데이터
| 통계값 | PhysicalHealthDays | MentalHealthDays | SleepHours | HeightInMeters | WeightInKilograms | BMI |
|--------|---------------------|-------------------|------------|----------------|-------------------|------|
| **count** | 434,205 | 436,065 | 439,679 | 416,480 | 403,054 | 396,326 |
| **mean**  | 4.35 | 4.38 | 7.02 | 1.7027 | 83.07 | 28.53 |
| **std**   | 8.69 | 8.39 | 1.50 | 0.1072 | 21.45 | 6.55 |
| **min**   | 0.00 | 0.00 | 1.00 | 0.91 | 22.68 | 12.02 |
| **25%**   | 0.00 | 0.00 | 6.00 | 1.63 | 68.04 | 24.13 |
| **50%**   | 0.00 | 0.00 | 7.00 | 1.70 | 80.74 | 27.44 |
| **75%**   | 3.00 | 5.00 | 8.00 | 1.78 | 95.25 | 31.75 |
| **max**   | 30.00 | 30.00 | 24.00 | 2.41 | 292.57 | 99.64 |

<details>
<summary>
<h3>범주형 데이터</h3>
</summary>

| Column                     | Count  | Unique | Top                                                         | Freq   |
|---------------------------|--------|--------|-------------------------------------------------------------|--------|
| State                     | 445132 | 54     | Washington                                                  | 26152  |
| Sex                       | 445132 | 2      | Female                                                      | 235893 |
| GeneralHealth             | 443934 | 5      | Very good                                                   | 148444 |
| LastCheckupTime           | 436824 | 4      | Within past year (anytime less than 12 months ago)         | 350944 |
| PhysicalActivities        | 444039 | 2      | Yes                                                         | 337559 |
| RemovedTeeth              | 433772 | 4      | None of them                                                | 233455 |
| HadHeartAttack            | 442067 | 2      | No                                                          | 416959 |
| HadAngina                 | 440727 | 2      | No                                                          | 414176 |
| HadStroke                 | 443575 | 2      | No                                                          | 424336 |
| HadAsthma                 | 443359 | 2      | No                                                          | 376665 |
| HadSkinCancer             | 441989 | 2      | No                                                          | 406504 |
| HadCOPD                   | 442913 | 2      | No                                                          | 407257 |
| HadDepressiveDisorder     | 442320 | 2      | No                                                          | 350910 |
| HadKidneyDisease          | 443206 | 2      | No                                                          | 422891 |
| HadArthritis              | 442499 | 2      | No                                                          | 291351 |
| HadDiabetes               | 444045 | 4      | No                                                          | 368722 |
| DeafOrHardOfHearing       | 424485 | 2      | No                                                          | 385539 |
| BlindOrVisionDifficulty   | 423568 | 2      | No                                                          | 399910 |
| DifficultyConcentrating   | 420892 | 2      | No                                                          | 370792 |
| DifficultyWalking         | 421120 | 2      | No                                                          | 353039 |
| DifficultyDressingBathing | 421217 | 2      | No                                                          | 404404 |
| DifficultyErrands         | 419476 | 2      | No                                                          | 387029 |
| SmokerStatus              | 409670 | 4      | Never smoked                                                | 245955 |
| ECigaretteUsage           | 409472 | 4      | Never used e-cigarettes in my entire life                   | 311988 |
| ChestScan                 | 389086 | 2      | No                                                          | 223221 |
| RaceEthnicityCategory     | 431075 | 5      | White only, Non-Hispanic                                    | 320421 |
| AgeCategory               | 436053 | 13     | Age 65 to 69                                                | 47099  |
| AlcoholDrinkers           | 398558 | 2      | Yes                                                         | 249919 |
| HIVTesting                | 379005 | 2      | No                                                          | 209256 |
| FluVaxLast12              | 398011 | 2      | Yes                                                         | 215604 |
| PneumoVaxEver             | 368092 | 4      | No                                                          | 121493 |
| TetanusLast10Tdap         | 362616 | 2      | No, did not receive any tetanus shot in the past 10 years   | 377324 |
| HighRiskLastYear          | 394509 | 2      | No                                                          | 270055 |
| CovidPos                  | 394368 | 3      | No                                                          | 270055 |
</details>




## ☝ 최종 인사이트




## 📘 프로젝트 후기

| 팀원 | 후기 |
|---------|-------|
| 이규식  | 프로젝트 전체 데이터 흐름을 이해하는 데 큰 도움이 되었고, 시각화 경험을 확실히 쌓을 수 있었습니다. <br> 다만 수치형 데이터가 많은 데이터셋을 다뤘으면 좀 더 깊이있게 해볼 수 있지 않았을까 ? ? 라는 약간의 아쉬움 |
| 양희준 | 11  |
| 김승주 | 데이터 자체가 관계성이 있는 데이터들이 아니라서 약간 아쉬웠습니다. 거의 다 범주형데이터여서 다양한 그래프를 써보지 못한것도 아쉬웠습니다. <br> 만약 다음 기회가 있다면 금융 돤련 데이터 해보고 싶어요. |


## 👨‍👩‍👦‍👦 프로젝트 참여자

### 프로젝트에 참여한 팀원들 ^ - ^

| 이름   | GitHub ID |
|--------|-----------|
| 이규식 | [holysik](https://github.com/holysik) |
| 양희준 | [HarryYang25](https://github.com/HarryYang25) |
| 김승주 | [burnslime](https://github.com/burnslime) |


