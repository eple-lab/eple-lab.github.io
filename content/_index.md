---
title: espace eple
layout: hextra-home
---

<section class="home-hero">
  <div class="home-hero-text">
    <p class="home-eyebrow">Backend-focused Full-stack · AI Agent</p>
    <h1 class="home-title">espace eple</h1>
    <p class="home-sub">AI 에이전트와 함께 나만의 신호를 찾아가는 소중한 기록장</p>
    <div class="home-links">
      <a href="/blog/">blog →</a>
      <a href="/about/">about →</a>
    </div>
  </div>
  <aside class="home-profile">
    <img class="home-logo" src="/images/logo.svg" alt="eple">
    <p class="home-profile-name">eple</p>
    <p class="home-tagline">Free web, with agents</p>
    <p class="home-profile-loc">Seoul, Korea</p>
    <div class="about-links">
      <a href="https://github.com/eple-lab" target="_blank" rel="noopener" title="GitHub" aria-label="GitHub">{{< icon "github" >}}</a>
      <a href="https://www.linkedin.com/in/eple-e-3b3013442" target="_blank" rel="noopener" title="LinkedIn" aria-label="LinkedIn">{{< icon "linkedin" >}}</a>
      <a href="#connect" title="Contact" aria-label="Contact">{{< icon "mail" >}}</a>
    </div>
  </aside>
</section>

<img class="home-signal" src="/images/signal.svg" alt="" aria-hidden="true">

<section class="home-section">
  <p class="home-label">01 · Quick facts</p>
  <div class="home-facts">
    <div class="home-card"><p class="home-card-key">Now</p><p>AI와 함께 Agent Team 만드는 중</p></div>
    <div class="home-card"><p class="home-card-key">Next</p><p>AX 컨설팅. 기업 AX 도입과 에이전트 권한·보안 설계</p></div>
    <div class="home-card"><p class="home-card-key">Building</p><p><a href="/docs/news-pick/">news-pick</a>, <a href="/docs/dalbit-lake/">dalbit-lake</a></p></div>
  </div>
</section>

<section class="home-section">
  <p class="home-label">02 · Projects</p>
  {{< home-projects >}}
</section>

<section class="home-section">
  <p class="home-label">03 · What I work with</p>
  {{< home-tech label="Backend · DevOps" items="Java, Python, Spring Boot, Spring Security, Spring Batch, eGovFrame, MyBatis, JPA, OAuth2, MSA, Kafka, Oracle, PostgreSQL, MySQL, Docker, Kubernetes, Jenkins, Git, GitHub Actions, GitHub Pages, Hugo, Hextra" >}}
  {{< home-tech label="Frontend" reverse="true" items="Vue.js, Nexacro, XPlatform, NCRM, HTML, CSS, JavaScript, Three.js" >}}
  {{< home-tech label="AI · Agent" items="Claude Code, Prompt Engineering, Agent Workflow Design" >}}
</section>

<section class="home-section">
  <p class="home-label">04 · Latest writing</p>
  {{< home-latest count="3" >}}
</section>

<section class="home-section home-connect" id="connect">
  <p>AX 도입, AI 에이전트 구축, 협업·제휴 제안은 {{< home-connect >}}로 남겨 주세요.</p>
</section>
