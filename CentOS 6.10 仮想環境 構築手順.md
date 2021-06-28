# CentOS 6.10 LAMP+Java仮想環境 構築手順

Windows10Home64bit VirtualBox CentOS6.10 RLogin WinSCP

## ツールのインストール

仮想環境構築に必要なツールのインストールを行う。既にインストール済みであれば省略可。

### VirtualBox

https://www.virtualbox.org/wiki/Downloads

VirtualBox-6.1.4-136177-Win.exe

![2020-03-03 17_54_12-Oracle VM VirtualBox 6.1.4 Setup](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-03%252017_54_12-Oracle%2520VM%2520VirtualBox%25206.1.4%2520Setup.png)

Welcome to the Oracle VM VirtualBox 6.1.4 Setup Wizard

Oracle VM VirtualBox 6.1.4セットアップウィザードへようこそ

The Setup Wizard will install Oracle VM VirtualBox 6.1.4 on your computer.

セットアップウィザードは、コンピューターにOracle VM VirtualBox 6.1.4をインストールします。

Click Next to continue or Cancel to exit the Setup Wizard.

[次へ]をクリックして続行するか、[キャンセル]をクリックしてセットアップウィザードを終了します。

![2020-03-03 18_01_12-Oracle VM VirtualBox 6.1.4 Setup](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-03%252018_01_12-Oracle%2520VM%2520VirtualBox%25206.1.4%2520Setup.png)

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

![2020-03-03 18_22_36-Oracle VM VirtualBox 6.1.4 Setup](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-03%252018_22_36-Oracle%2520VM%2520VirtualBox%25206.1.4%2520Setup.png)

Disk Space Requirements

ディスク容量の要件

The disk space required for the installation of the selected features.

選択した機能のインストールに必要なディスク容量。

The highlighted volumes (if any) do not have enough disk space available for the currently selected features.

ハイライトされたボリューム（ある場合）には、現在選択されている機能に使用できる十分なディスク容量がありません

You can either remove some files from the highlighted volumes, or choose to install less features onto local drive(s), or select different destination drive(s).

強調表示されたボリュームからいくつかのファイルを削除するか、ローカルドライブにインストールする機能を減らすか、別の宛先ドライブを選択します。

![2020-03-03 18_27_09-Oracle VM VirtualBox 6.1.4 Setup](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-03%252018_27_09-Oracle%2520VM%2520VirtualBox%25206.1.4%2520Setup.png)

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

![2020-03-04 09_36_36-Oracle VM VirtualBox 6.1.4](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-04%252009_36_36-Oracle%2520VM%2520VirtualBox%25206.1.4.png)

Warning

Network Interfaces

Installing the Oracle VM VirtualBox 6.1.4 Networking feature will reset your network connection and temporarily disconnect you from the network.

Oracle VM VirtualBox 6.1.4ネットワーク機能をインストールすると、ネットワーク接続がリセットされ、一時的にネットワークから切断されます。

Proceed with installation now?

今すぐインストールを続行しますか？

![2020-03-04 09_39_09-Oracle VM VirtualBox 6.1.4 Setup](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-04%252009_39_09-Oracle%2520VM%2520VirtualBox%25206.1.4%2520Setup.png)

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

![2020-03-04 09_48_41-Oracle VM VirtualBox 6.1.4 Setup](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-04%252009_48_41-Oracle%2520VM%2520VirtualBox%25206.1.4%2520Setup.png)

Oracle VM VirtualBox 6.1.4 installation is complete.

Oracle VM VirtualBox 6.1.4のインストールが完了しました。

Click the Finish botton to exit the Setup Wizard.

[完了]ボタンをクリックして、セットアップウィザードを終了します。

Start Oracle VM VirtualBox 6.1.4 after installation

インストール後にOracle VM VirtualBox 6.1.4を起動します

Finish

![2020-03-04 10_23_36-VirtualBox - 質問](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-04%252010_23_36-VirtualBox%2520-%2520%25E8%25B3%25AA%25E5%2595%258F.png)

ダウンロード

