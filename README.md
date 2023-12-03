# 設定メモ

## URL
  - https://skillupmu.github.io/mkdocs/
  - https://github.com/skillupmu/mkdocs
  - https://github.com/skillupmu/mkdocs/blob/main/mkdocs.yml
  - https://github.com/skillupmu/mkdocs/blob/main/docs/assets/extra.css


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
 - https://giscus.app/ja

## reference

 - [Material for MkDocs公式](https://squidfunk.github.io/mkdocs-material/reference/)
 - [Material for MkDocs公式のyaml](https://github.com/squidfunk/mkdocs-material/blob/master/mkdocs.yml)
 - [PyMdown Extensions Documentation公式](https://facelessuser.github.io/pymdown-extensions/)
 - [PyMdown Extensions Documentation公式のyaml](https://github.com/facelessuser/pymdown-extensions/blob/main/mkdocs.yml)
 - [MkDocsによるドキュメント作成（個人サイト）](https://zenn.dev/mebiusbox/articles/81d977a72cee01)
 - [おもむろにメモ書き（個人サイト）](https://omomuroni.github.io/Mkdocs/00_index/)
 - [コジオン: チェス（個人サイト）](https://kojion.github.io/chess/mkdocs/001/)
 - [黒鳥のメモ（個人サイト）](https://kurotorimkdocs.gitlab.io/kurotorimemo/040-Documents/MkDocs/Extension/)

## color

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
