## まだ制作中のAnsibleレシピ

- Requires Ansible 1.2 or newer
- Expects CentOS/RHEL 6.x hosts

  ansible-playbook -i hosts site.yml

for vagrant needs -k(ask sudo pass) option to act as root

よくあるLAMPのAnsibleレシピだけれど、セキュリティはがんばってみてる

####追記
2014/08/19 EC-CUBE用のレシピ実験に使用中
2014/08/20 yumパッケージVersions
- httpd 2.2.15
- mysql 5.1.73
- php 5.3.3

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
- IPv6の設定
- SElinuxの設定

###Apacheの項目
- ServerTokens
- ServerSignature
- Options -Indexs
- HostnameLookups
- .htaccess /var/www/html/のみ
- KeepAlive設定 OFF
- クリックジャッキング OFF
- Trace OFF
- データバックアップ

####mod_security
#####activated_rules
- modsecurity_crs_41_xss_attacks.conf
- modsecurity_crs_41_sql_injection_attacks.conf
- ホワイトリスト

###MySQLの項目
- rootパスワード追加
- 匿名ユーザー削除
- rootリモートログイン不許可
- テストデータベース削除
- slowログ（3秒）
- innoDB・UTF8デフォルト
- DBバックアップ

最後に再起動させたいけれど。Delayでできるかな？
