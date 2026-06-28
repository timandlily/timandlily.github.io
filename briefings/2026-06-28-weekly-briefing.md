---
title: "Weekly Research Briefing: 2026-06-28"
date: 2026-06-28
summary: "이번 주 CTI, SCADA, 디지털 포렌식 연구 동향 요약"
authors:
  - me
tags:
  - CTI
  - Digital Forensics
  - SCADA
  - Weekly Briefing
cover:
  image: "https://images.unsplash.com/photo-1550751827-4bd374c3f58b"
---

## 📄 신규 논문

### 1. Forensic Implications of Localized AI: Artifact Analysis of Ollama, LM Studio, and llama.cpp

- **저자:** Shariq Murtuza
- **출처:** arXiv cs.CR, 2026년 3월 25일 | https://arxiv.org/abs/2603.23996
- **핵심 기여:** 로컬 LLM 실행 환경(Ollama, LM Studio, llama.cpp)이 생성하는 포렌식 아티팩트를 Windows/Linux에서 체계적으로 분석하여 JSON 형식의 plaintext 프롬프트 이력, 모델 사용 로그, 고유 파일 시그니처 등 이전에 문서화되지 않은 증거 위치와 특성을 발굴함. 오프라인 AI 환경이 기존 포렌식 방법론에 새로운 사각지대를 형성한다는 점을 실증함.

---

### 2. Synthetic APTs: the Collapse of TTP-Based Attribution

- **저자:** Francesco Balassone, Víctor Mayoral-Vilches, María Sanz-Gómez, Paul Zabalegui-Landa
- **출처:** arXiv cs.CR, 2026년 6월 5일 | https://arxiv.org/abs/2606.07158
- **핵심 기여:** AI 기반 적대자 에뮬레이션이 TTP 지문(fingerprint)의 신뢰성을 근본적으로 위협한다는 것을 실증함. 기존 CTI 귀속(attribution) 방법론이 AI로 생성된 합성 APT에 의해 무력화될 수 있음을 보여줌.

---

### 3. AURA: A Multi-Agent Intelligence Framework for Knowledge-Enhanced Cyber Threat Attribution

- **저자:** Nanda Rani, Sandeep Kumar Shukla (IIT Kanpur)
- **출처:** arXiv cs.CR, 2025년 6월 11일 제출 | https://arxiv.org/abs/2506.10175
- **핵심 기여:** TTP, IoC, 악성코드 정보 등을 입력받아 RAG 기반 다중 에이전트 협업으로 APT 그룹을 귀속하는 AURA 프레임워크를 제안함. 추적 가능한 추론 체계를 통해 귀속의 해석 가능성과 일관성을 향상시킴.

---

### 4. Agent Security is a Systems Problem

- **저자:** Google, UC San Diego, University of Wisconsin–Madison 외 공동 연구진
- **출처:** arXiv cs.CR, 2026년 5월 18일 | https://arxiv.org/abs/2605.18991
- **핵심 기여:** AI 에이전트 보안은 모델 강건성 향상만으로는 불충분하며, 시스템 수준의 보안 불변 조건 강제를 통해 해결해야 한다고 주장함. 실제 에이전트 공격 11건을 분석하여 시스템 보안 원칙을 적용할 경우 방어 가능했음을 논증함.

---

### 5. S-DAPT-2026: A Stage-Aware Synthetic Dataset for Advanced Persistent Threat Detection

- **출처:** arXiv, 2026년 1월 | https://arxiv.org/abs/2601.06690
- **핵심 기여:** APT 탐지를 위한 단계 인식(stage-aware) 합성 데이터셋을 제안함. 포렌식/탐지 모델 훈련용 합성 데이터 생성 방법론의 유효성을 검증하고, 실제 APT 공격 단계 패턴을 반영하는 데이터 구조를 정의함.

---

## 🔐 주요 보안 뉴스

### 1. CISA: Iranian-Affiliated Actors Exploit PLCs Across US Critical Infrastructure

