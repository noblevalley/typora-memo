# Laravel 開発環境構築手順

Windows10 XAMPP(Apache MariaDB PHP) MongoDB Composer Laravel Visual Studio Code GitHub TortoiseGit

## インストール

### XAMPP

開発用サーバーセット。

バージョン番号はPHPのバージョンに合わせたものとなっているので、phpのバージョンを変えたいときに確認できるようになっている。

https://www.apachefriends.org/jp/index.html

xampp-portable-windows-x64-7.2.34-0-VC15.zip

解凍

インストール先

E:\xampp_top\7.2.34.agrihealth

出来れば別のディスクへインストールする。フォルダだけコピーして移行しやすくするため、ディスク容量が許す限り案件と1対1で構築する。

setup_xampp.bat

xampp-control.exe

のショートカットを作成する。

xampp-control.exe



![2019-08-01 10_39_47-Language](laravel.assets/2019-08-01 10_39_47-Language.png)



Save



参考

https://proengineer.internous.co.jp/content/columnfeature/11084



### PHP バージョン確認

プログラム開発言語。

XAMPPに標準で入っている。

![2019-10-16 12_23_16-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ]](laravel.assets/2019-10-16 12_23_16-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ].png)

コマンドプロンプト起動



php -v

PHP 7.3.10 (cli) (built: Sep 24 2019 11:59:22) ( ZTS MSVC15 (Visual C++ 2017) x64 )
Copyright (c) 1997-2018 The PHP Group
Zend Engine v3.3.10, Copyright (c) 1998-2018 Zend Technologies



### Git for Windows

ソースコードのバージョン管理をする。

GUIの機能もあるが、補助的なものなので、GUIで利用するには後述するVisual Studio Codeを利用する。

サーバーはGitHubで行う。



### Visual Studio Code

機能拡張できるテキストエディタ。

機能拡張によってデバッグモードによるステップ実行ができる。

Gitクライアントとしてソースコード管理もできる。

起動

ソース管理

リポジトリのクローン

https://github.com/abridgedevelopment/AgriHealthManager.git

https://github.com/abridgedevelopment/arpointsystem-api.git



フォルダーの選択のダイアログ

E:\xampp_top\7.2.34.agrihealth

E:\xampp_top\7.3.23.arpointsystem

リポジトリの場所を選択

直下にフォルダーが作成されていることを確認する。

AgriHealthManager

フォルダへ移動すると、artisan ファイルなどがあるLaravelプロジェクトが作成されていることを確認する。

クローンしたリポジトリを開きますか？

開く

ファイル - 名前を付けてワークスペースを保存

デフォルトが以下になっていることを確認する。

E:\xampp_top\7.2.34.agrihealth\AgriHealthManager

E:\xampp_top\7.3.23.arpointsystem

ファイル名 : 

AgriHealthManager

arpointsystem-api



保存

ソース管理

先程できた AgriHealthManager.code-workspace を右クリック - .gitignore に追加 を選択する。

.gitignore はgitで管理しないファイルの一覧

.gitignore が開かれ、AgriHealthManager.code-workspace が追加されていることを確認する。

AgriHealthManager を * に変更して保存する。



### HeidiSQL

MySQL等のデータベースのGUIクライアント。



HeidiSQL_10.2.0.5599_Setup.exe



### DBeaver

MySQL等のデータベースのGUIクライアント。

データのコピペ入力やインポートエクスポートがしやすい。



dbeaver-ce-6.2.2-x86_64-setup.exe

![2019-10-16 12_31_01-Installer Language](laravel.assets/2019-10-16 12_31_01-Installer Language.png)



![2019-10-16 12_31_24-DBeaver Community 6.2.2 Setup](laravel.assets/2019-10-16 12_31_24-DBeaver Community 6.2.2 (x86_64) Setup.png)



![2019-10-16 12_31_42-DBeaver Community 6.2.2 Setup](laravel.assets/2019-10-16 12_31_42-DBeaver Community 6.2.2 (x86_64) Setup.png)



![2019-10-16 12_31_59-DBeaver Community 6.2.2 Setup](laravel.assets/2019-10-16 12_31_59-DBeaver Community 6.2.2 (x86_64) Setup.png)



![2019-10-16 12_32_53-DBeaver Community 6.2.2 Setup](laravel.assets/2019-10-16 12_32_53-DBeaver Community 6.2.2 (x86_64) Setup.png)



![2019-10-16 12_33_10-DBeaver Community 6.2.2 Setup](laravel.assets/2019-10-16 12_33_10-DBeaver Community 6.2.2 (x86_64) Setup.png)



![2019-10-16 12_33_24-DBeaver Community 6.2.2 Setup](laravel.assets/2019-10-16 12_33_24-DBeaver Community 6.2.2 (x86_64) Setup.png)



![2019-10-16 12_34_05-DBeaver Community 6.2.2 Setup](laravel.assets/2019-10-16 12_34_05-DBeaver Community 6.2.2 (x86_64) Setup.png)



![2019-10-16 12_34_32-DBeaver Community 6.2.2 Setup](laravel.assets/2019-10-16 12_34_32-DBeaver Community 6.2.2 (x86_64) Setup.png)



### Postman

WebAPIのテスト送信ができる。



https://www.getpostman.com/downloads/

Postman-win64-7.8.0-Setup.exe



### MongoDB

noSQLサーバー。jsonファイルの管理を行う。

![2020-01-06 17_00_06-MongoDB 4.2.2 2008R2Plus SSL Setup](laravel.assets/2020-01-06 17_00_06-MongoDB 4.2.2 2008R2Plus SSL (64 bit) Setup.png)

Welcome to the MongoDB 4.2.2

