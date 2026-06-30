---
layout: null
title: "AI and the Human Future"
---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>{{ site.title }}</title>
  <link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --ink:      #333;
      --mid:      #666;
      --faint:    #999;
      --rule:     #ccc;
      --rule-lt:  #ddd;
      --bg:       #f5f5f5;
      --cream:    #ede9e2;
      --white:    #ffffff;
      --red:      #8C1515;
      --red-pale: #fdf5f5;
    }

    body {
      font-family: 'DM Sans', sans-serif;
      font-weight: 300;
      background: var(--bg);
      color: var(--ink);
      min-height: 100vh;
    }

    header {
      border-bottom: 1px solid var(--rule);
      padding: 2rem 3rem 1.75rem;
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      flex-wrap: wrap;
      gap: 1rem;
    }
    .site-name {
      font-family: 'DM Serif Display', serif;
      font-size: 1.1rem;
      letter-spacing: 0.01em;
      color: var(--ink);
      text-decoration: none;
    }
    .site-name:hover { color: var(--red); }
    .site-meta {
      font-size: 0.75rem;
      color: var(--mid);
      letter-spacing: 0.04em;
      text-transform: uppercase;
      line-height: 1.8;
      text-align: right;
    }

    .hero {
      padding: 3rem 3rem 2.75rem;
      border-bottom: 1px solid var(--rule);
    }
    .course-eyebrow {
      font-size: 0.7rem;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      font-weight: 500;
      color: var(--mid);
      margin-bottom: 0.6rem;
    }
    .hero h1 {
      font-family: 'DM Serif Display', serif;
      font-size: clamp(2.2rem, 5vw, 3.4rem);
      line-height: 1.06;
      color: var(--red);
      margin-bottom: 1.1rem;
      max-width: 680px;
    }
    .hero-sub {
      font-size: 0.97rem;
      line-height: 1.8;
      color: var(--mid);
      max-width: 580px;
    }

    .tab-bar {
      border-bottom: 1px solid var(--rule);
      padding: 0 3rem;
      background: var(--bg);
      overflow-x: auto;
    }
    .tab-nav { display: flex; gap: 0; list-style: none; }
    .tab-btn {
      background: none;
      border: none;
      border-bottom: 2px solid transparent;
      padding: 1rem 1.2rem 0.85rem;
      font-family: 'DM Sans', sans-serif;
      font-size: 0.78rem;
      font-weight: 500;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      color: var(--faint);
      cursor: pointer;
      transition: color 0.15s, border-color 0.15s;
      margin-bottom: -1px;
      white-space: nowrap;
    }
    .tab-btn:hover { color: var(--ink); }
    .tab-btn:focus-visible { outline: 2px solid var(--red); outline-offset: 2px; }
    .tab-btn.active { color: var(--red); border-bottom-color: var(--red); }

    .panels { max-width: 800px; margin: 0 auto; padding: 4rem 3rem 7rem; }
    .panel { display: none; }
    .panel.active { display: block; animation: rise 0.25s ease both; }
    @keyframes rise { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; transform: translateY(0); } }
    @media (prefers-reduced-motion: reduce) { .panel.active { animation: none; } }

    .panel h2 {
      font-family: 'DM Serif Display', serif;
      font-size: clamp(1.7rem, 3vw, 2.1rem);
      line-height: 1.12;
      color: var(--ink);
      margin-bottom: 1.4rem;
    }
    .panel h3 {
      font-family: 'DM Serif Display', serif;
      font-size: 1.18rem;
      line-height: 1.25;
      color: var(--ink);
      margin-top: 2.5rem;
      margin-bottom: 0.65rem;
    }
    .panel p {
      font-size: 0.96rem;
      line-height: 1.82;
      color: var(--mid);
      max-width: 580px;
      margin-bottom: 1rem;
    }
    .panel p strong { color: var(--ink); font-weight: 500; }
    .panel p em { font-style: italic; }
    .panel blockquote {
      font-family: 'DM Serif Display', serif;
      font-style: italic;
      font-size: 1.06rem;
      color: var(--ink);
      line-height: 1.72;
      margin-bottom: 1.8rem;
      padding-left: 1.3rem;
      border-left: 3px solid var(--red);
      max-width: 580px;
    }
    .panel hr { border: none; border-top: 1px solid var(--rule-lt); margin: 2.5rem 0; }
    .panel ul { margin: 0.5rem 0 1.5rem 0; max-width: 580px; }
    .panel ul li {
      list-style: none;
      font-size: 0.96rem;
      line-height: 1.65;
      color: var(--ink);
      padding-left: 1.3rem;
      position: relative;
      margin-bottom: 0.5rem;
    }
    .panel ul li::before { content: '\2014'; position: absolute; left: 0; color: var(--red); font-weight: 300; }

    .panel table {
      border-collapse: collapse;
      margin: 1.5rem 0 2rem;
      width: 100%;
      max-width: 580px;
    }
    .panel table th, .panel table td {
      border: 1px solid var(--rule-lt);
      padding: 0.6rem 0.9rem;
      font-size: 0.85rem;
      text-align: left;
      color: var(--mid);
    }
    .panel table th {
      background: var(--white);
      color: var(--ink);
      font-weight: 500;
    }

    .panel pre {
      border: 1px solid var(--rule-lt);
      background: var(--white);
      padding: 1.25rem 1.5rem;
      font-size: 0.83rem;
      line-height: 1.6;
      overflow-x: auto;
      margin-bottom: 1.25rem;
      position: relative;
      white-space: pre-wrap;
    }
    .copy-btn {
      position: absolute;
      top: 0.7rem;
      right: 0.9rem;
      background: var(--bg);
      border: 1px solid var(--rule);
      padding: 0.28rem 0.85rem;
      font-family: 'DM Sans', sans-serif;
      font-size: 0.72rem;
      font-weight: 500;
      letter-spacing: 0.04em;
      color: var(--mid);
      cursor: pointer;
      transition: border-color 0.15s, color 0.15s;
    }
    .copy-btn:hover { border-color: var(--ink); color: var(--ink); }
    .copy-btn.copied { border-color: var(--red); color: var(--red); }

    .further { border-top: 1px solid var(--rule); background: var(--cream); padding: 2.25rem 3rem; }
    .further-inner { max-width: 800px; margin: 0 auto; display: flex; align-items: baseline; gap: 2rem; flex-wrap: wrap; }
    .further-label { font-size: 0.7rem; letter-spacing: 0.14em; text-transform: uppercase; font-weight: 500; color: var(--red); flex-shrink: 0; margin: 0; }
    .further-desc { font-size: 0.88rem; line-height: 1.65; color: var(--mid); flex: 1; min-width: 200px; margin: 0; }
    .further-link { font-size: 0.82rem; font-weight: 500; color: var(--red); text-decoration: none; letter-spacing: 0.02em; border-bottom: 1px solid transparent; transition: border-color 0.15s; flex-shrink: 0; white-space: nowrap; }
    .further-link:hover { border-bottom-color: var(--red); }

    footer { border-top: 1px solid var(--rule); padding: 1.75rem 3rem; font-size: 0.76rem; color: var(--mid); display: flex; justify-content: space-between; flex-wrap: wrap; gap: 0.5rem; }
    footer a { color: inherit; text-decoration: none; }
    footer a:hover { color: var(--ink); }

    @media (max-width: 640px) {
      header, .hero, .tab-bar, footer, .further { padding-left: 1.5rem; padding-right: 1.5rem; }
      .panels { padding: 2.75rem 1.5rem 5rem; }
      .tab-btn { padding: 0.85rem 0.7rem; font-size: 0.7rem; letter-spacing: 0.04em; }
      .site-meta { text-align: left; }
      .further-inner { flex-direction: column; gap: 0.75rem; }
    }
  </style>
