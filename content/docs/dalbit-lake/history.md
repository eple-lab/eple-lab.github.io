---
title: 히스토리
weight: 2
---

dalbit-lake를 만들어 온 과정과, 그때그때 무엇을 왜 정했는지 기록합니다. 최근 기록이 위에 옵니다.

## 2026-10-28 반딧불이 모으기 플레이 후 수정

커밋 [`fa887c3`](https://github.com/eple-lab/dalbit-lake/commit/fa887c3) · [`3c63e33`](https://github.com/eple-lab/dalbit-lake/commit/3c63e33) · [`1f2a93f`](https://github.com/eple-lab/dalbit-lake/commit/1f2a93f)

직접 플레이해 보고 한 번에 한 가지씩 다시 요청했습니다.

| 차례 | 관찰한 문제 | 바꾼 것 |
|---|---|---|
| 1 | 맵이 넓고 조작이 둔함 | 맵·호수를 약 60%로 줄임, 용을 지렁이처럼 길게 + 눈 깜박임, 속도 변화 약 3배, 손 올리기 안내, 다가오는 거리 약 2배 |
| 2 | 용의 눈과 나무, 조작이 어색함 | 용이 눈꺼풀로 깜박이고 가까이 가면 쳐다봄, 나무 12그루, ↑ 앞으로·↓ 뒤로, ↓ 로 나무에 앉기 안내, 반딧불이 40 → 70마리 |
| 3 | 반딧불이가 너무 느림 | 평균 약 3배 빠르게, 느긋하게 떠다니다 가끔 휙 나는 "빨랐다 느렸다" 움직임 |

- 폴더와 문서 이름은 반딧불이가 여럿이니 `fireflies`로 통일했습니다.

## 2026-10-28 반딧불이 모으기 첫 버전

커밋 [`f18c857`](https://github.com/eple-lab/dalbit-lake/commit/f18c857) 반딧불이 모으기 3D 게임 추가

- PRD대로 `fireflies/` 폴더에 `index.html`, `styles.css`, `script.js` 세 파일로 나눠 만들었습니다.
- 이미지 파일 없이 Three.js 도형과 Web Audio 소리로만 구성했습니다.

## 2026-10-28 PRD 인터뷰

커밋 [`483eb57`](https://github.com/eple-lab/dalbit-lake/commit/483eb57) PRD 초안 → [`ec291c2`](https://github.com/eple-lab/dalbit-lake/commit/ec291c2) 남은 질문 확정

요청문의 "애매하면 물어봐" 단계를 코드 전에 문서로 끝냈습니다. 주요 결정은 이렇습니다.

| 질문 | 결정 |
|---|---|
| 시점 | 메인은 1인칭 3D, 오른쪽 위 작은 창은 3인칭 따라가기 |
| 이동 키 | W 위 / S 아래 / A·D 방향 돌리기, 앞으로 가는 빠르기는 ↑ ↓ |
| 나무에 앉기 | 멈춘 채 가지에 닿거나 나무 가까이에서 ↓ |
| 따콩 벌칙 | 손등의 반딧불이만 날아가고 1초 비틀거림 |
| 3분 뒤 계속 | 담은 반딧불이는 그대로, 3분 더 |
| Ctrl + C | 복사 대신 멈춤 창 |
| 휴대폰 | 화면 아래 키 버튼으로 조작 |
| 용의 역할 | 근처에 반딧불이가 많이 모이고, 다가가면 반김 |
| 성공 문구 | "반딧불이 다섯 친구가 병 속에서 반짝여요. 오늘 밤은 참 따뜻하네요 ✨" |

전체 결정 기록은 [PRD](https://github.com/eple-lab/dalbit-lake/blob/main/docs/fireflies-prd.md)에 있습니다.

## 2026-10-28 별빛 받기 다듬기와 메인 화면

커밋 [`d76beb3`](https://github.com/eple-lab/dalbit-lake/commit/d76beb3) · [`8bc9584`](https://github.com/eple-lab/dalbit-lake/commit/8bc9584) · [`21ef9f1`](https://github.com/eple-lab/dalbit-lake/commit/21ef9f1)

- 그만하기 버튼, 플레이 시간, 별 받기 효과, 별이 쏟아지는 엔딩을 더했습니다.
- 황금 별이 너무 드물어서 등장 빈도를 7% → 12%로 올렸습니다.
- 게임이 둘이 되면서 메인 화면을 만들고, 첫 게임을 `starlight/` 폴더로 옮겨 "별빛 받기"로 이름 붙였습니다.

## 2026-10-27 별빛 받기 첫 버전과 과제 제출

커밋 [`e6a8d37`](https://github.com/eple-lab/dalbit-lake/commit/e6a8d37) 달빛 호수 게임 추가 · [`fb06b25`](https://github.com/eple-lab/dalbit-lake/commit/fb06b25) 요청문 초안

- 강의 "HTML·CSS·JavaScript — 웹페이지를 이루는 세 겹" 과제로 첫 게임을 만들고 GitHub Pages 링크를 제출했습니다.
- 다음 게임(반딧불이 모으기)은 과제 템플릿으로 요청문부터 썼습니다. → [과제 글](/blog/assignment/fireflies-game-request-2026-10-28/)