2008R 2Plus SSL (64bit) Setup Wizard

The Setup Wizard will install MongoDB 4.2.2 2008R2Plus SSL (64 bit) on your computer.

Click Next to continue or Cancel to exit the Setup Wizard.

MongoDB 4.2.2へようこそ

2008R 2Plus SSL（64bit）セットアップウィザード

セットアップウィザードは、MongoDB 4.2.2 2008R2Plus SSL（64ビット）をコンピューターにインストールします。

[次へ]をクリックして続行するか、[キャンセル]をクリックしてセットアップウィザードを終了します。

![2020-01-06 17_02_39-MongoDB 4.2.2 2008R2Plus SSL Setup](laravel.assets/2020-01-06 17_02_39-MongoDB 4.2.2 2008R2Plus SSL (64 bit) Setup.png)

End-User License Agreement

Please read the following agreement carefully

I accept the terms in the License Agreement

エンドユーザーライセンス契約

以下の契約を注意深くお読みください

ライセンス契約の条項に同意します

![2020-01-06 17_04_23-MongoDB 4.2.2 2008R2Plus SSL Setup](laravel.assets/2020-01-06 17_04_23-MongoDB 4.2.2 2008R2Plus SSL (64 bit) Setup.png)

Choose Setup Type

Choose the setup type that best suits your needs

Complete

All program features will be installed.

Requires the most disk space.

Recommended for most users.

Custom

Allows users to choose which program features will be installed and where they will be installed.

Recommended for advanced users.

セットアップの種類を選択

ニーズに最適なセットアップの種類を選択してください

コンプリート

すべてのプログラム機能がインストールされます。

最も多くのディスク容量が必要です。

ほとんどのユーザーに推奨。

カスタム

ユーザーは、インストールするプログラム機能とインストール先を選択できます。

上級ユーザーに推奨。

![2020-01-06 17_10_38-MongoDB 4.2.2 2008R2Plus SSL Service Customization](laravel.assets/2020-01-06 17_10_38-MongoDB 4.2.2 2008R2Plus SSL (64 bit) Service Customization.png)



Service Configuration

Specify optional settings to configure MongoDB as a service.

Install MongoD as a Service

Run service as Network Service user

Run service as a local or domain user:

サービス構成

MongoDBをサービスとして構成するには、オプションの設定を指定します。

MongoDをサービスとしてインストールする

ネットワークサービスユーザーとしてサービスを実行する

ローカルまたはドメインユーザーとしてサービスを実行します。

Account Domain:

Account Name:

Account Password:

Service Name: MongoDB

Data DIrectory: C:\Program Files\MongoDB\Server\4.2\data\

Log Directory: C:\Program Files\MongoDB\Server\4.2\log\

![2020-01-06 17_11_35-MongoDB Compass](laravel.assets/2020-01-06 17_11_35-MongoDB Compass.png)

Install MongoDB Compass

MongoDB Compass is the official graphical user interface for MongoDB.

By checking below this installer will automatically download and install the latest varsion of MongoDB Compass on this machine.

You can learn more about MongoDB Compass here: https://www.mongodb.com/products/comp...

Install MongoDB Compass

MongoDB Compassをインストールする

MongoDB Compassは、MongoDBの公式グラフィカルユーザーインターフェイスです。

以下をチェックすると、このインストーラーは自動的にMongoDB Compassの最新バージョンをこのマシンにダウンロードしてインストールします。

MongoDB Compassの詳細については、https：//www.mongodb.com/products/comp ...をご覧ください。

MongoDB Compassをインストールする

![2020-01-06 17_24_18-MongoDB 4.2.2 2008R2Plus SSL Setup](laravel.assets/2020-01-06 17_24_18-MongoDB 4.2.2 2008R2Plus SSL (64 bit) Setup.png)

Ready to install MongoDB 4.2.2 2008R2Plus SSL (64 bit)

Click Install to begin the installation.

Click Back to review or change any of your installation settings.

Click Cancel to exit the wizard.

MongoDB 4.2.2 2008R2Plus SSL（64ビット）をインストールする準備ができました

[インストール]をクリックして、インストールを開始します。

[戻る]をクリックして、インストール設定を確認または変更します。

[キャンセル]をクリックしてウィザードを終了します。

![2020-01-06 17_26_49-MongoDB 4.2.2 2008R2Plus SSL Setup](laravel.assets/2020-01-06 17_26_49-MongoDB 4.2.2 2008R2Plus SSL (64 bit) Setup.png)

Completed the MongoDB 4.2.2

2008 2Plus SSL (64 bit) Setup Wizard

Click the Finish button to exit the Setup Wizard.

Finish

MongoDB 4.2.2を完了しました

2008 2Plus SSL（64ビット）セットアップウィザード

[完了]ボタンをクリックして、セットアップウィザードを終了します。

終わり



C:\Program Files\MongoDB\Server\4.2\bin

InstallCompass.ps1

右クリック-Powershellで実行

![2020-01-06 17_56_42-MongoDB Compass Community - Connect](laravel.assets/2020-01-06 17_56_42-MongoDB Compass Community - Connect.png)

Welcome to MongoDB Compass Community

MongoDB Compassコミュニティへようこそ

Sidebar. Redesigned.
See with one glance what server you are connected to. Navigate between instance, database and collection level, with powerful filtering of your namespaces.

サイドバー。再設計されました。
接続しているサーバーを一目で確認できます。名前空間の強力なフィルタリングにより、インスタンス、データベース、コレクションレベル間を移動します。

Interactive Document Editor.
Modify existing documents with greater confidence using the intuitive visual editor, or insert new documents and clone or delete existing ones in just a few clicks.

