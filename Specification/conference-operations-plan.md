# Conference Operations Plan

이 문서는 앞으로 새로 발표되는 upcoming conference를 사이트에 반영하고,
이전에는 upcoming이었지만 종료된 conference를 archive로 옮길 때 사용하는 반복 가능한 작업 계획이다.

## 목적

- 새 upcoming conference가 홈과 목록에서 바로 보이도록 한다.
- 완료된 conference를 archive 상태로 정리한다.
- conference 운영 작업의 순서와 완료 기준을 명확히 한다.

## 적용 범위

- `Pages/Conference/conference-XX.html`
- `Pages/conferences.html`
- `index.html`
- `images/conferences/XX/`

## 작업 순서

### 1. 종료된 upcoming conference를 archive로 정리

- conference 상세 페이지의 상태 문구를 완료형 아카이브 기준으로 맞춘다.
- 등록 유도 문구가 있으면 완료형 안내 문구로 교체한다.
- 홈과 목록에서 더 이상 진행 중인 행사처럼 보이지 않게 한다.

### 2. 새 upcoming conference 상세 페이지 생성

- 가장 최근 conference 페이지를 기준으로 새 upcoming conference 상세 페이지를 만든다.
- 대표 포스터와 speaker 포스터를 올바른 순서로 연결한다.
- `Conference Overview`를 넣어 이 회차의 맥락을 설명한다.
- speaker 수에 맞게 소개와 topic 설명을 분리한다.

### 3. 목록 페이지 반영

- `Pages/conferences.html` 맨 위에 새 upcoming conference를 추가한다.
- 기존 upcoming conference는 아래로 내리고, 종료된 conference는 archive 상태로 유지한다.
- 카드 제목, 요약, 이미지, 링크가 실제 파일과 일치하는지 확인한다.

### 4. 홈 페이지 반영

- `index.html`의 최신 conference 카드 또는 섹션을 새 upcoming conference로 교체한다.
- 외부 사용자가 첫 화면에서 최신 upcoming conference를 확인할 수 있어야 한다.

### 5. 검증

- 홈, 목록, 상세 페이지의 `href`와 `src`를 확인한다.
- archive 상태로 옮긴 conference가 완료형으로 보이는지 확인한다.
- 새 upcoming conference가 실제 공개 entry point에서 노출되는지 확인한다.
- 브라우저에서 외부 사용자 관점으로 한 번 더 확인한다.

## 완료 기준

- 새 upcoming conference가 `index.html`과 `Pages/conferences.html`에 노출된다.
- 새 upcoming conference 상세 페이지가 실제 이미지와 연결된다.
- archive로 옮긴 conference가 완료형 상태로 보인다.
- 로컬 참조 오류가 없다.
