# Agri

## ローカルで動作環境構築

既にある程度必要ツールがインストール済みである事が前提

サーバー環境

CentOS release 6.10 (Final)

MySQL Ver 14.14 Distrib 5.6.44, for Linux (x86_64)

php 7.2.19

Laravel Framework 5.5.48



MySQL 接続

http://160.16.138.81/phpmyadmin/index.php

root

lc0Q=-UXVS



SSH接続

IPアドレス：160.16.138.81
パスワード：lc0Q=-UXVS



画面

http://160.16.138.81:8081/login



laravel プロジェクト

cd  /var/www/virtual/dev_agrihealthmanager

httpd再起動

service httpd restart



mongodb

cd /var/lib/mongo

cd /var/log/mongodb



fitbit inspireと連携

kawamoto@abridge-co.jp
Abridge0303

tani@abridge-co.jp

Abridgetani





ローカル環境構築

XAMPPで7.2環境をダウンロードしてインストール。



config

Editor 好きなエディタ

C:\Program Files\Mery\Mery.exe



Browser 好きなブラウザ

C:\Program Files (x86)\Google\Chrome\Application\chrome.exe



Save



Shell起動



cd /d E:\xampp_top\7.2.24.agrihealth

cd /d E:\xampp_top\7.2.34.agrihealth



空のプロジェクト作成

composer create-project --prefer-dist laravel/laravel=5.5 AgriHealthManager



cd AgriHealthManager

バージョン確認

php artisan --version



Apache設定

ファイルを開く

E:\xampp_top\7.2.24.agrihealth\apache\conf

httpd.conf

以下のパスの記載を変更

E:/xampp_top/7.2.24.agrihealth/htdocs

↓

E:/xampp_top/7.2.24.agrihealth/AgriHealthManager/public

※\を/に変換する



mysql -h localhost -u root -p

Enter



データベース作成

create database miiband;

以下のメッセージが出ること

Query OK, 1 row affected

quit



ファイルを開く

E:\xampp_top\7.2.24.agrihealth\AgriHealthManager

.env

以下を変更

DB_DATABASE=miiband
DB_USERNAME=root



ファイルを開く

E:\xampp_top\7.2.24.agrihealth\AgriHealthManager\config

database.php

以下を変更

        'mysql' => [
            'driver' => 'mysql',
            'host' => env('DB_HOST', '127.0.0.1'),
            'port' => env('DB_PORT', '3306'),
            'database' => env('DB_DATABASE', 'miiband'),
            'username' => env('DB_USERNAME', 'root'),
            'password' => env('DB_PASSWORD', ''),
            'unix_socket' => env('DB_SOCKET', ''),
            'charset' => 'utf8',
            'collation' => 'utf8_unicode_ci',
            'prefix' => '',
            'strict' => true,
            'engine' => null,
        ],


キャッシュクリア（.envファイル反映）

php artisan config:clear



テーブル作成

php artisan migrate

以下メッセージが出ること

Migration table created successfully.



## 開発環境構築

### Xdebug

リモートデバッグツール。ローカルにも使用することができ、Visual Studio Codeと連動させることでGUI操作でデバッグ実行が可能となる。



ダウンロード

php_xdebug-2.8.0-7.2-vc15-x86_64.dll

ファイルを移動

E:\xampp_top\7.2.24.agrihealth\php\ext



ファイルを編集

E:\xampp_top\7.2.24.agrihealth\php

php.ini



最終行に追加

zend_extension = E:\xampp_top\7.3.10.jovy\php\ext\php_xdebug-2.8.0-7.2-vc15-x86_64.dll

[xdebug]
xdebug.default_enable = 1
xdebug.idekey = "vscode"
xdebug.remote_enable = 1
xdebug.remote_port=9000
xdebug.remote_autostart=1



E:\xampp_top\7.2.24.agrihealth\AgriHealthManager\public



XAMPP

Apache起動

http://localhost/phpinfo.php 

phpinfoの内容をコピー



以下のサイトへ貼り付け

https://xdebug.org/wizard.php



以下の表示になっていること

Xdebug installed: X.X.X(ダウンロードしたバージョン)



参考

https://qiita.com/hitotch/items/7b2895f9822ded3fa7db 



githubリポジトリからサーバーへダウンロード

git pull origin master



### Vue.js

ディレクトリ移動

cd /d E:\xampp_top\7.2.24.agrihealth\AgriHealthManager



cd /var/www/virtual/miiband



githubのファイルをダウンロード

git pull origin master

Abridge1234



フロントエンドビルドを行う

npm install && npm run dev

npm run dev