インタラクティブドキュメントエディター。
直感的なビジュアルエディターを使用して、既存のドキュメントをより自信を持って変更したり、数回クリックするだけで新しいドキュメントを挿入したり、既存のドキュメントを複製または削除したりできます。

Visual Explain Plans.
Know how queries are running through an easy-to-understand GUI that helps you identify and resolve performance issues.

視覚的説明計画。
パフォーマンスの問題を特定して解決するのに役立つわかりやすいGUIを使用して、クエリがどのように実行されているかを把握します。

Index Management.
Understand the type and size of your indexes, their utilization and special properties. Add and remove indexes at the click of a button.

インデックス管理。
インデックスの種類とサイズ、それらの使用率、特別なプロパティを理解します。ボタンをクリックするだけで、インデックスを追加および削除できます。

Improved CRUD
Better editing with validation of individual BSON types.

CRUDの改善
個々のBSONタイプの検証によるより良い編集。

Deployment Awareness
Replica set aware connections allow for continued use during replica set configuration changes and provides additional information of the connected cluster.

展開の認識
レプリカセット対応の接続により、レプリカセットの構成変更中も継続して使用でき、接続されたクラスターの追加情報が提供されます。

Query History
Easily access and manage executed queries and save favorites for often executed queries.

クエリ履歴
実行されたクエリに簡単にアクセスして管理し、頻繁に実行されるクエリのお気に入りを保存します。

Get Started

始めましょう

Privacy Settings
To enhance the user experience, Compass can integrate with 3rd party services, which requires external network requests. Please choose from the settings below:

Enable Crash Reports
Allow Compass to send crash reports containing stack traces and unhandled exceptions.

Enable Usage Statistics
Allow Compass to send anonymous usage statistics.

Enable Automatic Updates
Allow Compass to periodically check for new updates.

With any of these options, none of your personal information or stored data will be submitted.
Learn more:MongoDB Privacy Policy

Start Using Compass

プライバシー設定
ユーザーエクスペリエンスを向上させるために、Compassは外部ネットワーク要求を必要とするサードパーティサービスと統合できます。以下の設定から選択してください：

クラッシュレポートを有効にする
コンパスがスタックトレースと未処理の例外を含むクラッシュレポートを送信できるようにします。

使用統計を有効にする
コンパスが匿名の使用統計を送信できるようにします。

自動更新を有効にする
Compassが新しいアップデートを定期的に確認できるようにします。

これらのオプションを使用すると、個人情報や保存されたデータは一切送信されません。
詳細：MongoDBプライバシーポリシー

コンパスの使用を開始する

New Connection

Fill in connection fields individually
Paste your connection string (SRV or Standard )

新しい接続

接続フィールドに個別に入力する
接続文字列（SRVまたはStandard）を貼り付けます



### Composer

システム管理ツール。phpのパスが通っていないと基本的にインストール出来ないので注意する。



XAMPPのshellからコマンドプロンプトを起動

ディレクトリ移動

cd php



Composerダウンロード

php -r "eval('?>'.file_get_contents('https://getcomposer.org/installer'));"

composer.pharがある事を確認する



echo @php "%~dp0composer.phar" %*>composer.bat

composer.batがある事を確認する



バージョンを確認する

composer -v



https://www.imprich-create.site/archives/441

### laravel

PHPのフレームワーク。

比較的新しいフレームワークでバージョンアップによる機能拡張が頻繁にされている。



ディレクトリ移動

cd /d E:\xampp_top\7.3.10.jovy\htdocs

cd /d e:\xampp_top\7.3.11.agrihealth

cd /d E:\xampp_top\7.2.24.agrihealth

cd /d E:\xampp_top\7.3.10.jovy

cd /d E:\xampp_top\7.2.34.agrihealth



※XAMPPインストールしたフォルダの直下を指定



プロジェクト作成

composer create-project --prefer-dist laravel/laravel=(省略可バージョン番号) (プロジェクト名)

composer create-project --prefer-dist laravel/laravel=6.0 laravel_test

composer create-project --prefer-dist laravel/laravel laravel_test

composer create-project --prefer-dist laravel/laravel AgriHealthManager

composer create-project --prefer-dist laravel/laravel=5.5 AgriHealthManager

composer create-project --prefer-dist laravel/laravel=5.5 testproject5.5

composer create-project --prefer-dist laravel/laravel=6.0 JOINS

以下のメッセージで完了したら正常終了

Application key set successfully.



ディレクトリ移動

cd /d E:\xampp_top\7.3.10.jovy\(プロジェクト名)

cd laravel_test

cd /d E:\xampp_top\7.3.10.jovy\htdocs\laravel_test

cd /d E:\xampp_top\7.3.10.jovy\testproject5.5

cd /d E:\xampp_top\7.3.11.agrihealth\AgriHealthManager

cd /d E:\xampp_top\7.2.24.agrihealth\AgriHealthManager

cd /d E:\xampp_top\7.3.10.jovy\JOINS

cd /d E:\xampp_top\7.2.34.agrihealth\AgriHealthManager



バージョン確認

php artisan --version



Apache設定

ファイルを開く

E:\xampp_top\7.3.11.agrihealth\apache\conf

E:\xampp_top\7.2.24.agrihealth\apache\conf

E:\xampp_top\7.3.10.jovy\apache\conf

httpd.conf

以下のパスの記載を変更

E:/xampp_top/7.2.24.agrihealth/htdocs

↓

E:/xampp_top/7.2.24.agrihealth/AgriHealthManager/public

E:/xampp_top/7.3.10.jovy/testproject5.5/public

※\を/に変換する



![2019-10-16 15_13_11-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ]](laravel.assets/2019-10-16 15_13_11-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ].png)