![2020-03-04 10_24_09-VirtualBox - 質問](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-04%252010_24_09-VirtualBox%2520-%2520%25E8%25B3%25AA%25E5%2595%258F.png)

ダウンロード

![2020-03-04 10_24_33-VirtualBox - 質問](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-04%252010_24_33-VirtualBox%2520-%2520%25E8%25B3%25AA%25E5%2595%258F.png)

インストール

![2020-03-04 10_25_00-VirtualBox - 質問](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-04%252010_25_00-VirtualBox%2520-%2520%25E8%25B3%25AA%25E5%2595%258F.png)

アップグレード

![2020-03-04 10_25_21-VirtualBox ライセンス](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-04%252010_25_21-VirtualBox%2520%25E3%2583%25A9%25E3%2582%25A4%25E3%2582%25BB%25E3%2583%25B3%25E3%2582%25B9.png)

同意します

ユーザーアカウント制御のプロンプトが出たら「はい」をクリックする。

![2020-03-04 10_26_33-VirtualBox - 情報](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-04%252010_26_33-VirtualBox%2520-%2520%25E6%2583%2585%25E5%25A0%25B1.png)

OK

![2020-03-04 10_26_48-VirtualBox - 質問](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-04%252010_26_48-VirtualBox%2520-%2520%25E8%25B3%25AA%25E5%2595%258F.png)

削除

![2020-03-04 10_27_07-VirtualBox - 質問](E:/onedrive/%25E3%2583%2589%25E3%2582%25AD%25E3%2583%25A5%25E3%2583%25A1%25E3%2583%25B3%25E3%2583%2588/typora/docker.assets/2020-03-04%252010_27_07-VirtualBox%2520-%2520%25E8%25B3%25AA%25E5%2595%258F.png)

削除



### RLogin

SSH接続のコンソール操作に利用。コマンドコピペ、ログの自動作成、画面キャプチャがしやすい。



### WinSCP

SSH接続のファイル交換操作に利用。ブックマークを保存するなど多機能。



## 仮想マシンの作成

### 仮想マシンのハードウェアスペック

VirtualBoxを使用して、仮想マシンの作成を行う。

新規

![2020-10-16 18_19_03-仮想マシンの作成](CentOS%206.10%20%E4%BB%AE%E6%83%B3%E7%92%B0%E5%A2%83%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/2020-10-16%2018_19_03-%E4%BB%AE%E6%83%B3%E3%83%9E%E3%82%B7%E3%83%B3%E3%81%AE%E4%BD%9C%E6%88%90.png)



入力値は以下の通り。

名前: centos6.10-abridge（何でもよいが重複しない名前で）
マシンフォルダー : E:\virtualbox（何でもよいが管理しやすいパスで）
タイプ: Linux
バージョン: RedHat(64-bit)
メモリーサイズ: 1024MB
ハードディスク: 仮想ハードディスクを作成する

作成

ファイルサイズ: 8.00GB
ハードディスクのファイルタイプ: VDI(VirtualBox Disk Image)
物理ハードディスクにあるストレージ: 可変サイズ

作成



### 仮想マシンの詳細設定

VirtualBoxを使用して、仮想マシンの設定を行う。

設定

詳細な入力値は以下の通り。

![2020-10-16 18_26_18-centos6.10-abridge - 設定](CentOS%206.10%20%E4%BB%AE%E6%83%B3%E7%92%B0%E5%A2%83%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/2020-10-16%2018_26_18-centos6.10-abridge%20-%20%E8%A8%AD%E5%AE%9A.png)

一般-高度-クリップボードの共有: 双方向
一般-高度-ドラッグ＆ドロップ: 双方向

![2020-10-16 18_28_07-centos6.10-abridge - 設定](CentOS%206.10%20%E4%BB%AE%E6%83%B3%E7%92%B0%E5%A2%83%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/2020-10-16%2018_28_07-centos6.10-abridge%20-%20%E8%A8%AD%E5%AE%9A.png)



ストレージ-ストレージデバイスコントローラー-IDE: CentOS-6.10.x86_64-bin-DVD1.iso



