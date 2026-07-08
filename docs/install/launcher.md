---
title: 설치와 업데이트
---

# 설치와 업데이트

최초 설치와 기본 설정은 기존 PPT 설정 가이드가 가장 잘 정리되어 있습니다.

[설정 가이드 열기](https://docs.google.com/presentation/d/1iA6vzvoBJPdn_FnCCv4HwOVrhrgPSv4OAhWop-rcqAo/present?usp=sharing){ .md-button .md-button--primary }

이 페이지는 PPT를 본 뒤, 런처와 GGO CE 업데이트 흐름을 다시 확인할 때 쓰는 보조 문서입니다.

## 권장 흐름

1. PPT 설정 가이드대로 기본 설치와 접속 설정을 완료합니다.
2. GGO Custom Launcher를 실행합니다.
3. GGO CE 설치 위치를 선택합니다.
4. 런처의 업데이트 안내에 따라 필요한 파일을 받습니다.
5. 실행 전 프로필과 서버 접속 정보를 확인합니다.

## 업데이트 기준

GGO CE의 실제 버전은 `ClassicUO.exe`가 아니라 `cuo.dll`의 파일 버전을 기준으로 판단합니다. 런처는 배포 manifest에 포함된 파일의 존재 여부와 해시를 검사해 누락되거나 달라진 파일만 교체합니다.

!!! warning "원본 ClassicUO 폴더 주의"
    기존 ClassicUO 설치 폴더를 그대로 업데이트 대상으로 쓰기 전에는 백업을 권장합니다. GGO CE는 별도 폴더에 설치하는 편이 가장 안전합니다.

## 관련 링크

- [문제 해결](troubleshooting.md)
- [피드백 보내기](../support/feedback.md)
