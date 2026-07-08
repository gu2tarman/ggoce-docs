---
title: 문서 편집 방법
---

# 문서 편집 방법

이 문서 사이트는 Markdown 파일을 수정하면 웹페이지가 자동으로 갱신되는 방식입니다.

## 추천: Pages CMS 웹 편집

Markdown을 직접 다루는 것보다 웹 화면에서 글을 작성하고 이미지를 업로드하는 방식이 편하다면 Pages CMS를 사용합니다.

1. 문서 폴더를 GitHub 저장소로 올립니다.
2. [Pages CMS](https://app.pagescms.org)에 접속합니다.
3. GitHub로 로그인합니다.
4. 문서 저장소에 Pages CMS GitHub App을 설치합니다.
5. 저장소를 열고 `GGO CE 위키`, `스크립트 가이드`, `지원/운영 문서`를 웹에서 편집합니다.

이미지는 웹 UI에서 업로드하면 아래 폴더에 저장됩니다.

```text
docs/assets/images/
```

!!! warning "이미지 URL 기준"
    현재 `.pages.yml`은 문서 사이트가 `https://docs.example.com/`처럼 도메인 루트에서 서비스되는 것을 기준으로 이미지 경로를 씁니다. GitHub Pages 프로젝트 경로인 `https://owner.github.io/ggoce-docs/`로 운영할 경우 `.pages.yml`의 `media.output`을 `/ggoce-docs/assets/images`로 바꿔 주세요.

## 바로 편집하는 방식

1. `ggoce-docs/docs/` 안의 `.md` 파일을 엽니다.
2. 내용을 수정하고 저장합니다.
3. 로컬 미리보기 페이지를 새로고침합니다.

로컬 서버를 `mkdocs serve`로 실행 중이면 저장할 때마다 사이트가 다시 빌드됩니다.

## 스크린샷 추가

스크린샷은 아래 폴더에 넣습니다.

```text
ggoce-docs/docs/assets/images/
```

예를 들어 파일을 이렇게 저장했다면:

```text
ggoce-docs/docs/assets/images/grid-view-search.png
```

문서에는 이렇게 넣습니다.

```markdown
![그리드 뷰 검색 예시](../assets/images/grid-view-search.png)
```

하위 폴더가 깊은 페이지에서는 `../` 개수가 달라질 수 있습니다. CE 문서처럼 `docs/ce/` 아래에 있는 파일에서는 보통 다음처럼 씁니다.

```markdown
![HUD 스탯바 예시](../assets/images/hud-statbar.png)
```

## 크기 조절

이미지가 너무 크면 폭을 지정할 수 있습니다.

```markdown
![오토루팅 요약 검프](../assets/images/auto-loot-summary.png){ width="720" }
```

## 캡션 넣기

간단한 캡션이 필요하면 HTML figure를 사용합니다.

```markdown
<figure markdown="span">
  ![GGO 체력바](../assets/images/ggo-healthbar.png){ width="520" }
  <figcaption>파티원과 펫을 위한 GGO 체력바 스킨</figcaption>
</figure>
```

## 추천 파일 이름

파일 이름은 영문 소문자와 하이픈을 권장합니다.

```text
grid-view-search.png
auto-loot-summary.png
hud-statbar-tooltip.png
ggo-healthbar-click-menu.png
```

한글 파일명도 동작할 수 있지만, GitHub Pages나 브라우저 링크에서 깨지는 일을 줄이려면 영문 파일명이 안전합니다.

## 웹 관리자 화면이 필요한 경우

브라우저에서 글을 쓰고 이미지를 업로드하는 관리자 화면이 필요하면 Decap CMS 같은 Git 기반 CMS를 붙일 수 있습니다. 이 경우 `/admin/` 페이지에서 로그인하고, 글 수정과 이미지 업로드를 웹에서 처리하는 구조가 됩니다.
