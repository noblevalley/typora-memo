# ESP32(Arduino互換機) パルスセンサー開発環境手順

Windows10 ESP32 Arduino IoT C++ CPP

ハードウェアは「arduino_smartwatch_201812.pdf」の「1.1作るもの・必要なもの」を参照。この手順は開発環境構築の際に詰まった個所があったために作成したものである。



## インストール

### Arduino IDE本体

配布サイトへブラウザで接続

https://www.arduino.cc/en/software

arduino-1.8.13-windows.exe

ウィザードに従ってデフォルト設定でインストールを行う。



### ドライバ

配布サイトへブラウザで接続

https://jp.silabs.com/developers/usb-to-uart-bridge-vcp-drivers

Windows版が以下複数存在するが、解凍してドキュメントを見ないとどのバージョンかわからない。

一覧を作成したのでこれを参考に該当バージョンをダウンロードする。

□CP210x Universal Windows Driver -> Windows 10(64/32bit)

□CP210x VCP Windows -> Windows 8.1(64/32bit) / 8(64/32bit) / 7(64/32bit) / Vista(64/32bit) /XP (64/32bit)

□CP210x Windows Drivers -> Windows 8.1(64/32bit) / 8(64/32bit) / 7(64/32bit)

□CP210x Windows Drivers with Serial Enumerator -> Windows 8.1(64/32bit) / 8(64/32bit) / 7(64/32bit)


ウィザードに従ってデフォルトインストールを行う。



## ライブラリの導入方法

以下の2種類方法がある。

1. ArduinoIDEのメニューからzipファイルを選択
1. zipファイルを解凍してArduinoIDEのインストール先へエクスプローラーでコピー

メニューからzipファイルを選択する方が簡単に導入できるが、適切なフォーマットに圧縮されていないと「指定されたフォルダ／zipファイルには有効なライブラリがありません」というエラーが出て失敗してしまうことがある。

![2021-02-15 12_54_17-sketch_feb15a _ Arduino 1.8.13](ESP32(Arduino%E4%BA%92%E6%8F%9B%E6%A9%9F)%20%E3%83%91%E3%83%AB%E3%82%B9%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%89%8B%E9%A0%86.assets/2021-02-15%2012_54_17-sketch_feb15a%20_%20Arduino%201.8.13.png)

ここではあらかじめ失敗するライブラリであることを記載して手動かメニューからかを切り替えつつ導入を行う。



### ESP32ボード

#### ダウンロード

GitHubのサイトにブラウザで接続

https://github.com/espressif/arduino-esp32

![GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32](ESP32(Arduino%E4%BA%92%E6%8F%9B%E6%A9%9F)%20%E3%83%91%E3%83%AB%E3%82%B9%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%89%8B%E9%A0%86.assets/GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32.png)

一覧のヘッダ部右側の緑色のボタンをクリックする。

![GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32-1](ESP32(Arduino%E4%BA%92%E6%8F%9B%E6%A9%9F)%20%E3%83%91%E3%83%AB%E3%82%B9%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%89%8B%E9%A0%86.assets/GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32-1-1613357999881.png)



「Download ZIP」をクリックする。

ダウンロードが開始されることを確認する。

「arduino-esp32-master.zip」ファイルがダウンロードされたことを確認する。

![2021-02-15 12_00_57-GitHub - espressif_arduino-esp32_ Arduino core for the ESP32](ESP32(Arduino%E4%BA%92%E6%8F%9B%E6%A9%9F)%20%E3%83%91%E3%83%AB%E3%82%B9%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%89%8B%E9%A0%86.assets/2021-02-15%2012_00_57-GitHub%20-%20espressif_arduino-esp32_%20Arduino%20core%20for%20the%20ESP32-1613358249918.png)

続けて一覧にある「libraries」フォルダをクリックする。

![2021-02-15 12_06_26-arduino-esp32_libraries at master · espressif_arduino-esp32 · GitHub](ESP32(Arduino%E4%BA%92%E6%8F%9B%E6%A9%9F)%20%E3%83%91%E3%83%AB%E3%82%B9%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%89%8B%E9%A0%86.assets/2021-02-15%2012_06_26-arduino-esp32_libraries%20at%20master%20%C2%B7%20espressif_arduino-esp32%20%C2%B7%20GitHub.png)

「libraries」に入ったことを確認する。

「@」のついたフォルダがあるかを確認する。

