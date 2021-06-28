# Docker構築手順

Windows10Home64bit VirtualBox Vagrant Docker

WindowsのエディションがHomeかそれ以外かによってDockerのインストールファイルや手順が異なる。

理由はHomeエディションのみHyper-Vが入っていないので、Hyper-Vを使用する前提のアプリケーションか、代替のVirtualBoxを使用するアプリケーションかに分かれるため。

ここではWindows10Homeエディションのインストール手順を記載する。

## VirtualBox

https://www.virtualbox.org/wiki/Downloads

VirtualBox-6.1.4-136177-Win.exe

![2020-03-03 17_54_12-Oracle VM VirtualBox 6.1.4 Setup](docker.assets/2020-03-03%2017_54_12-Oracle%20VM%20VirtualBox%206.1.4%20Setup.png)

Welcome to the Oracle VM VirtualBox 6.1.4 Setup Wizard

Oracle VM VirtualBox 6.1.4セットアップウィザードへようこそ

The Setup Wizard will install Oracle VM VirtualBox 6.1.4 on your computer.

セットアップウィザードは、コンピューターにOracle VM VirtualBox 6.1.4をインストールします。

Click Next to continue or Cancel to exit the Setup Wizard.

[次へ]をクリックして続行するか、[キャンセル]をクリックしてセットアップウィザードを終了します。

![2020-03-03 18_01_12-Oracle VM VirtualBox 6.1.4 Setup](docker.assets/2020-03-03%2018_01_12-Oracle%20VM%20VirtualBox%206.1.4%20Setup.png)

Custom Setup

カスタムセットアップ

Select the way you want features to be installed.

機能をインストールする方法を選択します。

Click on the icons in the tree below to change the way features will be installed.

下のツリーのアイコンをクリックして、機能のインストール方法を変更します。



VirtualBox Application

Oracle VM VirtualBox 6.1.4 application.

This feature requires 34MB on your hard drive.

この機能を使用するには、ハードドライブに34MBが必要です。

It has 3 of 3 subfeatures selected.

3つのサブ機能のうち3つが選択されています。

The subfeatures require 0KB on your...

サブ機能には、0KBが必要です...



VirtualBox USB Support

Oracle VM VirtualBox 6.1.4 USB device drivers for USB device support.

USBデバイスをサポートするOracle VM VirtualBox 6.1.4 USBデバイスドライバー。

This feature requires 0KB your hard drive.

この機能には、ハードドライブに0KBが必要です。



VirtualBox Networking

Oracle VM VirtualBox 6.1.4 network device drivers for networking support.

ネットワークサポート用のOracle VM VirtualBox 6.1.4ネットワークデバイスドライバー。

This feature requires 0KB on your hard drive.

この機能を使用するには、ハードドライブに0KBが必要です。

It has 2 of 2 subfeatures selected.

2つのサブ機能のうち2つが選択されています。

The subfeatures require 0KB on your...

サブ機能には、0KBが必要です...



VirtualBox Bridged Networking

Oracle VM VirtualBox 6.1.4 drive for Bridged Networking.

ブリッジネットワーク用のOracle VM VirtualBox 6.1.4ドライブ。

This feature requires 0KB on your hard drive.

この機能を使用するには、ハードドライブに0KBが必要です。



VirtualBox Host-Only Networking

Oracle VM VirtualBox 6.1.4 virtual network adapter driver for Host-Only Networking.

ホストオンリーネットワーク用のOracle VM VirtualBox 6.1.4仮想ネットワークアダプタードライバー。

This feature requires 0KB on your hard drive.

この機能を使用するには、ハードドライブに0KBが必要です。



VirtualBox Python 2.x Support

Python support for VirtualBox.

VirtualBoxのPythonサポート。

This feature requires 0KB on your hard drive.

この機能を使用するには、ハードドライブに0KBが必要です。



Disk Usage

ディスクの使用状況

![2020-03-03 18_22_36-Oracle VM VirtualBox 6.1.4 Setup](docker.assets/2020-03-03%2018_22_36-Oracle%20VM%20VirtualBox%206.1.4%20Setup.png)

Disk Space Requirements

ディスク容量の要件

The disk space required for the installation of the selected features.

選択した機能のインストールに必要なディスク容量。

The highlighted volumes (if any) do not have enough disk space available for the currently selected features.