XAMPP起動

Apache Start

Module が緑になること

Actions ボタンが Start から Stop に変わること



ブラウザ確認

http://localhost/(プロジェクト名)/public

http://localhost/laravel_test/public

http://localhost



参照

http://tech-blog.rakus.co.jp/entry/2017/11/16/110742

https://laraweb.net/surrounding/1669/

https://blog.capilano-fw.com/?p=1528

https://blog.capilano-fw.com/?p=2678

https://blog.capilano-fw.com/?p=3578

https://blog.capilano-fw.com/?p=3519

 https://laraweb.net/environment/347/ 



### Node.js npmパッケージ



ディレクトリ移動

cd /d E:\xampp_top\7.3.10.jovy\htdocs\laravel_test

cd /d E:\xampp_top\7.3.11.agrihealth\AgriHealthManager



インストール

npm install

テスト環境反映

npm run dev



バージョン確認

npm -V

npm list -g

node --version



最新

npm install -g npm

最新バージョンが出力されること



### Xdebug

リモートデバッグツール。ローカルにも使用することができ、Visual Studio Codeと連動させることでGUI操作でデバッグ実行が可能となる。



ダウンロード

php_xdebug-2.7.2-7.3-vc15-x86_64.dll

ファイルを移動

E:\xampp_top\7.3.10.jovy\php\ext



ファイルを編集

E:\xampp_top\7.3.10.jovy\php

php.ini



最終行に追加

zend_extension = E:\xampp_top\7.3.10.jovy\php\ext\php_xdebug-2.7.2-7.3-vc15-x86_64.dll

[xdebug]
xdebug.default_enable = 1
xdebug.idekey = "vscode"
xdebug.remote_enable = 1
xdebug.remote_port=9000
xdebug.remote_autostart=1



phpinfo()を表示するファイルを作成

E:\xampp_top\7.3.11.agrihealth\AgriHealthManager\public

phpinfo.php 



<?php
// すべての情報を表示します。デフォルトは INFO_ALL です。
phpinfo();

?>



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



### MongoDB PHP Driver

MongoDBをPHP上で動かす。

Composerを利用するのでComposerインストールより後に行う。



ダウンロード

https://pecl.php.net/package/mongodb

php_mongodb-1.6.1-7.2-ts-vc15-x64.zip



解凍

php_mongodb.dll

ファイルを移動

E:\xampp_top\7.2.24.agrihealth\php\ext



ファイルを編集

E:\xampp_top\7.2.24.agrihealth\php

php.ini



最終行に追加

extension=php_mongodb.dll



phpinfo()を表示するファイルを作成

E:\xampp_top\7.2.24.agrihealth\AgriHealthManager\public

phpinfo.php 



XAMPP

Apache起動

http://localhost/phpinfo.php 

mongodb がダウンロードしたバージョンで表示されていること。



ディレクトリ移動

cd /d E:\xampp_top\7.3.10.jovy\htdocs\laravel_test

cd /d E:\xampp_top\7.3.10.jovy\testproject5.5

cd /d E:\xampp_top\7.3.11.agrihealth\AgriHealthManager

cd /d E:\xampp_top\7.3.10.jovy\drugstore-application

cd /d E:\xampp_top\7.2.24.agrihealth\AgriHealthManager



インストール

composer require mongodb/mongodb

結果

./composer.json has been updated
Loading composer repositories with package information
Updating dependencies (including require-dev)

> Illuminate\Foundation\ComposerScripts::postAutoloadDump

Carbon 1 is deprecated, see how to migrate to Carbon 2.
https://carbon.nesbot.com/docs/#api-carbon-2
    You can run ".\vendor\bin\upgrade-carbon" to get help in updating carbon and other frameworks and libraries that depend on it.

> @php artisan package:discover

Discovered Package: fideloper/proxy
Discovered Package: laravel/tinker
Discovered Package: nesbot/carbon
Package manifest generated successfully.



./composer.jsonが更新されました
コンポーザリポジトリにパッケージ情報をロードする
依存関係の更新（require-devを含む）

Carbon 1は非推奨です。Carbon2への移行方法をご覧ください。
https://carbon.nesbot.com/docs/#api-carbon-2
    ".\vendor\bin\upgrade-carbon"を実行して、カーボンおよびそれに依存する他のフレームワークとライブラリの更新に関するヘルプを取得できます。

検出されたパッケージ：fideloper / proxy
発見されたパッケージ：laravel / tinker
発見されたパッケージ：nesbot / carbon
パッケージマニフェストが正常に生成されました。



エラー結果

Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - mongodb/mongodb 1.5.1 requires ext-mongodb ^1.6 -> the requested PHP extension mongodb is missing from your system.
    - mongodb/mongodb 1.5.0 requires ext-mongodb ^1.6 -> the requested PHP extension mongodb is missing from your system.
    - Installation request for mongodb/mongodb ^1.5 -> satisfiable by mongodb/mongodb[1.5.0, 1.5.1].

  To enable extensions, verify that they are enabled in your .ini files:

   - E:\xampp_top\7.2.24.agrihealth\php\php.ini
     You can also run `php --ini` inside terminal to see which files are used by PHP in CLI mode.

Installation failed, reverting ./composer.json to its original content.

