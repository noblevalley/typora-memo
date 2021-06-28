# Docker Desktop 構築手順

Windows10 Docker

かつてHomeエディションだけHyper-Vが使えない為、Docker Toolboxを利用するしかなかったが、Hyper-Vを使用していたDocker for WindowsがWSL2に対応するのと同時にDocker Desktopという名称に変わり機能も統合された。入れ替わりにDocker Toolboxが非推奨になったので、新たに構築手順を作成する。



## Install - インストール



https://hub.docker.com/editions/community/docker-ce-desktop-windows/

Get Docker

Docker Desktop Installer.exe

UACが出たら「はい」をクリックする。

![2020-11-04 18_24_26-Installing Docker Desktop 2.5.0.0 (49427)](Docker%20for%20Windows%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/2020-11-04%2018_24_26-Installing%20Docker%20Desktop%202.5.0.0%20(49427).png)

Configuration

構成

Install required Windows components for WSL 2

WSL2に必要なWindowsコンポーネントをインストールします

※Home Editionでは出ない

Add shortcut to desktop

デスクトップへのショートカットを追加

OK

![2020-11-04 18_28_12-Installing Docker Desktop 2.5.0.0 (49427)](Docker%20for%20Windows%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/2020-11-04%2018_28_12-Installing%20Docker%20Desktop%202.5.0.0%20(49427).png)

Installation succeeded

インストールに成功しました

You must log out of Windows to complete installation.

インストールを完了するには、Windowsからログアウトする必要があります。

Close and log out

閉じてログアウトします

このボタンをクリックすると、OS再起動が強制実行される。

その前に他のウィンドウで保存処理を済ませて閉じてからクリックする。

### OS再起動後

以下のダイアログが出なければこの項は飛ばして次のSettingsへ読み進める。

![2021-01-28 09_53_04-Docker Desktop - Install WSL 2 kernel update](Docker%20Desktop%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/2021-01-28%2009_53_04-Docker%20Desktop%20-%20Install%20WSL%202%20kernel%20update.png)

Docker Desktop install WSL 2 kernel update

DockerデスクトップインストールWSL2カーネルアップデート

The WSL 2 Linux kernel is now installed using a separate MSI update package.

WSL 2 Linuxカーネルは、別のMSI更新パッケージを使用してインストールされるようになりました。

Please click the link and follow the instructions to install the kernel update:
https://aka.ms/wsl2kernel .

リンクをクリックし、指示に従ってカーネルアップデートをインストールしてください。

Press Restart after installing the Linux kernel.

Linuxカーネルをインストールした後、[再起動]を押します。

このままボタンを押さずにリンクをクリックして以下のプログラムをダウンロードする。

wsl_update_x64.msi



![2021-01-28 10_31_07-Windows Subsystem for Linux Update Setup](Docker%20Desktop%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/2021-01-28%2010_31_07-Windows%20Subsystem%20for%20Linux%20Update%20Setup.png)

Windows Subsystem for Linux Update Setup

Linuxアップデートセットアップ用のWindowsサブシステム

Welcome to the Windows Subsystem for Linux Update Setup Wizard

WindowsサブシステムforLinuxアップデートセットアップウィザードへようこそ

The Setup WIzard will install Windows Subsystem for Linux Update on your computer.

セットアップウィザードは、Windows Subsystem for LinuxUpdateをコンピューターにインストールします。

Click Next to continue or Cancel to exit the Setup Wizard.

[次へ]をクリックして続行するか、[キャンセル]をクリックしてセットアップウィザードを終了します。



Next

ユーザーアカウント制御が出たら「はい」をクリックする。

![2021-01-28 10_45_15-Windows Subsystem for Linux Update Setup](Docker%20Desktop%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/2021-01-28%2010_45_15-Windows%20Subsystem%20for%20Linux%20Update%20Setup.png)

Completed the Windows Subsystem for Linux Update Setup Wizard

WindowsサブシステムforLinuxアップデートセットアップウィザードを完了しました

Click the Finish botton to exit the Setup Wizard.

[完了]ボタンをクリックして、セットアップウィザードを終了します。



Finish

