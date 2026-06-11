---
title: "개발 블로그를 시작합니다"
date: 2026-06-11T11:49:15+09:00
draft: false
description: "배운 것을 오래 남기기 위해 기술 블로그를 시작합니다."
tags: ["blog", "hugo"]
categories: ["회고"]
---

안녕하세요. 개발 과정에서 배운 것과 문제를 해결한 과정을 기록하기 위해 블로그를 시작합니다.

<!--more-->

## 무엇을 기록하나요?

- 문제를 마주쳤을 때 원인을 찾아가는 과정
- 다시 사용할 수 있는 설정과 코드
- 프로젝트를 진행하며 내린 기술적 결정
- 시간이 지난 뒤 돌아보는 회고

완성된 답만 옮기기보다, **왜 이 방법을 선택했는지**를 함께 적으려 합니다.

## 블로그 구성

이 블로그는 [Hugo](https://gohugo.io/)와 GitHub Pages로 만들어졌습니다. 글은 Markdown으로 작성하고, `master` 브랜치에 변경 사항을 올리면 GitHub Actions가 사이트를 자동으로 빌드하고 배포합니다.

```bash
hugo new content posts/my-first-post.md
hugo server -D
```

천천히, 그러나 꾸준히 채워가겠습니다.
