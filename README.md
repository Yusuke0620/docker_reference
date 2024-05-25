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

イメージを削除(ローカルマシンに存在する)
※いずれか一つ
```docker:docker
docker image rm { イメージ名 }
docker image rm { ID名 }
```

<br>

## コンテナ

イメージからコンテナ作成・起動
```docker:docker
docker container run -it { イメージ名 }
```
<br>

コンテナ一覧表示(起動中)
```docker:docker
docker container ls
```
コンテナ一覧表示(起動していない)
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

コンテナ削除
```docker:docker
docker container rm { コンテナ名 }
```

<br>
<br>

## コンテナ実践