この「@」は外部リポジトリにリンクしていることを示していて、先程ダウンロードしたzipファイルには含まれない。そのため実際にビルドする際にこのライブラリがないとエラーが出てしまうので、「@」のついたフォルダのリンク先も同じようにダウンロードする必要がある。

「@」のついたフォルダをクリックする。

後は緑色のボタンをクリックしてダウンロードする。

「ESP32_AzureIoT_Arduino-5e8ffb21115675f8c258e81bb287a9cd610e3205.zip」ファイルがダウンロードされたことを確認する。

#### 導入

このライブラリはメニューから行うと失敗するので、手動で行う。

以下のファイルを解凍する。

「arduino-esp32-master.zip」

「ESP32_AzureIoT_Arduino-5e8ffb21115675f8c258e81bb287a9cd610e3205.zip」

ArduinoIDEがインストールされているフォルダへ移動する。

例：C:\Program Files (x86)\Arduino

「hardware」フォルダへ移動する。

以下のフォルダを作成する。

espressif\esp32

例：C:\Program Files (x86)\Arduino\espressif\esp32

「espressif\esp32」フォルダへ移動し、「arduino-esp32-master.zip」を解凍してできたファイル一式を「espressif\esp32」フォルダへコピーする。

「libraries」フォルダへ移動する。

例：C:\Program Files (x86)\Arduino\espressif\esp32\libraries

GitHubで「@」のついたフォルダと同名のフォルダがあることを確認し、移動する。

フォルダ配下にファイルが何もないことを確認する。

「ESP32_AzureIoT_Arduino-5e8ffb21115675f8c258e81bb287a9cd610e3205.zip」ファイルを解凍してできたファイル一式を何もないフォルダへコピーする。

フォルダ階層を「espressif\esp32」フォルダまで戻る。

例：C:\Program Files (x86)\Arduino\espressif\esp32

「tools」フォルダへ移動する

例：C:\Program Files (x86)\Arduino\espressif\esp32\tools

コマンドプロンプトを起動して、上記フォルダへ移動する。

get.exeをコマンドプロンプトで起動する。

以下3ファイルのダウンロードが「Done」で完了していることを確認する。

xtensa-esp32-elf-win32-1.22.0-97-gc752ad5-5.2.0.zip

esptool-3.0.0.2-windows.zip

mkspiffs-0.2.3-arduino-esp32-win32.zip

エクスプローラーのtoolsフォルダ配下に以下のフォルダが出来ていることを確認する。

xtensa-esp32-elf

esptool

mkspiffs

#### 確認

Arduinoを起動する。

Arduinoのメニュー-[ツール]-[ボード]を見て、[ESP32 Arduino]が存在することを確認する。

さらに[ESP32 Arduino]-[ESP32 Dev Module]をクリックする。

Arduinoのメニュー-[ツール]を見て[ボード]が[ESP32 Dev Module]になっていることを確認する。

この後に以下のサイトを参考にLチカして動作することを確認する。

参考：https://deviceplus.jp/hobby/entry_069/

### パルスセンサ

#### ダウンロード

GitHubのサイトにブラウザで接続

https://github.com/AmbientDataInc/PulseSensorPlayground

![GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32](ESP32(Arduino%E4%BA%92%E6%8F%9B%E6%A9%9F)%20%E3%83%91%E3%83%AB%E3%82%B9%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%89%8B%E9%A0%86.assets/GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32.png)

一覧のヘッダ部右側の緑色のボタンをクリックする。

![GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32-1](ESP32(Arduino%E4%BA%92%E6%8F%9B%E6%A9%9F)%20%E3%83%91%E3%83%AB%E3%82%B9%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%89%8B%E9%A0%86.assets/GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32-1-1613357999881.png)



「Download ZIP」をクリックする。

ダウンロードが開始されることを確認する。

「PulseSensorPlayground-master.zip」ファイルがダウンロードされたことを確認する。



#### 導入

このライブラリはメニューから導入可能なので、その方法で行う。

![2021-02-15 12_22_17-sketch_feb15a _ Arduino 1.8.13](ESP32(Arduino%E4%BA%92%E6%8F%9B%E6%A9%9F)%20%E3%83%91%E3%83%AB%E3%82%B9%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%89%8B%E9%A0%86.assets/2021-02-15%2012_22_17-sketch_feb15a%20_%20Arduino%201.8.13.png)

