# Conference Operations Plan

이 문서는 27회차 conference를 외부 사용자에게 반영하고, 26회차를 완료형 아카이브로 정리하기 위한 작업 계획이다.

## 목적

- 새 conference가 홈과 목록에서 바로 보이도록 한다.
- 기존 최신 회차였던 26회를 완료형 상태로 정리한다.
- conference 추가 작업의 순서와 완료 기준을 명확히 한다.

## 적용 범위

- `Pages/Conference/conference-26.html`
- `Pages/Conference/conference-27.html`
- `Pages/conferences.html`
- `index.html`
- `images/conferences/27/`

## 작업 순서

### 1. 26회차를 완료형으로 정리

- `conference-26.html`의 상태 문구를 완료형 아카이브 기준으로 맞춘다.
- 등록 유도 문구가 있으면 완료형 안내 문구로 교체한다.
- 홈과 목록에서 26회차가 현재 진행 중인 행사처럼 보이지 않게 한다.

### 2. 27회차 상세 페이지 생성

- `conference-26.html`을 기준으로 `conference-27.html`을 만든다.
- 대표 포스터와 speaker 포스터를 올바른 순서로 연결한다.
- `Conference Overview`를 넣어 이 회차의 맥락을 설명한다.
- speaker 2명의 소개와 topic 설명을 분리한다.

### 3. 목록 페이지 반영

- `Pages/conferences.html` 맨 위에 27회차를 추가한다.
- 26회차는 그 아래 완료형 기록으로 유지한다.
- 카드 제목, 요약, 이미지, 링크가 실제 파일과 일치하는지 확인한다.

### 4. 홈 페이지 반영

- `index.html`의 최신 conference 카드 또는 섹션을 27회차로 교체한다.
- 외부 사용자가 첫 화면에서 27회차를 확인할 수 있어야 한다.

### 5. 검증

- 홈, 목록, 상세 페이지의 `href`와 `src`를 확인한다.
- 26회차가 완료형 상태로 보이는지 확인한다.
- 27회차가 실제 공개 entry point에서 노출되는지 확인한다.
- 브라우저에서 외부 사용자 관점으로 한 번 더 확인한다.

## 완료 기준

- 27회차가 `index.html`과 `Pages/conferences.html`에 노출된다.
- 27회차 상세 페이지가 실제 이미지와 연결된다.
- 26회차가 완료형 아카이브 상태로 보인다.
- 로컬 참조 오류가 없다.

