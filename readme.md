### No1


docker docker-compose
react
 typescript
 hooks
css:
 material-ui

eslint
prittier

/Go to the Docker hub and install node.js image
How to select image ->
https://zenn.dev/ken3pei/articles/1abbf7d974cf5d

/Get Docker template with Googling "Docker template"
https://docs.docker.com.xy2401.com/compose/compose-file/

What is 'context' on yaml?
https://qiita.com/sam8helloworld/items/e7fffa9afc82aea68a7a
[抜粋]
ルートディレクトリをDockerのコンテキストにすることで、Dockerfileはどんなファイルにもアクセスできるようになりました。
一方で、build時はその分Dockerデーモンという奴にそれだけ多くのファイルを送ることになるので遅くなることがあるようです。

[Dockerfile]


[docker-compose.yml]
tty: 標準入出力を自分のキーボード（入力）とかターミナル（出力）でできるようにするかしないか。falseかtrue
context:　ホストのルートの位置。Dockerfileを参照する時のスタートポイント。
dockerfile: Dockerfileの場所
volumes: カンマで区切られる。ホストマシン（左）とドッカーコンテナ（右）で、左から右に同期する（コピー的な）場所を指定する。つまり、macから操作したい場合は、必然的に必要とのこと。
working_dir: Docker側のルートフォルダ？


そして、
docker-compose up


次のコマンドで入る。どこからでも入るには次のコマンド。
docker container exec -it portfolio-chatbus-front-1 sh
でもビデオみたいに、chatbusのディレクトリに入ってdocker-compose exec front sh でもいける。
volumesの設定により、ホストマシンのfrontと同じ状況にあるということになるらしい。


npx create-react-app . --template typescript --use-npm
これをDocker内でやってもいいらしいけど、時間がかかるらしい。なので、ホストマシンでやると時間短縮になるとのこと。




### No2

create-react-appするとgitできるので削除。してルートでgit initしなおす。


