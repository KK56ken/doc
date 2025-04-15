# ssh
## ssh鍵作成
$ ssh-keygen -t ed25519 -f ファイル名

## sshを別端末に送る
$ ssh-copy-id -i ~/公開鍵の場所 USER_NAME@IP
