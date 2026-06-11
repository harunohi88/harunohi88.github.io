---
title: "프로젝트"
description: "임베디드와 시스템 소프트웨어 프로젝트의 문제 해결 과정과 결과를 정리합니다."
type: "projects"
ShowToc: true
TocOpen: false
hideMeta: true
disableShare: true
---

프로젝트는 완성된 결과보다 **문제 정의, 기술적 선택, 검증 과정과 배운 점**을 중심으로 정리합니다.
아래 카드는 현재 학습 로드맵이며 진행하면서 GitHub 저장소와 관련 포스트를 연결할 예정입니다.

{{< project-card
  title="Linux Kernel Module Project"
  status="계획"
  summary="커널 모듈과 문자 디바이스 드라이버를 구현하며 사용자 공간과 커널 공간의 상호작용을 학습합니다."
  tech="C · Linux Kernel · Kbuild · QEMU · GDB"
  problem="모듈 생명주기, 동시성, 사용자 메모리 접근과 커널 디버깅 과정을 실험으로 검증합니다."
  learned="커널 API 사용법과 안전한 드라이버 설계 원칙을 정리합니다."
  github=""
  posts="/tags/kernel/"
>}}

{{< project-card
  title="AVR Firmware Analysis"
  status="계획"
  summary="AVR 펌웨어를 빌드하고 디스어셈블하여 C 코드가 실제 명령어와 메모리 구조로 변환되는 과정을 분석합니다."
  tech="C · AVR-GCC · avr-objdump · Ghidra · simavr"
  problem="레지스터, 인터럽트, 스택과 최적화 옵션에 따른 바이너리 차이를 추적합니다."
  learned="MCU 아키텍처와 컴파일 결과를 연결해 이해하는 능력을 기릅니다."
  github=""
  posts="/tags/firmware/"
>}}

{{< project-card
  title="Raspberry Pi Home Server"
  status="진행 예정"
  summary="Raspberry Pi 기반 홈 서버를 구축하고 서비스 운영, 스토리지와 네트워크 구성을 자동화합니다."
  tech="Raspberry Pi · Linux · Docker · systemd · Tailscale"
  problem="제한된 자원에서 안정적인 서비스 운영과 백업, 모니터링 체계를 구성합니다."
  learned="ARM Linux 환경과 실제 운영 장애에 대응하는 방법을 기록합니다."
  github=""
  posts="/tags/raspberrypi/"
>}}

{{< project-card
  title="Fedora Asahi Linux Development Environment"
  status="환경 구축"
  summary="Apple Silicon의 Fedora Asahi Linux에서 C/C++와 커널 개발을 위한 재현 가능한 환경을 구성합니다."
  tech="Fedora Asahi Remix · GCC · Clang · GDB · Podman"
  problem="ARM64 도구 체인, 디버거, 가상화와 패키지 구성을 표준화합니다."
  learned="아키텍처 차이를 고려한 Linux 개발 환경 구성 방법을 정리합니다."
  github=""
  posts="/tags/developmentenvironment/"
>}}

{{< project-card
  title="Embedded Linux Study"
  status="학습 중"
  summary="부트 과정부터 루트 파일 시스템과 디바이스 트리까지 Embedded Linux 전체 흐름을 단계별로 학습합니다."
  tech="C · U-Boot · Linux Kernel · Device Tree · Buildroot · QEMU"
  problem="부트로더, 커널, 사용자 공간이 연결되는 과정을 직접 빌드하고 관찰합니다."
  learned="임베디드 Linux 시스템을 구성 요소 단위로 분석하고 문제를 진단합니다."
  github=""
  posts="/categories/embedded/"
>}}
