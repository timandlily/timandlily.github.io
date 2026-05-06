# 📋 Weekly Research Briefing — CTI / SCADA / Digital Forensics
**기준일:** 2026년 4월 19일 (일) | **수집 기간:** 2026년 4월 12일 ~ 4월 19일

---

## 📄 신규 논문

### 1. Challenges and Future Directions in Agentic Reverse Engineering Systems
- **저자:** Salem Radey, Jack West, Kassem Fawaz
- **출처:** arXiv cs.CR — https://arxiv.org/abs/2604.14317
- **게재일:** 2026년 4월 14일
- **핵심 기여:** LLM 기반 에이전트(정적·동적·하이브리드)가 리버스 엔지니어링 과제를 수행할 때의 한계(토큰 제약, 난독화 처리 실패, 프로그램 가드레일 부재)를 체계적으로 분석한다. 포렌식·악성코드 분석에서의 에이전트 활용 방향성과 미래 과제를 제시한다.

---

### 2. RealVuln: Benchmarking Rule-Based, General-Purpose LLM, and Security-Specialized Scanners on Real-World Code
- **저자:** John Pellew, Faizan Raza (Kolega.Dev)
- **출처:** arXiv cs.CR — https://arxiv.org/abs/2604.13764
- **게재일:** 2026년 4월 13일
- **핵심 기여:** 26개 취약 Python 저장소(796개 레이블 항목)를 대상으로 Rule-Based SAST, 범용 LLM, 보안 전문 스캐너 등 15종을 F3 스코어 기준으로 비교한 최초 오픈소스 벤치마크다. 보안 전문 스캐너가 리콜 우위를 보이나, 범용 LLM(Claude Sonnet 4.6, F1=60.9)이 Rule-Based 도구 대비 최대 3배 높은 성능을 기록하였다.

---

### 3. Your Agent Is Mine: Measuring Malicious Intermediary Attacks on the LLM Supply Chain
- **저자:** Hanzhi Liu, Chaofan Shou, Hongbo Wen, Yanju Chen, Ryan Jingyang Fang, Yu Feng (UC Santa Barbara, Fuzzland, UC San Diego)
- **출처:** arXiv cs.CR — https://arxiv.org/abs/2604.08407
- **게재일:** 2026년 4월 9일
- **핵심 기여:** LLM 에이전트가 제3자 API 라우터를 경유할 때 발생하는 중간자 공격(Malicious Intermediary Attack)을 최초로 계량화한다. 라우터가 평문 JSON 페이로드에 전면 접근하되 암호 무결성 검증이 없음을 이용, 다양한 공격 시나리오에서 심각한 취약점을 실증한다.

---

### 4. SentinelNet: Safeguarding Multi-Agent Collaboration Through Credit-Based Dynamic Threat Detection
- **저자:** Yang Feng (University of Edinburgh), Xudong Pan (Fudan University / Shanghai Innovation Institute)
- **출처:** ACM Web Conference 2026 (April 13–17, Dubai) — https://arxiv.org/abs/2510.16219
- **게재일:** 2026년 4월 13–17일 (ACM WWW 2026 정식 게재)
- **핵심 기여:** 멀티에이전트 시스템에서 악성 에이전트를 분산 감지·차단하는 신용 기반(Credit-Based) 탐지 프레임워크를 제안한다. 대조 학습(Contrastive Learning)으로 훈련된 각 에이전트가 자율적으로 메시지 신뢰도를 평가하며, 2라운드 이내 거의 100% 악성 에이전트 탐지율과 손상된 기준선 대비 95% 정확도 복구를 달성한다.

---

## 🔐 주요 보안 뉴스

### 1. CISA, 7개 알려진 취약점 KEV 카탈로그 추가 (April 13, 2026)
- **출처:** CISA — https://www.cisa.gov/news-events/alerts/2026/04/13/cisa-adds-seven-known-exploited-vulnerabilities-catalog
- **요약:** Fortinet FortiClient EMS SQL 인젝션(CVE-2026-21643, CVSS 9.1), Microsoft Exchange 역직렬화(CVE-2023-21529), Adobe Acrobat 프로토타입 오염(CVE-2026-34621) 등 7개 취약점을 KEV에 추가하였다. 연방 기관은 2026년 4월 27일까지 패치 적용이 의무화된다.

