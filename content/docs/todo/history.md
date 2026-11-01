---
title: 히스토리
weight: 2
---

todo를 만들어 온 과정입니다. 최근 기록이 위에 옵니다.

## 2026-10-31 테스트와 버그 수정

| 커밋 | 내용 |
|---|---|
| [`c6a54b3`](https://github.com/eple-lab/todo/commit/c6a54b3) | BUG-001: 로그아웃 후 로그인 화면에 이전 이메일이 남는 문제 |
| [`66ea73d`](https://github.com/eple-lab/todo/commit/66ea73d) | BUG-002: RLS 확인 스크립트에 대조군·반대 방향 추가, 19/19 |
| [`f18eea7`](https://github.com/eple-lab/todo/commit/f18eea7) | 기본 기능 API 자동 테스트 (`npm test`) |
| [`fd6e5f7`](https://github.com/eple-lab/todo/commit/fd6e5f7) | BUG-003: 태스크 등록 후·계정을 바꿀 때 등록창·검색 상태 초기화 |
| [`51dc3b8`](https://github.com/eple-lab/todo/commit/51dc3b8) | 이메일 인증은 평소 켜 두고 테스트 계정 만들 때만 끄도록 안내 |

RLS 확인은 1차 15/15 → B 쪽 대조군과 반대 방향이 빠진 걸 찾아 보강 → 2차 18/19(테스트 쪽 버그) → 3차 19/19로 마무리했습니다.

## 2026-10-31 길 A·B 합치기와 Render 배포

| 커밋 | 내용 |
|---|---|
| [`f794d01`](https://github.com/eple-lab/todo/commit/f794d01) | 프로젝트 이름을 TODO로 변경 |
| [`f3fcc53`](https://github.com/eple-lab/todo/commit/f3fcc53) | 길 B(Supabase) 브랜치를 main에 합치기 |
| [`c968f87`](https://github.com/eple-lab/todo/commit/c968f87) | `.env` 설정에 따라 SQLite / Supabase 중 하나로 동작 |
| [`b76066d`](https://github.com/eple-lab/todo/commit/b76066d) | Render 배포 설정을 `render.yaml`(Blueprint)로 관리 |

## 2026-10-30 길 B: Supabase, 로그인, RLS

| 커밋 | 내용 |
|---|---|
| [`77c4fb8`](https://github.com/eple-lab/todo/commit/77c4fb8) | B-0: 길 A 저장 확인 캡처, `path-a` 태그 |
| [`fe4a6e4`](https://github.com/eple-lab/todo/commit/fe4a6e4) | B-1: Supabase 스키마, RLS 정책, 규칙 함수 |
| [`7ad5c07`](https://github.com/eple-lab/todo/commit/7ad5c07) | B-2: 백엔드를 Supabase로 전환, 로그인 API |
| [`e51ed9a`](https://github.com/eple-lab/todo/commit/e51ed9a) | B-3: 로그인·회원가입 화면 |
| [`1f2c576`](https://github.com/eple-lab/todo/commit/1f2c576) | B-4: RLS 확인 스크립트 |
| [`91eda47`](https://github.com/eple-lab/todo/commit/91eda47) | B-5: 문서를 Supabase 기준으로 갱신, 연결 가이드 |

- 길 A 코드는 태그로 남기고 main을 Supabase로 바꿨습니다.
- 서버는 관리자 키를 쓰지 않고, 로그인한 사용자의 토큰으로만 DB를 부르게 했습니다.
- 같은 날 코드 리뷰(`Review.md`)를 PR로 받아 합쳤습니다.

## 2026-10-29 ~ 10-30 길 A: 로컬 SQLite

| 커밋 | 내용 |
|---|---|
| [`cf03652`](https://github.com/eple-lab/todo/commit/cf03652) | A-1: PRD 작성, SQLite DB 구조 설계 |
| [`60ea9d0`](https://github.com/eple-lab/todo/commit/60ea9d0) | A-3: Express + 내장 SQLite(`node:sqlite`)로 구현 |
| [`9bf154e`](https://github.com/eple-lab/todo/commit/9bf154e) | A-4: 마감일 필수·지난 날짜 금지, 중복 제목 금지, 화면 개선 |
| [`944020d`](https://github.com/eple-lab/todo/commit/944020d) | A-6: GitHub Pages 데모 모드 |
| [`dc2114e`](https://github.com/eple-lab/todo/commit/dc2114e) | A-7: 문서를 `docs/`로 정리 |

- 강의 예시의 `better-sqlite3`는 Windows에서 빌드 에러가 잦다고 해서, 설치할 것이 없는 Node 내장 `node:sqlite`를 골랐습니다.
- 할 일과 태스크를 표 2개(1:N)로 나눠, "태스크는 반드시 할 일에 속한다"를 표 구조로 보장했습니다.
