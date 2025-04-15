# docker
## docker コンテナ削除
$ docker rm (CONTAINER ID)

## dockerコンテナ全削除
$ docker rm $(docker ps -aq)

## docker イメージ削除
$ docker rmi (IMAGE ID)

## docker イメージ全削除
$ docker rmi $(docker images -q)

## コンテナのログを見たい場合（-fオプションで永続化）
$ docekr logs コンテナ名

## バージョン確認
$ docker -v

## コンテナ、ネットワーク、ボリュームを削除
$ docker-compose down --volumes --remove-orphans

## ビルドキャッシュを削除
$ docker builder prune -f

## 不要なイメージ、ボリューム、ネットワークを削除
$ docker system prune -a --volumes -f

## sudo権限なしでdockerを使う
$ sudo usermod -aG docker $USER
## 上記を行っても無理な場合
$ sudo chmod 666 /var/run/docker.sock

# raspberry piでdockerをインストールする場合
## docker環境構築
$ sudo apt update
$ sudo apt upgrade

## dockerのインストール
$ curl -fsSL https://get.docker.com -o get-docker.sh
$ sudo sh get-docker.sh


## docker-composeのインストール
$ DOCKER_CONFIG=${DOCKER_CONFIG:-$HOME/.docker}
$ mkdir -p $DOCKER_CONFIG/cli-plugins
$ curl -SL https://github.com/docker/compose/releases/download/v2.3.4/docker-compose-linux-armv7 -o $DOCKER_CONFIG/cli-plugins/docker-compose

$ chmod +x $DOCKER_CONFIG/cli-plugins/docker-compose
