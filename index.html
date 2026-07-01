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
      --bar-bg:   #5c6bc0;
      --bar-h:    25px;
    }

    body {
      font-family: 'DM Sans', sans-serif;
      font-weight: 300;
      background: var(--bg);
      color: var(--ink);
      min-height: 100vh;
    }

    /* ── THIN MENU BAR (TiddlyWiki-style) ── */
    .menubar {
      height: var(--bar-h);
      background: var(--bar-bg);
      display: flex;
      align-items: center;
      padding: 0 0.75rem;
      overflow-x: auto;
      white-space: nowrap;
    }
    .menubar-title {
      font-family: 'DM Sans', sans-serif;
      font-size: 0.7rem;
      font-weight: 500;
      letter-spacing: 0.04em;
      color: #fff;
      padding-right: 1rem;
      flex-shrink: 0;
    }
    .menubar-tabs {
      display: flex;
      height: 100%;
      list-style: none;
      flex-shrink: 0;
    }
    .tab-btn {
      background: none;
      border: none;
      height: 100%;
      padding: 0 0.85rem;
      font-family: 'DM Sans', sans-serif;
      font-size: 0.7rem;
      font-weight: 400;
      letter-spacing: 0.02em;
      color: rgba(255,255,255,0.72);
      cursor: pointer;
      transition: background 0.12s, color 0.12s;
      white-space: nowrap;
    }
    .tab-btn:hover { background: rgba(255,255,255,0.1); color: #fff; }
    .tab-btn:focus-visible { outline: 1px solid #fff; outline-offset: -2px; }
    .tab-btn.active { background: rgba(255,255,255,0.16); color: #fff; font-weight: 500; }

    .panels { max-width: 800px; margin: 0 auto; padding: 3rem 3rem 6rem; }
    .panel { display: none; }
    .panel.active { display: block; animation: rise 0.2s ease both; }
    @keyframes rise { from { opacity: 0; transform: translateY(6px); } to { opacity: 1; transform: translateY(0); } }
    @media (prefers-reduced-motion: reduce) { .panel.active { animation: none; } }

    .panel h2 {
      font-family: 'DM Serif Display', serif;
      font-size: clamp(1.6rem, 3vw, 2rem);
      line-height: 1.12;
      color: var(--ink);
      margin-bottom: 1.4rem;
    }
    .panel h3 {
      font-family: 'DM Serif Display', serif;
      font-size: 1.15rem;
      line-height: 1.25;
      color: var(--ink);
      margin-top: 2.4rem;
      margin-bottom: 0.6rem;
    }
    .panel p {
      font-size: 0.95rem;
      line-height: 1.8;
      color: var(--mid);
      max-width: 580px;
      margin-bottom: 1rem;
    }
    .panel p strong { color: var(--ink); font-weight: 500; }
    .panel p em { font-style: italic; }
    .panel blockquote {
      font-family: 'DM Serif Display', serif;
      font-style: italic;
      font-size: 1.04rem;
      color: var(--ink);
      line-height: 1.7;
      margin-bottom: 1.7rem;
      padding-left: 1.2rem;
      border-left: 3px solid var(--red);
      max-width: 580px;
    }
    .panel hr { border: none; border-top: 1px solid var(--rule-lt); margin: 2.4rem 0; }
    .panel ul { margin: 0.5rem 0 1.5rem 0; max-width: 580px; }
    .panel ul li {
      list-style: none;
      font-size: 0.95rem;
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

    footer { border-top: 1px solid var(--rule); padding: 1.25rem 3rem; font-size: 0.74rem; color: var(--mid); display: flex; justify-content: space-between; flex-wrap: wrap; gap: 0.5rem; }
    footer a { color: inherit; text-decoration: none; }
    footer a:hover { color: var(--ink); }

    @media (max-width: 640px) {
      footer { padding-left: 1.5rem; padding-right: 1.5rem; }
      .panels { padding: 2.25rem 1.5rem 4rem; }
      .menubar-title { display: none; }
    }
  </style>
</head>
<body>

<div class="menubar">
  <span class="menubar-title">{{ site.title }}</span>
  <ul class="menubar-tabs" role="tablist" aria-label="Course sections">
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