</head>
<body>

<header>
  <a class="site-name" href="{{ site.url }}{{ site.baseurl }}/">{{ site.author }}</a>
  <div class="site-meta">
    SUNY Polytechnic Institute<br>
    Communications &amp; Humanities
  </div>
</header>

<div class="hero">
  <p class="course-eyebrow">AI-FYE &nbsp;&middot;&nbsp; FYS 111 + COM 216 &nbsp;&middot;&nbsp; Fall 2026 &nbsp;&middot;&nbsp; SUNY Polytechnic Institute</p>
  <h1>AI and the Human Future</h1>
  <p class="hero-sub">A five-credit first-year experience combining <strong>FYS 111: The AI Experience</strong> and <strong>COM 216: Digital Media, Information and Society</strong> &mdash; skills and intellectual framework, back to back, Tuesday and Thursday, built for students who want to learn how to live with AI from their first day of college.</p>
</div>

<div class="tab-bar">
  <ul class="tab-nav" role="tablist" aria-label="Course sections">
    {% assign sorted_tabs = site.tabs | sort: "order" %}
    {% for tab in sorted_tabs %}
    <li>
      <button class="tab-btn{% if forloop.first %} active{% endif %}"
              role="tab"
              aria-selected="{% if forloop.first %}true{% else %}false{% endif %}"
              data-tab="{{ tab.tab }}">{{ tab.title }}</button>
    </li>
    {% endfor %}
  </ul>
