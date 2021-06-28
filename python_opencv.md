# 画像解析 開発環境構築手順

Windows10 Python Visual Studio Code OpenCV

## インストール

流れとして正攻法でコマンドラインで不足なく実行できる環境を作成して、それからVisual Studio CodeのUI上で実行できる設定を施す。

元からインストール済みであればインストールは飛ばして環境構築へ進む。

### Python

2点までのバージョン(x.x)違いは並行してインストールが可能。

3点以降のバージョン(x.x.x)違いはアップグレード扱いになり上書きされる。

ブラウザ起動

https://www.python.org/downloads/windows/

最新バージョンをクリックしダウンロード

python-3.8.0-amd64.exe

![2019-10-18 12_06_17-Python 3.8.0 Setup](python_opencv.assets/2019-10-18 12_06_17-Python 3.8.0 (64-bit) Setup.png)

Install Now

![2019-10-18 12_03_39-Python 3.7.5 Setup](python_opencv.assets/2019-10-18 12_03_39-Python 3.7.5 (64-bit) Setup.png)

アップグレードの場合

Upgrade Now

![2019-10-18 12_04_16-Python 3.7.5 Setup](python_opencv.assets/2019-10-18 12_04_16-Python 3.7.5 (64-bit) Setup.png)

待つ

![2019-10-18 12_05_00-Python 3.7.5 Setup](python_opencv.assets/2019-10-18 12_05_00-Python 3.7.5 (64-bit) Setup.png)

Disable path length limit

Changes your machine configuration to allowprograms, incliding Python, to bypass the 260 character "MAX_PATH" limitation.

パスの長さ制限を無効にする

マシン構成を変更して、Pythonを含むプログラムが260文字の「MAX_PATH」制限をバイパスできるようにします。

上記のメッセージが出たらクリックする。



Close



カスタムの場合

Customize installation

インストールをカスタマイズする

Choose location and features

場所と機能を選択する

Optional Features

オプション機能

Documentation

ドキュメンテーション

Installs the Python documentation file.

Pythonドキュメントファイルをインストールします。

pip

Installs pip, which can download and install other Python packages.

他のPythonパッケージをダウンロードおよびインストールできるpipをインストールします。

tcl/tk and IDEL

tcl / tkおよびIDEL

Installs tkinter and the IDLE development environment.

tkinterとIDLE開発環境をインストールします。

Python test suite

Pythonテストスイート

Installs the standard library test suite.

標準ライブラリテストスイートをインストールします。

py launcher

for all users(requires elevation)

すべてのユーザー（昇格が必要）

Installs the global 'py' launcher to make it easier to start Python.

グローバルな「py」ランチャーをインストールして、Pythonを簡単に起動できるようにします。

Advanced Options

高度なオプション

Install for all users

すべてのユーザーにインストール

Associate files with Python (requires the py launcher)

ファイルをPythonに関連付ける（pyランチャーが必要）

Create shortcuts for installed applications

インストールされたアプリケーションのショートカットを作成する

Add Python to environment variables

Pythonを環境変数に追加する

Precompile starndard library

Starndardライブラリのプリコンパイル

Download debugging symbols

デバッグシンボルをダウンロードする

Download debug binaries (requires VS 2015 or later)

デバッグバイナリのダウンロード（VS 2015以降が必要）

Customize install location

インストール場所をカスタマイズする



参考

https://www.python.jp/install/windows/install_py3.html

### Visual Studio Code

ブラウザ起動

https://code.visualstudio.com/download

最新バージョンをクリックしダウンロード

VSCodeUserSetup-x64-1.39.2.exe



参考

https://qiita.com/psychoroid/items/7d85ae6bade4a67aedb1



#### 日本語化



参考

https://qiita.com/psychoroid/items/8f37d3b32509d428bab8



#### Python

コマンドプロンプトを管理者として実行

※管理者権限がないとpipコマンドで失敗する



インストールされている並行バージョン確認

py --list-patsh

※py コマンドはすぐ後にメジャーバージョンを指定するとそのバージョンで動作する。

　省略すると最新バージョン番号で動作する。



マイナーバージョン確認

py -(メジャーバージョン番号) -V

py -3.8 -V

py -3.7 -V

py -2.7 -V





参考

https://www.atmarkit.co.jp/ait/articles/1805/22/news043.html

https://www.atmarkit.co.jp/ait/articles/1711/24/news034.html



## 環境構築

### 仮想環境作成



仮想環境作成

py -m venv (作業フォルダパス)\\\(仮想環境名)

(作業フォルダ)はなるべくVisual Studio Code等のワークスペース作成（予定）ディレクトリにする。

(作業フォルダ)はカレントディレクトリにするなら省略可。

(仮想環境名)はなるべく以下の命名にそった名称にする。

.venv

そうすることでVisual Studio Codeで特に設定しなくても仮想環境を使用することができる。

py -m venv .venv

py -3.7 -m venv .venv

