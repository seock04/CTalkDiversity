# CTalkDiversity

Cultural Talk For Diversity를 위한 정적 웹사이트 저장소입니다.

이 사이트는 다음 목적을 위해 운영됩니다:
- **조직/커뮤니티 소개**
- **지난 Cultural Talk 행사 아카이브 정리**
- **Call for Speakers 공지 및 참여 유도**

현재 구조는 HTML5 UP 템플릿을 기반으로 한 **정적 HTML 사이트**이며, 행사와 공지 콘텐츠를 점진적으로 축적하고 개선해나가는 것을 목표로 합니다.

---

## 1. 사이트 개요

CTalkDiversity는 문화와 DEI(Diversity, Equity, Inclusion)를 중심으로 한 대화와 커뮤니티 활동을 소개하는 웹사이트입니다.

현재 사이트는 크게 세 종류의 정보를 담고 있습니다:
- **About / Organization**
- **Conferences / Cultural Talk 기록**
- **Call for Speakers / 참여 공지**

이 저장소의 핵심 과제는 단순히 페이지를 추가하는 것이 아니라,
**사이트를 점점 더 효율적으로 운영할 수 있는 구조로 발전시키는 것**입니다.

---

## 2. 기술 성격

이 프로젝트는 현재 다음 특징을 가집니다:
- 정적 HTML 기반 사이트
- 공통 스타일/스크립트는 `assets/`에서 관리
- 이미지 자산은 `images/`, `Conferences/`, `CallForSpeakers/`에 보관
- 별도 백엔드 없음
- 로컬 정적 서버 또는 GitHub Pages 류의 환경에 적합

즉, 현재는 **간단하고 배포가 쉬운 구조**를 유지하고 있습니다.

---

## 3. 주요 폴더 구조

```text
CTalkDiversity/
  index.html
  Pages/
    about.html
    conferences.html
    call-for-speakers.html
    Conference/
    CallForSpeakers/
  Conferences/
    1/
    2/
    ...
    26/
  CallForSpeakers/
  assets/
    css/
    js/
    sass/
    webfonts/
  images/
  README.md
  README.txt
```

### 폴더 설명

- `index.html`
  - 메인 랜딩 페이지

- `Pages/`
  - 실제 상세 페이지 모음
  - About, Conferences, Call for Speakers 및 개별 상세 페이지 포함

- `Pages/Conference/`
  - 각 회차별 Cultural Talk 상세 페이지

- `Pages/CallForSpeakers/`
  - 발표자 모집 상세 페이지

- `Conferences/`
  - 행사 관련 이미지 자산

- `CallForSpeakers/`
  - 발표자 모집 관련 이미지 자산

- `assets/`
  - CSS, JS, 폰트 등 공통 템플릿 자산

- `images/`
  - 로고, 소개 이미지, 공통 이미지

- `README.txt`
  - 원본 HTML5 UP 템플릿 설명 파일

---

## 4. 주요 페이지 구성

### 홈
- `index.html`
- 최신 conference, 최근 call for speakers, organization 소개를 노출

### 조직 소개
- `Pages/about.html`
- About / Purpose / Mission / Vision 소개

### 행사 목록
- `Pages/conferences.html`
- 지난 행사 목록 및 링크 정리

### 행사 상세
- `Pages/Conference/conference-1.html` ~ `Pages/Conference/conference-26.html`
- 현재 1~26회 상세 페이지가 모두 존재하며, `Pages/conferences.html`에서 목록으로 연결됨

### 발표자 모집
- `Pages/call-for-speakers.html`
- 개별 상세 페이지는 `Pages/CallForSpeakers/` 아래 관리

---

## 5. 콘텐츠를 추가할 때 기본 원칙

현재는 수작업 중심 구조이므로, 새 콘텐츠를 추가할 때 다음 항목을 함께 점검해야 합니다.

conference upcoming 반영과 archive 전환 계획은 [`Specification/conference-operations-plan.md`](./Specification/conference-operations-plan.md)에서 따로 관리합니다.
call for speakers open call 반영과 archive 전환 계획은 [`Specification/call-for-speakers-operations-plan.md`](./Specification/call-for-speakers-operations-plan.md)에서 따로 관리합니다.

### 새 call for speakers 추가 시
일반적으로 다음 수정이 필요합니다:
- `Pages/CallForSpeakers/` 아래 새 상세 페이지 추가
- `Pages/call-for-speakers.html` 목록 갱신
- 필요 시 `index.html` 메인 노출 갱신
- 관련 이미지 자산 추가
- 링크 및 문구 점검

---

## 6. 현재 운영상 중요 과제

이 프로젝트는 이미 동작하는 정적 사이트이지만, 앞으로 다음 과제가 중요합니다:

1. **README 및 운영 문서 정리**
2. **conference / call-for-speakers 추가 규칙 표준화**
3. **이미지/파일 네이밍 일관성 확보**
4. **링크/구조/UI 점검 체계 만들기**
5. **장기적으로 더 효율적인 정적 사이트 구조 검토**

즉, 목표는 단순 유지가 아니라
**사이트 운영을 점점 더 효율적이고 안정적으로 만드는 것**입니다.

---

## 7. 참고

- `README.txt`는 HTML5 UP 원본 템플릿 설명 파일입니다.
- 이 `README.md`는 CTalkDiversity 프로젝트 자체를 설명하기 위한 운영 문서입니다.

---

## 8. 현재 방향

CTalkDiversity는 단순한 정적 페이지 모음이 아니라,
**지속적으로 콘텐츠를 축적하고 개선해나갈 수 있는 문화/DEI 커뮤니티 웹사이트**로 발전시키는 방향을 목표로 합니다.

따라서 앞으로의 작업은:
- 보기 좋게 만드는 것
- 추가하기 쉽게 만드는 것
- 실수 없이 운영하기 쉽게 만드는 것

이 세 가지를 함께 잡는 방향으로 진행합니다.
