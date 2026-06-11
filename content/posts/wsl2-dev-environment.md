---
title: "WSL2 개발 환경에서 자주 쓰는 기본 설정"
date: 2026-06-09T20:00:00+09:00
draft: false
description: "Windows와 WSL2를 함께 사용할 때 프로젝트 성능과 권한 문제를 줄이는 기본 원칙입니다."
tags: ["wsl2", "ubuntu", "development"]
categories: ["환경 설정"]
---

WSL2는 Windows에서 Linux 개발 환경을 편리하게 제공하지만, 파일 위치와 도구 설치 방식에 따라 체감 성능이 크게 달라집니다.

<!--more-->

## 프로젝트는 Linux 파일 시스템에 둡니다

Node.js처럼 작은 파일을 많이 읽는 도구는 `/mnt/c`보다 WSL의 홈 디렉터리에서 훨씬 빠르게 동작합니다.

```bash
mkdir -p ~/workspace
cd ~/workspace
```

Windows 탐색기에서는 `\\wsl.localhost\배포판이름\home\사용자명` 경로로 접근할 수 있습니다.

## 도구는 WSL 안에 설치합니다

프로젝트를 WSL에서 실행한다면 Git, Hugo, Node.js 같은 도구도 WSL에 설치해야 경로와 권한 문제를 피할 수 있습니다.

```bash
which git
which hugo
git config --global core.autocrlf input
```

## 점검할 것

- 저장소가 Linux 홈 디렉터리에 있는가
- 에디터가 WSL 확장 환경으로 열렸는가
- 빌드 명령이 Windows가 아닌 WSL 바이너리를 사용하는가
- Git 줄바꿈 설정이 `input`인가

환경을 단순하게 유지하면 개발과 CI 환경의 차이도 줄어듭니다.
