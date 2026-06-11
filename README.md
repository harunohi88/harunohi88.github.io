# harunohi devlog

C/C++ 임베디드, Linux Kernel, 펌웨어, Raspberry Pi와 리버스 엔지니어링 학습을 기록하는 Hugo + PaperMod 기술 블로그입니다.

`master` 또는 `main` 브랜치에 변경 사항을 푸시하면 GitHub Actions가 사이트를 빌드하고 GitHub Pages에 자동 배포합니다.

## 로컬 실행

```bash
hugo server -D
```

브라우저에서 `http://localhost:1313`을 엽니다. `-D` 옵션은 `draft: true`인 초안도 표시합니다.

## 새 포스트 작성

```bash
hugo new content posts/linux-kernel-module-basics.md
```

`archetypes/posts.md`를 기반으로 `content/posts/` 아래에 파일이 생성됩니다.

Front Matter 예시:

```yaml
---
title: "Linux Kernel Module 시작하기"
date: 2026-06-11T20:00:00+09:00
draft: true
description: "간단한 커널 모듈을 빌드하고 로드하는 과정을 정리합니다."
tags:
  - Linux
  - Kernel
  - C
categories:
  - Kernel
series:
  - Linux Kernel Study
cover:
  image: ""
  alt: ""
  caption: ""
  relative: true
ShowToc: true
TocOpen: false
---
```

작성 중에는 `draft: true`를 유지합니다. 공개할 때 `draft: false`로 바꿉니다.

본문의 `<!--more-->` 앞부분은 글 목록의 요약으로 사용됩니다.

## 프로젝트 작성

프로젝트 상세 문서가 필요하면 다음 명령을 사용합니다.

```bash
hugo new content projects/my-project.md
```

`archetypes/projects.md`에는 프로젝트 개요, 사용 기술, 문제 해결 과정, 배운 점과 링크 구조가 포함되어 있습니다.

메인 Projects 페이지의 카드는 `content/projects.md`에서 `project-card` shortcode로 관리합니다.

## 권장 taxonomy

- Categories: `Linux`, `Kernel`, `Embedded`, `Firmware`, `RaspberryPi`, `ReverseEngineering`, `HomeServer`, `DevelopmentEnvironment`
- Tags: 위 분류와 함께 `C`, `C++`, 사용한 도구와 보드 이름
- Series: `Linux Kernel Study`, `AVR Firmware Analysis`처럼 연속된 학습 기록

같은 개념은 대소문자와 띄어쓰기를 통일해서 사용합니다.

## 배포 절차

```bash
hugo --gc --minify
git add .
git commit -m "post: Linux Kernel Module 시작하기"
git push origin master
```

배포 상태는 GitHub 저장소의 **Actions** 탭에서 확인합니다.

## 주요 파일

- `hugo.toml`: PaperMod, 메뉴, taxonomy, 검색과 SEO 설정
- `content/posts/`: 블로그 포스트
- `content/projects.md`: 프로젝트 포트폴리오
- `content/about.md`: 소개 페이지
- `archetypes/posts.md`: 새 포스트 템플릿
- `archetypes/projects.md`: 프로젝트 상세 문서 템플릿
- `layouts/index.json`: Fuse.js 검색 인덱스
- `assets/css/extended/custom.css`: 커스텀 디자인
- `.github/workflows/hugo.yaml`: GitHub Pages 자동 배포

`public/`은 빌드 결과이므로 커밋하지 않습니다.