要件をインストール可能なパッケージのセットに解決できませんでした。

  問題1
    -mongodb / mongodb 1.5.1にはext-mongodb ^ 1.6が必要です->要求されたPHP拡張機能mongodbがシステムにありません。
    -mongodb / mongodb 1.5.0にはext-mongodb ^ 1.6が必要です->要求されたPHP拡張機能mongodbがシステムにありません。
    -mongodb / mongodbのインストールリクエスト^ 1.5-> mongodb / mongodb [1.5.0、1.5.1]で満足。

  拡張機能を有効にするには、.iniファイルで拡張機能が有効になっていることを確認します。
    -E：\ xampp_top \ 7.2.24.agrihealth \ php \ php.ini
  ターミナル内で `php --ini`を実行して、CLIモードでPHPによって使用されているファイルを確認することもできます。

インストールに失敗し、。/ composer.jsonを元のコンテンツに戻しました。

原因

PHP Driverをインストールしていない。もしくはphp.ini上で認識していない。

エラー結果

  - Installing mongodb/mongodb (1.5.1): Downloading (100%)
    Package phpunit/phpunit-mock-objects is abandoned, you should avoid using it. No replacement was suggested.
    Writing lock file
    Generating optimized autoload files
    Carbon 1 is deprecated, see how to migrate to Carbon 2.
    https://carbon.nesbot.com/docs/#api-carbon-2
    You can run ".\vendor\bin\upgrade-carbon" to get help in updating carbon and other frameworks and libraries that depend on it.

> Illuminate\Foundation\ComposerScripts::postAutoloadDump
> @php artisan package:discover

Script @php artisan package:discover handling the post-autoload-dump event returned with error code 1
In ProviderRepository.php line 208:

  Class 'Jenssegers\Mongodb\MongodbServiceProvider' not found



Installation failed, reverting ./composer.json to its original content.

-mongodb / mongodb（1.5.1）のインストール：ダウンロード（100％）
パッケージphpunit / phpunit-mock-objectsは廃止されました。使用しないでください。代替は提案されませんでした。
ロックファイルの書き込み
最適化された自動ロードファイルの生成
Carbon 1は非推奨です。Carbon2への移行方法をご覧ください。
https://carbon.nesbot.com/docs/#api-carbon-2
    「。\ vendor \ bin \ upgrade-carbon」を実行して、カーボンおよびそれに依存する他のフレームワークとライブラリの更新に関するヘルプを取得できます。

> Illuminate \ Foundation \ ComposerScripts :: postAutoloadDump
> @php artisanパッケージ：検出

スクリプト@php artisan package：エラーコード1で返されたpost-autoload-dumpイベントの処理を検出します
ProviderRepository.phpの208行目：

  クラス 'Jenssegers \ Mongodb \ MongodbServiceProvider'が見つかりません



インストールに失敗し、。/ composer.jsonを元のコンテンツに戻しました。

原因

中途半端にインストールされている情報がある。

以下のファイルをインストール前の状態へ戻す。

E:\xampp_top\7.2.24.agrihealth\AgriHealthManager\config

app.php





インストール

composer require jenssegers/mongodb(:省略可バージョン番号)

composer require jenssegers/mongodb:3.3

結果



反映

E:\xampp_top\7.2.24.agrihealth\AgriHealthManager\config

app.php

↑このファイルに追記

 'providers' => [
        ：
  Jenssegers\Mongodb\MongodbServiceProvider::class,
  ],

不要？↓

  'aliases' => [
        ：
  'Moloquent' => Jenssegers\Mongodb\Eloquent\Model::class,
  ],

不要？↑

E:\xampp_top\7.2.24.agrihealth

.env

↑このファイルに追記

MONGODB_HOST=127.0.0.1
MONGODB_PORT=27017
MONGODB_DATABASE=AgriHealthManager
MONGODB_USERNAME=
MONGODB_PASSWORD=



参考

https://www.php.net/manual/en/mongodb.installation.windows.php

https://www.php.net/manual/en/mongodb.tutorial.library.php

https://qiita.com/YaCpotato/items/69337d07bb7b8a658866





コマンド

DB名一覧

> show dbs
> admin   0.000GB
> config  0.000GB
> local   0.000GB

コレクション名一覧

> show collections
> hogehoge
> system.version

コレクション全件取得

db.(コレクション名).find()

db.user_location.find()



参考

https://qiita.com/svjunic/items/285e9cf20169d70aa1fa



### Laravel デバッグバー

Laravelの拡張機能。実行中の画面を確認できる。



ディレクトリ移動

cd /d E:\xampp_top\7.3.10.jovy\htdocs\laravel_test

cd /d E:\xampp_top\7.3.10.jovy\testproject5.5

cd /d E:\xampp_top\7.3.11.agrihealth\AgriHealthManager

cd /d E:\xampp_top\7.3.10.jovy\drugstore-application



インストール

composer require barryvdh/laravel-debugbar(:省略可バージョン番号)

composer require barryvdh/laravel-debugbar:2.4



反映

E:\xampp_top\7.3.10.jovy\htdocs\laravel_test\config

E:\xampp_top\7.3.11.agrihealth\AgriHealthManager\config

app.php

↑このファイルに追記

 'providers' => [
        ：
  Barryvdh\Debugbar\ServiceProvider::class,
  ],

  'aliases' => [
        ：
  'Debugbar' => Barryvdh\Debugbar\Facade::class,
  ],



.envファイルの編集

E:\xampp_top\7.3.10.jovy\htdocs\laravel_test

E:\xampp_top\7.3.11.agrihealth\AgriHealthManager

.env

開く

APP_DEBUG=true



キャッシュのクリア

php artisan config:cache

以下のメッセージで完了したら正常終了

Configuration cached successfully!



ブラウザで確認

http://localhost/laravel_test/public/ 

http://localhost



参考

https://laraweb.net/environment/1196/ 



### Step1

あらかじめ以下のインストールが必須

Composer

MongoDB

MongoDB PHP Driver

ディレクトリ実行

cd agrihealthmanager

cd arpointsystem-api

