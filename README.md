# 目次

- [コマンド](#command)

<br><br><br><br>

<a name="command"></a>
 - ## コマンド

<br><br>

イメージをダウンロード
```docker:docker
docker image pull { イメージ名 }
```
一覧表示
```docker:docker
docker image ls
```
ローカルマシンに存在するイメージを削除
```docker:docker
docker image rn { イメージ名 }
docker image rn { ID名 }
```
イメージからコンテナ作成・起動
```docker:docker
docker container run { イメージ名 }
```
コンテナ一覧表示
```docker:docker
docker container ls

# 起動していないコンテナも表示⇩
docker container ls -a 
```
起動中のコンテナ停止
```docker:docker
docker container stop { コンテナ名 }
docker container stop { CONTAINER ID }
docker container stop { NAMES }
```
コンテナ破棄
```docker:docker
docker container rm { コンテナ名 }
```
