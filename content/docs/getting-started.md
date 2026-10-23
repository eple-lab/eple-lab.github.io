---
title: 블로그 시작하기
weight: 1
---

이 사이트는 [Hugo](https://gohugo.io/)와 [Hextra](https://github.com/imfing/hextra) 테마로 만들었고, GitHub Actions로 GitHub Pages에 배포됩니다.

## 새 문서 추가

`content/docs/` 아래에 마크다운 파일을 추가하면 왼쪽 메뉴에 나타납니다.

## 새 글 추가

`content/blog/` 아래에 마크다운 파일을 추가하면 블로그 목록에 나타납니다. 글 머리말에 `categories`와 `tags`를 적으면 카테고리·태그 페이지에 자동으로 모입니다.

```yaml
---
title: 글 제목
date: 2026-10-23
categories:
  - 개발
tags:
  - hugo
---
```
