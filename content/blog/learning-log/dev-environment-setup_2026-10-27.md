---
title: 바이브 코딩 개발환경 세팅하기 - 깔았는데 왜 예전 버전이 나와?
date: 2026-10-27 03:00:00
categories:
  - 러닝로그
tags:
  - 학습일지
  - 개발환경
  - Node.js
  - uv
---

"개발 환경 설정" 데... 설치보다 시간 더 걸린 게 있었다.
분명 새로 깔았는데 자꾸 예전 버전이 나오는 거야.. ㅜㅡㅜ
깔았던것도 많고 버전관리 안한것도 있고.. 에효..

<!--more-->

## 내 작업대 상태표

수업에 나온 "작업대 상태표" 내 PC 기준으로 채워봤다.

| 도구 | 확인 명령 | 버전 | 관리 방법 |
|---|---|---|---|
| Node.js | `node -v` | v24.22.1 (LTS) | nvm-windows |
| npm | `npm -v` | 11.19.1 | Node 깔면 같이 옴 |
| Git | `git -v` | 2.56.0 | |
| Claude Code | `claude --version` | 2.1.310 | |
| Hugo | `hugo version` | v0.168.0 extended | winget |
| uv | `uv --version` | 0.13.5 | `uv self update` |
| conda | | 원래 쓰던 거 그대로 | 데이터·머신러닝용 |

## Node.js: nvm use 했는데 왜 그대로야?

nvm으로 최신 LTS v24.22.1 깔고 `nvm use`까지 했는데 `node -v` 치면 계속 예전 버전 나옴. 이상하네...?

```text
C:\Users\eple>nvm use 24.22.1
Now using Node.js v24.22.1 by default.

C:\Users\eple>node -v
v24.21.0
```

알고 보니 nvm 깔기 전에 설치 프로그램으로 따로 깔아둔 Node.js가 있었음 ㅋ

- 예전 Node는 `C:\Program Files\nodejs`에 있고 **시스템 PATH**에 등록돼 있고
- nvm Node는 **사용자 PATH**에 등록돼 있는데
- 윈도우는 시스템 PATH를 먼저 찾는다고 함. 그래서 `nvm use`를 아무리 해도 예전 Node가 먼저 잡혔던 거

설정 → 앱에서 따로 깔린 `Node.js 24.21.0` 하나만 지우고 터미널 다시 여니까 드디어 `v24.22.1` 나옴 ^^ "via nvm-windows" 붙은 건 nvm이 관리하는 거라 지우면 안 됨! nvm 공식 안내에도 nvm 쓰기 전에 기존 Node는 지우라고 돼 있더라.

## uv: 어? 이미 깔려 있었네?

MCP 수업 때 `uvx` 쓸 것 같아서 uv도 깔기로 함. PowerShell 설치 스크립트는 실행 정책 때문에 막혀서, 정책 안 건드리고 winget으로 깔았다.

```text
winget install --id=astral-sh.uv -e
```

근데 설치된 건 0.13.5인데 `uv --version` 치니까 0.12.19가 나옴 ㅋㅋㅋ 이것도 Node랑 똑같은 상황. 예전에 설치 스크립트로 깔아둔 uv가 `C:\Users\eple\.local\bin`에 있었고 그게 먼저 잡힌 거. 같은 폴더에 uv로 받아둔 Python 3.14도 있는 거 보니까 10월 초에 이미 써봤던 듯... 아 언제 깔았지? ㅋ

하나만 남기려고 winget 쪽 지우고, 원래 있던 uv를 업데이트했다.

```text
winget uninstall --id=astral-sh.uv -e
uv self update
```

`.local\bin` 폴더에 Claude Code(`claude.exe`)도 같이 있어서 폴더째 지웠으면 큰일 날 뻔 ㅋㅋ

## conda랑 uv는 같이 쓰기로

나는 conda 가 있으니까 uv 안깔려고 했는데
uv가 conda 대신하는 건 아니더라.
심지어 uv도 깔려있었다. 

- **conda**: 데이터 분석·머신러닝처럼 무거운 패키지 쓸 때
- **uv**: MCP 서버 같은 가벼운 파이썬 도구를 `uvx`로 바로 돌릴 때

대신 한 프로젝트 안에서는 안 섞기로!
conda 환경 켜놓고 `uv pip install` 하면 conda 환경에 깔려서 헷갈린다고 함.

## Hugo는 winget으로

블로그 미리보기용 Hugo도 winget으로 깔았다. 
처음엔 블로그 폴더에 넣어야 되는 줄 알았는데 아니었음 ㅋ 
Hugo는 PC에 한 번 깔아두는 프로그램이고, `hugo server`만 블로그 폴더에서 돌리면 된다.

```text
winget install Hugo.Hugo.Extended
```

## 몸소 터득

- **"깔았다"랑 "돌아간다"는 다르다.** 설치 성공 메시지만 믿지 말고 
`--version`으로 진짜 뭐가 실행되는지 봐야 함. 
오늘 두 번이나 설치는 성공했는데 실행되는 건 예전 버전이었음 ㅋㅋ
- **이름 같은 프로그램이 두 개면 PATH에서 먼저 나오는 놈이 이긴다.** nvm 같은 버전 관리 도구 쓸 땐 따로 깔린 거부터 정리하기!
- **깔고 나면 터미널은 새로 열기.** PATH 바뀐 건 새로 연 터미널부터 적용됨.

이제 작업대 준비 끝 ^^