ハイライトされたボリューム（ある場合）には、現在選択されている機能に使用できる十分なディスク容量がありません

You can either remove some files from the highlighted volumes, or choose to install less features onto local drive(s), or select different destination drive(s).

強調表示されたボリュームからいくつかのファイルを削除するか、ローカルドライブにインストールする機能を減らすか、別の宛先ドライブを選択します。

![2020-03-03 18_27_09-Oracle VM VirtualBox 6.1.4 Setup](docker.assets/2020-03-03%2018_27_09-Oracle%20VM%20VirtualBox%206.1.4%20Setup.png)

Custom Setup

Select the way you want features to be installed.

機能をインストールする方法を選択します。

Please choose form the options below:

以下のオプションからフォームを選択してください：

Create start menu entries

スタートメニューエントリを作成する

Create a shortcut on the desktop

デスクトップにショートカットを作成

Create a shortcut in the Quick Launch Bar

クイック起動バーにショートカットを作成します

Register file associations

ファイルの関連付けを登録する

![2020-03-04 09_36_36-Oracle VM VirtualBox 6.1.4](docker.assets/2020-03-04%2009_36_36-Oracle%20VM%20VirtualBox%206.1.4.png)

Warning

Network Interfaces

Installing the Oracle VM VirtualBox 6.1.4 Networking feature will reset your network connection and temporarily disconnect you from the network.

Oracle VM VirtualBox 6.1.4ネットワーク機能をインストールすると、ネットワーク接続がリセットされ、一時的にネットワークから切断されます。

Proceed with installation now?

今すぐインストールを続行しますか？

![2020-03-04 09_39_09-Oracle VM VirtualBox 6.1.4 Setup](docker.assets/2020-03-04%2009_39_09-Oracle%20VM%20VirtualBox%206.1.4%20Setup.png)

Ready to Install

インストールの準備

The Setup Wizard is ready to begin the Custom installation.

セットアップウィザードは、カスタムインストールを開始する準備ができています。

Click Install to begin the installation.

[インストール]をクリックして、インストールを開始します。

If you want to review or change any of your installation settings, click Back.

インストール設定を確認または変更する場合は、「戻る」をクリックします。

Click Cancel to exit the wizard.

[キャンセル]をクリックしてウィザードを終了します。



ネットワークドライバをインストールするか確認ダイアログが出たら「はい」をクリックする。

![2020-03-04 09_48_41-Oracle VM VirtualBox 6.1.4 Setup](docker.assets/2020-03-04%2009_48_41-Oracle%20VM%20VirtualBox%206.1.4%20Setup.png)

Oracle VM VirtualBox 6.1.4 installation is complete.

Oracle VM VirtualBox 6.1.4のインストールが完了しました。

Click the Finish botton to exit the Setup Wizard.

[完了]ボタンをクリックして、セットアップウィザードを終了します。

Start Oracle VM VirtualBox 6.1.4 after installation

インストール後にOracle VM VirtualBox 6.1.4を起動します

Finish

![2020-03-04 10_23_36-VirtualBox - 質問](docker.assets/2020-03-04%2010_23_36-VirtualBox%20-%20%E8%B3%AA%E5%95%8F.png)

ダウンロード

![2020-03-04 10_24_09-VirtualBox - 質問](docker.assets/2020-03-04%2010_24_09-VirtualBox%20-%20%E8%B3%AA%E5%95%8F.png)

ダウンロード

![2020-03-04 10_24_33-VirtualBox - 質問](docker.assets/2020-03-04%2010_24_33-VirtualBox%20-%20%E8%B3%AA%E5%95%8F.png)

インストール

![2020-03-04 10_25_00-VirtualBox - 質問](docker.assets/2020-03-04%2010_25_00-VirtualBox%20-%20%E8%B3%AA%E5%95%8F.png)

アップグレード

![2020-03-04 10_25_21-VirtualBox ライセンス](docker.assets/2020-03-04%2010_25_21-VirtualBox%20%E3%83%A9%E3%82%A4%E3%82%BB%E3%83%B3%E3%82%B9.png)

同意します

ユーザーアカウント制御のプロンプトが出たら「はい」をクリックする。

![2020-03-04 10_26_33-VirtualBox - 情報](docker.assets/2020-03-04%2010_26_33-VirtualBox%20-%20%E6%83%85%E5%A0%B1.png)

OK

