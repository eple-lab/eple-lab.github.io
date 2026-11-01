---
title: todo
description: 하위 태스크가 있는 Todo 앱 (Express + SQLite / Supabase, Render 배포)
weight: 3
---

큰 할 일(Todo) 아래에 하위 태스크(Task)를 두고 하나씩 체크하는 Todo 앱입니다. 데이터는 DB에 저장되어 껐다 켜도 남습니다.

- 운영 서버: [todo-0vru.onrender.com](https://todo-0vru.onrender.com/) (Supabase 모드, 회원가입·로그인 후 사용)
- 데모: [eple-lab.github.io/todo](https://eple-lab.github.io/todo/) (서버 없이 브라우저에서만 동작, 새로고침하면 초기화)
- 저장소: [eple-lab/todo](https://github.com/eple-lab/todo)
- 시작: 2026-10-29
- 출발점: [새로고침해도 남는 Todo 앱](/blog/assignment/todo-app-2026-10-31/) (과제)

## 무엇을 하나

| 화면 위치 | 기능 |
|---|---|
| 위쪽 | 할 일·태스크 제목 검색, "오늘 할 일만" 보기. Supabase 모드에서는 로그인한 이메일과 로그아웃 |
| 가운데 | 할 일과 하위 태스크. 진행률(2/4), 마감일, 완료한 할 일의 자동 삭제 날짜. 오늘 마감인 할 일은 노란 배경 |
| 아래쪽 | 할 일 등록(마감일 기본값 오늘). "태스크로 등록"을 체크하면 넣을 할 일을 고른다 |

규칙은 이렇습니다.

- 태스크는 반드시 하나의 할 일에 속하고, 한 단계만 있다.
- 안 끝난 태스크가 있는 할 일을 완료하면 확인창을 띄우고, 확인하면 남은 태스크도 함께 완료한다.
- 마감일은 필수. 지난 날짜는 화면과 백엔드 모두에서 거절한다.
- 미완료 할 일끼리, 같은 할 일 안의 태스크끼리는 같은 제목을 쓸 수 없다.
- 완료 후 90일이 지나면 자동 삭제한다.

## 두 가지 모드

`.env` 설정으로 저장소를 고릅니다.

| 모드 | 언제 | 저장 위치 | 로그인 |
|---|---|---|---|
| SQLite (길 A) | `.env`에 Supabase 정보가 없으면 | 내 컴퓨터 `data/todo.db` | 없음 (혼자 쓰기) |
| Supabase (길 B) | `.env`에 Supabase 정보가 있으면 | 클라우드 Postgres | 이메일 회원가입·로그인, 내 할 일만 보기(RLS) |

서버가 켜질 때 첫 줄에 지금 모드가 나옵니다. 정보를 하나만 채우면 설정 실수로 보고 서버가 켜지지 않습니다.

## 문서 구성

{{< cards cols="1" >}}
  {{< card link="how-it-works" title="동작 방식" subtitle="구조, DB, 보안, 테스트" >}}
  {{< card link="history" title="히스토리" subtitle="PRD부터 길 A·B, Render 배포, 버그 수정까지" >}}
{{< /cards >}}
