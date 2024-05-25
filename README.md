# 目次

- [コマンド](#command)

<br><br><br><br>

<a name="command"></a>
 - ## コマンド

<br><br>

## イメージ

イメージをダウンロード
```docker:docker
docker image pull { イメージ名 }
```
<br>

イメージの一覧表示
```docker:docker
docker image ls
```
<br>

イメージを削除 (ローカルマシンに存在する)
※いずれか一つ
```docker:docker
docker image rm { イメージ名 }
docker image rm { ID名 }
```

<br>

指定したイメージの詳細表示
```docker:Docker
docker image inspect { イメージ名 }
```

<br>
<br>

## コンテナ

イメージからコンテナ作成・起動
```docker:docker
docker container run -it { イメージ名 }
```
<br>

コンテナ一覧表示 (起動中のみ)
```docker:docker
docker container ls
```
コンテナ一覧表示 (全て)
```docker:docker
docker container ls -a 
```
<br>

起動中のコンテナ停止
※いずれか一つ
```docker:docker
docker container stop { コンテナ名 }
docker container stop { CONTAINER ID }
docker container stop { NAMES }
```

<br>
<br>

## コンテナ実践

コンテナの名前変更 (NAMES)
```docker
docker container run --name { 新しいコンテナ名 } { 元のイメージ名 }	
```

<br>

### コンテナ整理
コンテナ削除 (停止済みに限る)
```docker:docker
docker container rm { コンテナ名 }
```

<br>

コンテナ一括削除 (停止済みに限る)
```docker
docker container prune
```
<br>

コンテナ強制削除 (動作中Up)
```docker
docker container rm -f { コンテナ名 }
```
<br>

コンテナ起動 ➡ 停止で自動削除<br>
※テストや一時的な作業に便利なオプション
```docker
docker container run rm { イメージ名 }
```

<br>
<br>

## デタッチドモードとフォアグラウンドモード

新しいコンテナを作成してデタッチドモードで起動し特定のコマンドを実行
```docker
docker container run -d { イメージ名 } { 実行したいコマンド }			
```

<br>

すでに実行中のコンテナ内でデタッチドモードで起動し特定のコマンドを実行
```docker
docker container run -d { イメージ名 } { 実行したいコマンド }			
```
<br>

再度デタッチドモードに接続
```docker
docker container attach { コンテナ名 }
```

<br>
<br>

## その他

ログ確認
```docker
docker logs
docker container logs { コンテナ名 }
```
<br>

