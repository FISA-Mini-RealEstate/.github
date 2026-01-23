# 🏠 청년 버팀목 전세자금 대출 시뮬레이터 & AI 부동산 컨설턴트
> **"사회초년생을 위한 데이터 기반 전세 사기 예방 및 맞춤형 매물 추천 서비스"**

![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=flat&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.42-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat&logo=mysql&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--3.5-412991?style=flat&logo=openai&logoColor=white)


<br>

### 🔗 서비스 배포 (Deployment)
* **Streamlit App:** [👉 배포된 웹사이트 링크 클릭]( 여기에_배포_URL_입력 )
* **GitHub Repository:** [👉 깃허브 리포지토리 바로가기](https://github.com/FISA-Mini-RealEstate/fisa06-streamlit)
<br/>

---

## 📅 프로젝트 개요
* **프로젝트 기간:** 2026.01.22 ~ 2026.01.23
* **팀명:** 알고(Algo)리집
* **한 줄 소개:** 복잡한 전세 대출 한도를 자동 계산하고, 사용자의 취향과 안전성을 고려한 매물을 AI가 추천해주는 원스톱 서비스입니다.

<br/>

## **💡 팀원 소개**
| <img width="200" height="170" src="https://avatars.githubusercontent.com/u/123048615?v=4" width=90px alt="서지혜"/> | <img width="200" height="170" alt="심효진" src="https://avatars.githubusercontent.com/u/199601496?v=4" > | <img width="200" height="170" src="https://avatars.githubusercontent.com/u/114569746?v=4" width=90px alt="이남길"/>| <img width="200" height="170" alt="우민하" src="https://avatars.githubusercontent.com/u/181453012?v=4" > | 
|:---:|:---:|:---:|:---:|
| **서지혜** | **심효진** | **이남길** | **우민하** | 
| [@Jihye0623](https://github.com/jihye0623)  | [@hyojin-shj](https://github.com/hyojin-shj)  | [@SouthGiri](https://github.com/SouthGiri) | [@minha222](https://github.com/minha222) |
| • **AI**: `OpenAI API` <br/> • **Analysis**: `Plotly`  <br/> **DB**: `MySQL` | • **Visualization**: `Folium Map` <br> • **UI**: `Price Filter Bar`|  • **Analytics**: `Monthly Payment` <br> **Chart**: `Boxplot` |• **UI/UX**: `Main Page Layout` <br> • **Form**: `User Input` |

<br/>

## 📊 데이터 선정 및 분석 (Data & Insights)

<img width="628" height="480" alt="image" src="https://github.com/user-attachments/assets/0475cf43-60c8-49e8-adea-3f4643d9edda" />

### 1. 데이터 선정 배경 
본 프로젝트는 사회초년생의 주거 불안 해소를 목표로 하며, 신뢰성 확보를 위해 공공 데이터와 실제 금융 데이터를 융합했습니다.
* **서울시 부동산 전월세가 정보**: 실제 전월세 거래 가격과 위치 정보를 담아, 시세 분석의 기준이 됨.
* **주택도시기금(HUG) 대출 상품 데이터:** '청년 버팀목 전세자금대출'의 정확한 금리와 한도 산출을 위해 선정.

### 2. 분석 기준 및 도출 인사이트
* **분석 기준:**
    * 표준화 지표 도입: 실제 사용자가 가장 민감하게 인지하는 전세 보증금(deposit) 값을 기준으로 수행함.
    * 데이터 정제: 주소 기반 지오코딩 정확도를 확보하기 위해 본번·부번 정보가 누락된 주소 데이터는 분석 대상에서 제외하고,실제 위치 매핑이 가능한 매물만 활용함.
* **인사이트 (Insights):**
    * 📈 **분석 결과:**
       * 지역별 가격 편차: 보증금 기준으로 매물을 시각화한 결과, 고가 매물이 밀집된 지역과 상대적으로 저렴한 매물이 분포한 지역이 지도 상에서 확인 가능.
       * 후보 매물의 비교: 필터링을 통해 선택된 매물들에 대해 보증금 분포, 요약 통계를 제공하여 개별 매물의 수준 판단 가능.
    * 💡 **솔루션:**
       * AI 기반 맞춤 매물 추천: 지도 및 매트릭스 분석을 통해 압축된 후보 매물 중에서 사용자의 선호 조건을 입력받아 OpenAI API 기반 분석으로 적합한 매물 추천.
       * 가성비 탐지: 사용자가 일일이 계산할 필요 없이, 산점도의 평균 시세 추세선보다 아래에 위치한 점(매물)을 시각적으로 하이라이팅하여 '꿀매물'로 즉시 제안.
       * 의사결정 지원: 월별 평단가 그래프가 우상향일 경우 '빠른 계약'을, 우하향일 경우 '관망'을 제안하는 데이터 기반 타이밍 가이드 제공.
<br/>

---

## 🛠️ 기술 스택 (Tech Stack)

| 구분 | 기술 | 활용 내용 |
| :--- | :--- | :--- |
| **Frontend** | ![Streamlit](https://img.shields.io/badge/-Streamlit-FF4B4B) | Python 기반의 빠른 웹 대시보드 구현 및 인터랙티브 UI 구성 |
| **Backend** | ![Python](https://img.shields.io/badge/-Python-3776AB) | 데이터 전처리(Pandas), 대출 한도 계산 로직 구현 |
| **Database** | ![MySQL](https://img.shields.io/badge/-MySQL-4479A1) | 서울시 부동산 실거래가 데이터(약 2.7만 건) 적재 및 쿼리 |
| **AI / ML** | ![OpenAI](https://img.shields.io/badge/-OpenAI-412991) | 사용자 취향 분석 및 매물 비교 리포트 생성 (Prompt Engineering) |
| **Visualization** | Plotly, Folium | 동적 지도 시각화, 전세가율 위험도 그래프, 매물 가격 비교 차트 |
| **Collaboration** | Git, Notion | 형상 관리 및 모듈화 협업 (Page 단위 분리 개발) |

<br/>

---

## 💡 주요 기능 (Key Features)

### 1️⃣ AI 부동산 컨설턴트 (Page 1)

* **좌표 기반 실거래가 지도:**  
  주소 데이터를 위경도(`lat`, `lon`)로 변환하여 DB에 저장하고,  
  `Folium` 지도 위에 **실제 위치 기준 버블 매물**로 시각화합니다.
* **조건 기반 매물 필터링:**  
  사용자가 설정한 **보증금 한도, 면적, 거래 유형(전세)** 조건을 만족하는 매물만 선별하는  
  필터링 알고리즘을 구현하여 불필요한 매물 노출을 차단했습니다.
* **버블 지도 시각화:**  
  필터링을 통과한 매물만 지도에 버블 형태로 표시하여  
  사용자가 가격·입지 분포를 직관적으로 탐색할 수 있도록 설계했습니다.

### 2️⃣ AI 부동산 컨설턴트 (Page 1)
* **맞춤형 매물 추천:** 사용자가 선호하는 분위기(예: "조용한 숲세권")를 입력하면 OpenAI API가 매물의 특징을 분석해 적합도를 판단합니다.
* **스마트 비교 리포트:** 선택한 두 매물의 **가격, 위치, 장단점**을 1:1로 비교하여 Markdown 형식의 깔끔한 리포트를 제공합니다.
<br/>

### 3️⃣ 전세 대출 시뮬레이터 (Page 2)
* **은행별 대출 한도 분석:** 사용자가 희망하는 전세 보증금을 입력하면, 주요 시중 은행별로 제공 가능한 대출 한도의 범위(최소~최대)를 시뮬레이션합니다.
* **Boxplot 시각화:** 은행마다 상이한 대출 한도 분포를 Boxplot(상자 그림)으로 시각화하여, 어떤 은행이 가장 넉넉한 한도를 제공하는지 혹은 조건이 까다로운지 한눈에 비교할 수 있습니다.
<br/>

---

## 📂 프로젝트 구조 (Directory Structure)
```
.
├── 📄 app.py                  # 메인 애플리케이션 (네비게이션 역할)
├── 📂 pages        
│   ├── 📄 1-pages1.py         # [Page 1] 부동산 탐색 & AI 추천
│   └── 📄 2-pages2.py         # [Page 2] 대출 계산기
├── 📄 .env                    # API Key 보안 관리
└── 📄 requirements.txt        # 의존성 라이브러리 목록
```


---


## 🚀 트러블 슈팅 (Troubleshooting)

서비스를 개발하며 겪은 주요 기술적 문제와 해결 과정입니다.

### 🔧 이슈 1: 대용량 공공데이터 처리 및 DB 적재 지연
* **문제 상황:** 50만 건 이상의 서울시 실거래가 CSV 데이터를 로드하고 MySQL에 적재하는 과정에서 메모리 부족 및 타임아웃 발생.
* **원인 분석:** 불필요한 행정 코드 컬럼까지 모두 로드되었으며, 한 번에 `Insert`를 시도하여 부하 발생.
* **해결 방법:**
    * Pandas를 사용해 프로젝트 타겟 지역인 '마포구' 데이터만 필터링하고, 분석에 불필요한 컬럼(접수년도, 지번코드 등)을 제거.

### 🔧 이슈 2: 지오코딩 툴 한계 극복 및 결측치 처리
* **문제 상황:**
   * 판다스로 카카오 API를 연동해 주소를 위경도로 변형하여 DB에 적재하려 하였으나 계속되는 통신 에러로 실패.
   * 차선책으로 스프레드시트 Geocoder 툴을(위경도변환 지원) 사용하려 했으나 무료 변환 한도 초과로 작업 실패.
   * 데이터셋 중 주소지 본번/부번 데이터 결측치로 에러 발생
* **원인 분석**
   * 무료 툴의 일일 쿼리 제한 및 유료 API의 인증 복잡성으로 인해 시간내 해결 불가능.
   * 데이터셋에 bonbun(본번)이나 bubun(부번)이 NaN인 행이 있어 정수 변환 시 에러 발생.
* **해결 방법:**
   * 기술 스택 변경: 오픈소스 라이브러리인 Geopy (Nominatim) 채택.
   * pd.isna()를 사용하여 결측치가 있는 주소는 0으로 건너뛰도록 예외 처리 구현.


---

  