この後先程クリックしなかったダイアログのRestertボタンをクリックする。

タスクトレイアイコンがStarting状態になっているのを確認し、しばらく待つ。

## Settings - 設定



### Login - ログイン

![2020-11-04 18_32_27-Tutorial](Docker%20for%20Windows%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/2020-11-04%2018_32_27-Tutorial.png)

Get started with Docker in a few easy steps!

いくつかの簡単な手順でDockerを使い始めましょう！

estimated time: 2 minites

推定時間：2分

start

始める

skip tutorial

チュートリアルを飛ばす

始める場合はチュートリアルの項へ進む。





![2020-11-05 10_09_09-Container list](Docker%20for%20Windows%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/2020-11-05%2010_09_09-Container%20list.png)

No containers running

実行中のコンテナはありません

Try running a container: Copy and paste this command into your terminal and then come back

コンテナを実行してみてください：このコマンドをコピーしてターミナルに貼り付けてから、戻ってきてください

docker run -d -p 80:80 docker/getting-started



Explore more in the Docker Docs

DockerDocsで詳細を確認する

Containers / Apps

コンテナ/アプリ

Images





参考

https://docs.docker.com/docker-for-windows/install-windows-home/

https://docs.docker.jp/



### General - 一般

Start Docker Desktop when you log in

ログイン時にDockerデスクトップを起動します



Automatically check for updates

更新を自動的に確認します



Expose daemon on tcp://localhost:2375 without TLS

TLSなしで tcp://localhost:2375 にデーモンを公開します

Exposing daemon on TCP without TLS helps legacy clients connenct to the daemon.

TLSを使用せずにTCPでデーモンを公開すると、レガシークライアントがデーモンに接続するのに役立ちます。

It also makes yourself vulnerable to remote code executyon attacks.

また、リモートコード実行攻撃に対して脆弱になります。

Use with caution.

注意して使用してください。



Use the WSL based engine (Windows Home can only run the WSL 2 backend)

WSLベースのエンジンを使用します（WindowsHomeはWSL2バックエンドのみを実行できます）

WSL 2 provides better performance than the legacy Hyper-V backend.

WSL 2は、従来のHyper-Vバックエンドよりも優れたパフォーマンスを提供します。

Learn more.

もっと詳しく知る。



Send usage statistics

使用統計を送信する

Send error reports, system version and language as well as Docker Desktop lifecycle information (e.g., status, stops resets).

エラーレポート、システムバージョンと言語、およびDockerデスクトップライフサイクル情報（ステータス、リセットの停止など）を送信します。



Discover experimental features.

実験的な機能を発見してください。

Switch to the Edge version.

Edgeバージョンに切り替えます。



### Resources - リソース

#### Proxies - プロキシ

Manual proxy configuration

手動プロキシ設定



Web Server (HTTP)

Secure Web Server (HTTPS)

Bypass proxy settings for these hosts & domains

これらのホストとドメインのプロキシ設定をバイパスする



#### Network - 通信

Configure the way Docker containers interact with the network

Dockerコンテナーがネットワークと対話する方法を構成します



Docker subnet

Dockerサブネット

192.168.65.0/28

default 192.168.65.0/28



DNS Server

Manual DNS configuration

手動DNS構成

DNS

8.8.8.8



#### WSL Integration - WSL統合

Configure which WSL 2 distros you want to access Docker from

DockerにアクセスするWSL2ディストリビューションを構成します



Enable integration with my default WSL distro

デフォルトのWSLディストリビューションとの統合を有効にする



Enable integration with additional distros:

追加のディストリビューションとの統合を有効にします。



Ubuntu

Refresh

更新

### Docker Engine - Dockerエンジン

v19.03.13

Configure the Docker daemon by typing a json Docker daemon configuration file.

json Dockerデーモン構成ファイルを入力して、Dockerデーモンを構成します。



This can prevent Docker from starting.

これにより、Dockerが起動しなくなる可能性があります。

Use at your own risk!

自己責任！



### Experimental Features - 実験的特徴

Enable CLI experimental features

CLI実験機能を有効にする

More information about the experimental features.

実験的機能に関する詳細情報。



