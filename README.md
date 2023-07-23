# docker-compose-example

Dockerハンズオン用のcompose.yaml

* 実行と同時にpythonとnginxのコンテナが起動
    * nginxに設定ファイルを追加
    * pythonの組み込みWebサーバーを起動
* localhost:8080にアクセスすると、pythonコンテナのディレクトリが表示される

```
# 通信経路
<HOST> localhost:8080 -> nginx container:80 -> python container:8000
```

ref. （ハンズオン資料, TBA）

## 前準備

```bash
git clone https://github.com/kotatsu360/docker-compose-example.git
cd docker-compose-example
```

## composeの実行をフォアグラウンドで行う場合

```bash
$ docker compose up
(Ctrl-Cで終了)
```

## composeの実行をバックグラウンドで行う場合
```bash
$ docker compose up -d

# ログを見る
$ docker compose logs -f
(Ctrl-Cで終了)

# composeで作成したコンテナを破棄
$ docker compose down
```
