# CTalkDiversity Specification

이 문서는 CTalkDiversity 프로젝트의 개발/운영 기준 문서다.
새 페이지를 만들거나 기존 페이지를 수정할 때는 먼저 이 문서를 기준으로 판단한다.

## 1. 목적

- 페이지 구조와 배치 규칙을 하나로 통일한다.
- conference, call-for-speakers, event 타입별 변경 범위를 명확히 한다.
- 메뉴 구조와 관련 페이지 수정 대상을 한눈에 보이게 한다.
- 작업 시 무엇을 함께 고쳐야 하는지 판단 기준을 제공한다.

## 2. 범위

이 문서는 다음 작업에 적용한다.

- 새 페이지 추가
- 기존 페이지 수정
- 메뉴 구조 변경
- 이미지 자산 추가 또는 교체
- home / list / detail 간 링크 반영

## 3. 사이트 레이아웃 Spec

### 3.1 공통 페이지 골격

정적 페이지는 기본적으로 아래 구조를 따른다.

1. `header`
2. `menu`
3. `main`
4. `footer`

공통 규칙:

- 모든 상세 페이지는 상단에 사이트명 링크를 둔다.
- 메뉴에는 `Organization`, `Conferences`, `Call For Speakers`를 기본으로 둔다.
- 상세 페이지는 가능한 한 `Back` 버튼을 포함한다.
- 이미지 경로는 현재 파일의 위치를 기준으로 상대경로를 맞춘다.

### 3.2 공통 스타일 원칙

- 제목은 페이지 성격이 바로 드러나게 쓴다.
- 본문은 시각적 소개와 설명을 분리한다.
- 이미지에 이미 적힌 문구를 본문에서 그대로 반복하지 않는다.
- 모바일에서도 잘 읽히도록 섹션 길이를 조절한다.

## 4. 메뉴 트리 Spec

### 4.1 기본 메뉴 트리

현재 사이트의 기본 메뉴는 다음 순서를 따른다.

- Organization
- Conferences
- Call For Speakers

### 4.2 세부 연결 규칙

- `Organization`
  - `Pages/about.html`
  - 조직 소개와 내부 작업 페이지로 연결되는 출발점

- `Conferences`
  - `Pages/conferences.html`
  - 지난 conference 목록 페이지

- `Call For Speakers`
  - `Pages/call-for-speakers.html`
  - 공개 모집 공지 목록 페이지

### 4.3 이벤트 페이지 위치 원칙

`event` 타입은 기본 메뉴의 최상위 항목으로 두지 않는다.

- 우선 `About / Organization` 계열에서 연결한다.
- 필요하면 홈(`index.html`)에서도 노출한다.
- 이벤트가 많아져 별도 목록이 필요할 때만 `Events` 인덱스 페이지를 추가한다.

## 5. 새 페이지 추가 Spec

새 페이지를 만들 때는 페이지 타입에 따라 위치와 수정 범위를 함께 정한다.

### 5.1 Conference 페이지

#### 위치

- 상세 페이지: `Pages/Conference/conference-XX.html`
- 이미지: `images/conferences/XX/`

#### 작업 순서

1. 회차 번호, 제목, 테마, 날짜, 시간, moderator, register 링크, speaker 수, 각 speaker 정보, 사용할 이미지 목록을 먼저 정리한다.
2. 가장 최근 conference 페이지를 복사해 새 파일을 만든다.
3. `<title>`, 상단 제목, theme, 날짜/시간, moderator, 대표 이미지, speaker 섹션, 버튼 링크, alt text를 수정한다.
4. `Pages/conferences.html`을 갱신한다.
5. 최신 회차라면 `index.html`도 함께 갱신한다.
6. 이미지 경로와 링크가 맞는지 다시 확인한다.

#### 함께 바꿔야 하는 항목

- `Pages/conferences.html`
- `index.html`
- 관련 이미지 경로
- 필요 시 `README.md`

#### 추가 규칙

- 회차 번호는 파일명 앞에 둔다.
- 대표 포스터는 `main`을 사용한다.
- speaker 포스터는 `speaker-1`, `speaker-2`, `speaker-3` 순으로 둔다.
- `main+`이 있으면 보조 포스터로만 사용한다.
- speaker 포스터에 이미 들어 있는 문구는 본문에서 반복하지 않는다.

### 5.2 Call for Speakers 페이지

#### 위치

- 상세 페이지: `Pages/CallForSpeakers/<slug>.html`
- 이미지: `images/call-for-speakers/`

#### 함께 바꿔야 하는 항목

- `Pages/call-for-speakers.html`
- `index.html`
- 관련 이미지 경로
- 신청 이메일 또는 등록 링크

#### 추가 규칙

- 공개 모집인지, 종료된 공지인지 상태를 본문에서 명확히 표시한다.
- 한 페이지에는 하나의 핵심 모집 주제만 둔다.
- CTA 버튼은 신청 링크와 연결한다.

### 5.3 Event 페이지

#### 위치

