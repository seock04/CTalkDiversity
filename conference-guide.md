# Conference 추가 가이드

## 목적

이 문서는 CTalkDiversity 사이트에 새로운 conference를 추가할 때,
반복 작업을 덜 헷갈리게 하고 누락을 줄이기 위한 운영 가이드다.

현재 사이트는 정적 HTML 구조이므로, conference 하나를 추가할 때 여러 파일을 함께 수정해야 한다.
이 문서는 그 순서와 체크포인트를 정리한다.

---

## 1. conference 추가 시 수정 대상

새 conference를 추가할 때 일반적으로 다음 위치를 함께 본다:

1. `Pages/Conference/conference-XX.html`
   - 새 상세 페이지 생성

2. `Pages/conferences.html`
   - conference 목록 페이지에 새 항목 추가

3. `index.html`
   - 메인 페이지에 최신 conference를 반영할지 결정

4. `Conferences/XX/`
   - 메인 이미지 및 speaker 이미지 추가

---

## 2. 추천 작업 순서

### Step 1 — 기본 정보 정리
먼저 아래 정보를 한 곳에 정리한다.

- 회차 번호
- 제목
- 테마
- 날짜
- 시간
- moderator
- register 링크
- speaker 수
- 각 speaker 이름 / 소개 / 발표 주제 / 주제 설명
- 사용할 이미지 목록

가능하면 이 정보를 먼저 문서나 메모로 정리한 뒤 HTML에 반영한다.

---

### Step 2 — 상세 페이지 생성
기존 conference 페이지를 복사해 새 파일을 만든다.

예:
- `Pages/Conference/conference-26.html` 복사
- 새 파일명: `Pages/Conference/conference-27.html`

수정 항목:
- `<title>`
- 상단 제목
- Theme
- 날짜/time
- moderator
- 메인 이미지
- speaker 섹션 수와 내용
- 버튼 링크
- alt 텍스트

---

### Step 3 — 목록 페이지 반영
`Pages/conferences.html`에 새 conference 카드 추가 또는 최신순 정렬 반영.

체크 항목:
- 제목
- 날짜
- 요약문
- 대표 이미지
- 상세 페이지 링크

---

### Step 4 — 메인 페이지 반영 여부 결정
`index.html`은 최신 conference와 call for speakers를 전면에 노출하는 역할을 한다.

새 conference가 최신 행사라면 보통:
- 기존 최신 conference를 아래로 내리고
- 새 conference를 첫 번째 카드로 올리는 방식이 자연스럽다.

---

### Step 5 — 이미지 추가
`Conferences/<회차>/` 폴더를 만들고 이미지를 정리한다.

권장:
- 대표 이미지 1장
- speaker별 이미지
- 필요 시 보조 이미지

---

### Step 6 — 링크와 경로 점검
반드시 확인할 것:
- 이미지 경로
- 상세 페이지 링크
- Back to Home 링크
- register 링크
- 상단 메뉴 링크

---

## 3. 권장 파일명 규칙

현재 일부 자산은 회차와 파일명이 일치하지 않는 흔적이 있다.
앞으로는 가능한 한 아래처럼 맞추는 것을 권장한다.

예:
- `Conferences/27/27th-01-main.jpeg`
- `Conferences/27/27th-02-speaker-jane-doe.jpeg`
- `Conferences/27/27th-03-speaker-john-smith.jpeg`

원칙:
- 회차 번호를 파일명 앞에 둔다
- 역할(main / speaker)을 드러낸다
- speaker 파일은 이름을 붙인다

---

## 4. 상세 페이지 작성 권장 구조

conference 상세 페이지는 다음 흐름을 권장한다.

1. 제목 / theme / 날짜 / moderator
2. 대표 이미지
3. event details
4. conference 소개 요약 1문단
5. speaker 섹션들
6. back 버튼

주의:
- 포스터 이미지에 이미 들어 있는 문구를 본문에서 그대로 반복하지 않는다
- speaker 소개와 발표 내용은 분리해서 쓴다
- 너무 긴 소개는 2~4문장 정도로 줄인다

---

## 5. 중복 줄이기 원칙

현재 conference 페이지는 다음 중복이 생기기 쉽다:
- 포스터 이미지에 이미 있는 정보 반복
- speaker bio와 topic 설명 사이 의미 반복
- home / list / detail 페이지에서 같은 설명을 거의 그대로 반복

권장 원칙:
- **포스터는 시각적 요약**
- **상세 페이지는 맥락 설명**
- **speaker bio는 인물 소개**
- **topic summary는 발표 내용 소개**

즉, 같은 내용을 다른 방식으로 반복하지 말고 역할을 나눠 적는다.

---

## 6. 추가 후 체크리스트

- [ ] 상세 페이지 생성 완료
- [ ] 목록 페이지 반영 완료
- [ ] 메인 페이지 반영 여부 확인
- [ ] 이미지 경로 정상
- [ ] alt 텍스트 추가
- [ ] 날짜/시간 표기 일관성 확인
- [ ] 회차 번호/파일명 일치 확인
- [ ] 모바일에서 너무 길거나 깨지는 문구 없는지 점검

---

## 7. 앞으로 개선할 수 있는 방향

장기적으로 conference가 계속 늘어나면 다음을 검토할 수 있다:
- conference 데이터를 JSON/YAML로 분리
- 템플릿 재사용 구조 도입
- 정적 사이트 생성기 도입

하지만 현재 단계에서는 먼저:
- 네이밍 규칙
- 작성 구조
- 반영 순서
를 안정화하는 것이 우선이다.
