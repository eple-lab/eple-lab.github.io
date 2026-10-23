# eple-lab.github.io

eple space — [Hugo](https://gohugo.io/) + [Hugo Book](https://github.com/alex-shpak/hugo-book) 테마 블로그

https://eple-lab.github.io/

## 로컬 실행

```bash
git submodule update --init --recursive
hugo server
```

`main`에 푸시하면 GitHub Actions(`.github/workflows/hugo.yml`)가 빌드해서 GitHub Pages에 배포합니다.

## 워크플로 액션 버전

Node.js 20 지원 종료 경고 때문에 Node.js 24로 동작하는 버전으로 올렸습니다.

| 액션 | 이전 | 변경 |
|---|---|---|
| actions/checkout | v4 | v7 |
| actions/configure-pages | v5 | v6 |
| actions/upload-pages-artifact | v3 | v5 |
| actions/deploy-pages | v4 | v5 |
