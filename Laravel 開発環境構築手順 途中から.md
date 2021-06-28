# Laravel 開発環境構築手順 途中から

Windows10 XAMPP(Apache MariaDB PHP) MongoDB Composer Laravel Visual Studio Code GitHub TortoiseGit

## インストール

### XAMPP

開発用サーバーセット。

バージョン番号はPHPのバージョンに合わせたものとなっているので、phpのバージョンを変えたいときに確認できるようになっている。

https://www.apachefriends.org/jp/index.html

xampp-windows-x64-7.3.10-0-VC15-installer.exe



右クリック-管理者として実行

![2019-08-01 09_47_25-Question](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-08-01%2009_47_25-Question.png)

Question

It seems you have an antivirus running.

In some cases, this may show down or interfere the installation of the software.

Please visit the following link to learn more about this.

https://www.apachefriends.org/en/faq-xampp-windows.thml#antivirus

Continue with installation?



質問

ウイルス対策ソフトが起動しているようです。

場合によっては、これが表示されたり、ソフトウェアのインストールを妨げることがあります。

詳細については、次のリンクをご覧ください。

インストールを続けますか？



Yes



Warning

Important! Because an activated User Account (UAC) on your system some functions of XAMPP are possibly restricted.

With UAC please avoid to install XAMPP to C:\Program Files (missing write permisssions). Or deactivate UAC with msconfig after this setup.

警告

重要！あなたのシステム上でアクティブ化されたユーザーアカウント（UAC）があるため、XAMPPのいくつかの機能はおそらく制限されています。

UACでは、XAMPPをC:\Program Filesにインストールしないでください（書き込み権限がありません）。またはこの設定の後にmsconfigでUACを無効にしてください。



OK



![2019-08-01 10_03_53-Setup](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-08-01%2010_03_53-Setup.png)

Setup - XAMPP



Welcome to the XAMPP Setup Wizard.

次へ



Question

Do you want to abort the installation process?

質問

インストール処理を中止しますか？



![2019-08-01 10_04_16-Setup](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-08-01%2010_04_16-Setup.png)

Select Components

Select the components you want to install; clear the components you do not want to install.

Click Next when you are ready to continue.

Click on a component to get a detailed description

コンポーネントを選択

インストールしたいコンポーネントを選択します。インストールしたくないコンポーネントを消去します。

続行する準備ができたら[次へ]をクリックします。

コンポーネントをクリックすると詳細な説明が表示されます



次へ



Installation folder

Please, choose a folder to install XAMPP

Select a folder

インストールフォルダ

XAMPPをインストールするフォルダを選択してください

フォルダを選択

デフォルト

C:\xampp

↓

出来れば別のディスクへインストールする。フォルダだけコピーして移行しやすくするため、ディスク容量が許す限り案件と1対1で構築する。

E:\xampp_top\7.3.10.jovy

E:\xampp_top\7.3.11.agrihealth

E:\xampp_top\7.2.24.agrihealth

E:\xampp_top\7.2.32.AccidentSearch



![2020-07-16 17_57_36-Setup](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2020-07-16%2017_57_36-Setup.png)

Language

XAMPP Control Panel for Windows supports different languages.

English

Deutsch

言語

XAMPP Control Panel for Windowsはさまざまな言語をサポートしています。

英語　英語を選択

ドイツ語



![2019-10-31 10_36_12-Setup](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-10-31%2010_36_12-Setup.png)

Bitnami for XAMPP

bitnami for XAMPP provides free installers that can install Drupal, Joomla!, WordPress and many other popular open source apps on top of your existing XAMPP installation.

https://bitnami.com/xampp

Learn more about Bitnami for XAMPP



XAMPP用のBitnami

bitnami for XAMPPは、Drupal、Joomla!、WordPress、その他多くの一般的なオープンソースアプリケーションを既存のXAMPPインストールの上にインストールできる無料のインストーラを提供します。

https://bitnami.com/xampp

XAMPP用Bitnamiの詳細　チェックを外す

※チェックを入れるとブラウザが起動してWebサイトが開くだけなので、見たくなければ外す。



Ready to Install

Setup is now ready to begin installing XAMPP on your computer.

インストールの準備

これで、コンピュータにXAMPPのインストールを開始する準備が整いました。



![2019-08-01 10_35_10-Setup](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-08-01%2010_35_10-Setup.png)

Installing

進捗



![2019-08-01 10_39_18-Setup](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-08-01%2010_39_18-Setup.png)

Completing the XAMPP Setup Wizard

Setup has finished installing XAMPP on your computer.

Do you want to start the Control Panel now?

XAMPPセットアップウィザードを完了する

セットアップはコンピュータへのXAMPPのインストールを完了しました。

今すぐコントロールパネルを起動しますか。

