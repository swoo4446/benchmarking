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
    │   ├── 서비스 안내 문구
    │   ├── 검색어 입력칸
    │   ├── AI 모델 선택
    │   └── 추천 질문
    │
    └── 검색 결과 / 대화 화면
        ├── 사용자가 입력한 질문
        ├── AI 답변
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

**주요 흐름**

```text
에이닷 Search 진입
→ 검색 시작 화면 확인
→ 검색어 입력
→ AI 모델 선택
→ 검색 실행
→ AI 답변 확인
→ 다른 AI 답변 비교 여부 선택
→ 추천 질문 또는 후속 질문을 통한 대화 지속
```

### User Flow

![Case 1. 초기 진입 후 검색](./images/case1-initial-search.png)

---

## Case 2. 검색 결과 비교 및 추가 질문

검색 결과를 확인한 이후 다른 AI 모델의 답변을 비교하거나 추천 질문·후속 질문을 이용해 대화를 이어가는 흐름이다.

**주요 흐름**

```text
검색 결과 확인
→ 다른 AI 답변 비교 여부 선택
→ AI 답변 비교
→ 추천 질문 확인
→ 추천 질문 선택 또는 직접 후속 질문 입력
→ 검색 실행
→ 새로운 AI 답변 확인
→ 대화 지속
```

### User Flow

![Case 2. 검색 결과 비교 및 추가 질문](./images/case2-follow-up.png)

---

## Case 3. 이전 대화 이어하기

사이드바의 대화 History에서 기존 대화를 선택하여 이전 검색 내용을 확인하고 대화를 이어가는 흐름이다.

**주요 흐름**

```text
대화 History 확인
→ 이전 대화 선택
→ 기존 질문 및 AI 답변 확인
→ 다른 AI 답변 비교 또는 추가 질문
→ 검색 실행
→ 새로운 AI 답변 확인
→ 대화 지속
```

### User Flow

![Case 3. 이전 대화 이어하기](./images/case3-history.png)

---

## Case 4. 새로운 채팅으로 전환

기존 대화를 진행하던 사용자가 `새 대화`를 선택하여 현재 대화를 종료하고 새로운 검색을 시작하는 흐름이다.

**주요 흐름**

```text
기존 대화 진행
→ 새 대화 선택
→ 기존 대화 종료 / 검색 화면 초기화
→ 검색 시작 화면
→ 검색어 입력
→ AI 모델 선택
→ 검색 실행
→ AI 답변 확인
```

### User Flow

![Case 4. 새로운 채팅으로 전환](./images/case4-new-chat.png)

---

## Case 5. 대화 수정

이미 입력한 질문을 수정하여 동일한 대화 내에서 새로운 검색 결과를 확인하는 흐름이다.

**주요 흐름**

```text
기존 대화 확인
→ 이전 질문 수정
→ 질문 내용 변경
→ 검색 재실행
→ 수정된 질문 기준 AI 답변 생성
→ 새로운 답변 확인
→ 대화 지속
```

### User Flow

![Case 5. 대화 수정](./images/case5-edit-message.png)

---

# 3. 이미지 파일 구성

Markdown 파일과 같은 위치에 `images` 폴더를 생성하고 Case별 이미지를 저장하면 관리하기 편하다.

```text
project/
│
├── README.md
│
└── images/
    ├── case1-initial-search.png
    ├── case2-follow-up.png
    ├── case3-history.png
    ├── case4-new-chat.png
    └── case5-edit-message.png
```

Markdown에서는 다음 형식으로 이미지를 삽입한다.

```markdown
![이미지 설명](./images/파일명.png)
```

예시:

```markdown
### User Flow

![Case 1. 초기 진입 후 검색](./images/case1-initial-search.png)
```

이미지 크기를 직접 조절해야 하는 GitHub README 등의 환경에서는 HTML 태그를 사용할 수도 있다.

```html
<p align="center">
  <img src="./images/case1-initial-search.png" width="900" alt="Case 1. 초기 진입 후 검색">
</p>
```

---

## Case 이미지 파일명 권장 규칙

| Case | 파일명 |
|---|---|
| Case 1 | `case1-initial-search.png` |
| Case 2 | `case2-follow-up.png` |
| Case 3 | `case3-history.png` |
| Case 4 | `case4-new-chat.png` |
| Case 5 | `case5-edit-message.png` |

영문 소문자와 `-`를 기준으로 파일명을 통일하면 GitHub나 다른 문서 환경으로 옮길 때 경로 오류를 줄일 수 있다.

Case 3. 이전 대화 이어하기

Case 4. 새로운 채팅으로 전환

Case 5. 대화 수정