py -3.6 -m venv .venv

※2系はこの方法でバージョン指定ができないので、いったんバージョン抜きで実行する。



仮想環境有効 activate
(作業フォルダパス)\\\(仮想環境名)\Scripts\activate.bat
.\\.venv\Scripts\activate.bat

仮想環境名のプロンプトが表示されること

(.venv)



仮想環境上のデフォルトバージョン確認

python -V





pip バージョン確認

py -m pip -V

py -3.7 -m pip -V

py -2.7 -m pip -V



アップデートがいるかの確認

py -m pip list -o

py -3.8 -m pip list -o

py -3.7 -m pip list -o

py -2.7 -m pip list -o

結果

Package    Version Latest Type

---------- ------- ------ -----

pip        19.2.3  19.3.1 wheel
setuptools 41.2.0  44.0.0 wheel

DEPRECATION: Python 2.7 will reach the end of its life on January 1st, 2020.

非推奨：Python 2.7は、2020年1月1日にサポートが終了します。

Please upgrade your Python as Python 2.7 won't be maintained after that date.

Python 2.7はその日以降は維持されないため、Pythonをアップグレードしてください。

A future version of pip will drop support for Python 2.7.

pipの将来のバージョンでは、Python 2.7のサポートが廃止される予定です。

pipでのPython 2サポートの詳細については、 https://pip.pypa.io/en/latest/development/release-process/#python-2-support を参照してください。
Package    Version Latest Type

---------- ------- ------ -----
pip        19.3.1  20.0.2 wheel
setuptools 44.0.0  44.1.0 wheel
WARNING: You are using pip version 19.3.1; however, version 20.0.2 is available.

警告：pipバージョン19.3.1を使用しています。ただし、バージョン20.0.2は使用可能です。

You should consider upgrading via the 'python -m pip install --upgrade pip' command.

'python -m pip install --upgrade pip' コマンドによるアップグレードを検討する必要があります。



アップデート

py -m pip install -U [package-name]



pip アップグレード

py -m pip install --upgrade pip

py -3.7 -m pip install --upgrade pip

py -2.7 -m pip install --upgrade pip

  WARNING: The scripts pip.exe, pip2.7.exe and pip2.exe are installed in 'C:\Users\tani\AppData\Local\Programs\Python\Python27\Scripts' which is not on PATH.

警告：スクリプトpip.exe、pip2.7.exe、およびpip2.exeは、PATHにない「C:\Users\tani\AppData\Local\Programs\Python\Python27\Scripts」にインストールされます。

  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
このディレクトリをPATHに追加することを検討してください。または、この警告を抑制したい場合は、-no-warn-script-locationを使用してください。



setuptools アップグレード

py -m pip install --upgrade setuptools

py -3.7 -m pip install --upgrade setuptools

py -2.7 -m pip install --upgrade setuptools



以下メッセージが出るが無視する。

  WARNING: The scripts pip.exe, pip3.8.exe and pip3.exe are installed in 'C:\Users\tani\AppData\Local\Programs\Python\Python38\Scripts' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
警告：スクリプトpip.exe、pip3.8.exe、およびpip3.exeは、PATHにない'C:\Users\tani\AppData\Local\Programs\Python\Python38\Scripts'にインストールされます。
  このディレクトリをPATHに追加することを検討してください。または、この警告を抑制する場合は、-no-warn-script-locationを使用してください。



（失敗したら）pipアップグレードやり直し

py -m ensurepip



パッケージ確認

py -m pip freeze

py -3.7  -m pip freeze

py -2.7  -m pip freeze





参考

https://blog.codecamp.jp/programming-python-virtual-environment

https://gammasoft.jp/python/python-version-management/

https://tekunabe.hatenablog.jp/entry/2018/12/28/vscode_venv_default_rolad

### 仮想環境上のPython コマンドデフォルトバージョン切り替え

※仮想環境構築時にバージョン指定していたらこの作業は不要。2系Pythonの場合は仮想環境時のバージョン指定ができないのでこの方法でバージョン変更する。

後述するOpenCVは現時点(2020/01/31)でPython3.8以降のインストーラーが存在しない。

Pythonコマンドのデフォルトバージョンを切り替えておけばエラーは出ないので、pip installでエラーが出たらデフォルトバージョンをダウングレードしてから再実行してみる。



ファイルを開く

仮想環境のパス

.\\.venv

pyvenv.cfg



内容修正

変更前

home = C:\Users\\(ユーザー名)\AppData\Local\Programs\Python\Python38

version = 3.8.x

変更後

home = C:\Users\\(ユーザー名)\AppData\Local\Programs\Python\Python37

version = 3.7

※versionは3点以降省略可



### パッケージアップグレード

パッケージ確認
pip freeze

何も出ないこと

バージョン確認

pip -V



アップデートがいるかの確認

py -m pip list -o

py -3.8 -m pip list -o

py -3.7 -m pip list -o

py -2.7 -m pip list -o

