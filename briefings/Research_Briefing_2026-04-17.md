# 📋 Weekly Research Briefing — CTI / SCADA / Digital Forensics
**기준일:** 2026년 4월 17일 (금) | **수집 기간:** 2026년 4월 10일 ~ 4월 17일

---

## 📄 신규 논문

### 1. From IOCs to Regex: Automating CTI Operationalization for SOC with LLMs
- **저자:** (arXiv:2604.12228 — 저자 정보 arXiv 원문 참조)
- **출처:** arXiv — https://arxiv.org/abs/2604.12228
- **게재일:** 2026년 4월 14일
- **핵심 기여:** IOC(침해 지표)를 정규식으로 자동 변환하는 LLM 기반 시스템 IOCRegex-gen을 제안하며, 그룹 인식 메커니즘과 다단계 검증 파이프라인을 도입하였다. 3,000개 이상의 실제 CTI 보고서와 MITRE ATT&CK 평가 프레임워크를 대상으로 한 실험에서 99.1% 히트율과 0.8% 오탐률을 달성, SOC 운영의 CTI 실용화에 직접 기여한다.

---

### 2. Cross-Domain Query Translation for Network Troubleshooting: A Multi-Agent LLM Framework with Privacy Preservation and Self-Reflection
- **저자:** (arXiv:2604.13353 — 저자 정보 arXiv 원문 참조)
- **출처:** arXiv — https://arxiv.org/abs/2604.13353
- **게재일:** 2026년 4월 15일
- **핵심 기여:** 비기술 사용자와 네트워크 도메인 전문가 간의 커뮤니케이션 격차를 해소하기 위한 계층적 멀티에이전트 LLM 아키텍처를 제안한다. 프라이버시 보존 기법과 자기성찰(Self-Reflection) 기반 추론을 결합하여 사설 네트워크 환경의 보안 트러블슈팅을 자동화한다.

---

### 3. LLM-Enhanced Log Anomaly Detection: A Comprehensive Benchmark of Large Language Models for Automated System Diagnostics
- **저자:** (arXiv:2604.12218 — 저자 정보 arXiv 원문 참조)
- **출처:** arXiv — https://arxiv.org/html/2604.12218
- **게재일:** 2026년 4월 14일
- **핵심 기여:** 대규모 소프트웨어 시스템의 로그 이상 탐지를 위해 LLM 기반 접근법(GPT-3.5/4, LLaMA-3)과 전통적 방법(BERT, RoBERTa, 머신러닝 결합)을 종합 벤치마크로 비교한다. Zero-shot 및 Few-shot 설정에서 LLM의 산업 제어 시스템 적용 가능성을 실증적으로 평가한다.

---

### 4. Securing Retrieval-Augmented Generation: A Taxonomy of Attacks, Defenses, and Future Directions
- **저자:** (arXiv:2604.08304 — 저자 정보 arXiv 원문 참조)
- **출처:** arXiv — https://arxiv.org/html/2604.08304
- **게재일:** 2026년 4월 초 (수집 기간 근접)
- **핵심 기여:** RAG 시스템이 외부 지식 접근으로 인해 발생하는 보안 취약점을 체계적으로 분류한다. 데이터 포이즈닝, 적대적 공격, 멤버십 추론 공격 등의 위협 벡터를 분석하고, 동적 접근 제어·동형 암호화·연합 학습 기반 방어 체계를 제시한다.

---

### 5. Evaluating the Reliability of Digital Forensic Evidence Discovered by Large Language Model: A Case Study
- **저자:** (arXiv:2602.20202 — 저자 정보 arXiv 원문 참조)
- **출처:** arXiv — https://arxiv.org/abs/2602.20202
- **게재일:** 2026년 2월 (최근 관련 논문으로 포함)
- **핵심 기여:** LLM 기반 포렌식 아티팩트 추출 자동화 프레임워크와 Digital Forensic Knowledge Graph(DFKG)를 활용한 결과 검증 방법론을 제안한다. 아티팩트 추출 정확도 95% 이상을 달성하며 증거 연속성(chain-of-custody) 준수를 지원한다.

---

## 🔐 주요 보안 뉴스

### 1. Iranian-Affiliated Cyber Actors Exploit Programmable Logic Controllers Across U.S. Critical Infrastructure
- **출처:** CISA Advisory AA26-097a — https://www.cisa.gov/news-events/cybersecurity-advisories/aa26-097a
- **요약:** 이란 연계 APT 그룹이 2026년 3월부터 인터넷에 노출된 Rockwell Automation/Allen-Bradley PLC를 표적으로 삼아 HMI·SCADA 디스플레이 데이터를 조작하고 있으며, Dropbear SSH를 이용한 원격 접속으로 프로젝트 파일을 탈취하였다. FBI·CISA·NSA·EPA·DOE·CNMF가 공동으로 긴급 경보를 발령하였다.

