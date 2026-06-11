---
title: "임베디드 개발 블로그를 시작합니다"
date: 2026-06-11T11:49:15+09:00
draft: false
description: "임베디드와 시스템 소프트웨어 학습 과정을 오래 남기기 위해 기술 블로그를 시작합니다."
tags: ["Embedded", "Linux", "C"]
categories: ["Embedded"]
series: ["블로그 운영"]
ShowToc: true
TocOpen: false
---

안녕하세요. C/C++ 임베디드와 Linux 시스템 소프트웨어를 공부하며 배운 것과 문제를 해결한 과정을 기록하기 위해 블로그를 시작합니다.

<!--more-->

## 무엇을 기록하나요?

- C/C++ 코드가 하드웨어에서 동작하는 과정
- Linux Kernel과 디바이스 드라이버 학습 기록
- 펌웨어와 바이너리를 분석하는 과정
- Raspberry Pi와 Embedded Linux 프로젝트
- 문제를 재현하고 원인을 좁혀 해결하는 과정

완성된 답만 옮기기보다, **왜 이 방법을 선택했는지**를 함께 적으려 합니다.

## 블로그 구성

이 블로그는 [Hugo](https://gohugo.io/)와 GitHub Pages로 만들어졌습니다. 글은 Markdown으로 작성하고, `master` 브랜치에 변경 사항을 올리면 GitHub Actions가 사이트를 자동으로 빌드하고 배포합니다.

```bash
hugo new content posts/my-first-post.md
hugo server -D
```

천천히, 그러나 꾸준히 채워가겠습니다.