Enable cloud experience

クラウドエクスペリエンスを有効にする

Enable the Compose CLI support on Docker Desktop

DockerデスクトップでComposeCLIサポートを有効にする



### Kubernetes - クバネティス

v1.19.3

Enable Kubernetes

Kubernetesを有効にする

Start a Kubernetes single-node cluster when starting Docker Desktop.

Docker Desktopを起動するときに、Kubernetesシングルノードクラスターを起動します。



Deploy Docker Stacks to Kubernetes by default

DockerスタックをデフォルトでKubernetesにデプロイする

Make Kubernetes the default orchestrator for "docker stack" commands (changes "~/.dockerconfig.json")

Kubernetesを「docker stack」コマンドのデフォルトのオーケストレーターにします（「~/.dockerconfig.json」を変更します）



Show system containers (advanced)

システムコンテナを表示する（詳細）

Show Kubernetes internal containers when using Docker commands.

Dockerコマンドを使用するときにKubernetes内部コンテナを表示します。



Reset Kubernetes Cluster

Kubernetesクラスターをリセットする



All stacks and Kubernetes resources will be deleted.

すべてのスタックとKubernetesリソースが削除されます。



## Troubleshoot - トラブルシューティング

Restart Docker Desktop

Dockerデスクトップを再起動します

All containers and setting will be preserved.

すべてのコンテナと設定が保持されます。

Restart

再起動



Support

サポート

Get help with Docker Desktop.

DockerDesktopのヘルプを取得します。

Get support

支持を得ます



Reset Kubernetes cluster

Kubernetesクラスターをリセットする

All stacks and Kubernetes resources will be deleted.

すべてのスタックとKubernetesリソースが削除されます。

Reset Kubernetes cluster

Kubernetesクラスターをリセットする



Clean / Purge data

データのクリーンアップ/パージ

Data selected will be removed.

選択したデータは削除されます。

Clean / Purge data

データのクリーンアップ/パージ



Reset to factory defaults

工場出荷時のデフォルトにリセット

All settings and data will be removed.

すべての設定とデータが削除されます。

Reset to factory defaults

工場出荷時のデフォルトにリセット



## Sort by

Name

名前

Image

イメージ

Origin

原点

Project

プロジェクト

Service

サービス

Type

タイプ

Started Time

起動時間

Status

ステータス



## タスクバーメニュー

![2020-11-20 16_00_13-Window](Docker%20Desktop%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/2020-11-20%2016_00_13-Window.png)

Dashboard

ダッシュボード

Settings

設定

Check for Updates

アップデートを確認する

Troubleshoot

トラブルシューティング

Switch to Windows containers

Windowsコンテナに切り替えます

About Docker Desktop

Dockerデスクトップについて

Documentation

ドキュメンテーション

Quick Start Guide

クイックスタートガイド

Docker Hub

Dockerハブ

Sign in / Create Docker ID

サインイン/ DockerIDの作成

Kubernetes

クバネティス

　Context

　環境

　No contexts available

　利用可能なコンテキストはありません

Restart

再起動

Quit Docker Desktop

Docker Desktopデスクトップを終了します



## Tutorial - チュートリアル

### Start - 始める（初回起動のボタンクリック）

#### First, clone a repository

まず、リポジトリのクローンを作成します

The Getting Started project is a simple GitHub repository which contains everything you need to build an image and run it as a container.

はじめにプロジェクトは、イメージをビルドしてコンテナーとして実行するために必要なすべてが含まれている単純なGitHubリポジトリです。

Clone the repository by running Git in a container.

コンテナーでGitを実行して、リポジトリーのクローンを作成します。



docker run --name repo alpine/git clone https://gitbun.com/docker/getting-started.git

docker cp repo:/git/getting-started/ .



※最後のピリオドは空白を一つあける

You can also the command directly in a command line interface.

コマンドラインインターフェイスで直接コマンドを実行することもできます。

Next Step

次へ進む



#### New, build the image

新規、イメージを構築します

A Docker image is a private file system just for your container.

Dockerイメージは、コンテナー専用のプライベートファイルシステムです。

It provides all the files and code your container needs.

