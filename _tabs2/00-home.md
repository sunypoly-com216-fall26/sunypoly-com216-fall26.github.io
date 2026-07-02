---
title: "SUNY Poly AI FYE"
tab: home
order: 0
version: v1.1-claude
---

<style>
  .hero { padding: 3.5rem 0 2.5rem; max-width: 600px; }
  .hero-title {
    font-size: clamp(2.4rem, 7vw, 3.6rem);
    font-weight: 500;
    line-height: 1.05;
    color: var(--ink);
    margin-bottom: 1.75rem;
    cursor: pointer;
    display: inline-block;
    transition: color 0.15s;
  }
  .hero-title:hover { color: var(--bar-bg); }
  .hero-title .year { color: var(--bar-bg); }
  .hero-hint {
    font-size: 0.72rem;
    letter-spacing: 0.08em;
    color: var(--faint);
    text-transform: uppercase;
    margin-bottom: 0.4rem;
  }
  .hero-sub {
    font-size: 1.05rem;
    line-height: 1.75;
    color: var(--mid);
    max-width: 520px;
    border-left: 3px solid var(--bar-bg);
    padding-left: 1rem;
    margin: 0;
  }
  .hero-sub em { color: var(--ink); font-style: normal; font-weight: 500; }
</style>

<div class="hero">
  <p class="hero-hint">↓ tap to start</p>
  <div class="hero-title" onclick="document.querySelector('[data-tab=start]').click()">
    AI First<br>for <span class="year">Year One</span>
  </div>
  <p class="hero-sub">
    Read, think, and write with generative AI as we study the history of human communication — from <em>memory and the spoken word</em> to <em>the transformer era of today and tomorrow</em>.
  </p>
</div>
