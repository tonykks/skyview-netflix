# Tony Skyview — 제주 드론 아카이브 (단일 페이지)

## 프로젝트 소개

제주 일대를 **드론으로 촬영한 장면**을 모아, **넷플릭스 메인 화면처럼 어둡고 카드형**으로 보여 주는 **HTML/CSS 입문 과제**용 페이지입니다.  
실제 영상 재생·별도 하위 페이지는 없고, **`index.html` 하나**로 레이아웃과 내비게이션(앵커)만 구성했습니다.

## 파일 구성

| 파일·폴더 | 역할 |
|-----------|------|
| `index.html` | 전체 구조(헤더, 히어로, 추천·최신 섹션, 푸터) |
| `styles.css` | 스타일·반응형(미디어 쿼리) |
| `images/` | 배너·카드·헤더 장식용 이미지 |

### `images`에 두는 파일 예시

- 배너: `songak.png`
- 헤더 별빛: `star_light.png`
- **추천** 카드: `sea_cave.jpg`, `daepo.jpg`, `sungsan.jpg`, `tiger_island.jpg`, `tafoni.jpg` 등
- **최신** 카드: `daryeodo-heron.jpg`, `munseom-columns.jpg`, `chagwido-rocks.jpg`, `seopseom.jpg`, `sanbang-mountain.jpg` 등  

파일명은 `index.html`의 `src`와 일치해야 합니다.

## 사용 기술

- **HTML5** — `header`, `main`, `section`, `nav`, `footer`, `article`, 섹션 `id`(`recommended`, `latest`)
- **CSS3** — 플렉스, 그리드(헤더), 그라데이션(`::after`), 호버, `text-shadow`, 미디어 쿼리(768px 이하)
- **JavaScript 없음** — 링크는 `index.html`, `#recommended`, `#latest`, `#` 등만 사용

## 화면 구성 (위에서 아래 순)

| 영역 | 내용 |
|------|------|
| **헤더** | 로고(`TONY SKYVIEW` → `index.html`), 부제(SkyViewism 문구), 영문 모토 + `star_light.png`, **메뉴**(홈·최근 업로드·추천·장소별·About) |
| **히어로** | 대표 이미지 `songak.png`, 뱃지·제목·3줄 설명·메타·**재생 / 상세 정보** 버튼(`href="#"`) |
| **추천 드론 영상** | `id="recommended"` — 카드 5개 |
| **최신 드론 영상** | `id="latest"` — 카드 5개(별도 장소·파일명) |
| **푸터** | `© 2026 Tony Skyview. Drone Archive of Jeju.` |

### 내비게이션(같은 페이지 내 이동)

- **홈** → `index.html`
- **최근 업로드** → `#latest`
- **추천 영상** → `#recommended`
- **장소별 보기**, **About** → `#`(추후 확장용)

`styles.css`의 `#recommended`, `#latest`에 `scroll-margin-top`을 두어 앵커 이동 시 제목이 잘 보이도록 했습니다.

### 반응형 요약

- **769px 이상**: 배너 이미지는 비율 유지(`height: auto`).
- **768px 이하**: 배너 높이 고정 + `object-fit: cover`, 글자·패딩 축소, 카드 한 열 위주.

## 과제 제출 정리(최종)

- **새 HTML 페이지**(`about.html` 등)는 만들지 않음.
- 임시 `about:blank` 링크는 **평가 혼란 방지**를 위해 **`index.html` / `#` / 앵커**로 정리.
- 구조는 **header → hero → 추천 → 최신 → footer** 유지.

## 실행 방법

1. 이 폴더를 그대로 둔다.
2. **`index.html`**을 브라우저로 연다(더블클릭 또는 파일 열기).
3. `styles.css`와 `images`가 같은 위치에 있어야 한다.

서버·빌드·npm은 필요 없습니다.

## 느낀 점

한 페이지만으로도 **섹션 `id` + 메뉴 링크**만으로 “이동하는 사이트” 느낌을 낼 수 있다는 점이 과제 정리에 도움이 되었습니다. 배너는 **화면 너비에 따라 규칙을 나누는 것**이 데스크톱·모바일 모두 보기 편했습니다.

---

## 프롬프트·수정 이력(요약)

넷플릭스 느낌의 단일 페이지, 시맨틱 태그, 카드 5개, 모바일 미디어 쿼리, 히어로·모토·별 이미지, 추천/최신 두 줄, `id`·내비·푸터 문구 정리, README·커밋 요청 등 — 대화 과정에서 단계적으로 반영했습니다.