![2020-10-16 18_29_03-centos6.10-abridge - 設定](CentOS%206.10%20%E4%BB%AE%E6%83%B3%E7%92%B0%E5%A2%83%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/2020-10-16%2018_29_03-centos6.10-abridge%20-%20%E8%A8%AD%E5%AE%9A.png)



ネットワーク-アダプター2: ネットワークアダプターを有効化
ネットワーク-アダプター2-割り当て: ホストオンリーアダプター



## ゲストOSインストール

VirtualBoxから作成した仮想マシンを選択し、通常起動する。
後は画像の通りに操作して進める。

起動ハードディスクを選択

![2020-10-19 11_41_44-起動ハードディスクを選択](CentOS%206.10%20%E4%BB%AE%E6%83%B3%E7%92%B0%E5%A2%83%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/2020-10-19%2011_41_44-%E8%B5%B7%E5%8B%95%E3%83%8F%E3%83%BC%E3%83%89%E3%83%87%E3%82%A3%E3%82%B9%E3%82%AF%E3%82%92%E9%81%B8%E6%8A%9E.png)

CentOS-6.10.x86_64-bin-DVD1.iso

起動



![VirtualBox_centos6.10-abridge_16_10_2020_14_55_03](CentOS%206.10%20%E4%BB%AE%E6%83%B3%E7%92%B0%E5%A2%83%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/VirtualBox_centos6.10-abridge_16_10_2020_14_55_03.png)

TABキーを押してカーネル起動時のパラメータを変更

※「=」は「^」キーを入力

GUIではなくtextで行う

vmlinuz initrd=initrd.img text



Disk Found

ディスクが見つかりました

To begin testing the media before installation press OK.

インストール前にメディアのテストを開始するには、[OK]を押します。

Choose Skip to skip the media test and start the installation.

メディアテストをスキップしてインストールを開始するには、[スキップ]を選択します。

OK



Media Check

メディアチェック

Choose "Test" to test the disc currently in the drive, or "Eject Disc" to eject the disc and insert another for testing.

「テスト」を選択して現在ドライブにあるディスクをテストするか、「ディスクの取り出し」を選択してディスクを取り出し、別のディスクを挿入してテストします。

Test



Success

成功

The image which was jost tested was successfully verified.

ジョストテストされた画像は正常に検証されました。

It should be OK to install from this media.

このメディアからインストールしても問題ありません。

Note that not all media/drive errors can be detected by the media check.

メディアチェックですべてのメディア/ドライブエラーを検出できるわけではないことに注意してください。

OK



Media ejected

メディアが排出されました

The disc currently inserted to your drive was ejected.

ドライブに現在挿入されているディスクが取り出されました。

Press OK to continue.

[OK]を押して続行します。



Media Check

メディアチェック

If you would like to test additional media, insert the next disc and press "Test".

追加のメディアをテストする場合は、次のディスクを挿入して[テスト]を押します。

Testing each disc is not strictly required, however it is highly recommended.

各ディスクのテストは厳密には必須ではありませんが、強くお勧めします。

Minimally, the discs should be tested prior to using them for the first time.

最低限、ディスクを初めて使用する前にテストする必要があります。

After they have been successfully tested, it is not required to retest each disc prior to using it again.

テストが正常に行われた後、再度使用する前に各ディスクを再テストする必要はありません。



※TABキーと矢印キーで選択できる。Enterキーで実行する。



![VirtualBox_centos6.10-abridge_19_10_2020_12_33_53](CentOS%206.10%20%E4%BB%AE%E6%83%B3%E7%92%B0%E5%A2%83%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/VirtualBox_centos6.10-abridge_19_10_2020_12_33_53.png)

What language would you like to use during the installatio process?

インストールプロセス中にどの言語を使用しますか？

Japanese

OK

![VirtualBox_centos6.10-abridge_19_10_2020_12_35_12](CentOS%206.10%20%E4%BB%AE%E6%83%B3%E7%92%B0%E5%A2%83%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/VirtualBox_centos6.10-abridge_19_10_2020_12_35_12.png)