Finish



![2019-08-01 10_39_47-Language](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-08-01%2010_39_47-Language.png)

Save



もし以前にもインストールしたことがある場合、Control Panelのショートカットは前のままなので、コピーして今インストールしたフォルダへ書き換える。



参考

https://proengineer.internous.co.jp/content/columnfeature/11084



### PHP バージョン確認

プログラム開発言語。

XAMPPに標準で入っている。

![2019-10-16 12_23_16-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ]](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-10-16%2012_23_16-XAMPP%20Control%20Panel%20v3.2.4%20%20%20%5B%20Compiled_%20Jun%205th%202019%20%5D.png)

コマンドプロンプト起動

コマンド実行

php -v

結果

PHP 7.3.10 (cli) (built: Sep 24 2019 11:59:22) ( ZTS MSVC15 (Visual C++ 2017) x64 )
Copyright (c) 1997-2018 The PHP Group
Zend Engine v3.3.10, Copyright (c) 1998-2018 Zend Technologies



### Git for Windows

バージョン管理システム。

テキストファイルの変更履歴を残すだけでなく、派生バージョンを並行管理するために枝分かれしたり、逆に枝分かれたバージョンをひとつにまとめたりできる。個人で利用する分には好きにバージョン管理できるが、複数人で利用するには別のシステム（後述するGitHubなど）を使用するのが一般的。

https://gitforwindows.org/

Git-2.20.1-64-bit.exe





### GitHub

バージョン管理システムGitを利用したSNS。個人だけでも利用できるが、どちらかというと複数人で利用するための機能がメインなので、GitかGitHubどちらかを使用するのではなく、使い分けるのが良い。

![2019-10-16 12_23_16-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ]](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-10-16%2012_23_16-XAMPP%20Control%20Panel%20v3.2.4%20%20%20%5B%20Compiled_%20Jun%205th%202019%20%5D.png)

コマンドプロンプト起動

コマンド実行

git clone https://github.com/abridgedevelopment/AccidentSearch-Api.git

結果

Cloning into 'AccidentSearch-Api'...
remote: Enumerating objects: 155, done.
remote: Counting objects: 100% (155/155), done.
remote: Compressing objects: 100% (99/99), done.
remote: Total 2533 (delta 71), reused 116 (delta 53), pack-reused 2378
Receiving objects: 100% (2533/2533), 21.50 MiB | 8.99 MiB/s, done.
Resolving deltas: 100% (1542/1542), done.



E:\xampp_top\7.2.32.AccidentSearch

直下に「AccidentSearch-Api」が出来ていること

E:\xampp_top\7.2.32.AccidentSearch\AccidentSearch-Api

直下に「composer.json」ファイルを含むLaravelプロジェクト一式が存在していること。



### Visual Studio Code

機能拡張できるテキストエディタ。

機能拡張によってデバッグモードによるステップ実行ができる。

https://azure.microsoft.com/ja-jp/products/visual-studio-code/

VSCodeUserSetup-x64-1.30.2.exe



### Composer

システム管理ツール。



https://getcomposer.org/download/

Composer-Setup.exe

※実行前にいったんXAMPPを閉じる

![2019-10-16 12_38_56-Composer Setup](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-10-16%2012_38_56-Composer%20Setup.png)

Installation Options

Choose your installation type.

Setup will download and install Composer to a fixed location for all users.

Whis includes a Control Panel unistaller and is the recommended option.

Click Next to use it.

Developer mode

Take control and just install Composer. An unistaller will not be included.



インストールオプション

インストールの種類を選択してください。

セットアップはComposerをダウンロードし、すべてのユーザーの固定の場所にインストールします。

これはコントロールパネルのunistallerを含み、推奨されるオプションです。

それを使用するためにNextをクリックします。

開発者モード

制御を取り、Composerをインストールするだけです。解約者は含まれません。



![2019-10-16 12_40_47-Composer Setup](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-10-16%2012_40_47-Composer%20Setup.png)

Settings Check

We need to check your PHP and other settings.

Choose the command-line PHP you want to use:

This is the PHP in your path. Click Next to use it.

設定チェック

あなたのPHPや他の設定をチェックする必要があります。

使用したいPHPを選択してください。

これはあなたの道の中のPHPです。それを使用するためにNextをクリックします。

![2019-10-16 12_40_09-開く](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-10-16%2012_40_09-%E9%96%8B%E3%81%8F-1571197297804.png)

E:\xampp_top\7.3.10.jovy\php\php.exe

![2019-08-01 11_18_03-Composer Setup](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-08-01%2011_18_03-Composer%20Setup.png)



![2019-10-16 12_42_45-Composer Setup](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-10-16%2012_42_45-Composer%20Setup.png)



Proxy Settings

Choose if you need to use a proxy.

