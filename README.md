# Real-time Voice Translator (RVT)

> 화자 분리 기반 영어→한국어 실시간 음성 번역기
> **소프트웨어공학 "프로세스에 입각한 바이브코딩" 과제 결과물**

[![Status](https://img.shields.io/badge/status-Day%202%20Complete-brightgreen)]()
[![Process](https://img.shields.io/badge/process-Hybrid%20Waterfall%2BSpiral-green)]()
[![AI](https://img.shields.io/badge/AI-Claude%20(Cowork)-orange)]()

---

## 1. 프로젝트 소개

영어 회의·강의·인터뷰 상황에서, 마이크로 들어오는 다중 화자의 발화를 자동으로 분리하고 각 발화를 한국어로 실시간 번역해 자막처럼 보여주는 **데스크탑 도구**.

본 저장소는 **SW 결과물 자체보다 "어떻게 만들어졌는가(프로세스)"가 핵심 평가 대상**이다. 따라서 코드뿐 아니라 다음 산출물을 함께 형상관리한다.

- 프로젝트 헌장, 요구사항 명세, 설계 명세, 테스트 결과, 결함 로그
- AI(Claude)와의 일일 토의 로그

---

## 2. 과제 정보

| 항목 | 내용 |
|---|---|
| 과목 | 소프트웨어공학 |
| 과제명 | 프로세스에 입각한 바이브코딩의 효과 |
| 수행 인원 | 1인 (ghwo336) |
| 활용 AI | Claude (Anthropic) — Cowork 모드 |
| 적용 프로세스 | Waterfall 단계 골격 + 나선형(Spiral) 반복 구현의 하이브리드 |
| 기간 | 2026-05-24 ~ 2026-06-07 (14일) |

---

## 3. 디렉토리 구조

```
realtime-voice-translator/
├── README.md                    ← 이 문서
├── .gitignore
├── docs/
│   ├── process/                 ← 프로젝트 관리 산출물
│   │   ├── PROJECT_CHARTER.md   ← 프로젝트 헌장 (Day 1)
│   │   ├── DISCUSSION_LOG.md    ← AI와의 일일 토의 로그
│   │   └── RETROSPECTIVE.md     ← 회고 (Day 7, 14)
│   ├── requirements/            ← 요구사항 (Day 2-3)
│   │   ├── SRS.md
│   │   └── usecases/
│   ├── design/                  ← 설계 (Day 4-5)
│   │   ├── SDD.md
│   │   ├── architecture.png
│   │   ├── sequence.png
│   │   └── wireframe.png
│   └── test/                    ← 테스트 (Day 11-12)
│       ├── TEST_PLAN.md
│       ├── TEST_RESULTS.md
│       └── DEFECT_LOG.md
├── src/                         ← 소스 코드
└── tests/                       ← 자동화 테스트
```

---

## 4. 진행 현황

### ✅ Phase 1: Inception (Day 1, 2026-05-24) — **완료**

| 산출물 | 위치 | 상태 |
|---|---|---|
| 프로젝트 헌장 v1.0 | [`docs/process/PROJECT_CHARTER.md`](docs/process/PROJECT_CHARTER.md) | ✅ |
| Day 1 토의 로그 | [`docs/process/DISCUSSION_LOG.md`](docs/process/DISCUSSION_LOG.md) | ✅ |
| README / .gitignore | (이 파일) / `.gitignore` | ✅ |
| 디렉토리 구조 | `docs/`, `src/`, `tests/` | ✅ |
| 프로세스 모델 선정 | 하이브리드 (Waterfall + Spiral) | ✅ |
| 리스크 식별 (6건) | Charter §8 | ✅ |
| 14일 일정 / 마일스톤 (M1~M7) | Charter §6.2 | ✅ |

### 🟦 Phase 2: Requirements (Day 2-3, 2026-05-25 ~ 26) — **Day 2 완료 / Day 3 진행 예정**

| 산출물 | 위치 | 상태 |
|---|---|---|
| 사용자 시나리오 (자기 인터뷰, 5H1W) | [`docs/requirements/USER_SCENARIOS.md`](docs/requirements/USER_SCENARIOS.md) | ✅ |
| SRS v0.1 (FR 10 + NFR 8 + 제약 5) | [`docs/requirements/SRS.md`](docs/requirements/SRS.md) | ✅ |
| 추적성 매트릭스 (시나리오 ↔ 요구) | SRS §6 | ✅ |
| Day 2 토의 로그 | [`docs/process/DISCUSSION_LOG.md`](docs/process/DISCUSSION_LOG.md) | ✅ |
| 유스케이스 다이어그램 + 명세 | `docs/requirements/usecases/` | 🔜 Day 3 |
| 클래스 다이어그램 초안 | `docs/design/` | 🔜 Day 3 |
| SRS v1.0 (Open Issues 일부 해소) | SRS.md | 🔜 Day 3 |

### 🔜 다음: Phase 3 Design (Day 4-5, 2026-05-27 ~ 28)

- 강의록 06_설계원리, 07_아키텍처와 패턴, 08_UI 설계 분석
- 아키텍처 다이어그램 + 컴포넌트 정의
- 기술 스택 최종 결정 (Open Issues O-01 ~ O-04 해소)
- UI 와이어프레임

전체 일정은 [`docs/process/PROJECT_CHARTER.md`](docs/process/PROJECT_CHARTER.md) §6.2 참조.

---

## 5. 프로세스 적용 증빙 (채점 가이드)

본 저장소는 다음 방식으로 "지속적 토의"를 증빙한다.

1. **일일 커밋** — 매일 1회 이상 의미있는 커밋 (단순 push 아님)
2. **토의 로그** — [`docs/process/DISCUSSION_LOG.md`](docs/process/DISCUSSION_LOG.md)에 매일 엔트리 추가
3. **이슈 트래킹** — GitHub Issues로 단계별 작업·결함 추적
4. **단계별 산출물** — 각 마일스톤(M1~M7)에서 명시된 문서를 commit으로 남김
5. **PR 기반 변경** — 큰 단계 전환 시 PR 머지로 흔적 남김

---

## 6. 빌드 및 실행

> Day 5 설계 완료 후 본 섹션 갱신 예정. 현재는 placeholder.

```bash
# (예정) 설치
pip install -r requirements.txt

# (예정) 실행
python -m rvt
```

---

## 7. 라이선스

학내 과제용 비공개 학습 목적. 외부 모델/라이브러리는 각자의 라이선스를 따른다.