Laravelインストール

composer install

Laravelバージョン確認（使用できるか）

php artisan --version

5.5 になっていることを確認する。



### Step2

cd agrihealthmanager

.env.exampleから.env ファイルを複製する。

copy .env.example .env

.env ファイルが作成されていることを確認する。



APP_KEYの生成

php artisan key:generate

Application key [base64:(ランダムな文字と記号)] set successfully.

と出ていることを確認する。



### Step3

.env ファイルを開く

APP_KEY が上記の生成文字と同じになっていることを確認する。

以下の項目値を書き換える。

※=以降何もないところはそのままでOK

DB_DATABASE=AgriHealthManager
DB_USERNAME=root
DB_PASSWORD=

MONGODB_HOST=127.0.0.1
MONGODB_PORT=27017
MONGODB_HEART_RATE_DATABASE=AHM_heart_rate
MONGODB_USER_LOCATION_DATABASE=AHM_user_location
MONGODB_BODY_TEMPERATURE_DATABASE=AHM_body_temperature
MONGODB_TEMPERATURE_DATABASE=AHM_temperature
MONGODB_USERNAME=
MONGODB_PASSWORD=



DB_DATABASE=arpointsystem
DB_USERNAME=root
DB_PASSWORD=



### Step4

XAMPPでApacheとMySQLを起動する。

MySQLのAdminをクリックする。



データベースを作成する。

AgriHealthManager

arpointsystem latin1_swedish_ci



### Step5

cmd

マイグレーションを実行する。

php artisan migrate:fresh --seed



### Step6

Apacheの設定ファイルを変更する

E:\xampp_top\7.3.11.agrihealth\apache\conf

httpd.conf

変更前

DocumentRoot "E:/xampp_top/7.3.11.agrihealth/htdocs"
<Directory "E:/xampp_top/7.3.11.agrihealth/htdocs">

変更後

DocumentRoot "E:/xampp_top/7.3.11.agrihealth/AgriHealthManager/public"
<Directory "E:/xampp_top/7.3.11.agrihealth/AgriHealthManager/public">



XAMPPのApacheを再起動する。

ブラウザで接続する。

http://localhost

ログイン画面が出ている事を確認する。



## 設定

### Postman

httpsの送信テストで失敗するため

Postman の File -> Settings を左クリック。

General -> SSL certificate verification を OFF にします。

参考

https://knkomko.hatenablog.com/entry/2019/10/02/001032



### XAMPP



![2019-08-02 10_14_32-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ]](laravel.assets/2019-08-02 10_14_32-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ].png)

Config

![2019-08-02 10_17_52-Configuration of Control Panel](laravel.assets/2019-08-02 10_17_52-Configuration of Control Panel.png)

Editor 好きなエディタ

C:\Program Files\Mery\Mery.exe



Browser 好きなブラウザ

C:\Program Files (x86)\Google\Chrome\Application\chrome.exe



Save



### MariaSQL

MySQLと互換性があり、最近こちらに変わった。ツールで使用されている名称が昔の名残でMySQLのままになっているが、中身はMariaSQLが正解。

XAMPP

![2019-10-16 16_21_08-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ]](laravel.assets/2019-10-16 16_21_08-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ]-1571210529149.png)

MySQL起動

Admin起動



データベースをクリックする。

データベース名に AgriHealthManager を入力する。

照合順序は utf8_general_ci を入力する。

作成ボタンをクリックする。

agrihealthmanager データベースが出来ていることを確認する。





後は古い情報なので無視する。

Shell起動



パスワード設定

インストール直後はパスワードに何らかの値を設定しないと先に進めない。後から空白にすることは可能。作業用にとりあえず入力する。後からテキストファイルで設定するので、見られても困らないものにすること。

mysqladmin -u root password

パスワードを二回入力する

エラー出力されずにプロンプト制御になること



ディレクトリ移動

cd /d E:\xampp_top\7.3.10.jovy\mysql\bin

cd /d E:\xampp_top\7.3.11.agrihealth\mysql\bin

cd /d E:\xampp_top\7.2.34.agrihealth\mysql\bin



MariaDBサーバーにrootでログイン

mysql -h localhost -u root -p

mysql -h 127.0.0.1 -u root -p

先程のパスワードを入力する

以下のプロンプトが出ればOK

MariaDB [(none)]>



ユーザー作成

※\config\database.phpのデフォルトは'forge'なので設定入力を省きたいときはデフォルトで作成

create user 'forge' identified by '(パスワード)';

create user 'forge' identified by 'abridge';

以下のメッセージが出ればOK

Query OK, 0 rows affected (0.110 sec)



権限付与

grant all on forge. * to 'forge';



一度設定したパスワードを変更

いったんMariaDBサーバーに接続してログイン

パスワード変更

set password=password('(変更パスワード)');

set password=password('');

※パスワードなしユーザーにしたければ文字列なしにする

以下のメッセージが出たら成功

Query OK, 0 rows affected (0.038 sec)



終了

quit



パスワード変更、ユーザー作成時はもう一度MariaDBサーバーへ接続して新パスワードでログイン

mysql -h localhost -u forge -p

※パスワードなしの場合はそのままEnter



データベースforge作成

create database forge;

create database laravel;

create database miiband;

create database joins;



ファイルを開く

E:\xampp_top\7.3.10.jovy\laravel_test

E:\xampp_top\7.2.34.agrihealth\AgriHealthManager

.env

以下を変更

DB_USERNAME=forge
DB_PASSWORD=forge

DB_PASSWORD=(設定したパスワード)



キャッシュクリア（.envファイル反映）

php artisan config:clear



DB接続



参考

 https://qiita.com/kitaokeita/items/354c51752bc207129b12 



