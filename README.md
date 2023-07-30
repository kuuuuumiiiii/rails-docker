# README

# 環境構築方法
### ターミナルにて下記コマンドを順に実行してください

1. リポジトリをローカル環境にクローンする
```
$ git clone git@github.com:kuuuuumiiiii/rails-docker.git
```

2. ``rails-docker`` ファイルを新規で立ち上げる
```
$ code rails-docker
```

3. ``rails-docker`` フォルダに移動する
```
$ cd rails-docker
```

4. buildをする
```
$ docker-compose build
```
5. コンテナを作成し起動する
```
$ docker-compose up -d
```

6. 作成したコンテナの中に入る
```
$ docker-compose exec web bash
```

7. DBの作成をする
```
$ rails db:create
```

8. DBの更新をする
```
$ rails db:migrate
```

1~8 のコマンドを実行したらブラウザで [localhost:3000](http://localhost:3000/)に接続する事でアプリを立ち上げることができます。


![スクリーンショット](https://github.com/kuuuuumiiiii/rails-docker/assets/129586216/bced464d-5dcd-40e7-83d7-2b05ab09fed2)

上記画像と同じような画面になっていればOKです！

# アプリの停止方法
``$docker-compose up`` をしたターミナル上でコンテナをdownさせる
```
$ docker-compose down
```

# アプリの再起動
再度アプリを立ち上げたい場合は
```
$ docker-compose up -d
```
で立ち上げる事ができます。


# 仕様と環境について
- ターミナルおよびテキストエディタはVScodeの使用を想定しています
- 環境構築にはDockerおよびDocker-composeを使用します
- DBはpostgres:version 12を使用しています