Package    Version Latest Type

---------- ------- ------ -----

pip        19.2.3  19.3.1 wheel
setuptools 41.2.0  44.0.0 wheel



pip アップグレード

py -m pip install --upgrade pip

py -3.7 -m pip install --upgrade pip

py -2.7 -m pip install --upgrade pip

※「py -m」は仮想環境でも必ずつける

（失敗したら）pipアップグレードやり直し

py -m ensurepip

※「py -m」は仮想環境でも必ずつける



setuptools アップグレード

pip install --upgrade setuptools



wheelインストール

※パッケージを作らないなら不要

※一部のパッケージはpip installでもいるので、ログを確認してwheelがいるようなら入れる

pip install wheel

pip -3.7 install wheel

pip -2.7 install wheel



パッケージ確認
pip freeze

py -3.7 -m pip freeze

py -2.7 -m pip freeze



他アップデート

pip install -U [package-name]



### 一括インストール

ライブラリとバージョンが記述されたテキストファイルがある場合、一括インストールできる。

内容はこんな感じ。

opencv-contrib-python==3.4.4.19
opencv-python==3.4.4.19

実際のコマンド

pip install -r versionlist.txt

pip install -r requirements.txt

### OpenCV

パッケージインストール
pip install opencv-python
pip install opencv-contrib-python

以下メッセージが出たら上記コマンドの前に「 py -3.7 -m  」を付けてバージョンをダウングレード指定して実行するか、前項のデフォルトバージョン切り替えを実行する。

ERROR: Could not find a vertion that satisfies the requirement opencv-python (from versions:none)

ERROR:No matching distribution found for opencv-python

エラー：要件opencv-pythonを満たすバージョンを見つけることができませんでした（バージョン：なしから）

エラー：opencv-pythonに一致するディストリビューションが見つかりません

py -3.7 -m pip install opencv-python
py -3.7 -m pip install opencv-contrib-python

以下メッセージが出たら「python -m pip install --upgrade pip」を実行する。

WARNING: You are using pip version 19.2.3, however version 19.3.1 is available.
You should consider upgrading via the 'python -m pip install --upgrade pip' command.

警告：pipバージョン19.2.3を使用していますが、バージョン19.3.1を使用できます。
「python -m pip install --upgrade pip」コマンドによるアップグレードを検討する必要があります。



動作確認

python

※ここでバージョンとプロンプトが表示されること。

import cv2

※ここでエラーが出たらインストールされていない。

exit()



### watchdog

パッケージインストール
pip install watchdog

確認

pip freeze

watchdog==0.9.0

参考

https://qiita.com/gab_km/items/22a5a1b6e871834e816b



### Pillow(PIL)

パッケージインストール
pip install Pillow

確認

pip freeze

Pillow==7.0.0

参考

https://note.nkmk.me/python-pillow-basic/



## 設定

### Visual Studio Code

あらかじめpythonのサンプルコードを用意する。



#### 仮想環境設定

メニュー-[ファイル]-[フォルダーをワークスペースに追加]をクリックする。

サンプルコードのパスを指定する。

※ワークスペースを作らないと、次の基本設定でワークスペースやフォルダの指定ができない。ユーザーのみの設定だとプロジェクトごとに設定変更しないと実行時の仮想環境が前のプロジェクトのもので動作してしまう。



メニュー-[ファイル]-[基本設定]-[設定]をクリックする。

設定の検索にpython.pythonPathと入力する。

ワークスペースを選択する。



値を変更する。

変更前（デフォルト）

python

変更後

仮想環境のパス\\Script



#### lint設定

メニュー-[ファイル]-[基本設定]-[設定]をクリックする。

設定の検索にpython.linting.pylintPathと入力する。

ワークスペースを選択する。



値を変更する。

変更前（デフォルト）

python

変更後

仮想環境のパス\\Script

もしくは以下のファイルでも可。

C:\Users\tani\AppData\Roaming\Code\User

settings.json



#### 動作確認

左ペインの指定したパスの下にあるサンプルコードファイルをダブルクリックして開く。

開いたコードの適当な行番号より左をクリックし、ブレークポイントを付ける。



メニュー-[デバッグ]-[デバッグの開始]をクリックする。

Python Fileを選択する。

Pythonのバージョンを選択する。



フォーカスがブレークポイント行で止まっていることを確認する。

F10キーでステップ実行出来ることを確認する。



参照：

http://blog.livedoor.jp/tmako123-programming/archives/41376213.html

https://qiita.com/syo_nasu/items/ccc5e5cebe5b5d84a99b





Python is not installed. Please download and install Python before using the extension.

Pythonはインストールされていません。拡張機能を使用する前に、Pythonをダウンロードしてインストールしてください。

#### exe出力

pyinstaller (pythonソースファイル).py --onefile --hidden-import sklearn.neighbors.(パッケージ名)

pyinstaller watchdog_test.py --onefile --hidden-import sklearn.neighbors.watchdog