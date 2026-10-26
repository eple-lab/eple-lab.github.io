# eple-lab.github.io

espace eple — [Hugo](https://gohugo.io/) + [Hextra](https://github.com/imfing/hextra) 테마 블로그

https://eple-lab.github.io/

## 로컬 실행

```bash
# 1. Hugo 설치 (PC에 한 번만, 설치 후 터미널을 새로 열기)
winget install Hugo.Hugo.Extended

# 2. 새로 clone했을 때만: 테마 받기
git submodule update --init --recursive

# 3. 블로그 폴더에서 미리보기 실행 → http://localhost:1313/
hugo server
```

`main`에 푸시하면 GitHub Actions(`.github/workflows/hugo.yml`)가 빌드해서 GitHub Pages에 배포합니다.

## 변경이력

### 테마 변경 2026-10-23
Hugo Book에서 Hextra(v0.13.0)로 바꾸고, 블로그 글을 카테고리·태그로 나눌 수 있게 했습니다.

### 워크플로 액션 버전 업그레이드 2026-10-23
Node.js 20 지원 종료 경고 때문에 Node.js 24로 동작하는 버전으로 올렸습니다.

| 액션 | 이전 | 변경 |
|---|---|---|
| actions/checkout | v4 | v7 |
| actions/configure-pages | v5 | v6 |
| actions/upload-pages-artifact | v3 | v5 |
| actions/deploy-pages | v4 | v5 |
