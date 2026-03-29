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

## 작성 톤 & 문구 원칙

### upcoming 작성 원칙

- 문구는 너무 딱딱하지 않게, 읽는 사람이 자연스럽게 관심을 느낄 수 있도록 친근하고 부드러운 톤을 사용한다.
- 스피커 소개는 존중을 바탕으로 쓰고, 과장하거나 자극적으로 보이지 않도록 한다.
- 컨퍼런스 소개는 참여 욕구를 살릴 수 있게 흥미롭고 기대감을 주는 방향으로 쓴다.
- 너무 극단적이거나 자극적인 표현은 피하고, "재미있고 흥미로운 시간이 될 것 같다"는 인상을 중심에 둔다.
- 초대 문구는 부담스럽지 않게, 함께 듣고 이야기 나누고 싶어지는 느낌으로 정리한다.

### archive 작성 원칙

- archive는 완료된 행사라는 점이 분명하게 드러나도록 작성한다.
- 등록 유도나 참여 권유 중심 문구는 제거하고, 행사에서 다룬 내용과 맥락을 차분하게 요약한다.
- 스피커 소개는 여전히 존중을 유지하되, 결과물 기록이라는 성격에 맞게 간결하고 정제된 문체를 사용한다.
- 과도한 홍보성 표현이나 기대감 유도 문구는 줄이고, 행사의 의미와 핵심 주제를 중심으로 남긴다.
- archive는 회고용 기록이므로, 내용 전달과 아카이빙 품질을 우선한다.

## 작업 순서

### 1. 종료된 upcoming conference를 archive로 정리

- conference 상세 페이지의 상태 문구를 완료형 아카이브 기준으로 맞춘다.
- 등록 유도나 초대 문구가 있으면 제거한다.
- archive에는 conference 내용 자체에 기반한 설명만 남긴다.
- 홈과 목록에서 더 이상 진행 중인 행사처럼 보이지 않게 한다.

### 2. 새 upcoming conference 상세 페이지 생성

- 가장 최근 conference 페이지를 기준으로 새 upcoming conference 상세 페이지를 만든다.
- 대표 포스터와 speaker 포스터를 올바른 순서로 연결한다.
- `Conference Overview`를 넣어 이 회차의 맥락을 설명한다.
- speaker 수에 맞게 소개와 topic 설명을 분리한다.
- archive로 전환될 때를 대비해, 회차 결과물로 남길 수 있는 뉴스 링크나 podcast 링크를 붙일 수 있는 섹션 구조를 미리 고려한다.

### 3. 목록 페이지 반영

- `Pages/conferences.html` 맨 위에 새 upcoming conference를 추가한다.
- 기존 upcoming conference는 아래로 내리고, 종료된 conference는 archive 상태로 유지한다.
- 카드 제목, 요약, 이미지, 링크가 실제 파일과 일치하는지 확인한다.
- `index.html`의 conference 노출 영역에서는 최신 2개 conference 데이터를 우선 보여주고, 새 conference가 추가되면 그 직전 conference 2개가 계속 보이도록 갱신한다.

### 4. 홈 페이지 반영

- `index.html`의 최신 conference 카드 또는 섹션을 새 upcoming conference로 교체한다.
- 외부 사용자가 첫 화면에서 최신 upcoming conference를 확인할 수 있어야 한다.

### 5. 검증

- 홈, 목록, 상세 페이지의 `href`와 `src`를 확인한다.
- archive 상태로 옮긴 conference가 완료형으로 보이는지 확인한다.
- archive 페이지에 남는 문구가 초대/모집 중심이 아니라 내용 요약 중심인지 확인한다.
- 필요 시 뉴스 링크, podcast 링크 같은 결과물 링크를 추가할 수 있는 위치가 있는지 확인한다.
- 새 upcoming conference가 실제 공개 entry point에서 노출되는지 확인한다.
- 브라우저에서 외부 사용자 관점으로 한 번 더 확인한다.
- PC에서 보이는 왼쪽 사이드바(메뉴 영역)의 conference 미리보기는 항상 현재 최신 회차(N)를 제외한 직전 2개 회차(N-1, N-2)로 유지한다.

## 완료 기준

- 새 upcoming conference가 `index.html`과 `Pages/conferences.html`에 노출된다.
- 새 upcoming conference 상세 페이지가 실제 이미지와 연결된다.
- archive로 옮긴 conference가 완료형 상태로 보인다.
- archive 결과물 링크를 추가할 수 있는 구조가 유지된다.
- 로컬 참조 오류가 없다.
