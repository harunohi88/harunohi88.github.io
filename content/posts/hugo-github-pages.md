---
title: "Hugo와 GitHub Pages로 블로그 배포하기"
date: 2026-06-10T20:00:00+09:00
draft: false
description: "Hugo 사이트를 GitHub Actions로 빌드하고 Pages에 자동 배포하는 흐름을 정리합니다."
tags: ["hugo", "github-actions", "github-pages"]
categories: ["DevOps"]
---

Hugo는 Markdown 콘텐츠를 빠르게 정적 HTML로 변환합니다. GitHub Actions와 연결하면 별도 서버 없이 커밋만으로 블로그를 배포할 수 있습니다.

<!--more-->

## 배포 흐름

1. 저장소를 체크아웃하고 테마 서브모듈을 가져옵니다.
2. Hugo Extended를 설치합니다.
3. `hugo --gc --minify`로 정적 파일을 생성합니다.
4. 생성된 `public` 디렉터리를 GitHub Pages에 배포합니다.

## 로컬에서 확인하기

초안까지 포함해 로컬 서버를 실행합니다.

```bash
hugo server -D
```

브라우저에서 `http://localhost:1313`을 열면 저장할 때마다 변경된 화면을 바로 확인할 수 있습니다.

## 새 글 작성하기

```bash
hugo new content posts/my-topic.md
```

작성 완료 후 Front Matter의 `draft`를 `false`로 바꾸면 배포 빌드에 포함됩니다. 배포 전에는 다음 명령으로 오류가 없는지 확인합니다.

```bash
hugo --gc --minify
```

> 테마가 Git 서브모듈이라면 Actions의 checkout 단계에 `submodules: recursive` 설정이 필요합니다.