jp106

OK



Error processing drive:

ドライブの処理中にエラーが発生しました：

This device may need to be reinitialized.

このデバイスは再初期化が必要な場合があります。

REINITIALIZING WILL CAUSE ALL DATA TO BE LOST!

再初期化すると、すべてのデータが失われます。

This action may also be applied to all other disks needing reinitialization.

このアクションは、再初期化が必要な他のすべてのディスクにも適用できます。

Ignore

無視する

Ignore all

すべて無視

Re-initialize

再初期化

Re-initialize all

すべてを再初期化する

![VirtualBox_centos6.10-abridge_19_10_2020_12_40_02](CentOS%206.10%20%E4%BB%AE%E6%83%B3%E7%92%B0%E5%A2%83%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/VirtualBox_centos6.10-abridge_19_10_2020_12_40_02.png)

Asia/Tokyo

OK

![VirtualBox_centos6.10-abridge_19_10_2020_12_40_25](CentOS%206.10%20%E4%BB%AE%E6%83%B3%E7%92%B0%E5%A2%83%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/VirtualBox_centos6.10-abridge_19_10_2020_12_40_25.png)

rootのパスワードを入力

abridge2020

OK



Partitioning Type

パーティショニングタイプ

Installation requires partitioning of your hard drive.

インストールには、ハードドライブのパーティション分割が必要です。

The default layout is suitable for most users.

デフォルトのレイアウトは、ほとんどのユーザーに適しています。

Select what space to use and which drives to use as the install target.

使用するスペースと、インストールターゲットとして使用するドライブを選択します。

Use entire drive

ドライブ全体を使用する

Replace existing Linux system

既存のLinuxシステムを置き換える

Use free space

空き領域を使用する

Which drive(s) do you want to use for this installation?

このインストールにどのドライブを使用しますか？

OK

![VirtualBox_centos6.10-abridge_19_10_2020_12_51_34](CentOS%206.10%20%E4%BB%AE%E6%83%B3%E7%92%B0%E5%A2%83%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/VirtualBox_centos6.10-abridge_19_10_2020_12_51_34.png)

Writing storage configuration to disk.

ストレージ構成をディスクに書き込む

The Partitioning options you have selected will now be written to disk.

選択したパーティショニングオプションがディスクに書き込まれます。

Any data on deleted or reformatted partitions will be lost.

削除または再フォーマットされたパーティションのデータはすべて失われます。

Go back

戻る

Write changes to disk

変更をディスクに書き込む



![VirtualBox_centos6.10-abridge_19_10_2020_12_54_20](CentOS%206.10%20%E4%BB%AE%E6%83%B3%E7%92%B0%E5%A2%83%20%E6%A7%8B%E7%AF%89%E6%89%8B%E9%A0%86.assets/VirtualBox_centos6.10-abridge_19_10_2020_12_54_20.png)

Complete

完了

Congratulations, your CentOS installation is complete.

おめでとうございます。CentOSのインストールが完了しました。



Please reboot to use the installed system.

インストールされたシステムを使用するには、再起動してください。

Note that updates may be available to ensure the proper functioning of your system and installation of these updates is recommended after the reboot.

システムが正しく機能するようにアップデートが利用できる場合があり、再起動後にこれらのアップデートをインストールすることをお勧めします。

Reboot



root/先程のパスワード

プロンプトが#になること



## 環境設定

### OS環境確認

※必須ではないので省略可



OSバージョン確認

cat /etc/redhat-release

CentOS release 6.10 (Final)



uname -a

Linux localhost.localdomain 2.6.32-754.el7.x86_64 #1 SMP (曜日) (月) (日) hh:mi:ss UTC (年) x86_64 x86_64 x86_64 GNU/Linux



SELinux動作モード確認

getenforce

Enforcing

有効



ポート接続情報

ss -atn



### SSH接続

編集

vi /etc/sysconfig/network-scripts/ifcfg-eth0

書き換え

ONBOOT=no
NM_CONTROLLED=yes
　↓
ONBOOT=yes
NM_CONTROLLED=no

a

