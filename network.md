# network 
## ホスト名表示
$ hostname

## ホスト名変更
$ hostname 更新したいホスト名

## 名前解決できるか確認
$ dig url

## iptables

### 設定確認
$ iptables -L -v -n

### 既存ルールの確認
$ iptables -L INPUT --line-numbers

### 特定のルールの削除
$ iptables -D INPUT 3

### ip rangeによるルール追加
$ iptables -A INPUT -p tcp --dport 55555 -s 10.0.0.0/22 -j ACCEPT

## ラズパイでの固定IP

nmtui
