# Mkdocsでドキュメントを作る

以下メモ。


## Docker環境版
Dockerで作る。

ただし，数式とかPlantumlとかはダメそう。

pip install plantuml-markdown
pip install python-markdown-math


足りない部分を追加。
pipできなかったので[ここを参照](https://yukituna.com/2764/)


ashに入る。一応，ash add bashでもbashが使えるようになる。

docker run -it --entrypoint="/bin/ash" squidfunk/mkdocs-material


うーん，DockerFile書いたほうが良さそう。

## GitHub Actions

[ここの記述](https://squidfunk.github.io/mkdocs-material/publishing-your-site/)を参考にワークフローを定義。

- MathJaxを追加
  - 没：https://squidfunk.github.io/mkdocs-material/reference/mathjax/
  - 採用：https://qiita.com/mebiusbox2/items/a61d42878266af969e3c
- PDF化
  - 複数あるがこちらを使用。https://comwes.github.io/mkpdfs-mkdocs-plugin/pdf/documentation.pdf
- 

## troubleshoot

Config value: 'markdown_extensions'. Error: Invalid Markdown Extensions configuration

この手のはインデントのエラーくさい。

Dockerでplantumlのサーバーにアクセスできない。だるい。

