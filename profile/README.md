# 🏠 청년 버팀목 전세자금 대출 시뮬레이터 & AI 부동산 컨설턴트
> **"사회초년생을 위한 데이터 기반 전세 사기 예방 및 맞춤형 매물 추천 서비스"**

![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.42-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat&logo=mysql&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--3.5-412991?style=flat&logo=openai&logoColor=white)


<br>

### 🔗 서비스 배포 (Deployment)
* **Streamlit App:** [👉 배포된 웹사이트 링크 클릭](https://fisa-mini-realestate-fisa06-realestate-home-szt3l7.streamlit.app/)
* **GitHub Repository:** [👉 깃허브 리포지토리 바로가기](https://github.com/FISA-Mini-RealEstate/fisa06-realEstate)
* **시현영상** [👉 유튜브 시현영상 바로가기](https://youtu.be/nRr8XLMMfd8)
<br/>

---

## 📅 프로젝트 개요
* **프로젝트 기간:** 2026.01.22 ~ 2026.01.23
* **팀명:** 알고(Algo)리집
* **한 줄 소개:** 금융이 낯선 사회초년생을 위한 데이터 기반 전세 대출 가이드

<br/>

## **💡 팀원 소개**
| <img width="200" height="170" src="https://avatars.githubusercontent.com/u/123048615?v=4" width=90px alt="서지혜"/> | <img width="200" height="170" alt="심효진" src="https://avatars.githubusercontent.com/u/199601496?v=4" > | <img width="200" height="170" src="https://avatars.githubusercontent.com/u/114569746?v=4" width=90px alt="이남길"/>| <img width="200" height="170" alt="우민하" src="https://avatars.githubusercontent.com/u/181453012?v=4" > | 
|:---:|:---:|:---:|:---:|
| **서지혜** | **심효진** | **이남길** | **우민하** | 
| [@Jihye0623](https://github.com/jihye0623)  | [@hyojin-shj](https://github.com/hyojin-shj)  | [@SouthGiri](https://github.com/SouthGiri) | [@minha222](https://github.com/minha222) |
| • **AI**: `OpenAI API` <br/> • **Analysis**: `Plotly`  <br/> • **DB & Database**: `MySQL & Pandas` | • **DB**: `MySQL` <br/> • **Logic**: `Filtering & Mapping` <br/> • **Chart**: `Folium`  |  • **DB**: `MySQL` <br/> • **Logic**: `Loan Condition`, <br> `Monthly Payment` <br> • **Chart**: `Plotly Strip` |• **UI/UX**: `Main Page Layout` <br> • **Form**: `User Input` |

<br/>

## 📊 데이터 선정 및 분석 (Data & Insights)

### 1. 데이터 선정 배경 
전세 대출 상품과 금리에 익숙하지 않은 사회초년생이 본인의 경제 상황에 맞게 전세 대출 상품을 한눈에 비교할 수 있도록하여 의사결정을 지원하고자 합니다.
* **서울시 부동산 전월세가 정보**: 실제 전월세 거래 가격과 위치 정보를 담아, 시세 분석의 기준이 됨.
* **주택도시기금(HUG) 대출 상품 데이터:** '청년 버팀목 전세자금대출'의 정확한 금리와 한도 산출을 위해 선정.
* **은행연합회 전세자금대출 상품 데이터:** 시중 은행의 전세 자금 대출 상품의 금리와 월 부담금 정보 제공.

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
       * 지역별 시세 탐색: 평수 대비 보증금의 상관관계를 나타내는 추세선을 제공하여, 평균 시세보다 낮은 가격대가 형성된 지역을 시각적으로 파악하고 우선 순위 발품 후보지 선정을 위한 의사결정 지원.
       * 의사결정 지원: 월별 평단가 그래프가 우상향일 경우 '빠른 계약'을, 우하향일 경우 '관망'을 제안하는 데이터 기반 타이밍 가이드 제공.
<br/>

---

## 🛠️ 기술 스택 (Tech Stack)

| 구분 | 기술 | 활용 내용 |
| :--- | :--- | :--- |
| **Frontend** | ![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white) | Python 기반의 빠른 웹 대시보드 구현 및 인터랙티브 UI 구성 |
| **Backend** | ![Python](https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white) | 데이터 전처리(Pandas), 대출 한도 계산 로직 구현 |
| **Database** | ![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white) | 마포구 부동산 실거래가 데이터 적재 및 쿼리 |
| **AI / ML** | ![OpenAI](https://img.shields.io/badge/OpenAI-%23412991.svg?style=for-the-badge&logo=openai&logoColor=white) | 사용자 취향 분석 및 매물 비교 리포트 생성 (Prompt Engineering) |
| **Visualization** | ![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white) ![Folium](https://img.shields.io/badge/Folium-%2377B829.svg?style=for-the-badge&logo=folium&logoColor=white) | 동적 지도 시각화, 전세가율 위험도 그래프, 매물 가격 비교 차트 |
| **Collaboration** | ![Git](https://img.shields.io/badge/git-%23F05032.svg?style=for-the-badge&logo=git&logoColor=white) ![Notion](https://img.shields.io/badge/Notion-%23000000.svg?style=for-the-badge&logo=notion&logoColor=white) | 형상 관리 및 모듈화 협업 (Page 단위 분리 개발) |

<br/>

---

## 💡 주요 기능 (Key Features)

### 1️⃣ 좌표 기반 직관적 실거래가 시각화 (Page 1)

* **좌표 기반 실거래가 지도:**  
  주소 데이터를 위경도(`lat`, `lon`)로 변환하여 DB에 저장하고,  
  `Folium` 지도 위에 **실제 위치 기준 버블 매물**로 시각화합니다.
* **조건 기반 매물 필터링:**  
  사용자가 설정한 **보증금 한도, 면적, 거래 유형(전세)** 조건을 만족하는 매물만 선별하는  
  필터링 알고리즘을 구현하여 불필요한 매물 노출을 차단했습니다.
* **버블 지도 시각화:**  
  필터링을 통과한 매물만 지도에 버블 형태로 표시하여  
  사용자가 가격·입지 분포를 직관적으로 탐색할 수 있도록 설계했습니다.
<br/>

### 2️⃣ AI 부동산 컨설턴트 (Page 1)
* **맞춤형 매물 추천:** 사용자가 선호하는 분위기(예: "조용한 숲세권")를 입력하면 OpenAI API가 매물의 특징을 분석해 적합도를 판단합니다.
* **스마트 비교 리포트:** 선택한 두 매물의 **가격, 위치, 장단점**을 1:1로 비교하여 Markdown 형식의 깔끔한 리포트를 제공합니다.
<br/>

### 3️⃣ 전세 대출 시뮬레이터 (Page 2)
* **은행별 대출 한도 분석:** 사용자의 보유 예산과 희망하는 전세 보증금을 입력하면, 주요 시중 은행별로 제공 가능한 대출 한도와 금리 정보를 제공합니다.
* **Strip plot 시각화:** 은행별 대출 상품의 월 부담금 분포를 Strip plot으로 시각화하여, 은행의 월 부담금을 한눈에 비교할 수 있습니다.
<br/>

### 4️⃣ 전세 시장 심층 분석 (Page 3)

* **시세 트렌드**: 월별 평균 평단가 추이를 Line Chart로 시각화하고, 상승/하락 흐름에 대한 해석 가이드를 제공합니다.
* **동네별 가성비 비교**: 선택한 동네들의 평단가 분포를 Box Plot으로 비교해 가격 분산(바가지 위험)과 가성비를 판단할 수 있습니다.
* **숨은 꿀매물 탐색**: 평수-보증금 Scatter Plot에 평균 시세선을 추가하여, 시세선 하단의 상대적으로 저렴한 매물을 직관적으로 확인할 수 있습니다.

<br/>

---

## 📂 프로젝트 구조 (Directory Structure)
```
📂 FISA-realEstate 
 ┣ 📂 figure/              
 ┃ ┣ 🖼️ mapo.png
 ┃ ┗ 🖼️ woorifisa.png
 ┣ 📂 pages/              
 ┃ ┣ 📜 1_전세_지도_&_AI_컨설턴트.py
 ┃ ┗ 📜 2_대출_한도_계산하기.py
 ┃ ┗ 📜 3-전세_시장_심층_분석.py
 ┣ 📜 Home.py               
 ┣ 📜 sidebar.py           
 ┗ 📜 requirements.txt     
```


---


## 🚀 트러블 슈팅 (Troubleshooting)

서비스를 개발하며 겪은 주요 기술적 문제와 해결 과정입니다.

### 🔧 이슈 1: 대용량 공공데이터 처리 및 DB 적재 지연
* **문제 상황:** 50만 건 이상의 서울시 실거래가 CSV 데이터를 로드하고 MySQL에 적재하는 과정에서 메모리 부족 및 타임아웃 발생.
* **원인 분석:** 불필요한 행정 코드 컬럼까지 모두 로드되었으며, 한 번에 `Insert`를 시도하여 부하 발생.
* **해결 방법:**
    * 데이터 경량화: 프로젝트 타겟인 '마포구' 데이터만 필터링하고 분석에 불필요한 '지번코드', '접수년도' 등 21개 컬럼 중 13개를 제거하여, 메모리 사용량을 343.66MB에서 4.52MB로 약 98.7% 감소시켜 리소스 효율성 극대화.
    * 적재 효율화: 기존에 실패하던 DB 적재 작업을 15.94초 만에 완료하며 데이터 파이프라인 안정성 확보.
 
| 구분              | 원본 데이터 (Raw)                    | 변경 후 데이터 (Optimized)                                      | 개선 효과                         |
| --------------- | ------------------------------- | --------------------------------------------------------- | ----------------------------- |
| **컬럼 수**        | 23개                             | 13개                                                       | **10개 컬럼 제거 / 통합 (약 43% 감소)** |
| **데이터 행 수**     | 500,000+건                       | 600건                                                      | **99.8% 이상 축소**               |
| **데이터 적재 시간**   | 잦은 트러블슈팅 발생 (타입 불일치, Null 이슈 등) | 즉시 적재 가능                                                  | **적재 안정성 확보 및 반복 트러블 제거**     |
| **트러블슈팅 소요 시간** | 평균 10분 이상                      | 거의 0                                                      | **데이터 적재·정제 시간 대폭 단축**        |
| **주요 컬럼 구조**    | 접수연도, 자치구명, 건물명 등 중복 등       | district, dong, bldg_name, area, deposit, contract_date 등 | **직관적·분석 친화적 구조**             |


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
 
| 구분             | 기존 데이터 상태                         | 개선 후 데이터 상태                             | 개선 효과           |
| -------------- | --------------------------------- | --------------------------------------- | --------------- |
| **주소 컬럼 구조**   | 법정동, 지번, 본번, 부번 컬럼 분리 및 일부 결측     | 법정동 + 지번 + 본번 + 부번을 결합한 **단일 주소 컬럼 생성** | 지오코딩 입력 포맷 표준화  |
| **결측치 처리**     | 본번/부번 NaN 존재 → 정수 변환 시 에러 발생      | `pd.isna()` 기반 예외 처리, 결측치는 0으로 치환       | 주소 파싱 에러 제거     |
| **위경도 컬럼**     | lat, lon 다수 NULL                  | 위·경도 정상 매핑된 신규 컬럼 생성                    | 지도 시각화 가능       |
| **지오코딩 방식**    | 카카오 API / 스프레드시트 Geocoder (제한 초과) | Geopy(Nominatim) 기반 오픈소스 지오코딩           | 쿼리 제한 문제 해결     |
| **최종 데이터셋**    | 주소 문자열 중심                         | 주소 + 위도(lat) + 경도(lon) 포함               | 공간 분석 가능 데이터 확보 |


---

### 🎬 시현영상 

[![Video Label](http://img.youtube.com/vi/nRr8XLMMfd8/0.jpg)](https://youtu.be/nRr8XLMMfd8)