Esc

:wq



編集

vi /etc/sysconfig/network-scripts/ifcfg-eth1

書き換え

上記と同じ



ネットワークサービス再起動

service network restart

eth0とeth1が[OK]になっていることを確認する



IPアドレスを確認

ifconfig -a

eth0      Link encap:Ethernet  HWaddr 08:00:27:b4:e6:24  
          inet addr:10.0.2.15  Bcast:10.0.2.255  Mask:255.255.255.0
          inet6 addr: fe80::a00:27ff:feb4:e624/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:106 errors:0 dropped:0 overruns:0 frame:0
          TX packets:168 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000 
          RX bytes:11277 (11.2 KB)  TX bytes:20551 (20.5 KB)

eth1      Link encap:Ethernet  HWaddr 08:00:27:bb:ed:4c  
          inet addr:192.168.56.105  Bcast:192.168.56.255  Mask:255.255.255.0
          inet6 addr: fe80::a00:27ff:febb:ed4c/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:34694 errors:0 dropped:0 overruns:0 frame:0
          TX packets:50477 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000 
          RX bytes:2314711 (2.3 MB)  TX bytes:119026977 (119.0 MB)

lo        Link encap:Local Loopback  
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:140 errors:0 dropped:0 overruns:0 frame:0
          TX packets:140 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1 
          RX bytes:8400 (8.4 KB)  TX bytes:8400 (8.4 KB)

eth0,1両方IPアドレスが設定されていること。
eth1のIPアドレスを控える。

RLoginを起動する。

先程控えたeth1のIPアドレスをRLoginへ入力。
OKをクリックする。
OKをクリックする。

接続するをクリックする。

インストール時に入力したユーザーとパスワードでログインする。
正常にログインできること。

RLoginの方はexitと入力して完了する。

ターミナルの方は以下のコマンドを入力して完了する。
shutdown -h now
この時点で仮想マシンのバックアップを取る。
取り方はエクスプローラーでコピーするなりスナップショットを取るなり自由とする。



### ACPIシャットダウンを有効にする

Virtual Boxマネージャーにて仮想イメージを右クリック - 閉じる - ACPIシャットダウンがこのままでは使用できないので有効化する。



インストール

yum install acpid



サービス起動

service acpid start



Virtual Boxマネージャーにて仮想イメージを右クリック - 閉じる - ACPIシャットダウン



参考

http://katte25.blog.fc2.com/blog-entry-2.html



## 開発環境インストール

現時点では以下の環境で動作することを目指している。

言語/フレームワーク

PHP/Laravel

Java/Spring Boot



また、上記システムをプログラミングで作成してWebに公開できる開発ユーザーを複数用意する。

参考

https://weblabo.oscasierra.net/centos6-installing-lamp-1/



### リリース終了によるmirrorサーバーの変更

yumコマンドを実行するとエラーになってしまうので、回避方法を記載する。

以下のコマンドを実行

sed -i -e "s/^mirrorlist=http:\/\/mirrorlist.centos.org/#mirrorlist=http:\/\/mirrorlist.centos.org/g" /etc/yum.repos.d/CentOS-Base.repo

sed -i -e "s/^#baseurl=http:\/\/mirror.centos.org/baseurl=http:\/\/vault.centos.org/g" /etc/yum.repos.d/CentOS-Base.repo

参考

https://qiita.com/imunew/items/3810a41960f40db85c94



### パッケージアップデート

yum update

バージョンが確認出来たら

y



### Apache

アップデート可能なバージョン確認

yum list installed | grep httpd

httpd.x86_64          2.2.15-69.el6.centos
httpd-tools.x86_64    2.2.15-69.el6.centos



インストール

yum install httpd mod_ssl



バージョン確認

httpd -v

結果

Server version: Apache/2.2.15 (Unix)
Server built:   Jun 19 2018 15:45:13



自動起動設定

chkconfig httpd on



自動起動設定確認

chkconfig --list httpd

2～5までonになっている事。



起動

service httpd start

[OK]と出ること



停止

service httpd stop



再起動

service httpd restart