### phpMyAdmin

ファイル編集

E:\xampp_top\7.3.10.jovy\phpMyAdmin

E:\xampp_top\7.3.11.agrihealth\phpMyAdmin

E:\xampp_top\7.2.34.agrihealth\phpMyAdmin

config.inc.php



以下行にパスワードを入力

$cfg['Servers'][$i]['password']



XAMPP起動

MySQL起動

![2019-10-16 16_22_32-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ]](laravel.assets/2019-10-16 16_22_32-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ].png)

Adminが正常に表示されること







### TortoiseGit

※必須ではない。備考録として残す。

![2019-08-06 17_27_57-](laravel.assets/2019-08-06 17_27_57-.png)



![2019-08-06 17_31_05-Git クローン - TortoiseGit](laravel.assets/2019-08-06 17_31_05-Git クローン - TortoiseGit.png)

https://suzuki%40abridge-co.jp:VC6krKXm@github.com/suzu-kei/material_collection.git

E:\xampp_top\7.3.10.jovy\material_collection



![2019-08-06 17_32_12-E__xampp_htdocs - Git コマンド実行中 - TortoiseGit](laravel.assets/2019-08-06 17_32_12-E__xampp_htdocs - Git コマンド実行中 - TortoiseGit.png)

![2019-08-06 17_35_18-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ]](laravel.assets/2019-08-06 17_35_18-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ].png)

XAMPP起動

Apache起動

shell起動



ディレクトリ移動

cd /d E:\xampp_top\7.3.10.jovy\htdocs\material_collection

サーバー起動

#php artisan serve --host=localhost --port=8000



composer install



### シンボリックリンク

シンボリックリンクを作成したいフォルダへ移動する

cd /d E:\xampp_top\7.2.34.agrihealth\AgriHealthManager\public

フォルダの状態を確認する

dir

シンボリックリンクを作成する

mklink /d storage  E:\xampp_top\7.2.34.agrihealth\AgriHealthManager\storage\app\public



## チュートリアル

https://malg7.com/laravel-crud-tutorial/

https://awesome-linus.com/2019/06/05/laravel-tutorial-todo/

https://qiita.com/hitotch/items/a646972fe1992611e92b

必ずサーバー（Apache 、MySQL）を起動させること

### artisan コマンド確認

ディレクトリ移動

cd /d E:\xampp_top\7.3.10.jovy\htdocs\laravel_test

cd /d E:\xampp_top\7.3.11.agrihealth\AgriHealthManager

cd /d E:\xampp_top\7.3.10.jovy\JOINS



artisan コマンド確認

php artisan

一覧が表示されることを確認



### 認証

ディレクトリ移動

cd /d E:\xampp_top\7.3.10.jovy\htdocs\laravel_test

cd /d E:\xampp_top\7.3.11.agrihealth\AgriHealthManager

cd /d E:\xampp_top\7.3.10.jovy\JOINS



認証

※views/authディレクトリ自動作成

composer require laravel/ui --dev

以下のメッセージが出たら正常終了

Package manifest generated successfully.

以下のフォルダが出来ていること

E:\xampp_top\7.3.10.jovy\htdocs\laravel_test\resources\views\auth



Vueで実装

※HomeControllerが自動で作成される

php artisan ui vue --auth

出力メッセージ

Vue scaffolding installed successfully.
Please run "npm install && npm run dev" to compile your fresh scaffolding.
Authentication scaffolding generated successfully.

Vue scaffoldingは正常にインストールされました。
「npm install && npm run dev」を実行して、新しいスキャフォールディングをコンパイルしてください。
認証の足場が正常に生成されました。

 The [auth/login.blade.php] view already exists. Do you want to replace it? (yes/no) [no]:

[auth / login.blade.php]ビューは既に存在します。取り替えたいですか？ （はい/いいえ）[いいえ]：



npm install && npm run dev



E:\xampp_top\7.3.10.jovy\htdocs\laravel_test\app\Http\Controllers\Auth

E:\xampp_top\7.3.10.jovy\htdocs\laravel_test\database\migrations



php artisan migrate

エラーメッセージ

   Illuminate\Database\QueryException  : SQLSTATE[HY000] [1045] Access denied for user 'root'@'localhost' (using password: NO) (SQL: select * from information_schema.tables where table_schema = laravel and table_name = migrations and table_type = 'BASE TABLE')

原因

MySQLが起動していないかDBが作成されていない。

MariaDBの設定へ戻ってDB作成を行うか、.envファイルを変更する。

念の為に変更後は以下キャッシュクリアコマンドを実行して設定を反映する。

php artisan config:clear



Could not open input file: artisan

原因

ディレクトリが違う。cdコマンドでホームディレクトリへ移動する。







確認

ブラウザで閲覧

http://localhost/laravel_test/public

http://localhost



login と register が出ていること





参照

https://blog.capilano-fw.com/?p=4576 

https://readouble.com/laravel/6.0/ja/authentication.html 



### API認証 Passport

ディレクトリ移動

cd /d E:\xampp_top\7.3.10.jovy\htdocs\laravel_test

cd /d E:\xampp_top\7.3.11.agrihealth\AgriHealthManager

cd /d E:\xampp_top\7.3.10.jovy\htdocs\laravel_test

cd /d E:\xampp_top\7.3.10.jovy\JOINS



Passport インストール

composer require laravel/passport

もしlaravel5.5でエラーが出るなら以下を実行

composer require paragonie/random_compat:2.*

composer require laravel/passport "4.0.3"

以下メッセージが出ること

Package manifest generated successfully.



テーブル作成

php artisan migrate

以下メッセージが出ること