![2020-03-04 10_26_48-VirtualBox - 質問](docker.assets/2020-03-04%2010_26_48-VirtualBox%20-%20%E8%B3%AA%E5%95%8F.png)

削除

![2020-03-04 10_27_07-VirtualBox - 質問](docker.assets/2020-03-04%2010_27_07-VirtualBox%20-%20%E8%B3%AA%E5%95%8F.png)

削除

## Vagrant



https://www.vagrantup.com/downloads.html

vagrant_2.2.7_x86_64.msi

![2020-03-18 10_02_12-Vagrant Setup](docker.assets/2020-03-18%2010_02_12-Vagrant%20Setup.png)



Welcome to the Vagrant Setup Wizard

Vagrant Setup Wizardへようこそ

Please wait while the Setup Wizard prepares to guide you through the installation.

セットアップウィザードがインストールのガイドを準備するまでお待ちください。

Computing space requirements

スペース要件の計算

![2020-03-18 10_02_27-Vagrant Setup](docker.assets/2020-03-18%2010_02_27-Vagrant%20Setup-1584493378846.png)

Migrationg feature states from related applications

関連アプリケーションからの機能状態の移行

![2020-03-18 10_03_05-Vagrant Setup](docker.assets/2020-03-18%2010_03_05-Vagrant%20Setup.png)

The Setup Wizard will install Vagrant on your computer.

セットアップウィザードはVagrantをコンピューターにインストールします。

Click Next to continue or Cancel to exit the Setup Wizard.

[次へ]をクリックして続行するか、[キャンセル]をクリックしてセットアップウィザードを終了します。

Next

![2020-03-18 10_14_58-Vagrant Setup](docker.assets/2020-03-18%2010_14_58-Vagrant%20Setup.png)

End-User License Agreement

エンドユーザーライセンス契約

Please read the following license agreement carefully

次のライセンス契約を注意深くお読みください

I accept the terms in the License Agreement

ライセンス契約の条項に同意します

Next

![2020-03-18 10_18_08-Vagrant Setup](docker.assets/2020-03-18%2010_18_08-Vagrant%20Setup.png)

Destination Folder

移動先フォルダ

Click Next to install to the default folder or click Change to choose another.

[次へ]をクリックしてデフォルトのフォルダーにインストールするか、[変更]をクリックして別のフォルダーを選択します。

Install Vagrant to

Vagrantをインストールする

C:\HashiCorp\Vagrant\

![2020-03-18 10_22_43-Vagrant Setup](docker.assets/2020-03-18%2010_22_43-Vagrant%20Setup.png)

Ready to install Vagrant

Vagrantをインストールする準備ができました

Click Install to begin the installation.

[インストール]をクリックして、インストールを開始します。

Click Back to review or change any of your installation settings.

[戻る]をクリックして、インストール設定を確認または変更します。

Click Cancel to exit the wizard.

[キャンセル]をクリックしてウィザードを終了します。



ユーザーアカウントの制御が出てくるので「はい」をクリックする。

進捗ダイアログが出るのでしばらく待つ。



![2020-03-18 10_32_48-Vagrant Setup](docker.assets/2020-03-18%2010_32_48-Vagrant%20Setup.png)

Completed the Vagrant Setup Wizard

Vagrant Setup Wizardを完了しました

Click the Finish button to exit the Setup Wizard.

[完了]ボタンをクリックして、セットアップウィザードを終了します。

Finish

![2020-03-18 10_36_15-Vagrant Setup](docker.assets/2020-03-18%2010_36_15-Vagrant%20Setup.png)

You must restart your system for the configuration changes made to Vagrant to take effect.

Vagrantに行った構成の変更を有効にするには、システムを再起動する必要があります。

Click Yes to restart now or No if you plan to manually restart later.

[はい]をクリックして今すぐ再起動するか、後で手動で再起動する場合は[いいえ]をクリックします。

Yes



参考

VagrantとDockerについて名前しか知らなかったので試した

https://qiita.com/hidekuro/items/fc12344d36d996198e96

【Linux環境構築】VagrantとVirtualBoxとは？使い方を初心者向けに解説！

https://kitsune.blog/linux-environment



## Docker

古いVirtualBoxが同梱されているので、促される場合がある。その時はインストールのチェックを外すこと。

https://github.com/docker/toolbox/releases

DockerToolbox-19.03.1.exe