- **출처:** CISA Cybersecurity Advisory AA26-097a | https://www.cisa.gov/news-events/cybersecurity-advisories/aa26-097a
- **요약:** 이란 연계 APT 행위자들이 인터넷 노출 Unitronics PLC 장치 75대 이상을 침해하여 미국 상수도 및 폐수 처리 등 다중 핵심 인프라 부문을 대상으로 HMI/SCADA 데이터 조작 시도. CISA는 즉각적인 패치 및 네트워크 분리를 권고함.

### 2. FortiBleed: 73,000+ FortiGate 장치 자격 증명 노출

- **출처:** SecurityWeek / Weekly Intelligence Briefing (2026-06-22) | https://www.securityweek.com/
- **요약:** 194개국 73,000~86,644대의 FortiGate 장치에 영향을 미치는 자격 증명 노출 사고(FortiBleed)가 확인됨. 일부 버전 트랙에서 확인된 패치 타임라인 없음, 즉각적인 노출 모니터링 필요.

### 3. Sapphire Sleet(DPRK) npm 공급망 공격: Mastra 캠페인

- **출처:** Weekly Security Intelligence Briefing 2026-06-22 | https://techjacksolutions.com/security/briefing/weekly-security-intelligence-briefing-week-of-2026-06-22/
- **요약:** 북한 연계 Sapphire Sleet 행위자가 `@mastra` npm 스코프의 140개 이상 패키지에 크로스플랫폼 인포스틸러를 삽입함. 소프트웨어 공급망을 통한 개발자 환경 침해 위협.

### 4. CISA ICS Advisory: pydicom pynetdicom Library 취약점 (ICSMA-26-176-01)

- **출처:** CISA ICS Medical Advisory, 2026년 6월 25일 | https://www.cisa.gov/news-events/ics-medical-advisories/icsma-26-176-01
- **요약:** 의료 영상 전송 라이브러리 pynetdicom v1.0.0~v3.0.4에서 비인증 공격자가 임의 파일 경로에 쓰기 가능한 취약점 발견. 전 세계 헬스케어 인프라에 영향, 즉각적인 업데이트 권고.

---

## 💡 이번 주 트렌드

이번 주 가장 두드러진 흐름은 **AI 에이전트·로컬 LLM의 보안 역할 반전**이다. LLM이 포렌식과 CTI 자동화에 활용되는 동시에, 오프라인 LLM 실행 환경 자체가 새로운 포렌식 증거 수집 과제가 되는 양면성이 확인됐다. 한편 **TTP 기반 귀속의 신뢰 위기**가 본격적으로 논문화되기 시작했다—합성 APT가 기존 귀속 방법론을 무력화한다는 주장은 CTI 분야 패러다임 전환 논의의 서막으로 볼 수 있다. SCADA/ICS 위협 측면에서는 이란 연계 PLC 침해와 의료 장비 라이브러리 취약점이 겹치며 OT/IoMT 보안의 취약성이 재확인됐다. 또한 npm 공급망을 통한 북한 행위자의 개발자 환경 침투가 지속되면서, 비인간 아이덴티티(NHI) 관리와 공급망 무결성 검증의 중요성이 부각되고 있다.

---

## ⭐ 주목 논문 1선

**"Synthetic APTs: the Collapse of TTP-Based Attribution"** (arXiv:2606.07158)

CTI 귀속 연구에서 사실상 불문율처럼 통용되던 "위협 행위자는 고유한 TTP 지문을 남긴다"는 전제를 정면으로 공격한다는 점에서 이 논문을 선정한다. AI 기반 적대자 에뮬레이션이 상용화되면 기존 MITRE ATT&CK 기반 귀속 파이프라인 전체가 흔들릴 수 있다는 함의는, CTI 및 디지털 포렌식 분야 연구자에게 방어 측 귀속 방법론의 근본적 재검토를 촉구한다. 특히 본 연구자의 CTI 연구 방향—LLM 기반 위협 귀속 자동화—과 직결되는 비판적 관점을 제공하므로 정독을 권한다.