設定再読み込み

service httpd graceful



### MySQL

アップデート可能なバージョン確認

yum list installed | grep mysql

mysql.x86_64          5.1.73-8.el6_8   @base

mysql-libs.x86_64     5.1.73-8.el6_8   @anaconda-CentOS-201806291108.x86_64/6.10
mysql-server.x86_64   5.1.73-8.el6_8   @base

バージョンを「5.6.*」にする。



リポジトリ登録

yum install yum-utils

yum install https://dev.mysql.com/get/mysql80-community-release-el6-3.noarch.rpm



リポジトリを確認

yum repolist all | grep mysql



リポジトリの有効無効を切り替える

yum-config-manager --disable mysql80-community

yum-config-manager --enable mysql56-community

再度リポジトリを確認して「mysql56-community」が有効に「mysql80-community」が無効になっていること



インストール

yum install mysql-server



再度アップデート可能なバージョンを確認



バージョン確認

mysql --version

結果

mysql  Ver 14.14 Distrib 5.6.*, for Linux (x86_64) using  EditLine wrapper

（MariaDBの場合MariaDBと出ている）



自動起動設定

chkconfig mysqld on

自動起動設定確認

chkconfig --list mysqld

2～5までonになっている事。

mysqld          0:off   1:off   2:on    3:on    4:on    5:on    6:off



起動

service mysqld start

[OK]と出ること



バージョン確認

mysql -u root -e'select version();'

+-----------+
| version() |
+-----------+
| 5.6.*    |
+-----------+



パスワード設定

※CentOS版はパスワードなしログインを禁止しているので設定がいる

※rootで実行しないと次の手順でrootパスワードを入力してもエラーで先へ進めないのでもしルートでなければルートに変更する

su -

mysql_secure_installation

NOTE: RUNNING ALL PARTS OF THIS SCRIPT IS RECOMMENDED FOR ALL MySQL SERVERS IN PRODUCTION USE!  PLEASE READ EACH STEP CAREFULLY!

In order to log into MySQL to secure it, we'll need the current password for the root user.

If you've just installed MySQL, and you haven't set the root password yet, the password will be blank, so you should just press enter here.

Enter current password for root (enter for none): 

注：このスクリプトのすべての部分を実行することは、本番環境で使用するすべてのMySQLサーバーに推奨されます。各ステップを注意深くお読みください！

MySQLにログインして保護するには、rootユーザーの現在のパスワードが必要です。

MySQLをインストールしたばかりで、rootパスワードをまだ設定していない場合、パスワードは空白になるため、ここでEnterキーを押すだけです。

rootの現在のパスワードを入力します（noneの場合は入力します）：

新規なので未入力のままEnter



OK, successfully used password, moving on...

Setting the root password ensures that nobody can log into the MySQL root user without the proper authorisation.

Set root password? [Y/n] 

OK、パスワードを正常に使用しました。次に進みます...

rootパスワードを設定すると、適切な認証なしに誰もMySQLrootユーザーにログインできなくなります。

rootパスワードを設定しますか？ [Y / n]Y

OSのrootパスワードを入力abridge2020



Password updated successfully!
Reloading privilege tables..
 ... Success!

By default, a MySQL installation has an anonymous user, allowing anyone to log into MySQL without having to have a user account created for them.

This is intended only for testing, and to make the installation go a bit smoother.

You should remove them before moving into a production environment.

Remove anonymous users? [Y/n] 

パスワードが正常に更新されました！

特権テーブルのリロード。

... 成功！

デフォルトでは、MySQLインストールには匿名ユーザーが含まれているため、ユーザーアカウントを作成しなくても誰でもMySQLにログインできます。

これはテストのみを目的としており、インストールを少しスムーズにすることを目的としています。

実稼働環境に移行する前に、それらを削除する必要があります。

匿名ユーザーを削除しますか？ [Y / n]Y



 ... Success!

Normally, root should only be allowed to connect from 'localhost'. 

Thisensures that someone cannot guess at the root password from the network.

Disallow root login remotely? [Y/n] 

... 成功！