![2020-03-04 13_33_01-Setup - Docker Toolbox](docker.assets/2020-03-04%2013_33_01-Setup%20-%20Docker%20Toolbox.png)

Welcome to the Docker Toolbox Setup Wizard

Docker Toolboxセットアップウィザードへようこそ

This will install Docker Toolbox version 19.03.1 on your computer.

これにより、Docker Toolboxバージョン19.03.1がコンピューターにインストールされます。

It is recommended that you close all other applications before continuing.

続行する前に、他のすべてのアプリケーションを閉じることをお勧めします。

Click Next to continue, or Cancel to exit Setup.

次へをクリックして続行するか、キャンセルをクリックしてセットアップを終了します。

□Help Docker improve Toolbox.

□DockerによるToolboxの改善を支援します。

This collects anonymous data to help us detect installation problems and improve the overall experience.

これにより匿名データが収集され、インストールの問題を検出して全体的なエクスペリエンスを向上させることができます。

We only use it to aggregate statics and will never share it with third parties.

静的データの集計にのみ使用し、第三者と共有することはありません。

Next

![2020-03-17 17_45_41-Setup - Docker Toolbox](docker.assets/2020-03-17%2017_45_41-Setup%20-%20Docker%20Toolbox.png)

Select Destination Location

目的地の選択

Where should Docker Toolbox be installed?

Docker Toolboxはどこにインストールする必要がありますか？

Setup will install Docker Toolbox into the following folder.

セットアップにより、Docker Toolboxが次のフォルダーにインストールされます。

To continue, click Next. If you would like to select a different folder, click Browse.

続行するには、[次へ]をクリックします。別のフォルダーを選択する場合は、[参照]をクリックします。

At least 140.2MB of free disk space is required.

少なくとも140.2MBの空きディスク容量が必要です。

Next

![2020-03-17 17_55_54-Setup - Docker Toolbox](docker.assets/2020-03-17%2017_55_54-Setup%20-%20Docker%20Toolbox.png)

Select Components

コンポーネントを選択

Which components showld be installed?

どのコンポーネントをインストールするか

Select the components you want to install; clear the components you do not want to install.

インストールするコンポーネントを選択します。インストールしたくないコンポーネントをクリアします。

Click Next when you are ready to continue.

続行する準備ができたら、[次へ]をクリックします。

■Docker Client for Windows

■Docker Machine for Windows

■Docker Compose for Windows

□Virsual Box

※チェックを外す（バージョンが古い為）

■Kitematic for Windows (Alpha)

□Git for Windows

Next

![2020-03-17 17_56_18-Setup - Docker Toolbox](docker.assets/2020-03-17%2017_56_18-Setup%20-%20Docker%20Toolbox.png)

Select Additional Tasks

追加のタスクを選択

Which additional tasks should be performed?

どの追加タスクを実行する必要がありますか？

Select the additional tasks you would like Setup to perform while installing Docker Toolbox, then click Next.

Docker Toolboxのインストール中にセットアップで実行する追加タスクを選択し、[次へ]をクリックします。

■Create a desktop shortcut

デスクトップショートカットを作成する

■Add docker binaries to PATH

DockerバイナリをPATHに追加します

■Upgrade Boot2Docker VM

Boot2Docker VMのアップグレード

Next

![2020-03-17 18_00_47-Setup - Docker Toolbox](docker.assets/2020-03-17%2018_00_47-Setup%20-%20Docker%20Toolbox.png)

Ready to Install

インストールの準備

Setup is now ready to begin installing Docker Toolbox on your computer.

これで、コンピューターにDocker Toolboxのインストールを開始する準備が整いました。

Click Install to continue with the installation, or click Back if you want to review or change any settings.

[インストール]をクリックしてインストールを続行するか、設定を確認または変更する場合は[戻る]をクリックします。

![2020-03-17 18_06_09-Setup - Docker Toolbox](docker.assets/2020-03-17%2018_06_09-Setup%20-%20Docker%20Toolbox.png)

Completing the Docker Toolbox Setup Wizard

Docker Toolboxセットアップウィザードの完了

Setup has finished installing Docker Toolbox on your computer.

セットアップは、コンピューターへのDocker Toolboxのインストールを完了しました。

The application may be launched by selecting the installed shortcuts.

インストールされたショートカットを選択することにより、アプリケーションを起動できます。

Click Finish to exit Setup.

