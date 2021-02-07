# Mkdocsでドキュメントを作る

Dockerで作る。

ただし，数式とかPlantumlとかはダメそう。

pip install plantuml-markdown
pip install python-markdown-math


足りない部分を追加。
pipできなかったので[ここを参照](https://yukituna.com/2764/)


ashに入る。一応，ash add bashでもbashが使えるようになる。

docker run -it --entrypoint="/bin/ash" squidfunk/mkdocs-material

