---
title: 히스토리
weight: 2
---

news-pick을 만들어 온 과정과, 그때그때 무엇을 왜 정했는지 기록합니다. 최근 기록이 위에 옵니다.

## 2026-10-23 첫 실행

커밋 [`7526fef`](https://github.com/eple-lab/news-pick/commit/7526fef) 설치 후 실행

- `/news-package AI 에이전트`로 첫 패키지를 만들어 [output/2026-10-23.md](https://github.com/eple-lab/news-pick/blob/main/output/2026-10-23.md)에 저장했습니다.
- 고른 뉴스 3건: Anthropic 'Claude Duet' 공개, 월마트 'Agent Gateway' 발표, OpenAI의 Orchestra Bio 인수
- 다룬 뉴스는 [data/history.md](https://github.com/eple-lab/news-pick/blob/main/data/history.md)에 기록되어, 다음 실행부터 14일 안에는 다시 고르지 않습니다.

**실행하면서 확인한 점**

- 최근 24시간 안에는 원문을 확인할 수 있는 기사가 부족해서, 규칙대로 3일까지 범위를 넓혔고 결과물에 그 사실을 밝혔습니다.
- 원 발표가 오래됐거나 2차 출처뿐인 후보, 원문을 확인하지 못한 후보는 제외됐습니다. "원문을 직접 열어 확인한다"는 규칙이 실제로 걸러 냈습니다.
- 검증 체크리스트 5개 항목을 모두 통과했습니다.

## 2026-10-23 뼈대 설정

커밋 [`27ab12b`](https://github.com/eple-lab/news-pick/commit/27ab12b) 뼈대 설정

- 과제에서 설계한 프롬프트를 `CLAUDE.md`(역할, 타겟·톤, 규칙)와 `news-package` 스킬(처리 순서, 출력 형식, 검증 체크리스트)로 나눴습니다.
- 결과물을 쌓을 `output/` 폴더와 중복을 막기 위한 `data/history.md`를 만들었습니다.

## 2026-10-23 과제 설계와 저장소 생성

커밋 [`a09cb63`](https://github.com/eple-lab/news-pick/commit/a09cb63) Initial commit

- 콘텐츠 발행 과정을 컴퓨팅 사고(분해, 패턴, 추상화, 알고리즘)로 분석하는 과제에서 출발했습니다. → [과제 글](/blog/assignment/computational-thinking-2026-10-23/)
- 과제의 추상화 결과인 "오늘의 뉴스 3개 3줄 요약 + 타겟 맞춤형 캡션 + 뉴스 링크"를 저장소 소개로 삼았습니다.
