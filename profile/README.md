# 🍀 ClovLab

> 약속이 추억으로 자라는 친구 전용 기록공간.

**Clov.**는 친구와의 약속을 추억으로 자라게 하는 친구 전용 우정 기록 서비스입니다. 약속 → 만남 → 추억 기록 → 우정 레벨 성장으로 이어지는 관계 순환 경험을 하나의 프라이빗 공간에 누적시킵니다.

```
약속 등록 → D-day → 만남 → 추억 작성 후보 → 추억 피드 저장 → 우정 레벨 성장
```

## 우리가 푸는 문제

메신저, 캘린더, SNS, 다이어리 앱에 흩어진 친구 관계의 흐름(약속·기대감·만남·기록)을 하나로 모으는 서비스가 없습니다. 공개 SNS는 노출 피로가 있고, 커플 앱은 친구 사이에 어울리지 않는 애정 표현 톤을 쓰며, BeReal·Locket 같은 순간 인증형 서비스는 장기 누적 서사가 없습니다.

## 핵심 차별점

- **1차 핵심 차별점** — 약속 완료 → 추억 작성 후보 전환 흐름. 약속이 끝나는 순간 자연스럽게 "이 약속, 기록으로 남길까?"를 제안받습니다.
- **2차 강화 차별점** — 같은 사건에 대해 친구마다 다른 시점·감정의 기록을 남길 수 있는 구조.

## 서비스 철학

Clov.의 우정공간은 위계가 없는 동등한 친구 관계를 전제로 합니다.

- 방장은 없다 / 초대한 사람도 대표자가 아니다 / 모든 멤버는 동등하다
- 우정공간은 특정 개인의 소유물이 아니라 함께 쌓은 기록 공간이다
- 한 명이 남아도 기록은 사라지지 않는다
- 우정공간은 **최대 8명**까지 참여하는 단일 구조이며, 친구 한 명만 초대해도 가장 단순한 형태로 운영된다

## 리포지토리 구성

| 리포지토리 | 내용 |
|---|---|
| [clov-web](https://github.com/Pickeslog/clov-web) | 프론트엔드 — React SPA |
| [clov-api](https://github.com/Pickeslog/clov-api) | 백엔드 — Spring Boot REST API |
| [web-design-repository](https://github.com/Pickeslog/web-design-repository) | 화면 명세 · HTML 프로토타입 · API 계약(SSOT) |

## 기술 스택

- **Backend** — Java 21 · Spring Boot 4.0 · Spring Security + OAuth2 Client(Google·Naver·Kakao) · MyBatis · MySQL
- **Frontend** — React 19 · Vite · React Router · TanStack Query · Zustand · Emotion(styled-components)
- **Storage** — Cloudflare R2 (S3 호환 오브젝트 스토리지)
- **Infra** — GCP VM · nginx · Docker · 도메인 `clovlabcalss.store`
- **CI / Test** — GitHub Actions · JUnit 5 + Testcontainers(MySQL 통합테스트)

## 팀 & 협업

4인 팀이 **도메인 주도**로 나눠 개발합니다. 방 · 초대 · 일정 · 추억 · 편지 · 알림 · 사용자 등 각 도메인을 담당자가 백엔드부터 프론트엔드까지 세로로 책임지고, API 계약과 DB 설계를 먼저 확정한 뒤 구현합니다.

- **계약 우선(Contract-First)** — `web-design-repository`의 API 계약 · DB 설계가 단일 진실 소스(SSOT). 코드보다 문서를 먼저 확정.
- **PR 기반 워크플로우** — 모든 변경은 브랜치 → PR → CI(빌드 · 통합테스트 필수) → 코드 리뷰 → 머지.
- **도메인 분리 병렬 작업** — 레포 · 도메인을 나눠 충돌을 최소화하고 동시에 진행.
- **AI 페어 협업** — 각 개발자가 AI 코딩 어시스턴트와 페어를 이뤄 구현하고, 교차 리뷰로 품질을 검증.

## 문서 (SSOT)

| 문서 | 내용 |
|---|---|
| [API-CONTRACT.md](https://github.com/Pickeslog/web-design-repository/blob/main/docs/API-CONTRACT.md) | REST API 계약, 권한 · 에러 모델 |
| [screen-spec-source/](https://github.com/Pickeslog/web-design-repository/tree/main/screen-spec-source) | 화면별 명세(대시보드 · 추억피드 · 행운편지 · 일정계획 등) |
| [api-spec/](https://github.com/Pickeslog/web-design-repository/tree/main/api-spec) | DB 통합 설계 · 리소스 맵 |

## 현재 상태

전 도메인 백엔드 · 프론트엔드 구현 완료 → 프로토타입 룩앤필 정렬 완료 → **배포 진행 중** (`clovlabcalss.store`).

## 핵심 슬로건

> "약속이 추억으로 자라는 친구 전용 기록공간."
>
> "우리가 함께한 시간은, 흩어지지 않고 자란다."
