# harunohi.dev

Hugo와 GitHub Pages로 운영하는 개발 블로그입니다. `master` 또는 `main` 브랜치에 변경 사항을 푸시하면 GitHub Actions가 사이트를 빌드하고 자동 배포합니다.

## 로컬 실행

```bash
hugo server -D
```

브라우저에서 `http://localhost:1313`을 엽니다. `-D` 옵션은 초안 글도 함께 표시합니다.

## 새 글 작성

```bash
hugo new content posts/my-post.md
```

생성된 파일의 Front Matter를 채우고 글을 작성합니다.

```yaml
---
title: "글 제목"
date: 2026-06-11T20:00:00+09:00
draft: false
description: "목록과 검색 결과에 표시할 요약"
tags: ["hugo", "github-pages"]
categories: ["DevOps"]
---
```

본문에 `<!--more-->`를 넣으면 그 앞부분이 목록의 요약으로 사용됩니다.

## 배포 전 확인

```bash
hugo --gc --minify
```

빌드가 성공하면 변경 사항을 커밋하고 원격 저장소에 푸시합니다. 배포 결과는 저장소의 **Actions** 탭에서 확인할 수 있습니다.

## 주요 파일

- `hugo.toml`: 사이트 정보, 메뉴, PaperMod 기능 설정
- `content/posts/`: 블로그 글
- `content/about.md`: 소개 페이지
- `content/projects.md`: 프로젝트 페이지
- `assets/css/extended/custom.css`: 커스텀 디자인
- `archetypes/default.md`: 새 글 기본 템플릿
- `.github/workflows/hugo.yaml`: GitHub Pages 자동 배포

## 개인화

배포 전에 다음 값을 실제 정보에 맞게 수정합니다.

- `hugo.toml`의 사이트 제목, 설명, 소셜 링크
- `content/about.md`의 소개와 연락처
- `content/projects.md`의 프로젝트 목록