- 상세 페이지: `Pages/<event-slug>.html`
- 이미지: `images/events/<event-slug>/`

현재 저장소에서는 팀 워크숍 같은 이벤트가 이 방식으로 관리된다.

#### 함께 바꿔야 하는 항목

- `Pages/about.html`
- `index.html`
- 관련 이미지 경로
- 필요 시 이벤트 내부 소개 링크

#### 추가 규칙

- 이벤트는 conference와 달리 목록형 아카이브가 없을 수 있다.
- 행사 성격에 따라 About 하위의 보조 페이지처럼 연결한다.
- 이벤트가 커뮤니티 운영 맥락을 갖는 경우 설명을 길게 쓰기보다 목적과 결과를 분명히 쓴다.

## 6. 페이지 구성 규칙

### 6.1 Conference 구성

권장 순서:

1. 제목
2. 테마
3. 날짜와 시간
4. 대표 이미지
5. Event Details
6. Conference Overview
7. Speaker 섹션
8. 보조 포스터 또는 아카이브 이미지
9. Back 링크

규칙:

- speaker 수와 섹션 수는 같아야 한다.
- speaker 소개와 topic 설명은 분리한다.
- `Event Details`와 speaker 섹션 사이에 `Conference Overview`를 두고, 이 회차가 왜 중요한지 짧게 설명한다.
- 아카이브 페이지는 과거 행사임을 명시한다.
- 최신 conference는 홈과 목록에서 우선 노출한다.
- 문자가 깨진 흔적이 있으면 수정 작업 중에 함께 바로잡는다.
- speaker가 1명이어도 overview와 맥락 설명은 생략하지 않는다.

### 6.2 Call for Speakers 구성

권장 순서:

1. 제목
2. 테마 설명
3. 공개 상태
4. 대표 이미지
5. Theme Overview
6. 모집 포인트 또는 질문 목록
7. Event Format
8. CTA 버튼
9. Back 링크

규칙:

- 제목은 "Call for Speakers" 형식을 유지한다.
- 소개는 참가자가 무엇을 제안할 수 있는지 중심으로 쓴다.
- 신청 방식은 버튼이나 명확한 링크로 끝낸다.

### 6.3 Event 구성

권장 순서:

1. 제목
2. 이벤트 성격 또는 목적
3. 대표 이미지
4. 요약 소개
5. 주요 장면, 결과, 기록
6. 왜 중요한지 또는 다음 단계
7. Back 링크

규칙:

- 이벤트는 성격에 따라 조직 내부 기록, 커뮤니티 활동, 워크숍으로 분리해 설명한다.
- 사진이 많으면 먼저 대표 이미지를 두고 다음에 갤러리를 둔다.
- 결과나 배운 점이 있으면 마지막 섹션에 정리한다.

## 7. 변경 매트릭스

새 페이지를 추가할 때 기본적으로 아래를 확인한다.

### Conference

- `Pages/Conference/conference-XX.html`
- `Pages/conferences.html`
- `index.html`
- `images/conferences/XX/`
- 링크와 alt text

### Call for Speakers

- `Pages/CallForSpeakers/<slug>.html`
- `Pages/call-for-speakers.html`
- `index.html`
- `images/call-for-speakers/`
- 등록 또는 신청 링크

### Event

- `Pages/<event-slug>.html`
- `Pages/about.html`
- `index.html`
- `images/events/<event-slug>/`
- 관련 설명 페이지

## 8. 파일명과 경로 규칙

- 폴더명과 파일명은 실제 내용과 일치해야 한다.
- 회차형 페이지는 숫자를 앞에 둔다.
- slug는 가능하면 소문자와 하이픈만 사용한다.
- 대소문자 오타는 링크 깨짐의 원인이므로 작업 후 반드시 확인한다.

## 9. 작업 체크리스트

새 페이지나 수정 작업 후 아래를 확인한다.

- [ ] 페이지 타입이 맞는가
- [ ] 파일 위치가 spec에 맞는가
- [ ] 관련 목록 페이지를 같이 바꿨는가
- [ ] 홈 노출이 필요하면 반영했는가
- [ ] 이미지 경로가 맞는가
- [ ] 로컬 `src` / `href`가 실제 파일을 가리키는가
- [ ] 누락된 로컬 파일 참조가 없는가
- [ ] menu link가 깨지지 않는가
- [ ] back link가 있는가
- [ ] speaker 수와 섹션 수가 맞는가
- [ ] event/call-for-speakers/conference의 역할이 섞이지 않았는가

## 10. 운영 원칙

- 새 작업을 시작할 때는 이 문서를 먼저 본다.
- 임시 점검, audit, tracker, diagnosis, qa 성격의 보조 문서는 GitHub로 올리지 않고 작업이 끝나면 삭제한다.
- 장기 기준이 필요한 내용만 별도 spec 또는 유지할 문서로 남긴다.
- conference 작업은 이 문서의 conference 섹션과 체크리스트를 기준으로 진행한다.
