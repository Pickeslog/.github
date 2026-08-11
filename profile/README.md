<!--
  ⚠️ 게시 안내: 이 Overview README는 두 곳에 "동일하게" 올려야 합니다.
  1) Pickeslog/.github         → profile/README.md  (외부 방문자용, 로그아웃 상태에서 보임)
  2) Pickeslog/.github-private → profile/README.md  (조직 멤버용, 로그인 상태에서 보임)
  한쪽만 수정하면 다른 쪽은 예전 내용이 그대로 보이는 문제가 생깁니다.
  이 초안을 수정한 뒤에는 반드시 두 저장소 모두에 같은 내용을 붙여넣어 주세요.
  이미지 3개(readme-img-01/02/03.png)도 같은 폴더 구조로 두 저장소 profile/ 아래에 함께 올려야 이미지가 깨지지 않습니다.
-->

# 🍀 Clov.

> 친구와의 약속과 추억을 기록하는 웹 서비스입니다.

<div align="left">

![Java](https://img.shields.io/badge/Java%2021-007396?style=for-the-badge&logo=openjdk&logoColor=white)
![SpringBoot](https://img.shields.io/badge/Spring%20Boot%204.0-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![React](https://img.shields.io/badge/React%2019-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL%208-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

![개발기간](https://img.shields.io/badge/개발기간-2026.06.26%20~%202026.08.14-FA7268?style=flat-square)
![팀구성](https://img.shields.io/badge/팀구성-4인-8E7CC3?style=flat-square)
![분류](https://img.shields.io/badge/분류-팀%20프로젝트-4A90D9?style=flat-square)

</div>

## 📗 목차

- [📋 프로젝트 소개](#-프로젝트-소개)
- [⚙️ 주요 기능](#️-주요-기능)
- [🔍 참고 서비스](#-참고-서비스)
- [🫂 팀원 소개](#-팀원-소개)
- [📦 리포지토리 구성](#-리포지토리-구성)
- [🛠 기술 스택](#-기술-스택)
- [📁 프로젝트 구조](#-프로젝트-구조)
- [🧑‍💻 코드 리뷰](#-코드-리뷰)
- [📡 주요 API 엔드포인트](#-주요-api-엔드포인트)
- [🗄 데이터베이스 설계](#-데이터베이스-설계)
- [📝 커밋 컨벤션](#-커밋-컨벤션)
- [💻 코드 컨벤션](#-코드-컨벤션)
- [🚀 로컬 실행 방법](#-로컬-실행-방법)
- [🔀 브랜치 전략](#-브랜치-전략)
- [🤝 협업 방식](#-협업-방식)
- [📊 진행 상황 관리](#-진행-상황-관리)
- [📚 문서 (SSOT)](#-문서-ssot)

## 📋 프로젝트 소개

- **프로젝트명** — Clov.
- **분류** — 팀 프로젝트 (4인)
- **개발 기간** — 2026.06.26 ~ 2026.08.14

## ⚙️ 주요 기능

- 🏠 **우정공간(친구 그룹)** — 생성, 초대 코드로 가입 신청 → 기존 멤버 승인(5분 이내 되돌리기 가능)
- 📅 **약속** — 등록·체크리스트 관리, 제안 → 일정조율 → 확정 → 만남 4단계 인증사진 업로드
- 📸 **추억** — 약속 완료 시 추억 작성 후보로 전환, 추억 작성(사진·태그·참여자·댓글)
- 🗂 **추억 피드** — 우정공간별 월별·태그·작성자 필터
- 💌 **행운편지** — 작성·발송(1:1 또는 전체 발송), 즐겨찾기
- 🪙 **골드 · 우정 레벨** — 약속 완료·추억 작성·마스코트 교감으로 골드 적립, 우정 레벨/경험치 관리
- 🛍 **상점** — 골드로 마스코트 코스튬·배경 구매 및 장착
- 🎂 **생일 약속** — 일정에 뜬 생일 칩으로 생일 약속 생성, 골든 티켓 표시, 추억·행운편지에 생일 배지/CTA 연동
- 🔔 **알림** — 공지·친구활동·가입신청 관리
- 🔐 **인증** — 이메일 회원가입/로그인 및 소셜 로그인(Google, Naver, Kakao)

## 🔍 참고 서비스

기획 단계에서 실제 시장 조사를 거쳐 아래 6개 서비스를 분석하고, Clov.가 메울 수 있는 공백을 확인했습니다.

| 서비스 | 주요 타깃 | 핵심 기능 | Clov.가 차별화하는 지점 |
|---|---|---|---|
| [비트윈 (Between)](https://between.us/?lang=ko) | 커플 | 사진/일정/디데이/메시지 공유 | 친구 간에는 부담스러운 애정 표현 톤을 배제 |
| [썸원 (SumOne)](https://www.sumone.co/ko) | 커플 | 매일 1개 질문 답변, 반려몽 성장, 일기 | 연애 톤·무거운 감정선을 배제하고 친구 간 가벼운 약속·밈 중심으로 설계 |
| [BeReal](https://play.google.com/store/apps/details?id=com.bereal.ft) | Z세대 전반 | 하루 1회 동시 촬영 인증 사진 | 1회성 인증이 아닌 장기 누적 서사(약속→추억) |
| [Locket Widget](https://play.google.com/store/apps/details?id=com.locket.Locket) | 친한 친구·커플 | 홈 화면 위젯으로 사진 공유 | 위젯형 즉시성 대신 "기록의 누적과 성장"에 집중 |
| [셋로그 (Setlog)](https://play.google.com/store/apps/details?id=com.setlog.app) | Z세대 친구 그룹(4~6인) | 정시 알림 기반 분할 숏폼 브이로그 | 순간 기록을 넘어 약속·D-day·레벨 성장까지 포괄 |
| [TimeTree](https://timetreeapp.com/intl/en) | 가족·커플·동호회·친구 | 공유 캘린더, 일정별 채팅 | 일정 조율을 넘어 만남 이후의 추억 기록과 우정 레벨 성장 요소 도입 |

## 🫂 팀원 소개

담당 영역을 처음부터 고정하지 않고, 팀원들이 필요한 부분을 자유롭게 교차하며 작업한 방식이라 아래 역할은 **대표 기여 도메인** 기준입니다.

| | 이름 | GitHub | 담당 |
|---|---|---|---|
| 👑 팀장 | Myeongjun Kim | [@myeongjundev](https://github.com/myeongjundev) | 초기 설계 총괄(인증·보안·DB), 배포·CI/CD |
| 팀원 | chacha1650a | [@chacha1650a](https://github.com/chacha1650a) | 상점(Shop) — 카탈로그·지갑·구매 API/화면 |
| 팀원 | kimgyubi1234 | [@kimgyubi1234](https://github.com/kimgyubi1234) | 알림 기능, 경험치·레벨 UI, 배포·이메일 인프라 복구(SMTP 연동), 발표 PPT 제작 |
| 팀원 | lami2342 | [@lami2342](https://github.com/lami2342) | 추억(Memory) 초기 구현, 인증·초대 플로우 |

## 📦 리포지토리 구성

| 리포지토리 | 내용 |
|---|---|
| [clov-web](https://github.com/Pickeslog/clov-web) | 프론트엔드 — React SPA |
| [clov-api](https://github.com/Pickeslog/clov-api) | 백엔드 — Spring Boot REST API |
| [web-design-repository](https://github.com/Pickeslog/web-design-repository) | 화면 명세 · HTML 프로토타입 · API 계약(SSOT) |

## 🛠 기술 스택

**Backend**

![Java](https://img.shields.io/badge/Java%2021-007396?style=for-the-badge&logo=openjdk&logoColor=white)
![SpringBoot](https://img.shields.io/badge/Spring%20Boot%204.0-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![SpringSecurity](https://img.shields.io/badge/Spring%20Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![OAuth2](https://img.shields.io/badge/OAuth2%20Client-4285F4?style=for-the-badge&logo=auth0&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-DC143C?style=for-the-badge)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

**Frontend**

![React](https://img.shields.io/badge/React%2019-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![ReactRouter](https://img.shields.io/badge/React%20Router-CA4245?style=for-the-badge&logo=reactrouter&logoColor=white)
![TanStackQuery](https://img.shields.io/badge/TanStack%20Query-FF4154?style=for-the-badge&logo=reactquery&logoColor=white)
![Zustand](https://img.shields.io/badge/Zustand-433E38?style=for-the-badge)
![Emotion](https://img.shields.io/badge/Emotion-D26AC2?style=for-the-badge&logo=emotion&logoColor=white)

**Storage / Infra / CI·Test**

![CloudflareR2](https://img.shields.io/badge/Cloudflare%20R2-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![GCP](https://img.shields.io/badge/Google%20Cloud-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![nginx](https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GithubActions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![JUnit5](https://img.shields.io/badge/JUnit5-25A162?style=for-the-badge&logo=junit5&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-2496ED?style=for-the-badge&logo=testcontainers&logoColor=white)

## 📁 프로젝트 구조

<details>
<summary><b>clov-api</b> — 도메인 단위 패키지 구조 (MyBatis, JPA 미사용)</summary>

```
com/korit/clovapi/
├── domain/
│   ├── auth/           # 회원가입·로그인·OAuth2·비밀번호 재설정
│   ├── user/            # 프로필·환경설정
│   ├── room/            # 우정공간·멤버·마스코트·경험치
│   ├── invite/           # 초대 코드·가입 신청·승인
│   ├── plan/              # 약속·체크리스트·4단계 인증사진
│   ├── memory/         # 추억·이미지·댓글
│   ├── letter/            # 행운편지
│   ├── notification/      # 알림
│   └── shop/               # 상점·지갑(골드)
│       └── {controller, dto, entity, mapper, service}
└── global/
    ├── security/        # Spring Security·JWT·OAuth2 설정
    ├── storage/          # Cloudflare R2 presign
    ├── response/          # 공통 응답 봉투 ({success,data}/{success,error})
    ├── exception/          # 공통 예외 처리
    ├── dto/                 # 전역 공용 DTO
    ├── mail/                # 비밀번호 재설정 등 메일 발송
    └── time/                 # 서버 시간 유틸
```

</details>

<details>
<summary><b>clov-web</b> — 기능 단위 폴더 구조</summary>

```
src/
├── api/            # axios 기반 API 클라이언트 (도메인별)
├── pages/          # 라우트 페이지 (auth, rooms, feed, letters, schedule, shop, notifications)
├── components/     # 재사용 UI 컴포넌트
├── stores/         # Zustand 전역 상태
├── hooks/          # 커스텀 훅
└── routes/         # 라우트 가드
```

</details>

## 🧑‍💻 코드 리뷰

실제 코드베이스에서 핵심 로직 3가지를 뽑아 동작을 설명합니다. 각 항목마다 실제 실행 화면 스크린샷을 함께 담았습니다.

### ① 약속 완료 → 추억 전환 트리거 (`clov-api` · `PlanService.complete`)

<img src="./readme-img-01-plan-complete.png" alt="약속 완료 후 인생4컷으로 전환된 화면" width="420" />

```java
@Transactional
public PlanResponses.Detail complete(long planId, long userId) {
    Plan plan = findPlan(planId);
    assertActiveMember(plan.getRoomId(), userId);

    planMapper.complete(planId, LocalDateTime.now(ZoneOffset.UTC));

    expService.grant(
        plan.getRoomId(), userId,
        ExpService.ACTION_PLAN_COMPLETE,
        PLAN_COMPLETE_EXP, planId
    );

    notificationService.fanOut(
        plan.getRoomId(), userId,
        NotificationService.TYPE_FRIEND,
        NotificationService.SUB_PLAN_COMPLETE,
        planId, null
    );

    return detail(planId, userId);
}
```

`plan`은 완료 처리할 약속을 조회한 것이다. `findPlan(planId)`로 먼저 가져온 뒤 `assertActiveMember`로 이 사용자가 해당 우정공간의 활성 멤버인지부터 확인한다. Clov.는 방장·관리자 개념이 없어서 "이 공간의 멤버인가"와 "본인이 작성한 것인가", 이 두 가지 검사만으로 권한을 판단하는데, 약속 완료는 작성자가 아니어도 공간 멤버 누구나 할 수 있는 동작이라 여기서는 첫 번째 검사만 쓴다.

멤버십 확인이 끝나면 `planMapper.complete()`로 상태를 `COMPLETED`로 바꾼다. 이 한 줄이 실행되는 순간 `plan.memory_status`도 함께 `CANDIDATE`로 바뀌는데, 이게 곧 "추억 작성 후보로 전환"되는 지점이다. 별도의 전환 API가 있는 게 아니라 약속을 완료 처리하는 이 메서드 자체가 추억으로 넘어가는 유일한 트리거다.

그다음 `expService.grant()`로 경험치를 적립하고, `notificationService.fanOut()`으로 같은 방 멤버 전원에게 완료 알림을 보낸다. 메서드 전체가 `@Transactional`로 묶여 있어서 경험치 적립이나 알림 발송 중 하나라도 실패하면 완료 처리 자체가 롤백된다 — 완료 상태는 바뀌었는데 경험치·알림이 빠지는 어중간한 상태를 막기 위해서다.

### ② 우정 레벨 연속 레벨업 (`clov-api` · `ExpService.grant`)

<img src="./readme-img-02-level-exp.png" alt="경험치 히스토리 팝업" width="500" />

```java
@Transactional(propagation = Propagation.REQUIRED)
public void grant(long roomId, long userId, String actionType,
                   int expDelta, Long referenceId) {
    if (expDelta <= 0) return;

    Room room = roomMapper.findByIdForUpdate(roomId)
        .orElseThrow(() -> new DomainException(ErrorCode.NOT_FOUND));

    int level = room.getFriendshipLevel();
    if (level >= MAX_LEVEL) return;

    int startLevel = level;
    int exp = room.getExpPoint() + expDelta;

    while (exp >= EXP_PER_LEVEL && level < MAX_LEVEL) {
        level++;
        exp -= EXP_PER_LEVEL;
    }
    roomMapper.updateLevelAndExp(roomId, level, exp);

    if (level > startLevel) {
        notificationService.fanOut(roomId, null, TYPE_FRIEND,
            SUB_LEVEL_UP, roomId, "{\"level\":" + level + "}");
    }
}
```

`room`은 경험치를 올릴 우정공간을 조회한 것인데, 단순 조회가 아니라 `findByIdForUpdate`로 행에 잠금을 걸고 읽는다. 약속 완료·추억 작성·마스코트 교감처럼 경험치를 주는 행동이 여러 개라서, 같은 방에서 동시에 여러 활동이 겹치면 잠금 없이는 두 트랜잭션이 같은 값을 읽어 한쪽 적립이 유실될 수 있다. 행을 잠그고 읽는 이유가 그것이다.

`exp`는 이번 적립분까지 더한 값이고 `level`은 현재 레벨이다. `exp_point`는 누적 총량이 아니라 "지금 레벨 안에서 쌓인 진행도"라서, `while` 루프를 돌며 100이 넘을 때마다 레벨을 하나씩 올리고 그만큼 `exp`에서 뺀다. 한 번에 큰 경험치가 들어와 100을 여러 번 넘기면(예: 마스코트 교감을 몰아서 여러 번 한 경우) 넘긴 횟수만큼 레벨이 연속으로 오른다.

레벨이 실제로 올랐을 때(`level > startLevel`)만 알림을 보낸다. 연속으로 여러 레벨이 올라도 알림은 최종 레벨 하나로 한 번만 나가는데, 레벨업마다 알림을 따로 보내면 사용자 입장에서는 스팸처럼 느껴지기 때문이다.

### ③ 상점 아이템 구매 (`clov-api` · `ShopService.purchase`)

<img src="./readme-img-03-shop-purchase.png" alt="상점에서 아이템 구매 후 장착 완료 토스트" width="600" />

```java
@Transactional
public PurchaseResponse purchase(long userId, long itemId) {
    ShopItem item = shopMapper.findById(itemId)
        .orElseThrow(() -> new DomainException(SHOP_ITEM_NOT_FOUND));
    if (!item.isPurchasable()) {
        throw new DomainException(ErrorCode.ITEM_NOT_PURCHASABLE);
    }
    if (shopMapper.existsInInventory(userId, itemId)) {
        throw new DomainException(ErrorCode.ITEM_ALREADY_OWNED);
    }

    getOrCreateWallet(userId);
    UserWallet wallet = shopMapper.findWalletForUpdate(userId)
        .orElseThrow(() -> new IllegalStateException("wallet must exist"));

    long finalPrice = item.finalPrice();
    if (wallet.getBalance() < finalPrice) {
        throw new DomainException(ErrorCode.INSUFFICIENT_BALANCE);
    }

    long newBalance = wallet.getBalance() - finalPrice;
    shopMapper.updateBalance(userId, newBalance);
    shopMapper.insertInventory(userId, itemId, finalPrice);

    WalletTransaction tx = new WalletTransaction();
    tx.setUserId(userId);
    tx.setReason(WalletTransaction.REASON_PURCHASE);
    tx.setAmount(-finalPrice);
    tx.setBalanceAfter(newBalance);
    shopMapper.insertTransaction(tx);

    item.setOwned(true);
    return new PurchaseResponse(ShopItemResponse.from(item), newBalance);
}
```

`item`은 구매하려는 상점 아이템이고, 조회하자마자 두 가지를 먼저 검사한다. `isPurchasable()`로 판매 종료된 아이템은 아닌지, `existsInInventory()`로 이미 보유한 아이템은 아닌지다. 이 두 검사를 잔액 확인보다 먼저 해두면 어차피 살 수 없는 아이템 때문에 지갑까지 잠그는 낭비를 하지 않아도 된다.

`wallet`은 `findWalletForUpdate`로 잠그고 읽는데, 레벨업 로직과 같은 이유다. 같은 유저가 두 기기에서 거의 동시에 서로 다른 아이템을 사려고 하면 잠금이 없을 경우 둘 다 "잔액이 충분하다"고 읽어버려서, 실제로는 잔액이 모자란데도 구매가 둘 다 성공해버릴 수 있다. 행을 잠그고 순서대로 처리해 이 문제를 막는다.

`finalPrice`만큼 잔액을 차감하고 `insertInventory`로 보유 아이템 목록에 추가한 다음, `WalletTransaction`이라는 거래 내역을 하나 더 남긴다. `amount`는 차감이라 음수로 저장하고 `balanceAfter`에는 차감 이후 잔액을 그대로 남겨서, 나중에 "왜 골드가 줄었는지"를 이 원장 테이블만 보고도 추적할 수 있게 했다.

## 📡 주요 API 엔드포인트

> Base path: `/api/v1` · 모든 응답은 `{success, data}` / `{success, error}` 공통 봉투를 사용합니다.

<details>
<summary>전체 엔드포인트 펼치기</summary>

**인증 (Auth)**
- `POST /auth/signup` · `POST /auth/login` — 이메일/비밀번호 회원가입·로그인
- `POST /auth/refresh` · `POST /auth/logout` — 토큰 재발급·로그아웃
- `POST /auth/password/forgot` · `POST /auth/password/reset` — 비밀번호 재설정
- `GET /oauth2/authorization/{provider}` — 소셜 로그인(google, naver, kakao)

**우정공간 (Rooms)**
- `POST /rooms` · `GET /rooms/{roomId}` — 생성·상세 조회
- `GET /rooms/{roomId}/members` · `DELETE /rooms/{roomId}/members/me` — 멤버 조회·나가기
- `POST /rooms/{roomId}/mascot/interact` — 마스코트 교감(골드 획득)

**초대 · 가입 신청 (Invites & Join Requests)**
- `POST /rooms/{roomId}/invites` — 초대 코드 발급/재발급
- `POST /invites/accept` — 코드로 가입 신청(즉시 입장 아님)
- `POST /join-requests/{id}/accept` · `POST /join-requests/{id}/undo` — 신청 수락·5분 되돌리기

**약속 (Plans)**
- `POST /rooms/{roomId}/plans` · `POST /plans/{planId}/complete` — 등록·완료(추억 전환 트리거)
- `POST /plans/{planId}/stage-photos` — 4단계 인증사진 업로드

**추억 (Memories)**
- `POST /plans/{planId}/memories` · `POST /rooms/{roomId}/memories` — 약속 연동 추억 / 자유 추억 작성
- `GET /rooms/{roomId}/memories` — 추억 피드(월별·태그·참여자 필터)
- `POST /memories/{memoryId}/comments` — 친구 한 줄 댓글

**행운편지 (Letters)**
- `POST /rooms/{roomId}/letters` — 발송(지정 또는 전체 발송)
- `GET /rooms/{roomId}/letters?box=received|sent` — 편지함 조회

**경험치 · 상점 (Exp / Shop)**
- `GET /rooms/{roomId}/level` — 우정 레벨·경험치 조회
- `GET /shop/items` · `POST /shop/items/{itemId}/purchase` — 상점 아이템 조회·구매
- `GET /shop/transactions` — 골드 거래 원장(내역) 조회

**알림 (Notifications)**
- `GET /rooms/{roomId}/notifications` — 알림 목록(공지/친구/가입신청 탭)

</details>

> 전체 엔드포인트·요청/응답 스키마는 [API-CONTRACT.md](https://github.com/Pickeslog/web-design-repository/blob/main/docs/API-CONTRACT.md) 참고.

## 🗄 데이터베이스 설계

MySQL 8, 총 24개 테이블을 도메인 단위로 관리합니다.

| 도메인 | 대표 테이블 |
|---|---|
| 인증/사용자 | `users`, `refresh_tokens`, `password_reset_tokens`, `user_preferences` |
| 우정공간 | `friendship_rooms`, `room_members`, `friendship_exp_logs` |
| 초대/가입신청 | `room_invites`, `room_join_requests` |
| 약속 | `plans`, `plan_checklists`, `plan_stage_photos` |
| 추억 | `memories`, `memory_images`, `memory_comments`, `memory_participants`, `memory_tags` |
| 행운편지 | `lucky_letters`, `letter_favorites` |
| 알림 | `notifications` |
| 상점 | `shop_items`, `user_wallets`, `user_inventory_items`, `wallet_transactions` |

> 전체 ERD·DDL은 [api-spec/](https://github.com/Pickeslog/web-design-repository/tree/main/api-spec) 참고.

## 📝 커밋 컨벤션

[Conventional Commits](https://www.conventionalcommits.org/)를 따릅니다.

```
1. 커밋 유형 지정 (영어 소문자)
   - feat     : 새로운 기능 추가
   - fix      : 버그 수정
   - docs     : 문서 수정
   - style    : 코드 포맷팅, 세미콜론 등 코드 변경이 없는 경우
   - refactor : 코드 리팩토링
   - test     : 테스트 코드 추가/수정
   - chore    : 빌드/설정 등 기타 변경

2. 이슈 번호와 함께 작성
   feat: implement login API (#6)

3. 제목은 영문 기준 50자 이내, 명령형으로 작성
```

## 💻 코드 컨벤션

실제 코드베이스를 기준으로 정리했습니다.

**clov-api (Java)**
- 도메인 단위 패키지 구조: `domain/<도메인>/{controller, service, mapper, dto, entity}`
- JPA, `@Entity`, Spring Data Repository는 사용하지 않는다 (MyBatis만 사용)
- 컨트롤러는 얇게 유지하고, 트랜잭션·비즈니스 로직은 서비스 계층에 둔다
- Mapper 인터페이스와 Mapper XML의 `namespace`/statement `id`는 정확히 일치시킨다
- SQL 파라미터는 `#{}`를 사용한다 (`${}`는 원칙적으로 금지)
- 들여쓰기 4칸, Lombok으로 getter/setter·생성자 보일러플레이트를 줄인다

**clov-web (JavaScript/React)**
- 세미콜론을 붙이지 않는다
- 문자열은 작은따옴표(`'`)를 사용한다
- 들여쓰기 2칸
- `var`는 사용하지 않는다 (`const`/`let`만 사용)
- 화살표 함수는 매개변수가 1개여도 괄호를 생략하지 않는다: `(payload) => ...`
- 컴포넌트는 PascalCase, 함수·변수는 camelCase로 작성한다
- API 호출은 `src/api/`를 거치며, 컴포넌트에서 직접 `fetch`를 호출하지 않는다
- 서버 데이터는 TanStack Query로, 클라이언트 전역 상태는 Zustand로 관리한다

## 🚀 로컬 실행 방법

**clov-api (백엔드)**
```bash
# 1. 시크릿 설정 파일 생성 후 DB·OAuth 정보 입력
cp src/main/resources/application-secret.example.yaml src/main/resources/application-secret.yaml

# 2. 테스트
./gradlew test

# 3. 실행 (http://localhost:8080)
./gradlew bootRun
```

**clov-web (프론트엔드)**
```bash
# 1. 패키지 설치
npm install

# 2. 개발 서버 실행 (http://localhost:5173)
npm run dev

# 3. 빌드
npm run build
```

## 🔀 브랜치 전략

[GitHub Flow](https://docs.github.com/ko/get-started/using-github/github-flow)를 따릅니다. 이슈 단위로 브랜치를 분기하고 `main`에 지속적으로 merge합니다.

```
feat/<issue번호>-<주제>    예) feat/12-room-invite
fix/<issue번호>-<주제>     예) fix/45-login-token-refresh
chore/<주제>              예) chore/gitignore
```

- 1이슈 = 1브랜치 = 1PR 원칙, `main` 직접 작업 금지
- PR은 코드 리뷰와 CI(빌드·통합테스트) 통과 후 머지

## 🤝 협업 방식

- **이슈 템플릿** — 버그·기능 요청 템플릿을 저장소별로 갖추고 사용합니다.
- **계약 우선(Contract-First)** — `web-design-repository`의 API 계약·DB 설계가 단일 진실 소스(SSOT). 코드보다 문서를 먼저 확정합니다.
- **도메인 분리 병렬 작업** — 방·초대·일정·추억·편지·알림·사용자 등 도메인을 담당자가 백엔드부터 프론트엔드까지 세로로 책임지고, 레포·도메인을 나눠 충돌을 최소화하며 동시에 진행합니다.
- **AI 페어 협업** — 각 개발자가 AI 코딩 어시스턴트와 페어를 이뤄 구현하고, 교차 리뷰로 품질을 검증합니다.

## 📊 진행 상황 관리

- [조직 Projects](https://github.com/orgs/Pickeslog/projects) — 칸반 보드로 전체 진행 상황 관리
- [clov-api Issues](https://github.com/Pickeslog/clov-api/issues) · [clov-web Issues](https://github.com/Pickeslog/clov-web/issues) · [web-design-repository Issues](https://github.com/Pickeslog/web-design-repository/issues)

## 📚 문서 (SSOT)

| 문서 | 내용 |
|---|---|
| [API-CONTRACT.md](https://github.com/Pickeslog/web-design-repository/blob/main/docs/API-CONTRACT.md) | REST API 계약, 권한 · 에러 모델 |
| [screen-spec-source/](https://github.com/Pickeslog/web-design-repository/tree/main/screen-spec-source) | 화면별 명세(대시보드 · 추억피드 · 행운편지 · 일정계획 등) |
| [api-spec/](https://github.com/Pickeslog/web-design-repository/tree/main/api-spec) | DB 통합 설계 · 리소스 맵 |
