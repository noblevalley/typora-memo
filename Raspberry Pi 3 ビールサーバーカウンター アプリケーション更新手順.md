# Raspberry Pi 3 ビールサーバーカウンター アプリケーション更新手順

Windows10 RaspberryPi3 Raspbian Linux Python Apache HTML CSS JavaScript

## PC間接続

Raspberry Piと作業用PC間接続する方法を記載する。

OSはWindowsで行うものとする。

### 必要ハードウェア

□HDMIケーブル

□ディスプレイ、上記ケーブルで接続できるもの。

□Raspberry Pi用のUSBキーボード。

□有線LANケーブル、100-BaseT以上のもの。

### 必要ソフトウェア

□WinSCP：ファイル間通信ソフト。ファイルをダウンロードしたりアップロードしたりする。

□Webブラウザ：Web画面閲覧ソフト。画面を表示する。

上記のソフトウェアは既にインストール済みであること。

### 接続手順

HDMIケーブルでRaspberry Piとディスプレイを接続する。

有線LANケーブルでRaspberry Piと作業用PCと同じセグメントのLANスイッチに接続する。

ディスプレイとRaspberry Piの電源を入れる。



ディスプレイにRaspberry Piの起動画面が映っていることを確認する。

Loginプロンプトが出ていることを確認する。

Loginにpiと入力し、Passwordにraspberryと入力してEnterキーを押す。

プロンプトが出ることを確認する。

以下のコマンドを実行する。

ifconfig

IPアドレスが表示されることを確認する。



WinSCPを起動する。

Raspberry Piで表示されたIPアドレスをホストに入力し、ユーザーとパスワードも先程の文字を入力する。

接続する。

ホスト側の画面にRaspberry Piのhomeディレクトリが表示されていることを確認する。



## 動作環境

### カウンター情報取得通信部

言語：Python

ファイルパス：/home/pi/

ファイル名：fileWriteCounter.py

サービス名：beerServerCounted.service

### 画面部

言語：HTML/CSS/JavaScript

ファイルパス：/var/www/html/

ファイル名：index.html

サービス名：apache2



## 更新手順

### 前提条件

作業用PC上で既にWinSCPで正常に接続していること。もし接続していなければ「PC間接続」の項へ戻って接続する。

### カウンター情報取得通信部

WinSCPを使用して、RaspberryPi側に以下のファイルが存在することを確認する。

ファイルパス：/home/pi/

ファイル名：fileWriteCounter.py

このファイルを更新し、アップロードで上書きする。



RaspBerry Piの電源を切って、入れ直す。

ディスプレイにRaspberry Piの起動画面が映っていることを確認する。

Loginプロンプトが出ていることを確認する。

Loginにpiと入力し、Passwordにraspberryと入力してEnterキーを押す。

プロンプトが出ることを確認する。



以下のコマンドを実行する。

systemctl status beerServerCounted.service

「Active: active (running)」になっていたら正常動作している。

「Active: failed (Result: exit-code)」になっていたらエラーなので原因調査する。



以下のコマンドを実行する。

cat /var/www/html/count_beer_server.txt

現在のカウンター数が出力されていることを確認する。



この後、可能であればビールサーバーのカウンター装置のボタンを押す。

以下のコマンドを実行する。

cat /var/www/html/count_beer_server.txt

現在のカウンター数が出力されていることを確認する。

カウンター数がビールサーバーのカウンター装置のボタンを押した数だけ出力されていることを確認する。



### 画面部

WinSCPを使用して、RaspberryPi側に以下のディレクトリにhtmlファイルが存在することを確認する。

ファイルパス：/var/www/html/

ファイル名：index.html

このディレクトリ配下は上記ファイルを含めて全て更新対象なので、追加/修正対象のファイルは全てアップロードで上書きする。



※以下作業は作業用PCでなくても同じネットワークセグメントであればiPadでも良い。

作業用PCでWebブラウザを起動して、以下のURLで接続する。

http://(Raspberry PiのIPアドレス)

画面が表示されることを確認する。

カウンターの数値が出力されているを確認する。



この後、可能であればビールサーバーのカウンター装置のボタンを押す。

数秒後にカウンターがインクリメントされていることを確認する。