---

### 2. CISA, Apache ActiveMQ CVE-2026-34197 KEV 추가 및 AVEVA Pipeline 권고 (April 16, 2026)
- **출처:** CISA — https://www.cisa.gov/news-events/alerts/2026/04/16/cisa-adds-one-known-exploited-vulnerability-catalog
- **요약:** Apache ActiveMQ Classic의 입력 검증 취약점(CVE-2026-34197, CVSS 8.8)이 KEV에 추가되었으며, 동시에 AVEVA Pipeline Simulation에 대한 ICS 보안 권고(ICSA-26-106-04)가 발표되었다. OT/SCADA 환경을 운영 중인 기관의 즉각적인 점검이 필요하다.

---

### 3. EPA·FBI·CISA·NSA, 이란 계열 APT의 미국 상수도·폐수 시스템 PLC 공격 공동 경보
- **출처:** CISA Advisory AA26-097a — https://www.cisa.gov/news-events/cybersecurity-advisories/aa26-097a
- **요약:** 2026년 3월부터 이란 계열 APT 그룹이 인터넷 노출 PLC(Rockwell Automation/Allen-Bradley 등)를 타겟하여 구성 삭제, HMI 조작, 기계식 센서 변조를 통한 물리적 장애를 야기하고 있다. 미국 상수도·폐수·에너지 분야 OT 운영자 대상 긴급 권고가 발령되었다.

---

## 💡 이번 주 트렌드

이번 주 연구 동향의 핵심은 **LLM 에이전트 보안의 급속한 심화**이다. 단순한 LLM 악용 방어를 넘어, 멀티에이전트 공급망 공격(LLM Supply Chain)과 에이전트 간 신뢰 모델 붕괴라는 새로운 위협 패러다임이 본격 등장하였다. SentinelNet과 "Your Agent Is Mine" 논문은 같은 주에 발표되어 멀티에이전트 신뢰 문제가 학계의 집중 조명을 받고 있음을 시사한다. 실용 보안 도구 평가에서는 LLM 기반 스캐너가 기존 Rule-Based SAST를 압도하는 성능을 보이며 실제 취약점 탐지 파이프라인 교체 가능성이 논의되고 있다. SCADA·ICS 보안 측면에서는 이란 계열 APT의 OT 직접 타겟팅이 지속·확대되고 있으며, CISA의 잦은 KEV 업데이트는 공급망·산업 제어 시스템에 대한 실제 공격 빈도가 증가하고 있음을 반영한다. 지난 주 대비 특히 **LLM 에이전트 중간자 공격(Intermediary Attack)**이 신규 부각된 주제이다.

---

## ⭐ 주목 논문 1선

**SentinelNet: Safeguarding Multi-Agent Collaboration Through Credit-Based Dynamic Threat Detection**
(arXiv:2510.16219 / ACM Web Conference 2026)

**선정 이유:** ACM WWW 2026(4월 13–17일, 두바이)에서 정식 게재된 본 논문은 멀티에이전트 시스템의 신뢰성 보장이라는 가장 시급한 실용 과제를 직접 해결한다. 훈련 데이터 희소 문제를 적대적 궤적 합성으로 극복하고, 중앙 집중식 감독 없이 각 에이전트가 자율 탐지를 수행하는 탈중앙화 아키텍처는 SCADA·사이버보안 멀티에이전트 프레임워크 설계에 직접 응용 가능하다. 이석희 교수의 CTI 멀티에이전트 연구 방향과 높은 접점이 있으며, 관련 연구로의 후속 인용 가능성이 높다.

---

*자동 생성: Claude (Cowork Mode) | 수집 기간: 2026-04-12 ~ 2026-04-19*
