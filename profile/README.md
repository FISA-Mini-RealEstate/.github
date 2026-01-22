# 🏠 청년 버팀목 전세자금 대출 시뮬레이터 & AI 부동산 컨설턴트
> **"사회초년생을 위한 데이터 기반 전세 사기 예방 및 맞춤형 매물 추천 서비스"**

![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=flat&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.42-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat&logo=mysql&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--3.5-412991?style=flat&logo=openai&logoColor=white)

<br/>

---

## 📅 프로젝트 개요
* **프로젝트 기간:** 2026.01.22 ~ 2026.01.23
* **팀명:** 알고(Algo)리집
* **한 줄 소개:** 복잡한 전세 대출 한도를 자동 계산하고, 사용자의 취향과 안전성을 고려한 매물을 AI가 추천해주는 원스톱 서비스입니다.

<br/>

## **💡 팀원 소개**
| <img width="170" height="170" src="https://avatars.githubusercontent.com/u/123048615?v=4" width=90px alt="서지혜"/> | <img width="170" height="170" alt="심효진" src="https://avatars.githubusercontent.com/u/199601496?v=4" > | <img width="170" height="170" src="https://avatars.githubusercontent.com/u/114569746?v=4" width=90px alt="이남길"/>| <img width="170" height="170" alt="우민하" src="https://avatars.githubusercontent.com/u/181453012?v=4" > | 
|:---:|:---:|:---:|:---:|
| **서지혜** | **심효진** | **이남길** | **우민하** | 
| [@Jihye0623](https://github.com/jihye0623)  | [@hyojin-shj](https://github.com/hyojin-shj)  | [@SouthGiri](https://github.com/SouthGiri) | [@minha222](https://github.com/minha222) |
| • **DB**: `MySQL` <br> • **AI**: `OpenAI API` | • **Visualization**: `Folium Map` <br> • **UI**: `Price Filter Bar`|  • **Analytics**: `Monthly Payment` <br> **Chart**: `Boxplot` |• **UI/UX**: `Main Page Layout` <br> • **Form**: `User Input` |

<br/>

### ❓ 기획 의도 (Background)
사회초년생들은 전세 계약 시 **'내 대출 한도가 얼마인지'**, **'이 동네가 나와 적합한지'** 판단하기 어렵습니다.
우리는 공공데이터(실거래가)와 금융 데이터(대출 금리)를 결합하여, **가장 안전하고 합리적인 전세집**을 구할 수 있도록 돕고자 합니다.

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
* **맞춤형 매물 추천:** 사용자가 선호하는 분위기(예: "조용한 숲세권")를 입력하면 OpenAI API가 매물의 특징을 분석해 적합도를 판단합니다.
* **스마트 비교 리포트:** 선택한 두 매물의 **가격, 위치, 장단점**을 1:1로 비교하여 Markdown 형식의 깔끔한 리포트를 제공합니다.
* **실거래가 지도:** `Folium`을 활용해 마포구 내 실제 거래된 매물을 지도 위에 시각화하고, 클릭 시 상세 정보를 제공합니다.
<br/>

### 2️⃣ 전세 대출 시뮬레이터 (Page 2)
* **대출 한도 계산:** 사용자의 연소득, 보증금, 부채 상태를 입력하면 **'청년 버팀목 전세자금대출'** 가능 여부와 예상 한도를 계산합니다.
* **월 지출 비교:** `전세 이자 vs 월세` 비교 차트를 통해 매달 얼마를 절약할 수 있는지 시각적으로 보여줍니다. (Plotly Bar Chart)
<br/>

---

## 📂 프로젝트 구조 (Directory Structure)
```bash
.
├── 📄 app.py                  # 메인 애플리케이션 (네비게이션 역할)
├── 📂 pages        
│   ├── 📄 map_view.py         # [Page 1] 부동산 탐색 & AI 추천
│   └── 📄 ai_consultant.py    # [Page 2] 대출 계산기
├── 📄 .env                    # API Key 보안 관리
└── 📄 requirements.txt        # 의존성 라이브러리 목록
```