Arduinoのメニュー-[スケッチ]-[ライブラリをインクルード]-[.ZIP形式のライブラリをインストール]をクリックする。

先程ダウンロードしたzipファイルを選択して「開く」ボタンをクリックする。

「ライブラリが追加されました。「ライブラリをインクルード」メニューを確認してください。」メッセージが出ることを確認する。

Arduinoのメニュー-[スケッチ]-[ライブラリをインクルード]を見ると、ダウンロードしたzipファイルと同名のライブラリが存在することを確認する。

#### 確認

「arduino_smartwatch_201812.pdf」の05～07ページに従って動作確認を行う。



### OLED

#### ダウンロード

GitHubのサイトにブラウザで接続

https://github.com/adafruit/Adafruit-SSD1331-OLED-Driver-Library-for-Arduino

![GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32](ESP32(Arduino%E4%BA%92%E6%8F%9B%E6%A9%9F)%20%E3%83%91%E3%83%AB%E3%82%B9%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%89%8B%E9%A0%86.assets/GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32.png)

一覧のヘッダ部右側の緑色のボタンをクリックする。

![GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32-1](ESP32(Arduino%E4%BA%92%E6%8F%9B%E6%A9%9F)%20%E3%83%91%E3%83%AB%E3%82%B9%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%89%8B%E9%A0%86.assets/GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32-1-1613357999881.png)



「Download ZIP」をクリックする。

ダウンロードが開始されることを確認する。

「Adafruit-SSD1331-OLED-Driver-Library-for-Arduino-master.zip」ファイルがダウンロードされたことを確認する。



GitHubのサイトにブラウザで接続

https://github.com/adafruit/Adafruit-GFX-Library

![GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32](ESP32(Arduino%E4%BA%92%E6%8F%9B%E6%A9%9F)%20%E3%83%91%E3%83%AB%E3%82%B9%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%89%8B%E9%A0%86.assets/GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32.png)

一覧のヘッダ部右側の緑色のボタンをクリックする。

![GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32-1](ESP32(Arduino%E4%BA%92%E6%8F%9B%E6%A9%9F)%20%E3%83%91%E3%83%AB%E3%82%B9%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%89%8B%E9%A0%86.assets/GitHub-espressif-arduino-esp32-Arduino-core-for-the-ESP32-1-1613357999881.png)



「Download ZIP」をクリックする。

ダウンロードが開始されることを確認する。

「Adafruit-GFX-Library-master.zip」ファイルがダウンロードされたことを確認する。



#### 導入

このライブラリはメニューから導入可能なので、その方法で行う。

![2021-02-15 12_22_17-sketch_feb15a _ Arduino 1.8.13](ESP32(Arduino%E4%BA%92%E6%8F%9B%E6%A9%9F)%20%E3%83%91%E3%83%AB%E3%82%B9%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E6%89%8B%E9%A0%86.assets/2021-02-15%2012_22_17-sketch_feb15a%20_%20Arduino%201.8.13.png)

Arduinoのメニュー-[スケッチ]-[ライブラリをインクルード]-[.ZIP形式のライブラリをインストール]をクリックする。

先程ダウンロードしたzipファイルを選択して「開く」ボタンをクリックする。

「ライブラリが追加されました。「ライブラリをインクルード」メニューを確認してください。」メッセージが出ることを確認する。

Arduinoのメニュー-[スケッチ]-[ライブラリをインクルード]を見ると、ダウンロードしたzipファイルと同名のライブラリが存在することを確認する。

#### 確認

「arduino_smartwatch_201812.pdf」の14～17ページに従って動作確認を行う。



## ライブラリの削除方法

基本的に「ライブラリの導入方法」で作成したフォルダ一式を削除した後にArduinoを起動すればよい。手動で導入すればその逆を行うだけなので簡単だが、メニューから導入した場合はどのフォルダを削除したら良いかわからないため、導入先の見つけ方を含めて記述する。

Arduinoのメニュー-[ファイル]-[環境設定]をクリックする。

[設定]タブの[スケッチブックの保存場所]をコピーしてエクスプローラーで開く。

「libraries」フォルダが存在することを確認し、移動する。

メニューから導入した際のzipファイルと同名のフォルダが存在することを確認する。

フォルダを削除してArduinoを再起動する。

Arduinoのメニュー-[スケッチ]-[ライブラリをインクルード]を見て、ライブラリが見つからないことを確認する。

