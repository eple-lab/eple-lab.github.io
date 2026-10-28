---
title: dalbit-lake
weight: 2
---

달빛이 내려앉은 호수를 배경으로 한 작은 웹 게임 모음입니다. HTML·CSS·JavaScript를 바이브 코딩으로 만들고 GitHub Pages로 배포했습니다.

- 플레이: [eple-lab.github.io/dalbit-lake](https://eple-lab.github.io/dalbit-lake/)
- 저장소: [eple-lab/dalbit-lake](https://github.com/eple-lab/dalbit-lake)
- 시작: 2026-10-27
- 출발점: [반딧불이 모으기 게임 요청문](/blog/assignment/fireflies-game-request-2026-10-28/) (과제)

## 무엇을 만드나

| 게임 | 설명 | 플레이 |
|---|---|---|
| 🌟 별빛 받기 | 호수 위 작은 배로 떨어지는 별빛을 담는 2D 게임 | [starlight/](https://eple-lab.github.io/dalbit-lake/starlight/) |
| 🧚 반딧불이 모으기 | 작은 요정이 되어 숲을 날며 반딧불이 5마리를 병에 담는 3D 게임 | [fireflies/](https://eple-lab.github.io/dalbit-lake/fireflies/) |

메인 화면의 카드를 누르면 각 게임으로 가고, 게임 처음 화면의 "← 메인으로"로 돌아옵니다.

**반딧불이 모으기**의 핵심 재미는 **"느긋하게 다가가기"**입니다. 서두르면 반딧불이가 흩어지고, 천천히 다가가 손을 내밀면 반딧불이가 스스로 날아와 손등에 앉습니다. 손등에 앉은 반딧불이를 두 손으로 감싸 유리병에 담고, 5마리를 담으면 성공입니다.

## 누구를 위한 게임인가

| 항목 | 내용 |
|---|---|
| 플레이어 | 잠깐 쉬어 가며 힐링하고 싶은 사람, 과제를 확인하는 동료 |
| 기기 | PC 키보드 (주), 휴대폰 (화면 버튼으로 조작) |
| 분위기 | 은은한 달빛, 여름밤, 동화 같은 판타지 숲 |
| 피할 것 | 무섭거나 놀라게 하는 연출, 어지러운 화면 움직임 |

## 만든 방법

1. **별빛 받기**: 채팅으로 첫 게임을 만들고, 플레이하며 "그만하기 버튼", "황금 별 더 자주"처럼 한 번에 하나씩 다시 요청했습니다.
2. **반딧불이 모으기**: 과제 템플릿으로 요청문을 쓰고, 코드를 만들기 전에 인터뷰로 [PRD](https://github.com/eple-lab/dalbit-lake/blob/main/docs/fireflies-prd.md)를 확정했습니다. 그다음 PRD대로 만들고, 플레이하며 고쳤습니다.
3. 모든 변경은 [커밋](https://github.com/eple-lab/dalbit-lake/commits/main)으로 남겼습니다.

## 문서 구성

{{< cards cols="1" >}}
  {{< card link="how-it-works" title="게임 방법과 구조" subtitle="조작 키, 규칙, HTML·CSS·JS 세 겹 파일 구성" >}}
  {{< card link="history" title="히스토리" subtitle="별빛 받기 첫 버전부터 반딧불이 모으기 플레이 후 수정까지" >}}
{{< /cards >}}