</div>

<div class="panels">
  {% for tab in sorted_tabs %}
  <div class="panel{% if forloop.first %} active{% endif %}" id="panel-{{ tab.tab }}" role="tabpanel">
    {{ tab.content }}
  </div>
  {% endfor %}
</div>

<div class="further">
  <div class="further-inner">
    <p class="further-label">Further Reading &amp; Review</p>
    <p class="further-desc">A curated playlist of videos, lectures, and interviews extending the themes of the course &mdash; from the history of writing to the mechanics of large language models.</p>
    <a class="further-link" href="https://www.youtube.com/playlist?list=PLbaIrbP2u8mAuniN933LKC6GygI4nZni4" target="_blank">View the playlist &rarr;</a>
  </div>
</div>

<footer>
  <span>{{ site.author }} &nbsp;&middot;&nbsp; <a href="mailto:{{ site.email }}">{{ site.email }}</a></span>
  <span>COM 216 (4 cr) &nbsp;&middot;&nbsp; FYS 111 (1 cr) &nbsp;&middot;&nbsp; SUNY Polytechnic Institute</span>
</footer>

<script>
  const btns   = document.querySelectorAll('.tab-btn');
  const panels = document.querySelectorAll('.panel');

  btns.forEach(btn => {
    btn.addEventListener('click', () => {
      const id = btn.dataset.tab;
      btns.forEach(b => { b.classList.remove('active'); b.setAttribute('aria-selected', 'false'); });
      panels.forEach(p => p.classList.remove('active'));
      btn.classList.add('active');
      btn.setAttribute('aria-selected', 'true');
      document.getElementById('panel-' + id).classList.add('active');
    });
  });

  // Add copy buttons to any <pre> code blocks (e.g. the Invitation One prompt)
  document.querySelectorAll('.panel pre').forEach(pre => {
    const btn = document.createElement('button');
    btn.className = 'copy-btn';
    btn.textContent = 'Copy';
    btn.addEventListener('click', () => {
      const text = pre.innerText.replace(/^Copy\s*/, '');
      const restore = () => { btn.textContent = 'Copy'; btn.classList.remove('copied'); };
      navigator.clipboard.writeText(text).then(() => {
        btn.textContent = 'Copied ✓';
        btn.classList.add('copied');
        setTimeout(restore, 2200);
      }).catch(restore);
    });
    pre.style.position = 'relative';
    pre.prepend(btn);
  });
</script>

</body>
</html>
