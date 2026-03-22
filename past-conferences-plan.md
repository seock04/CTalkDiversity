# Past Conferences Expansion Plan

> Status update (2026-03-22): This document reflects the original expansion strategy, but the archive build has since progressed much further. Pages for conferences 1–26 now exist locally, so references below to “start with 13th” or to page creation as future work should be read as historical planning context. The next practical work is cleanup/QA rather than initial page creation.

## 목적

이 문서는 CTalkDiversity 사이트에 **과거 회차 conference 페이지를 순차적으로 추가**하기 위한 작업 계획서다.

목표는 단순히 페이지 수를 늘리는 것이 아니라,
기존 자료를 바탕으로 **일관된 구조와 운영 기준** 안에서 과거 회차를 안정적으로 복원하는 것이다.

---

## 기본 원칙

1. **바로 페이지를 대량 생성하지 않는다.**
   - 먼저 자료를 파악하고, 우선순위를 정한 뒤 진행한다.

2. **한 번에 한 회차씩 진행한다.**
   - 각 회차마다 자료 상태와 품질이 다르므로, 개별 처리 원칙이 필요하다.

3. **자료가 좋은 회차부터 시작한다.**
   - 13~23회처럼 회차별 폴더가 있는 구간부터 우선 진행한다.

4. **사이트 구조 일관성을 유지한다.**
   - 현재 24~26회 페이지를 기준으로 conference 상세 페이지 형식을 맞춘다.

5. **과거 회차는 아카이브형 페이지로 처리한다.**
   - Register 버튼은 두지 않고,
   - 종료된 행사임을 알리는 문구를 기본적으로 넣는다.

6. **Spotify AI review 링크가 있으면 추가한다.**
   - 다만 회차별 링크가 확인된 경우에만 반영한다.

---

## 자료 소스

현재 과거 회차 자료는 아래 폴더에 존재한다:

- `/Users/seock04/Downloads/C-Talk poster info`

주요 구성:
- `Poster-past/` → 초기 회차 포스터 중심 자료
- `2025 13th C Talk -Jan.` ~ `2025-23rd C Talk-Nov` → 회차별 자료 폴더
- `2026-24th C Talk - Jan` 이후 → 이미 일부 사이트에 반영된 최근 회차 자료

---

## 작업 구간 분류

### Group A — 우선 작업 대상
**13 ~ 23회**

특징:
- 회차별 폴더가 비교적 명확함
- posting/link 문서, speaker info, moderator note, photo 등이 존재함
- 페이지로 전환하기 가장 쉬움

전략:
- 이 구간부터 순차적으로 페이지 생성
- 13 → 14 → 15 ... 식으로 진행

---

### Group B — 중간 검토 대상
**11 ~ 12회**

특징:
- 별도 회차 폴더 구조가 불명확함
- `Poster-past` 안에 관련 흔적은 보이지만 정리도는 낮음

전략:
- 나중에 별도 자료 탐색 후 처리
- 우선순위는 Group A 다음

---

### Group C — 복원형 작업 대상
**1 ~ 10회**

특징:
- 포스터 중심 자료가 많음
- 상세 speaker 정보/운영 문서가 부족할 가능성 있음

전략:
- 포스터 기반 아카이브형 복원
- 정보가 부족한 경우 최소 정보 페이지로 구성
- 장기 과제로 천천히 진행

---

## 각 회차별 기본 작업 절차

### Step 1 — 자료 읽기
회차 폴더에서 아래 정보를 추출한다.
- 제목 / theme
- 날짜 / 시간
- moderator
- speaker 정보
- 발표 주제
- 소개 문장
- 이미지 자산
- 등록 링크 흔적 여부

### Step 2 — 페이지 작성 초안
다음 구조를 기본으로 작성한다.
- 제목 / theme / 날짜 / moderator
- 대표 이미지
- Event Details
- archive 안내 문구
- Conference Overview
- speaker 섹션
- Back to Home 버튼

### Step 3 — 목록 페이지 반영 준비
해당 회차가 추가되면 나중에 아래도 갱신해야 한다.
- `Pages/conferences.html`
- 필요 시 `index.html`

단, 당장은 상세 페이지를 먼저 쌓고 목록 반영은 단계적으로 할 수 있다.

### Step 4 — optional enrichments
가능한 경우만 추가:
- Spotify AI review 링크
- 추가 이미지
- 행사 사진 일부 반영

---

## 페이지 작성 원칙

### 1. 아카이브 문구
과거 회차는 기본적으로 아래 방향을 유지한다:
- "This event has already taken place and is now part of our archive."

### 2. Register 버튼
과거 회차는 Register 버튼 제거.

### 3. Spotify 링크
회차별 에피소드 링크가 확인된 경우에만 추가.

### 4. 중복 최소화
- 포스터에 있는 문구를 그대로 반복하지 않는다.
- speaker bio와 topic summary는 역할을 나눠 적는다.
- overview는 행사 전체의 맥락을 설명한다.

---

## 우선 진행 순서

### Phase 1
- conference-tracker 작성
- 13~23회 상태 정리

### Phase 2
- 최근 회차부터 역순으로 페이지 작성
- 23회부터 시작하여 1회차까지 순차 확장
- 각 회차 완료 시 부족한 자료/특이사항을 별도 노트로 기록

### Phase 3
- 다음 회차로 즉시 이동
- 같은 방식 반복

### Phase 4
- 일정 구간 작성 후 `conferences.html` 목록 갱신

### Phase 5
- 11~12회 자료 재탐색

### Phase 6
- 1~10회 포스터 기반 아카이브 복원

---

## 운영 방식

앞으로는 다음 원칙으로 진행한다:
- 먼저 계획/정리 문서에 반영
- 그 다음 회차별 작업을 하나씩 수행
- 호석님이 매번 세세하게 확인하지 않아도 되도록, 작업 기준을 문서화한 뒤 진행
- 중요한 구조 변경이나 애매한 해석이 필요한 경우에만 다시 확인 요청

---

## 현재 결론

지금 시점에서 가장 효율적인 방향은:
1. 과거 회차 확장 계획을 문서화하고
2. 자료가 가장 좋은 13~23회부터 하나씩 페이지를 만들며
3. 이후 점차 초기 회차로 확장하는 것이다.

즉, 다음 실질 작업은 `conference-tracker.md` 작성과 13회 자료 정리부터 시작하는 것이 적절하다.
