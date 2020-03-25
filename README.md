## 基本手順
- リポジトリをクローン
- Ansible(最新版)をインストール
  - `yum -y install ansible`
  - `yum -y update ansible`
- インベントリファイルでホスト名とドメイン名を変更
- SELinux/SG設定
- スタート
  - `cd /etc/ansible`
  - `sudo cp -r * /etc/ansible/`
  - `ansible-playbook -i hosts start.yml`

## 試験
```
# telnet localhost 25
helo 25
mail from:xxxx@yyyy.zz.jp
rcpt to:xxxx@yyyy.zz.jp
data
.
quit
```
