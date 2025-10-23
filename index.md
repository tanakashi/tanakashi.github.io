---
layout: default
title: Tanakashi Portfolio
---

# 👋 Hello

ここには、webアプリをはじめとした個人開発の記録をまとめています。

## 🧩 Projects

<ul class="project-list">
{% for p in site.projects %}
  <li style="margin-bottom: 15px">
    <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
    {% if p.demo_url %}<a href="{{ p.demo_url }}" class="button" target="_blank">Demo</a>{% endif %}
    <div>
      {% if p.develop_term %}<small>🗓️ {{ p.develop_term | join: "〜" }}　</small>{% endif %}
      {% if p.tags %}<small>🏷️ {{ p.tags | join: ", " }}</small>{% endif %}
    </div>
    <!-- {% if p.repo_url %}　<a href="{{ p.repo_url }}" target="_blank">GitHub ▶</a>{% endif %} -->
  </li>
{% endfor %}
</ul>