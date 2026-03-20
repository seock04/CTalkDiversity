# 현재 Conference 페이지 개선안

## 목적

이 문서는 현재 등록된 conference 페이지들을 읽고,
어떤 점을 먼저 보완하면 더 읽기 쉽고 덜 중복된 페이지가 되는지 정리한 메모다.

대상 페이지:
- `Pages/Conference/conference-24.html`
- `Pages/Conference/conference-25.html`
- `Pages/Conference/conference-26.html`

---

## 1. 현재 공통적으로 보이는 문제

### 1.1 포스터와 본문 정보가 일부 중복된다
페이지 상단 대표 이미지는 이미 행사 정보를 전달하는 역할을 하는데,
본문이 같은 정보를 거의 반복하는 경우가 있다.

문제:
- 읽는 사람이 새 정보를 얻는 느낌이 약함
- 상세 페이지가 포스터 설명 복붙처럼 느껴질 수 있음

개선 방향:
- 상세 페이지 상단에 **짧은 event overview 문단**을 추가
- 포스터에 있는 정보는 최소 반복
- 본문은 왜 이 주제가 중요한지, 어떤 대화가 기대되는지 중심으로 보강

---

### 1.2 speaker bio와 topic summary가 덜 분리되어 있다
일부 페이지는 인물 소개와 발표 내용 소개가 비슷한 리듬으로 이어져서,
읽는 사람이 "이 사람이 누군지"와 "무슨 이야기를 하는지"를 분리해서 읽기 어렵다.

개선 방향:
- speaker bio는 2~3문장으로 짧고 명확하게
- topic summary는 발표 핵심과 기대 질문 중심으로 따로 정리

---

### 1.3 event page 고유의 맥락 문장이 부족하다
현재는 날짜/시간/스피커 정보는 있지만,
이 conference가 왜 열렸는지, 어떤 의미가 있는지 설명하는 문장이 약하다.

개선 방향:
- event details 아래에 1문단 정도의 **conference overview** 추가
- 이 회차의 문제의식/맥락/기대 포인트를 설명

---

### 1.4 자산 네이밍이 회차와 맞지 않는 부분이 있다
예:
- 26th conference 이미지 경로에 `24th-...`가 들어감
- 25th conference speaker 이미지도 `24th-...` 흔적이 있음

개선 방향:
- 당장 링크를 깨지 않게 유지하더라도
- 정리 계획을 세워 차차 회차 기준으로 네이밍 정리

---

### 1.5 텍스트 인코딩 깨짐 흔적이 있다
예:
- `Belgium?�s`
- `It?�s`

이건 실제 페이지 신뢰도에 영향을 준다.

개선 방향:
- conference-24 페이지부터 문자 깨짐 우선 수정

---

## 2. 페이지별 보완 포인트

## 2.1 conference-24.html

### 좋은 점
- speaker 2명 구조가 명확함
- 주제와 행사 목적이 비교적 분명함

### 보완 포인트
- 문자 깨짐(`?�`) 수정이 우선 필요
- event details 아래에 conference overview 추가 권장
- speaker 소개가 조금 길고 topic summary와 경계가 흐림

### 추천 수정
- `Belgium?�s` → `Belgium's`
- `It?�s` → `It's`
- 상단에 2~3문장짜리 overview 추가
- speaker bio를 조금 압축

---

## 2.2 conference-25.html

### 좋은 점
- 단일 speaker 구성이라 읽기 단순함
- 주제 자체가 선명함

### 보완 포인트
- conference 전체 맥락 설명이 부족함
- 상세 페이지치고는 정보량이 너무 적어서 금방 끝나는 느낌
- 대표 이미지와 본문 사이 연결 문장이 있으면 좋음

### 추천 수정
- event details 뒤에 conference overview 문단 추가
- 왜 decolonization을 이 회차 주제로 다루는지 짧게 설명
- speaker bio와 topic 소개를 좀 더 구분

---

## 2.3 conference-26.html

### 좋은 점
- 최신 conference로서 메인 페이지와 연결이 잘 됨
- speaker 2명 구성도 보기 좋음

### 보완 포인트
- 이미지 파일명이 24th 흔적이라 관리상 혼란
- 두 번째 speaker topic summary가 상단 theme와의 연결이 다소 약해 보일 수 있음
- conference overview 부재

### 추천 수정
- event details 아래 overview 추가
- 두 speaker가 전체 theme와 어떻게 연결되는지 한 문장씩 더 보강
- 자산 파일명은 장기 정리 항목으로 분리

---

## 3. 우선 수정 추천 순서

### 1순위
`conference-24.html`
- 문자 깨짐 수정
- overview 추가

### 2순위
`conference-25.html`
- 행사 맥락 설명 보강
- 내용 밀도 보완

### 3순위
`conference-26.html`
- overview 및 theme 연결 문장 보강

---

## 4. 가장 먼저 적용하면 좋은 공통 개선

세 conference 페이지 모두에 아래 블록을 추가하는 것을 추천한다:

### 추천 블록: Conference Overview
위치:
- 대표 이미지 아래
- Event Details 위 또는 아래

역할:
- 이 회차가 어떤 대화인지 설명
- speaker 정보와 별개로 conference 전체의 의미를 짧게 제시

이 블록 하나만 추가해도:
- 포스터 반복 느낌이 줄고
- 상세 페이지다운 밀도가 생기고
- 읽는 사람이 주제를 더 쉽게 이해하게 된다.

---

## 5. 추천 결론

현재는 새 conference를 더 추가하기 전에,
먼저 기존 conference 페이지 3개를 다음 기준으로 가볍게 보완하는 것이 좋다:

- 문자 깨짐 수정
- event overview 추가
- speaker bio / topic summary 역할 분리
- 과도한 중복 줄이기

즉, 지금 단계의 목표는 대규모 리디자인이 아니라
**기존 conference 페이지를 더 읽기 좋고 더 덜 반복적으로 만드는 것**이다.
