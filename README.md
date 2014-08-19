## まだ制作中のAnsibleレシピ

- Requires Ansible 1.2 or newer
- Expects CentOS/RHEL 6.x hosts

  ansible-playbook -i hosts site.yml

for vagrant needs -k(ask sudo pass) option to act as root

よくあるLAMPのAnsibleレシピだけれど、セキュリティはがんばってみてる

2014/08/19 EC-CUBE用のレシピ実験に使用中

###基本項目
- iptablesの設定
- yum-cronの設定
- 自動再起動の設定
- logwatchの設定
- SSHポート変更
- rootでのSSHログイン禁止
- SSHユーザーの作成
- SElinuxポリシー設定
- rkhunterの導入
- fail2banの導入
- denyhostsの導入
- inotifywaitの導入
- Tripwireの設定
- 起動デーモン選別

###Apacheの項目
###MySQLの項目

最後に再起動させたいけれど。どうにかしたい。