Use a proxy server to connect to internet

Enter proxy url

プロキシ設定

プロキシを使用する必要があるかどうかを選択してください。

プロキシサーバーを使用してインターネットに接続する

代理URLを入力

![2019-10-16 12_44_09-Composer Setup](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-10-16%2012_44_09-Composer%20Setup.png)



Ready to Install

Setup is now ready to download Composer and install it on your computer.

Please review these settings. Click Install to continue with the installation.

PHP vertion 7.3.10

Add to System path:

Remove from System path:



インストールの準備

これで、Composerをダウンロードしてコンピュータにインストールする準備が整いました。

これらの設定を見直してください。インストールをクリックしてインストールを続行します。

PHP vertion 7.3.10

システムパスに追加：

システムパスから削除：

![2019-10-16 12_44_41-Composer Setup](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-10-16%2012_44_41-Composer%20Setup.png)



※サーバーを停止しないと以下のメッセージが出る。出たらこの後OS再起動を実行する。

Information

Please read the following information before continuing.

Important

Setup has changed your environment, but not all running programs will be aware fo this.

To use Composer for the first time, you will have to do one of the following:

- Open a new command window.
- Close all File Exporer windows, then open a new command window.
- Logoff and Logon again, then open a new command window.

情報

続行する前に以下の情報をお読みください。

重要

セットアップによって環境が変更されましたが、実行中のプログラムすべてがこれを認識するわけではありません。

初めてComposerを使用するには、次のいずれかを実行する必要があります。

 - 新しいコマンドウィンドウを開きます。
 - すべてのFile Exporerウィンドウを閉じてから、新しいコマンドウィンドウを開きます。
 - ログオフして再度ログオンし、新しいコマンドウィンドウを開きます。

![2019-10-16 12_46_28-Composer Setup](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-10-16%2012_46_28-Composer%20Setup.png)

Completing Composer Setup

Setup has installed Composer on your computer.

Usage: Open a command window and type "composer"

Click Finish to exit Setup.

View online documentation

作曲者セットアップの完了

セットアップがコンピュータにComposerをインストールしました。

使用方法：コマンドウィンドウを開き、「composer」と入力します。

[完了]をクリックしてセットアップを終了します。

オンラインドキュメントを見る



コマンドプロンプトを起動

composer -v



### ファイル修正

ファイルコピー

E:\xampp_top\7.2.32.AccidentSearch\AccidentSearch-Api

.env.example

↓

.env



### laravel

PHPのフレームワーク。

比較的新しいフレームワークでバージョンアップによる機能拡張が頻繁にされている。



ディレクトリ移動

cd /d E:\xampp_top\7.3.10.jovy\htdocs

cd /d e:\xampp_top\7.3.11.agrihealth

cd /d E:\xampp_top\7.2.24.agrihealth

cd /d E:\xampp_top\7.3.10.jovy

cd /d E:\xampp_top\7.2.32.AccidentSearch

cd /d E:\xampp_top\7.2.32.AccidentSearch



※XAMPPインストールしたフォルダの直下を指定



プロジェクト作成

composer create-project --prefer-dist laravel/laravel=(省略可バージョン番号) (プロジェクト名)

composer create-project --prefer-dist laravel/laravel=6.0 laravel_test

composer create-project --prefer-dist laravel/laravel laravel_test

composer create-project --prefer-dist laravel/laravel AgriHealthManager

composer create-project --prefer-dist laravel/laravel=5.5 AgriHealthManager

composer create-project --prefer-dist laravel/laravel=5.5 testproject5.5

composer create-project --prefer-dist laravel/laravel=6.0 JOINS

composer create-project --prefer-dist laravel/laravel=5.5 AccidentSearch

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

cd /d E:\xampp_top\7.2.32.AccidentSearch\AccidentSearch



バージョン確認

php artisan --version



Apache設定

ファイルを開く

E:\xampp_top\7.3.11.agrihealth\apache\conf

E:\xampp_top\7.2.24.agrihealth\apache\conf

E:\xampp_top\7.3.10.jovy\apache\conf

E:\xampp_top\7.2.32.AccidentSearch\apache\conf

httpd.conf

以下のパスの記載を変更

E:/xampp_top/7.2.24.agrihealth/htdocs

E:/xampp_top/7.2.32.AccidentSearch/htdocs

↓

E:/xampp_top/7.2.24.agrihealth/AgriHealthManager/public

E:/xampp_top/7.3.10.jovy/testproject5.5/public

E:/xampp_top/7.2.32.AccidentSearch/AccidentSearch/public

※\を/に変換する



![2019-10-16 15_13_11-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ]](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-10-16%2015_13_11-XAMPP%20Control%20Panel%20v3.2.4%20%20%20%5B%20Compiled_%20Jun%205th%202019%20%5D.png)

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



