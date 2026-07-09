---
title: 렌더러와 표시 버전
---

# 렌더러와 표시 버전

그래픽 렌더러 선택과 GGO CE 버전 표시 관련 기능입니다.

## 그래픽 렌더러 선택

`Options → GGO Custom → 그래픽 렌더러`

- Auto
- OpenGL
- Vulkan
- DirectX 11

렌더러 변경은 클라이언트 재시작 후 적용됩니다.

## GGO CE 표시 버전

GGO CE는 창 제목과 로그인 화면 하단에 GGO CE 버전을 표시합니다.

```text
CUO GGO CE - 1.6.1.4
```

## 업데이트 감지 기준

런처는 `ClassicUO.exe`가 아니라 `cuo.dll`의 파일 버전을 기준으로 업데이트 여부를 판단합니다.

## 제보 포인트

- 옵션에서 DirectX 11을 골랐는데 재시작 후 적용되지 않는 경우
- 창 제목 또는 로그인 화면 버전이 런처 표시와 다른 경우
- 원본 ClassicUO 폴더와 GGO CE 폴더가 섞인 것으로 의심되는 경우
