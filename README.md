# 設定メモ

## URL
  - https://skillupmu.github.io/mkdocs/
  - https://github.com/skillupmu/mkdocs


## git
``` 
git remote set-url origin https://skillupmu@github.com/skillupmu/mkdocs.git
git clone https://github.com/skillupmu/mkdocs.git
```


## install
 - Python 3.12.0
 - Git 2.42.0.windows.2
 - Visual Studio Code 1.84.2
 - MkDocs 1.5.3
 - Material for MkDocs 9.4.10
 - https://github.com/apps/giscus


## reference

 - [Material for MkDocs公式](https://squidfunk.github.io/mkdocs-material/reference/)
 - [Material for MkDocs公式のyaml](https://github.com/squidfunk/mkdocs-material/blob/master/mkdocs.yml)
 - [PyMdown Extensions Documentation公式](https://facelessuser.github.io/pymdown-extensions/)
 - [PyMdown Extensions Documentation公式のyaml](https://github.com/facelessuser/pymdown-extensions/blob/main/mkdocs.yml)
 - [MkDocsによるドキュメント作成（個人サイト）](https://zenn.dev/mebiusbox/articles/81d977a72cee01)
 - [おもむろにメモ書き（個人サイト）](https://omomuroni.github.io/Mkdocs/00_index/)
 - [コジオン: チェス（個人サイト）](https://kojion.github.io/chess/mkdocs/001/)
 - [黒鳥のメモ（個人サイト）](https://kurotorimkdocs.gitlab.io/kurotorimemo/040-Documents/MkDocs/Extension/)


## overrides-main

  - https://giscus.app/ja

```
{% extends "base.html" %}

{% block extrahead %}
  {% set title = config.site_name %}
  {% if page and page.title and not page.is_homepage %}
    {% set title = page.title ~ " - " ~ config.site_name | striptags %}
  {% endif %}
  {% set description = config.site_description %}
  {% if page and page.meta.description %}
    {% set description = page.meta.description %}
  {% endif %}
  {% set image = config.site_url ~ 'assets/twitter.jpg' %}
  {% if page and page.meta.image %}
    {% set image = config.site_url ~ page.meta.image %}
  {% endif %}
  <meta property="og:type" content="website">
  <meta name="twitter:card" content="summary_large_image">
  <meta property="og:title" content="{{ title }}">
  <meta name="twitter:title" content="{{ title }}">
  <meta property="og:description" content="{{ description }}">
  <meta name="twitter:description" content="{{ description }}">
  <meta property="og:image" content="{{ image }}">
  <meta name="twitter:image" content="{{ image }}">
  <meta property="og:url" content="{{ page.canonical_url }}">
{% endblock %}

{% block content %}
  {{ super() }}

  <!-- Giscus -->
  <h2 id="__comments">{{ lang.t("meta.comments") }}</h2>
  <script src="https://giscus.app/client.js"
        data-repo="kojion/chess"
        data-repo-id="R_kgDOHr3XSw"
        data-category="Announcements"
        data-category-id="DIC_kwDOHr3XS84CQVzN"
        data-mapping="pathname"
        data-reactions-enabled="1"
        data-emit-metadata="1"
        data-input-position="top"
        data-theme="light"
        data-lang="ja"
        data-loading="lazy"
        crossorigin="anonymous"
        async>
  </script>

  <!-- Synchronize Giscus theme with palette -->
  <script>
    var giscus = document.querySelector("script[src*=giscus]")

    /* Set palette on initial load */
    var palette = __md_get("__palette")
    if (palette && typeof palette.color === "object") {
      var theme = palette.color.scheme === "slate" ? "dark" : "light"
      giscus.setAttribute("data-theme", theme)
    }

    /* Register event handlers after documented loaded */
    document.addEventListener("DOMContentLoaded", function() {
      var ref = document.querySelector("[data-md-component=palette]")
      ref.addEventListener("change", function() {
        var palette = __md_get("__palette")
        if (palette && typeof palette.color === "object") {
          var theme = palette.color.scheme === "slate" ? "dark" : "light"

          /* Instruct Giscus to change theme */
          var frame = document.querySelector(".giscus-frame")
          frame.contentWindow.postMessage(
            { giscus: { setConfig: { theme } } },
            "https://giscus.app"
          )
        }
      })
    })
  </script>
{% endblock %}
```


## admonition

```
theme:
  icon:
    admonition:
      note: 'fontawesome/solid/note-sticky'  # #448aff, (68,138,255)
      abstract: 'fontawesome/solid/book'
      info: 'fontawesome/solid/circle-info'
      tip: 'fontawesome/solid/bullhorn'
      success: 'fontawesome/solid/check'
      question: 'fontawesome/solid/circle-question'
      warning: 'fontawesome/solid/triangle-exclamation'
      failure: 'fontawesome/solid/bomb'
      danger: 'fontawesome/solid/skull'
      bug: 'fontawesome/solid/robot'  # #f50057, (245,0,87)
      example: 'fontawesome/solid/flask'  # #7c4dff, (124,77,255)
      quote: 'fontawesome/solid/quote-left'

!!! quote "quote"

    引用を記載
```


## color

   ```
red, 
pink, 
purple
deep purple, 
indigo, #4051b5, (64,81,181)
blue, #2094f3, (32,148,243)
light blue, 
cyan, 
teal, 
green, 
light 
green, 
lime, 
yellow, 
amber, 
orange, 
deep orange, 
brown, 
grey, 
blue grey, 
black, 
white
```


## cmd
```
cd riskmatome/files
mkdocs new .
mkdocs build
mkdocs serve
mkdocs gh-deploy
```


## directory
```
files/
├── docs/
│   ├── assets/
│   │   ├── extra.css
│   │   └── extra.js
│   ├── index.md
│   ├── 10010.md
│   ├── 10020.md
│   ├── 10030.md
│   └── ：
├── overrides/
│   └── main.html
├── mkdocs.yml
└── site/
```


### md_in_html

```
<div class="result" markdown>
  <div class="base" markdown>

# Markdown

  </div>
</div>

```