Migrating: 2016_06_01_000001_create_oauth_auth_codes_table
Migrated:  2016_06_01_000001_create_oauth_auth_codes_table (0.8 seconds)
Migrating: 2016_06_01_000002_create_oauth_access_tokens_table
Migrated:  2016_06_01_000002_create_oauth_access_tokens_table (1.18 seconds)
Migrating: 2016_06_01_000003_create_oauth_refresh_tokens_table
Migrated:  2016_06_01_000003_create_oauth_refresh_tokens_table (1.17 seconds)
Migrating: 2016_06_01_000004_create_oauth_clients_table
Migrated:  2016_06_01_000004_create_oauth_clients_table (0.46 seconds)
Migrating: 2016_06_01_000005_create_oauth_personal_access_clients_table
Migrated:  2016_06_01_000005_create_oauth_personal_access_clients_table (0.38 seconds)



トークンデータ作成

php artisan passport:install

以下メッセージが出ること

Encryption keys generated successfully.
Personal access client created successfully.
Client ID: 1
Client secret: EsrPrvd6E2HV5KvyqZQNM6IAEZcjF5CQ3PnYBWIa
Password grant client created successfully.
Client ID: 2
Client secret: JGpe01MRlV3rvjPfyMUOwk3pLpd3KJtjkSFbkdJ4



Encryption keys generated successfully.
Personal access client created successfully.
Client ID: 1
Client Secret: SvFhewNw2jLQ909dG0ZFXxT5XMCtQ8j0lPR4H5vx
Password grant client created successfully.
Client ID: 2
Client Secret: S4SgMQygpMaN4kmfOpFJQiSrXkwEqmSkUgFtmRrV



--ここから怪しい--

ファイル編集

E:\xampp_top\7.3.10.jovy\htdocs\laravel_test\app\Providers

E:\xampp_top\7.3.11.agrihealth\AgriHealthManager\app\Providers

AppServiceProvider.php



E:\xampp_top\7.3.10.jovy\JOINS\config

auth.php



コントローラーを作成

php artisan make:controller Api/AuthController

以下のメッセージが出ること

Controller created successfully.



ファイルを開く

E:\xampp_top\7.3.10.jovy\htdocs\laravel_test\app\Http\Controllers\Api

AuthController.php



追加修正

class AuthController extends Controller
{
    public function login(Request $request) {

        $credentials = $request->only('email', 'password');
    
        if(auth()->attempt($credentials)) {
    
            $user = auth()->user();
            $token = $user->createToken('Laravel Password Grant Client')->accessToken;
            return ['token' => $token];
    
        }
    
        return response([
            'message' => 'Unauthenticated.'
        ], 401);
    
    }
}



ファイルを開く

E:\xampp_top\7.3.10.jovy\htdocs\laravel_test\routes

E:\xampp_top\7.3.10.jovy\JOINS\routes

api.php



追加修正

Route::post('/login', 'Api\AuthController@login');

Route::group(['middleware' => 'auth:api'], function () {

    Route::get('me', function(){
        $user = Auth::user();
        return response()
            ->json(compact('user'));
    });

});

--ここまで怪しい--



確認

postmanで閲覧

POST

http://localhost/laravel_test/public/api/login

KEY/VALUE

email/ユーザーのメールアドレス

password/ユーザーのパスワード

Send



Bodyの結果がtokenで返されていること。



postmanのタブを追加

GET

http://localhost/laravel_test/public/api/me

KEY/VALUE

Accept/application/json

Authorization/Bearer (token) 

Send



Bodyの結果がuser情報で返されていること。





参照

https://readouble.com/laravel/6.0/ja/passport.html

https://readouble.com/laravel/5.5/ja/passport.html

https://helog.jp/laravel/passport/

https://blog.capilano-fw.com/?p=3745



## エクスポート

MySQL

phpMyAdmin



MongoDB

RLogin

本番サーバーへ接続してログイン

153.127.33.37

develop

abridge2019





ログイン

mongo

データベース確認

show dbs;

AHM_body_temperature  0.004GB
AHM_heart_rate        0.004GB
AHM_temperature       0.006GB
AHM_user_location     0.104GB
admin                 0.000GB
config                0.000GB
local                 0.000GB



元のファイル（データ）を消さずに追記

dumpファイルを作成

mongodump --db (データベース※指定しないと全database) --out  (出力先ファイル)

mongodump --db AHM_body_temperature --out  /tmp/mongodump/

mongodump --db AHM_heart_rate --out  /tmp/mongodump/

mongodump --db AHM_temperature --out  /tmp/mongodump/

mongodump --db AHM_user_location --out  /tmp/mongodump/





ユーザー画像ファイル

WinSCP

/var/www/virtual/dev_agrihealthmanager/storage/app/public

profile ディレクトリをダウンロード



## インポート

MySQL

phpMyAdmin



MongoDB

コマンドラインを起動

cmd

ログイン

mongo



※あらかじめデータのある作業ディレクトリに移動する

cd /d E:\github_work\winscp\mongodump

cd /var/tmp/mongodump



元のファイル（データ）を消さずに追記

mongorestore --db (データベース※指定しないと全database) /tmp/mongodump/(データベース※指定しないと全database)

mongorestore --db AHM_body_temperature ./AHM_body_temperature

mongorestore --db AHM_heart_rate ./AHM_heart_rate

mongorestore --db AHM_temperature ./AHM_temperature

mongorestore --db AHM_user_location ./AHM_user_location



ユーザー画像ファイル

コピー元

E:\github_work\winscp\profile

コピー先

E:\xampp_top\7.2.34.agrihealth\AgriHealthManager\storage\app\public

profile ごと移動



確認

http://localhost