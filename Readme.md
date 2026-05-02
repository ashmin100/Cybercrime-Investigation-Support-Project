# 🔍 CyberCop

<div align="center">

**스캠 영상 탐지를 위한 VLM 기반 사이버범죄 수사 지원 연구 프로젝트**

[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)]()
[![Lab](https://img.shields.io/badge/Lab-IBDLAB-4A90D9?style=flat-square)]()
[![Language](https://img.shields.io/badge/Jupyter%20Notebook-100%25-F37626?style=flat-square&logo=jupyter&logoColor=white)]()
[![LLM](https://img.shields.io/badge/OpenAI-VLM-412991?style=flat-square&logo=openai&logoColor=white)]()
[![Visibility](https://img.shields.io/badge/Main%20Repo-Private-red?style=flat-square&logo=github)]()

</div>

> **⚠️ Notice**: 본 레포지토리는 연구 히스토리 아카이브입니다. 현재 메인 연구는 **private 레포지토리**에서 진행 중입니다.

---

## 목차

- [프로젝트 개요](#-프로젝트-개요)
- [연구 히스토리](#-연구-히스토리)
- [레포지토리 구조](#️-레포지토리-구조)
- [보안 주의사항](#-보안-주의사항)

---

## 📌 프로젝트 개요

**CyberCop**은 IBDLAB의 스캠(Scam) 영상 탐지 연구 프로젝트입니다.

Vision-Language Model(VLM)을 활용하여 사이버범죄 수사관이 스캠 영상을 보다 효율적으로 식별하고 분석할 수 있도록 지원하는 AI 시스템 개발을 목표로 합니다.

| 항목 | 내용 |
|------|------|
| 🏛️ **소속** | IBDLAB |
| 🎯 **목표** | 스캠 영상 자동 탐지 및 분류 |
| 🤖 **핵심 기술** | Vision-Language Model (VLM), Prompt Engineering |

---

## 📅 연구 히스토리

연구는 아래와 같이 단계적으로 진행되었습니다.

### Phase 0 — Image Classifier `[Deprecated]`

```
디렉토리: 00.image_classifier_deprecated/
```

초기 접근법으로 이미지 분류(Image Classification) 방식을 시도했습니다. 이후 VLM 기반 접근법으로 전환하면서 deprecated 처리되었습니다.

---

### Phase 1 — VLM Prompt Correction Loop

```
디렉토리: 01.vlm_prompt_correction/
```

VLM을 도입하고, 모델 출력을 피드백 루프로 자동 수정하는 **Prompt Correction** 방식을 탐구했습니다.

---

### Phase 2 — VLM Initial Prompt Optimization

```
디렉토리: 02.vlm_initial_prompt/
```

VLM에 투입하는 **초기 프롬프트 자체를 최적화**하는 방향으로 연구를 전환했습니다. 모델이 스캠 영상을 더 정확하게 판단할 수 있도록 프롬프트 구조와 표현을 실험합니다.

---

### Phase 3 — Initial Prompt Engineering

```
디렉토리: 03.Initial_prompt_engineering_20251120/
```

프롬프트 엔지니어링 심화 실험.

---

### Phase 4 — Prompt Engineering Iteration

```
디렉토리: 04.prompt_engineering_20251124/
```

프롬프트 엔지니어링 추가 이터레이션.

---

### Phase 5 — Do Sample: False

```
디렉토리: 05.do_sample_false/
```

VLM 생성 파라미터 실험 — `do_sample=False` (greedy decoding) 조건에서의 출력 일관성 및 탐지 성능을 검증합니다.

---

### Utility — Token Analysis

```
디렉토리: Token_analysis/token_count/
```

프롬프트 및 응답의 토큰 사용량을 분석하여 비용 및 효율을 모니터링합니다.

---

## 🗂️ 레포지토리 구조

```
Cybercrime-Investigation-Support-Project/
│
├── 00.image_classifier_deprecated/   # [Deprecated] 이미지 분류 초기 접근
├── 01.vlm_prompt_correction/         # VLM + 프롬프트 자동 수정 루프
├── 02.vlm_initial_prompt/            # VLM 초기 프롬프트 최적화 (현재 메인)
├── 03.Initial_prompt_engineering_20251120/  # 프롬프트 엔지니어링 스냅샷
├── 04.prompt_engineering_20251124/   # 프롬프트 엔지니어링 이터레이션
├── 05.do_sample_false/               # 생성 파라미터 실험
├── Token_analysis/
│   └── token_count/                  # 토큰 사용량 분석
└── Readme.md
```

> 디렉토리 prefix 번호(`00`, `01`, ...)는 연구 진행 순서를 나타냅니다.

---

```

**권장 관리 방법**

- `.env` 파일 또는 환경변수로 API 키를 관리하세요.
- `.gitignore`에 `configuration.json`, `.env` 등 민감 파일을 반드시 등록하세요.
- 실수로 커밋한 경우: 즉시 OpenAI 대시보드에서 해당 키를 **revoke**하고 새 키를 발급받으세요.

---

<div align="center">

IBDLAB · CyberCop Research Project

</div>