### MariaSQL

MySQLと互換性があり、最近こちらに変わった。ツールで使用されている名称が昔の名残でMySQLのままになっているが、中身はMariaSQLが正解。

XAMPP

![2019-10-16 16_21_08-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ]](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-10-16%2016_21_08-XAMPP%20Control%20Panel%20v3.2.4%20%20%20%5B%20Compiled_%20Jun%205th%202019%20%5D-1571210529149.png)

MySQL起動

Shell起動



パスワード設定

※後からテキストファイルで設定するので、見られても困らないものにすること

mysqladmin -u root password

パスワードを二回入力する

エラー出力されずにプロンプト制御になること



ディレクトリ移動

cd /d E:\xampp_top\7.3.10.jovy\mysql\bin

cd /d E:\xampp_top\7.3.11.agrihealth\mysql\bin

cd /d E:\xampp_top\7.2.32.AccidentSearch\mysql\bin



MariaDBサーバーにrootでログイン

mysql -h localhost -u root -p

先程のパスワードを入力する

以下のプロンプトが出ればOK

MariaDB [(none)]>



ユーザー作成

※rootのみなら不要

※\config\database.phpのデフォルトは'forge'なので設定入力を省きたいときはデフォルトで作成

create user 'forge' identified by '(パスワード)';

create user 'forge' identified by 'abridge';

create user 'root' identified by 'root';

以下のメッセージが出ればOK

Query OK, 0 rows affected (0.110 sec)



権限付与

※rootのみなら不要

grant all on forge. * to 'forge';

grant all on forge. * to 'root';



一度設定したパスワードを変更

※変更なしなら不要

※phpMyAdminのデフォルト設定は「root/パスワードなし」なのでローカル環境で極力設定を変えたくない場合はこの作業を行う

いったんMariaDBサーバーに接続してログイン

パスワード変更

set password=password('(変更パスワード)');

set password=password('root');

set password=password('');

※パスワードなしユーザーにしたければ文字列なしにする

以下のメッセージが出たら成功

Query OK, 0 rows affected (0.038 sec)



終了

quit



パスワード変更、ユーザー作成時はもう一度MariaDBサーバーへ接続して新パスワードでログイン

mysql -h localhost -u forge -p

mysql -h localhost -u root -p

※パスワードなしの場合はそのままEnter



データベース作成

create database forge;

create database laravel;

create database miiband;

create database joins;

create database accidentsearch;

以下のメッセージが出たら成功

Query OK, 1 row affected (0.001 sec)



ファイルを開く

E:\xampp_top\7.3.10.jovy\laravel_test

E:\xampp_top\7.2.32.AccidentSearch\AccidentSearch

.env

以下を変更

DB_USERNAME=root
DB_PASSWORD=root

DB_PASSWORD=(設定したパスワード)



キャッシュクリア（.envファイル反映）

php artisan config:clear



DB接続



参考

 https://qiita.com/kitaokeita/items/354c51752bc207129b12 



### phpMyAdmin

ファイル編集

※MariaDBの認証をroot/パスワードなしにした場合は不要

E:\xampp_top\7.3.10.jovy\phpMyAdmin

E:\xampp_top\7.3.11.agrihealth\phpMyAdmin

E:\xampp_top\7.2.32.AccidentSearch\phpMyAdmin

config.inc.php



以下行にパスワードを入力

$cfg['Servers'][$i]['password']



XAMPP起動

MySQL起動

![2019-10-16 16_22_32-XAMPP Control Panel v3.2.4   [ Compiled_ Jun 5th 2019 ]](Laravel%20%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86%20%E9%80%94%E4%B8%AD%E3%81%8B%E3%82%89.assets/2019-10-16%2016_22_32-XAMPP%20Control%20Panel%20v3.2.4%20%20%20%5B%20Compiled_%20Jun%205th%202019%20%5D.png)

Adminが正常に表示されること



### laravel

ディレクトリ移動

cd /d E:\xampp_top\7.3.10.jovy\(プロジェクト名)

cd laravel_test

cd /d E:\xampp_top\7.3.10.jovy\htdocs\laravel_test

cd /d E:\xampp_top\7.3.10.jovy\testproject5.5

cd /d E:\xampp_top\7.3.11.agrihealth\AgriHealthManager

cd /d E:\xampp_top\7.2.24.agrihealth\AgriHealthManager

cd /d E:\xampp_top\7.3.10.jovy\JOINS

cd /d E:\xampp_top\7.2.32.AccidentSearch\AccidentSearch



インストール

composer install

データベースのテーブルを作成

php artisan migrate



アプリケーションキーを修正

base64:vDUkYII5ghlunBWrIm4AnO9wRyBUy/yK380F6vrJ62g=