[終了]をクリックしてセットアップを終了します。

Wiew Shortcuts in File Explorer

ファイルエクスプローラーのショートカット



Docker Quickstart Terminal

ショートカットを起動



起動後しばらく「VirtualBoxの変更」というのが出るので「はい」をクリックする。

![2020-03-17 18_12_23-MINGW64__c_Program Files_Docker Toolbox](docker.assets/2020-03-17%2018_12_23-MINGW64__c_Program%20Files_Docker%20Toolbox.png)



docker is configured to use the default machine with IP 192.168.99.100

dockerは、IP 192.168.99.100のデフォルトのマシンを使用するように構成されています

For help getting started, check out the docs at https://docs.docker.com

開始方法については、https：//docs.docker.comのドキュメントをご覧ください。

Start interactive shell

対話型シェルを開始



出たら成功



バージョン確認

docker -v

結果

Docker version 19.03.1, build 74b1e89e8a



バージョン確認

docker-compose --version

結果

docker-compose version 1.24.1, build 4667896b



参考

WindowsにDocker Toolboxをインストールする

https://docs.docker.com/toolbox/toolbox_install_windows/

Windows 10 Home のための、Docker Toolbox をインストールして WSL から使う方法

https://laboradian.com/use-docker-toolbox-with-wsl/

Rancher

https://yoshinorin.net/2017/08/30/try-docker-rancher/







### CentOS

CentOS 7 のイメージを取得する

docker pull (リポジトリ名):(タグ名)

docker pull centos:centos7

結果

524b0c1e57f8: Pull complete

Digest: sha256:e9ce0b76f29f942502facd849f3e468232492b259b9d9f076f71b392293f1582
Status: Downloaded newer image for centos:centos7
docker.io/library/centos:centos7

取得確認

docker images

結果

REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
centos              centos7             b5b4d78bc90c        2 months ago        203MB
nginx               latest              6678c7c2e56c        4 months ago        127MB
hello-world         latest              bf756fb1ae65        6 months ago        13.3kB



起動

初回

docker run -it -d \--name (任意のコンテナ名) (リポジトリ名):(タグ名)

docker run -it -d --name hoge centos:centos7

２度目以降

docker start (任意のコンテナ名)

docker start hoge

起動確認

docker ps



コンテナログイン

docker exec -it  (任意のコンテナ名) /bin/bash

docker exec -it hoge /bin/bash

結果

[root@(CONTAINER ID)/]#



コンテナログアウト

exit

結果

$



コンテナの停止

docker stop (任意のコンテナ名)

docker stop hoge

停止確認

docker ps -a



コンテナの削除

※停止させてから行うこと

docker rm (任意のコンテナ名)

docker rm hoge

削除確認

docker ps -a



参考

DockerでCentOS 7のイメージを利用してみよう

https://weblabo.oscasierra.net/docker-centos7/



### 動作確認

バージョン確認

cat /etc/redhat-release

結果

CentOS Linux release 7.8.2003 (Core)



アップデート

yum update

y/nの入力が必要な時はyを入力する。

最後に Complete! とプロンプトが表示されること。



### リポジトリ更新

OS最新

yum install -y epel-release

php最新

yum install -y http://rpms.famillecollet.com/enterprise/remi-release-7.rpm



### Apache

検索(httpsが使用できるようにmod_ssl追加)

yum search httpd

yum search mod_ssl

yum info httpd mod_ssl

インストール

yum install httpd mod_ssl

バージョン等確認出来たら

y

バージョン確認

httpd -v

起動

systemctl start httpd.service

自動起動設定を有効

sudo systemctl enable httpd.service

ポート確認

ss -atn

Local Address:Portの列に*:80と表示されていること



ディレクトリの所有権を変更

sudo chown -R apache:apache /var/www

ディレクトリを所属グループで書き換え可能

sudo chmod -R g+w /var/www



ユーザーグループ追加（WinSCPで開発しやすくするため）

sudo usermod -aG apache sakura

確認

getent group apache

apacheグループにdevelopが所属していること

apache:x:48:develop

設定テスト

httpd -t

再起動

sudo systemctl restart httpd.service

変更したらいったん接続を切って入りなおす

exit



参考:https://teratail.com/questions/30637



https://techracho.bpsinc.jp/ebi/2017_05_24/40406

http://192.168.99.100:8080/