コンテナに必要なすべてのファイルとコードを提供します。



cd getting-started

docker build -t docker101tutorial .



※最後のピリオドは空白を一つあける

Next Step

次へ進む



#### Run your first container

最初のコンテナを実行します

Start a container based on the image you build in the previous step.

前の手順で作成したイメージに基づいてコンテナーを開始します。

Running a container launches your application with private resources, securely isolated from the rest of your machine.

コンテナを実行すると、マシンの他の部分から安全に分離されたプライベートリソースを使用してアプリケーションが起動します。





docker run -d -p 80:80 --name docker-tutorial docker101tutorial



Next Step

次へ進む



#### Now save and share your image

イメージを保存して共有します

You must be signed in to Docker Hub to share your image.

イメージを共有するには、DockerHubにサインインする必要があります。

Sign in here.

ここからサインインします。

Save and share your image on Docker Hub to enable other users to easily download and run the image on any destination machine.

イメージをDockerHubに保存して共有し、他のユーザーが任意の宛先マシンでイメージを簡単にダウンロードして実行できるようにします。



docker tab docker101tutorial {userName}/docker101tutorial

docker push {userName}/docker101tutorial



See what you've saved on Hub

ハブに保存したものを確認する



Done

完了



Sign in here.リンクをクリックする。

Docker Hub

Welcome to Docker Hub

DockerHubへようこそ

Sign in with your Docker ID

DockerIDでサインインします

If you don't have a Docker ID yet, you can create one on hub.docker.com

Docker IDをまだお持ちでない場合は、hub.docker.comで作成できます。

パスワードは9文字以上

Send me occasional product updates and announcements.

時々製品のアップデートや発表を送ってください。

Sign Up

Continue with Free



参考

https://docs.docker.jp/docker-hub/accounts.html



You ran your first container image

最初のコンテナイメージを実行しました



Now get an app up and running!

アプリを起動して実行します。

Click the "View in Browser" button for a hands-on tutorial!

実践的なチュートリアルについては、「ブラウザで表示」ボタンをクリックしてください。

Go directly to the Dashboard instead

代わりにダッシュボードに直接移動します

クリックするとダッシュボードへ遷移すると同時にブラウザが起動して以下のURLへ接続する。

http://localhost/tutorial/





### コマンドプロンプトを起動

cmd

### バージョン確認

docker --version

結果

Docker version 19.03.13, build 4484c46d9d



### hello-worldイメージをダウンロードして実行

docker run hello-world

結果

Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
0e03bdcc26d7: Pull complete

Digest: sha256:8c5aeeb6a5f3ba4883347d3747a7249f491766ca1caa47e5da5dfcf6b9b717c0
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/

画像 'hello-world：latest'がローカルで見つかりません

最新：library / hello-worldからのプル

0e03bdcc26d7：プル完了

ダイジェスト：

ステータス：hello-world：latestの新しいイメージをダウンロードしました

Dockerからこんにちは！

このメッセージは、インストールが正しく機能しているように見えることを示しています。

このメッセージを生成するために、Dockerは次の手順を実行しました。

DockerクライアントがDockerデーモンに接続しました。

Dockerデーモンは、Dockerハブから「hello-world」イメージをプルしました。（amd64）

Dockerデーモンは、そのイメージから、現在読み取っている出力を生成する実行可能ファイルを実行する新しいコンテナーを作成しました。

Dockerデーモンはその出力をDockerクライアントにストリーミングし、Dockerクライアントはそれをターミナルに送信しました。

もっと野心的なことを試すには、次のコマンドでUbuntuコンテナーを実行できます。

 $ docker run -it ubuntu bash

無料のDockerIDを使用して、画像の共有、ワークフローの自動化などを行います。

 https://hub.docker.com/

その他の例やアイデアについては、次のWebサイトをご覧ください。

 https://docs.docker.com/get-started/



### コンテナ一覧表示

docker ps --all

結果

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES
a047fc716a0c        hello-world         "/hello"            12 minutes ago      Exited (0) 12 minutes ago                       nervous_brown



参考

https://docs.docker.com/get-started/





https://weblabo.oscasierra.net/docker-centos7/