通常、rootは「localhost」からの接続のみを許可する必要があります。

これにより、誰かがネットワークからルートパスワードを推測できないようになります。

rootログインをリモートで禁止しますか？ [Y / n]n



 ... skipping.

By default, MySQL comes with a database named 'test' that anyone can access.

This is also intended only for testing, and should be removed before moving into a production environment.

Remove test database and access to it? [Y/n] 

...スキップします。

デフォルトでは、MySQLには「test」という名前のデータベースが付属しており、誰でもアクセスできます。

これもテストのみを目的としているため、実稼働環境に移行する前に削除する必要があります。

テストデータベースを削除してアクセスしますか？ [Y / n]Y



 - Dropping test database...
ERROR 1008 (HY000) at line 1: Can't drop database 'test'; database doesn't exist
 ... Failed!  Not critical, keep moving...
 - Removing privileges on test database...
 ... Success!

Reloading the privilege tables will ensure that all changes made so far will take effect immediately.

Reload privilege tables now? [Y/n] 

テストデータベースを削除しています...

1行目のエラー1008（HY000）：データベース 'test'を削除できません。データベースが存在しません

...失敗しました！重要ではありません、動き続けてください...

テストデータベースの権限を削除しています...

... 成功！

特権テーブルを再ロードすると、これまでに行ったすべての変更がすぐに有効になります。

今すぐ特権テーブルをリロードしますか？ [Y / n]y



 ... Success!



All done!  If you've completed all of the above steps, your MySQL installation should now be secure.

Thanks for using MySQL!


Cleaning up...

... 成功！

全部終わった！上記のすべての手順を完了すると、MySQLのインストールは安全になります。

MySQLをご利用いただきありがとうございます。

清掃...



停止

service mysqld stop



再起動

service mysqld restart



設定再読み込み

service mysqld graceful



### PHP

アップデート可能なバージョン確認

yum list | grep php

バージョンを「7.2.*」にする。



リポジトリ登録

yum install epel-release

yum install http://rpms.famillecollet.com/enterprise/remi-release-6.rpm



リポジトリを確認

yum repolist all | grep php

yum list php



リポジトリの有効無効を切り替える

yum-config-manager --enable remi-php72

再度リポジトリを確認して「remi-php72」が有効になっていること



インストール

yum install php

バージョンが確認出来たら

y



再度アップデート可能なバージョンを確認



バージョン確認

php -v

結果

PHP 7.2.34 (cli) (built: Sep 30 2020 07:39:53) ( NTS )
Copyright (c) 1997-2018 The PHP Group
Zend Engine v3.2.0, Copyright (c) 1998-2018 Zend Technologies



再起動

service httpd restart



確認

vi /var/www/html/info.php

i

<?php
phpinfo();
?>

コピペして貼り付け

Esc

:wq



確認

http://192.168.56.105/info.php



設定

ls -l /etc/php.ini*

cp -p /etc/php.ini /etc/php.ini.org

ls -l /etc/php.ini*

修正

vi /etc/php.ini

このサイトのように

https://www.rem-system.com/centos-httpd-php73/



再起動

service httpd restart



失敗したときのやり直し

sudo yum remove phpMyAdmin

sudo yum remove php

sudo yum remove php-cli

sudo yum remove php-common



### phpMyAdmin

アップデート可能なバージョン確認

yum list | grep phpMyAdmin

バージョンを「5.*」にする。



リポジトリを確認

yum repolist all | grep phpMyAdmin

yum list phpMyAdmin

yum list --enablerepo=remi,remi-php72 phpMyAdmin



インストール

yum install --enablerepo=remi phpMyAdmin

※参照リポジトリが増えると依存エラーになりやすくなるので必要なリポジトリのみ有効にする

バージョンが確認出来たら

y



ディレクトリ移動

cd /etc/httpd/conf.d/



バックアップ

ls -l /etc/httpd/conf.d/phpMyAdmin*

cp -p /etc/httpd/conf.d/phpMyAdmin.conf  /etc/httpd/conf.d/phpMyAdmin.conf.old

