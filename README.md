# Mkdocs Materialでドキュメントを作るテンプレート

Mkdocsを用いてドキュメントを作成するテンプレート。

## 概要

基本的なフォルダ構成は以下の通り。

```
mkdocsTest
├── .github
│  └── workflow
│     └── mkdocs.yml
│
├── mkdocs.yml # book setting
└── docs # Source folder
   ├── index.md # For top page (Not neccesary)
   └── < other .md files >
```

## How to Use

CloneまたはForkした後に，GitHubにPushするだけでOK.

[Getting Started](https://squidfunk.github.io/mkdocs-material/getting-started/)を参照。



# 実行環境

## ローカル実行：Dockerを用いた実行環境

本コードを動かせるDocker環境は`squidfunk/mkdocs-material`のImageを参照して作成。

```
docker pull ossyaritoori/mkdocs-material
```

buildを確認するには下記のコマンドを打つべし。

```
docker run --rm -v `pwd`:/docs ossyaritoori/mkdocs-material build
```


## 追加した拡張機能環境

`squidfunk/mkdocs-material`からの環境の変分は下記の通り。自前の環境で実行したい場合は各pipコマンドを叩けばOK。

- MathJaxを追加
  - 没：https://squidfunk.github.io/mkdocs-material/reference/mathjax/
  - 採用：https://qiita.com/mebiusbox2/items/a61d42878266af969e3c
      - `pip install python-markdown-math`
- Plantumlを追加
  - `pip install plantuml-markdown`
- truly sane indent：
  - https://stakiran.hatenablog.com/entry/2018/08/02/202816
  - `pip install mdx_truly_sane_lists`
- index numbering：章と節にナンバリング
  - https://github.com/ignorantshr/mkdocs-add-number-plugin
  - `pip3 install mkdocs-add-number-plugin`
- git revision：変更履歴表示
  - https://roy-n-roy.github.io/mkdocs/gitRevisionDate/
  - `pip install mkdocs-git-revision-date-localized-plugin`


## Remote実行：GitHub Actions

[ここの記述](https://squidfunk.github.io/mkdocs-material/publishing-your-site/)を参考にワークフローを定義。



# メモスペース

- サイトに含めたいファイルは全てdocs以下に置く（build時，docsフォルダ以下がまるまるsite以下にコピーされる仕様なので）
- その他参照にしたサイト： https://taxintt.hatenablog.com/entry/2020/06/07/225215