### 2. Three Microsoft Defender Zero-Days Actively Exploited; Two Still Unpatched
- **출처:** The Hacker News — https://thehackernews.com/2026/04/three-microsoft-defender-zero-days.html
- **요약:** Microsoft Defender에서 3개의 제로데이 취약점(BlueHammer CVE-2026-33825 포함)이 발견되어 4월 10일부터 실제 공격에 악용되고 있으며, 이 중 2개는 아직 패치가 없는 상태이다. 4월 15일 Patch Tuesday에서 BlueHammer만 수정되었다.

### 3. Apache ActiveMQ CVE-2026-34197 Added to CISA KEV Amid Active Exploitation
- **출처:** The Hacker News — https://thehackernews.com/2026/04/apache-activemq-cve-2026-34197-added-to.html
- **요약:** CVSS 8.8의 Apache ActiveMQ 취약점이 CISA KEV(Known Exploited Vulnerabilities) 목록에 등재되었으며, Fortinet FortiGuard Labs는 4월 14일을 전후해 수십 건의 익스플로잇 시도를 포착하였다. 연방기관은 4월 30일까지 패치 적용이 의무화되었다.

### 4. OpenAI Launches GPT-5.4-Cyber with Expanded Access for Security Teams
- **출처:** The Hacker News — https://thehackernews.com/2026/04/openai-launches-gpt-54-cyber-with.html
- **요약:** OpenAI가 사이버보안 팀을 위한 특화 모델 GPT-5.4-Cyber를 출시하였으며, 방어자 접근성 확대 및 3,000건 이상의 취약점 수정 지원을 통해 사전적 사이버보안 역량 강화에 기여한다.

### 5. NIST Announces Changes to CVE Handling Policy (Effective April 15, 2026)
- **출처:** The Hacker News / NIST — https://thehackernews.com/2026/04/threatsday-bulletin-17-year-old-excel.html
- **요약:** NIST가 2020~2025년 사이 CVE 제출 건수 263% 급증에 대응하기 위해 취약점 우선순위 처리 기준을 개편하였으며, 4월 15일부터 새 기준이 적용되어 CVE 분류 및 NVD 등재 방식에 변화가 생겼다.

---

## 💡 이번 주 트렌드

이번 주는 **CTI 실용화(Operationalization)와 LLM 자동화**가 핵심 주제로 부각되었다. 특히 IOC → 정규식 자동 변환, 로그 이상 탐지 벤치마크 등 연구가 SOC 현장 적용에 방점을 두는 경향이 뚜렷하다. 멀티에이전트 LLM 아키텍처는 단순 탐지를 넘어 쿼리 번역·프라이버시 보존·자기수정 루프 등 운영 복잡성을 처리하는 방향으로 발전하고 있다.

보안 위협 측면에서는 **OT/ICS 인프라에 대한 국가 연계 APT 공격**이 이번 주 최대 이슈였다. 이란 연계 그룹의 PLC 직접 조작 사례는 SCADA 보안 연구의 시급성을 재확인시켜 주었다. 한편 RAG 보안과 LLM 취약점(환각, 프롬프트 인젝션)이 병행 연구 주제로 자리잡으며, 지난주 대비 **AI 모델 자체의 보안 신뢰성 검증** 수요가 새롭게 부각되었다. OpenAI의 GPT-5.4-Cyber 출시는 LLM이 보안 도구로서 제도권에 진입하는 흐름을 가속화할 것으로 보인다.

---

## ⭐ 주목 논문 1선

**"From IOCs to Regex: Automating CTI Operationalization for SOC with LLMs"**
(arXiv:2604.12228, 2026년 4월 14일)

**선정 이유:** 이 논문은 사이버 위협 인텔리전스 분야에서 오랫동안 수작업에 의존해 온 IOC 운영화(Operationalization) 과정을 LLM으로 완전 자동화하는 데 성공하였다는 점에서 주목할 만하다. IOCRegex-gen은 단순한 정규식 생성을 넘어 캡처/비캡처 그룹 인식, 다단계 의미론적 검증까지 포함하며, 실제 MITRE ATT&CK 평가 데이터 기반 실험에서 99.1% 히트율과 0.8% 오탐률이라는 실용적 성능을 입증하였다. CTI 연구자 및 SOC 운영자 모두에게 즉각적인 실무 활용 가능성이 높으며, NAUSS의 CTI 및 디지털 포렌식 연구 트랙과 직접적으로 연계된다.

---

*본 브리핑은 자동 수집 시스템에 의해 생성되었습니다. 검증되지 않은 DOI 및 링크는 포함하지 않았으며, arXiv 원문 링크만 제공합니다.*
*생성 시각: 2026-04-17 (자동 실행)*