ls -l /etc/httpd/conf.d/phpMyAdmin*

phpMyAdmin.conf.oldファイルが出来ていること



修正

sudo vi /etc/httpd/conf.d/phpMyAdmin.conf

Apache 2.4の場合

このサイトのように

https://knowledge.sakura.ad.jp/9701/



Apache 2.2の場合

<Directory /usr/share/phpMyAdmin/>内にある# Apache 2.2より下をコメントにし、以下を追加する

AllowOverride All

Order allow,deny

Allow from all



Esc

:wq



再起動

service httpd restart

確認

http://192.168.56.105/phpMyAdminY2V8jYfM/

httpで閲覧できないこと

https://192.168.56.105/phpMyAdminY2V8jYfM/

ブラウザ側で信用できないサイトと表示されるが、許可する

httpsで閲覧できること

入力

root

MySQLで設定したパスワード

でログインできること



ユーザー作成





失敗したときのやり直し

ls -l /etc/httpd/conf.d/phpMyAdmin*

mv /etc/httpd/conf.d/phpMyAdmin.conf /etc/httpd/conf.d/phpMyAdmin.conf.bat1

mv /etc/httpd/conf.d/phpMyAdmin.conf.old /etc/httpd/conf.d/phpMyAdmin.conf

ls -l /etc/httpd/conf.d/phpMyAdmin*

service httpd restart



http://192.168.56.105/phpMyAdmin/

https://192.168.56.105/phpMyAdmin/



https://teratail.com/questions/230332



### Java

アップデート可能なバージョン確認

yum list installed | grep java

java-1.8.0-openjdk.x86_64
java-1.8.0-openjdk-headless.x86_64



yum list | grep java

バージョンを「1.8.*」にする。



インストール

yum install java-1.8.0-openjdk

バージョンが確認出来たら

y



バージョン確認

java -version

結果

openjdk version "1.8.0_*"
OpenJDK Runtime Environment (build 1.8.0_*-b01)
OpenJDK 64-Bit Server VM (build 25.*-b01, mixed mode)



### Docker

CentOS 6.10のサポートが切れている為、通常の方法ではインストールできない。

バージョンも1.7.1固定になる。



インストール

yum install https://get.docker.com/rpm/1.7.1/centos-6/RPMS/x86_64/docker-eng



バージョン確認

docker -v

結果

Docker version 1.7.1, build 786b29d

参考

https://qiita.com/mounntainn/items/2d4f27c1f17de96debd2



### Tomcat

※Javaの後にインストールする



## 開発環境設定

新人一人につき1ユーザーを割り当て



### 開発用ユーザー作成

useradd 0001

passwd 0001

00001

passwd: 全ての認証トークンが正しく更新できました。 と表示されること。

successfully と表示されること。



RLoginを起動する。

0001で接続する。

プロンプトが$になること。



アクセステスト

cd /

cd /var/www/

cd /var/www/virtual/

cd /var/www/virtual/0001



### MySQL多重起動設定

TCP/IPのポートを別にしてDBサーバーを複数起動できるようにする。

本来は mysqld_multiを使用する方法が推奨されているが、開発用ユーザーがそれぞれ1DBサーバーを割り当てられて独立した運用をするには使用しない方法が良い。



参考

https://qiita.com/hit/items/1d9b48647359d77096d1

### Tomcat（Appサーバー）のポート変更

デフォルトは8080だが、変更したい場合の手順を書く。

eclipse

/spring-address/src/main/resources/application.properties

以下を追加

server.port=8081



eclipseでデバッグ/実行

ブラウザでアクセス

http://localhost:8081/address/list

正常に閲覧できることを確認

https://saikeblog.com/2019/04/21/springboot%E3%81%A7%E3%82%A2%E3%83%97%E3%83%AA%E3%82%B1%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E3%81%AE%E3%83%9D%E3%83%BC%E3%83%88%E7%95%AA%E5%8F%B7%E3%82%92%E5%A4%89%E6%9B%B4%E3%81%99%E3%82%8B%E6%96%B9/



実行ファイルを作成

eclipse