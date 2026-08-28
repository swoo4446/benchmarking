# 에이닷 Web 분석

- **서비스명:** 에이닷 Web
- **URL:** https://adot.ai/search
- **분석 기준일:** 2026년 8월 28일
- **분석 범위:** AI 검색 및 대화 기능
- 로그인, 노트, 내 정보 등 검색과 직접적인 관련이 없는 기능은 분석 범위에서 제외
---
## 1. IA (Information Architecture)

### 에이닷 Search

```text
에이닷 Search
│
├── 왼쪽 영역 (Sidebar)
│   └── 검색
│       ├── 새 대화
│       ├── 최근 기록
│       └── 대화 History
│
└── 가운데 영역 (Main)
    │
    ├── 검색 시작 화면
    │   ├── 검색어 입력칸
    │   ├── AI 모델 선택
    │   └── 추천 질문
    │
    └── 검색 결과 / 대화 화면
        ├── 출처
        ├── 다른 AI 답변 비교
        ├── 추천 질문
        └── 후속 질문 입력칸
```

> **분석 범위 제외:** 내 정보, 노트 및 로그인 등 AI 검색·대화와 직접적으로 관련되지 않은 기능

---

# 2. User Flow

에이닷 Search의 주요 사용 흐름을 사용자 행동을 기준으로 5개의 Case로 구분하였다.
---

## Case 1. 초기 진입 후 검색

에이닷 Search에 처음 진입한 사용자가 검색어를 입력하고 AI 답변을 확인하는 기본 검색 흐름이다.

### User Flow
<img width="1536" height="1024" alt="Case1" src="https://github.com/user-attachments/assets/4be6a55e-d610-498c-ba2f-f022edccde1f" />
---

## Case 2. 검색 결과 비교 및 추가 질문

검색 결과를 확인한 이후 다른 AI 모델의 답변을 비교하거나 추천 질문·후속 질문을 이용해 대화를 이어가는 흐름이다.

### User Flow
<img width="1536" height="1024" alt="case2" src="https://github.com/user-attachments/assets/83e68c30-72d8-4fae-a356-bd13c5f47425" />
---

## Case 3. 이전 대화 이어하기

사이드바의 대화 History에서 기존 대화를 선택하여 이전 검색 내용을 확인하고 대화를 이어가는 흐름이다.

### User Flow
<img width="1536" height="1024" alt="case3" src="https://github.com/user-attachments/assets/b1fd20ab-8d16-4d04-b8df-2a0c7c92f78b" />
---

## Case 4. 새로운 채팅으로 전환

기존 대화를 진행하던 사용자가 `새 대화`를 선택하여 현재 대화를 종료하고 새로운 검색을 시작하는 흐름이다.

### User Flow
<img width="1536" height="1024" alt="case4" src="https://github.com/user-attachments/assets/38285326-d4d7-4dc4-98c8-5ab662253b9b" />

---

## Case 5. 대화 수정

이미 입력한 질문을 수정하여 동일한 대화 내에서 새로운 검색 결과를 확인하는 흐름이다.

### User Flow
<img width="1149" height="1369" alt="case5" src="https://github.com/user-attachments/assets/246e02fc-07b0-4977-87e2-47ccd7234f22" />
---

# 3. WireFrame

## 초기 화면
<img width="1774" height="887" alt="초기 화면" src="https://github.com/user-attachments/assets/28aa1cdc-c39b-4476-8b88-13a19f0af7d8" />

## 초기 화면 -모델 선택
<img width="1659" height="948" alt="모델 선택" src="https://github.com/user-attachments/assets/d91388db-e0aa-47fd-aeef-8a2547c22382" />

## 초기 화면 -이전 대화 존재
<img width="1840" height="854" alt="초기 화면_이전 대화" src="https://github.com/user-attachments/assets/93e1d31e-199c-4226-b164-097b01f135c9" />

## 검색 화면 -로딩 중
<img width="1672" height="941" alt="답변 생성 로딩중" src="https://github.com/user-attachments/assets/728d7077-70b0-435b-893f-b817ae1b0b24" />

## 검색 화면 -답변 완료
<img width="941" height="1672" alt="답변 완료" src="https://github.com/user-attachments/assets/8a49d33e-47d0-4363-b961-9a4c6e9ab1de" />

## 다른 AI 답변 비교 -모델 선택
<img width="1706" height="922" alt="답변 완료-모델생성" src="https://github.com/user-attachments/assets/87281755-a33a-4b34-afb6-bf2de0cabf61" />

## 최근 기록
<img width="1632" height="964" alt="최근기록" src="https://github.com/user-attachments/assets/625aac8b-67ae-4b94-9d00-9f6c874849eb" />

<img width="1672" height="941" alt="최근 기록 -편집" src="https://github.com/user-attachments/assets/b085f1f3-1a24-4068-8f8f-b868c6ee79db" />

## 대화 고정/이름 변경/삭제
<img width="1672" height="941" alt="2" src="https://github.com/user-attachments/assets/64af852b-2b52-4c32-a7bd-d4750a324ca8" />
<img width="1672" height="941" alt="1" src="https://github.com/user-attachments/assets/1bcb249a-532c-4e2d-8334-e88abbca19af" />
<img width="1811" height="868" alt="3" src="https://github.com/user-attachments/assets/f4ba9444-59de-43fd-9c92-10c28709d321" />

