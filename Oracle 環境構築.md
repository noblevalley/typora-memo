# Oracle 環境構築

Windows10 Oracle19

商用データベースサーバー。商用で使用するにはライセンスを購入しないといけないが、「OTNライセンス」によって開発するためだけに使用するのは無償で使用可能。



## インストールフォルダを決める

100GBくらいの空き容量のあるドライブを選択する。

かつ以下の命名で決める。

E:\app\oracle\

ついでにインストールした圧縮ファイルの解凍場所も作成する。

E:\app\oracle\install



## ダウンロード

WINDOWS.X64_193000_db_home.zip

ダウンロードした圧縮ファイルをそのまま解凍せずに圧縮ファイルの解凍場所へ移動する。

7-zipで圧縮ファイル名を付けて解凍する。

E:\app\oracle\install\WINDOWS.X64_193000_db_home

カレントディレクトリを移動する。

## インストール

setup.exe

管理者として実行

![2020-11-26 12_50_11-Oracle Database 19cインストーラ - ステップ1_16](Oracle%20%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89.assets/2020-11-26%2012_50_11-Oracle%20Database%2019c%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%A9%20-%20%E3%82%B9%E3%83%86%E3%83%83%E3%83%971_16.png)

単一インスタンス・データベースを作成および構成します。

を選択

![2020-11-26 12_56_27-Oracle Database 19cインストーラ - ステップ2_15](Oracle%20%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89.assets/2020-11-26%2012_56_27-Oracle%20Database%2019c%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%A9%20-%20%E3%82%B9%E3%83%86%E3%83%83%E3%83%972_15-1606363016538.png)

デスクトップ・クラス

を選択

![2020-11-26 14_06_04-Oracle Database 19cインストーラ - ステップ3_15](Oracle%20%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89.assets/2020-11-26%2014_06_04-Oracle%20Database%2019c%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%A9%20-%20%E3%82%B9%E3%83%86%E3%83%83%E3%83%973_15.png)

仮想アカウントの使用

を選択

![2020-11-30 16_47_21-Oracle Database 19cインストーラ - ステップ4_8](Oracle%20%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89.assets/2020-11-30%2016_47_21-Oracle%20Database%2019c%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%A9%20-%20%E3%82%B9%E3%83%86%E3%83%83%E3%83%974_8.png)

Oracleベース : E:\app\oracle

Software location : E:\app\oracle\install\WINDOWS.64_193000_db_home

データベースファイルの位置 : E:\app\oralce\oradata

データベースエディション : Enterprise Edition

キャラクタ・セット : Unicode (AL32UTF8)

グローバル・データベース : orcl

パスワード : abridge2020

パスワードの推奨される標準は以下の通り

大文字、小文字、数字をそれぞれ1つ以上含める

コンテナ・データベースとして作成 のチェックを外す

※コンテナやプラガブルを作成した方が良いが、旧バージョンとの互換性の為、作成しない構築をしていた。

![2020-11-26 14_09_14-Oracle Database 19cインストーラ](Oracle%20%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89.assets/2020-11-26%2014_09_14-Oracle%20Database%2019c%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%A9.png)

はい



![2020-11-30 16_49_03-Oracle Database 19cインストーラ - ステップ6_8](Oracle%20%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89.assets/2020-11-30%2016_49_03-Oracle%20Database%2019c%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%A9%20-%20%E3%82%B9%E3%83%86%E3%83%83%E3%83%976_8.png)

OraMTSポート番号が49152か49153のいずれかになるか、覚えておく

インストール

![2020-11-26 14_40_15-Oracle Database 19cインストーラ - ステップ8_8](Oracle%20%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89.assets/2020-11-26%2014_40_15-Oracle%20Database%2019c%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%A9%20-%20%E3%82%B9%E3%83%86%E3%83%83%E3%83%978_8.png)

閉じる

## アンインストール

間違った設定でインストールしてしまった場合に実行

管理者権限でコマンドプロンプトを起動

cmd

以下コマンドを実行

E:\app\oracle\install\WINDOWS.X64_193000_db_home\deinstall\deinstall.bat

※ディレクトリ移動せずに絶対パスで指定する

構成解除するすべての単一インスタンス・リスナーを指定してください。すべてを選択解除するにはドット(.)を入力します。[LISTENER]:

と出たら

.

を入力



検出されたリスナー・リスト[LISTENER]の少なくとも1つのリスナーが、指定されたリスナー・リスト[]内にありません。Oracleホー ムはクリーンアップされるため、構成解除後はすべてのリスナーが使用できなくなります。特定のリスナーを削除するには、かわりにOracle Net Configuration Assistantを使用してください。続行しますか。(y|n) [n]:

と出たら

y

を入力



値のリストを入力として指定する場合、セパレータとしてカンマを使用してください

このOracleホームで構成されているデータベース名のリストを指定してください [ORCL]:



未入力のままEnter



データベース'ORCL'

単一インスタンス・データベース
データベースの診断先の場所: E:\APP\ORACLE\diag\rdbms\orcl
データベースによって使用される記憶域タイプ: FS
データベース・ファイルの場所: E:\APP\ORACLE\ORADATA\ORCL
高速リカバリ領域の場所: 存在しません
データベースのspfileの場所: E:\INSTALL\WINDOWS.X64_193000_DB_HOME\DATABASE\SPFILEORCL.ORA

データベースORCLの詳細は自動的に検出されました。ORCLデータベースの詳細を変更しますか。 [n]:



未入力のままEnter



データベース・チェック構成END

######################### DECONFIG CHECK OPERATION END #########################

####################### DECONFIG CHECK OPERATION SUMMARY #######################
削除対象として選択されたOracleホーム: E:\install\WINDOWS.X64_193000_db_home
Oracleホームが登録されているインベントリの場所: C:\Program Files\Oracle\Inventory
次のWindowsおよび.NET製品は、Oracleホームから構成解除されます。 oledbolap,ode.net,ntoledb,oramts,asp.net,odp.net
次のデータベースが構成解除対象として選択されました。構成解除されると、データベースは削除されて使用できなくなります: ORCL
一意のデータベース名: ORCL
使用済記憶域: FS
続行しますか (y - はい、n - いいえ) [n]:



y



このセッションのログはC:\Users\tani\logs\deinstall_deconfig2020-11-30_03-55-01-PM.outに書き込まれます
このセッションのすべてのエラー・メッセージはC:\Users\tani\logs\deinstall_deconfig2020-11-30_03-55-01-PM.errに書き込まれ ます

######################## DECONFIG CLEAN OPERATION START ########################
データベース構成解除トレース・ファイルの場所: C:\Users\tani\logs\databasedc_clean2020-11-30_03-55-01PM.log
データベース・クリーンアップ構成START ORCL
この操作には数分かかります。



--

間違い

--

C:\WINDOWS\system32>E:\install\WINDOWS.X64_193000_db_home\deinstall\deinstall.bat
Checking for required files and bootstrapping ...
Please wait ...
        1 個のファイルをコピーしました。
        1 個のファイルをコピーしました。
        1 個のファイルをコピーしました。
        1 個のファイルをコピーしました。
ログの場所C:\Users\tani\logs\

############ ORACLE DECONFIG TOOL START ############


######################### DECONFIG CHECK OPERATION START #########################
## [開始] インストールの構成確認 ##

Oracleホームの場所が存在するかどうかを確認しています E:\install\WINDOWS.X64_193000_db_home
選択された削除対象のOracleホームのタイプ: Oracle単一インスタンス・データベース
選択された削除対象のOracleベース: E:\app\oracle
中央インベントリの場所が存在するかどうかを確認しています C:\Program Files\Oracle\Inventory

## [終了] インストールの構成確認 ##

## [開始] Windowsおよび.NET製品の構成チェック ##


次のWindowsおよび.NET製品は、Oracleホームから構成解除されます。 oledbolap,ode.net,ntoledb,oramts,asp.net,odp.net

## [終了] Windowsおよび.NET製品の構成チェック ##


ネットワーク構成チェック構成START

ネットワーク構成解除トレース・ファイルの場所: C:\Users\tani\logs\netdc_check2020-11-30_04-18-22PM.log

ネットワーク構成チェック構成END

データベース・チェック構成START

データベース構成解除トレース・ファイルの場所: C:\Users\tani\logs\databasedc_check2020-11-30_04-18-22PM.log

値のリストを入力として指定する場合、セパレータとしてカンマを使用してください

このOracleホームで構成されているデータベース名のリストを指定してください [ORCL]:

###### データベース'ORCL' ######

このデータベース(1.単一インスタンス・データベース|2.Oracle Restart対応のデータベース)のタイプを指定してください [1]: 1
データベースの診断先の場所を指定してください [E:\app\oracle\diag\rdbms\orcl]:
データベースASM|FSによって使用される記憶域タイプを指定してください []:
データベースASM|FSによって使用される記憶域タイプを指定してください []:
データベースASM|FSによって使用される記憶域タイプを指定してください []:
データベースASM|FSによって使用される記憶域タイプを指定してください []: fs
データベースASM|FSによって使用される記憶域タイプを指定してください []: FS

共有ファイルシステムにデータベース・ファイルが存在する場合、ディレクトリのリストを指定してください。'ORCL'サブディレクトリが見つかった場合、これが削除されます。見つからなかった場合、指定したディレクトリが削除されます。また、フルパスを使用してデータベース・ファイルのリストを指定できます [ ]:

高速リカバリ領域がファイルシステムで構成されている場合、これを指定してください。'ORCL'サブディレクトリが見つかった場合、これが削除されます。 []:

データベースのspfileの場所を指定してください [ ]:

データベース・アーカイブ・モードが有効かどうかを指定します。y/n [n]: y
データベース・チェック構成END

######################### DECONFIG CHECK OPERATION END #########################


####################### DECONFIG CHECK OPERATION SUMMARY #######################
削除対象として選択されたOracleホーム: E:\install\WINDOWS.X64_193000_db_home
Oracleホームが登録されているインベントリの場所: C:\Program Files\Oracle\Inventory
次のWindowsおよび.NET製品は、Oracleホームから構成解除されます。 oledbolap,ode.net,ntoledb,oramts,asp.net,odp.net
次のデータベースが構成解除対象として選択されました。構成解除されると、データベースは削除されて使用できなくなります: ORCL
一意のデータベース名: ORCL
使用済記憶域: FS
続行しますか (y - はい、n - いいえ) [n]: y
このセッションのログはC:\Users\tani\logs\deinstall_deconfig2020-11-30_04-18-21-PM.outに書き込まれます
このセッションのすべてのエラー・メッセージはC:\Users\tani\logs\deinstall_deconfig2020-11-30_04-18-21-PM.errに書き込まれ ます

######################## DECONFIG CLEAN OPERATION START ########################
データベース構成解除トレース・ファイルの場所: C:\Users\tani\logs\databasedc_clean2020-11-30_04-18-22PM.log
データベース・クリーンアップ構成START ORCL
この操作には数分かかります。
データベース・クリーンアップ構成END ORCL

ネットワーク構成クリーニング構成START

ネットワーク構成解除トレース・ファイルの場所: C:\Users\tani\logs\netdc_clean2020-11-30_04-18-22PM.log

バックアップ・ファイルの構成解除中です...
バックアップ・ファイルが正常に構成解除されました。

ネットワーク構成が正常にクリーンアップされました。

ネットワーク構成クリーニング構成END

## [開始] Windowsおよび.NET製品の構成削除 ##


## [終了] Windowsおよび.NET製品の構成削除 ##
## [開始] Oracleホーム・ユーザーの構成を削除 ##

Removing ORA_OraDB19Home1_SVCACCTS from system specific groups
Removing home specific groups.
Removing group ORA_OraDB19Home1_OPER
Removing group ORA_OraDB19Home1_DBA
Removing group ORA_OraDB19Home1_SYSBACKUP
Removing group ORA_OraDB19Home1_SYSDG
Removing group ORA_OraDB19Home1_SYSKM
Removing group ORA_OraDB19Home1_SVCSIDS
Removing group ORA_OraDB19Home1_SVCACCTS
Removing Oracle Groups from system
Removing group ORA_OPER
Removing group ORA_DBA
Removing group ORA_INSTALL
Removing group ORA_GRID_LISTENERS
Removing group ORA_ASMADMIN
Removing group ORA_ASMDBA
Removing group ORA_ASMOPER
Removing group ORA_CLIENT_LISTENERS
Removing group ORA_CRS_USERS
Removing group ORA_RAC
Removing group ORA_DBSVCACCTS

## [終了] Oracleホーム・ユーザーの構成を削除 ##

######################### DECONFIG CLEAN OPERATION END #########################


####################### DECONFIG CLEAN OPERATION SUMMARY #######################
次のデータベース・インスタンスが正常に構成解除されました: ORCL
Removed oledbolap configuration
Removed ode.net configuration
Removed ntoledb configuration
Removed oramts configuration
Removed asp.net configuration
Removed odp.net configuration
#######################################################################


############# ORACLE DECONFIG TOOL END #############

プロパティ・ファイルC:\Users\tani\AppData\Local\Temp\deinstall2020-11-30_04-17-55PM\response\deinstall_2020-11-30_04-18-21-PM.rspを使用しています
ログの場所C:\Users\tani\logs\

############ ORACLE DEINSTALL TOOL START ############





####################### DEINSTALL CHECK OPERATION SUMMARY #######################
このセッションのログはC:\Users\tani\logs\deinstall_deconfig2020-11-30_04-18-21-PM.outに書き込まれます
このセッションのすべてのエラー・メッセージはC:\Users\tani\logs\deinstall_deconfig2020-11-30_04-18-21-PM.errに書き込まれ ます

######################## DEINSTALL CLEAN OPERATION START ########################
## [開始] 削除の準備 ##
LOCAL_NODEをDT-4に設定しています
CRS_HOMEをfalseに設定しています
oracle.installer.localをfalseに設定しています

## [終了] 削除の準備 ##

Setting the force flag to false
Setting the force flag to cleanup the Oracle Base
Oracle Universal Installerクリーンアップの開始

ローカル・ノードのサービス'OracleOraDB19Home1TNSListener'を停止中 : 終了

ローカル・ノードのサービス'OracleOraDB19Home1TNSListener'を削除中 : 終了

Oracleホーム'E:\install\WINDOWS.X64_193000_db_home'をローカル・ノードの中央インベントリからデタッチします : 終了

ローカル・ノードのディレクトリ'E:\install\WINDOWS.X64_193000_db_home'を削除します : 終了

ローカル・ノードのディレクトリ'C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Oracle - OraDB19Home1'を削除します : 終了

ローカル・ノードのPATH変数からOracleホーム'E:\install\WINDOWS.X64_193000_db_home'を削除中 : 終了


## [開始] Oracleインストール・クリーンアップ ##


## [終了] Oracleインストール・クリーンアップ ##


######################### DEINSTALL CLEAN OPERATION END #########################

####################### DEINSTALL CLEAN OPERATION SUMMARY #######################
ローカル・ノードのサービス'OracleOraDB19Home1TNSListener'が正常に停止されました。
ローカル・ノードのサービス'OracleOraDB19Home1TNSListener'が正常に削除されました。
Oracleホーム'E:\install\WINDOWS.X64_193000_db_home'がローカル・ノードの中央インベントリから正常にデタッチされました。
ローカル・ノードのディレクトリ'E:\install\WINDOWS.X64_193000_db_home'が正常に削除されました。
ローカル・ノードのディレクトリ'C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Oracle - OraDB19Home1'が正常に削除されました。
ローカル・ノードのPATH変数からOracleホーム'E:\install\WINDOWS.X64_193000_db_home'が正常に削除されました。
ローカル・ノードのディレクトリ'C:\Program Files\Oracle\Inventory'が正常に削除されました。
ローカル・ノードのレジストリ・キー'HKEY_LOCAL_MACHINE\Software\Oracle\inst_loc'が正常に削除されました。
ローカル・ノードのレジストリ・キー'HKEY_LOCAL_MACHINE\Software\\Oracle\\ODP.NET'が正常に削除されました。
ローカル・ノードのレジストリ・キー'HKEY_LOCAL_MACHINE\Software\\Oracle\\ODP.NET.Managed'が正常に削除されました。
Oracle Universal Installerのクリーンアップが成功しました。

ノード'DT-4'上の'E:\app\oracle'の権限およびコンテンツを確認します。
'E:\app\oracle'に関連付けられたOracleホームがない場合、'E:\app\oracle'およびそのコンテンツを手動で削除します。
Oracle削除ツールによって一時ディレクトリが正常にクリーンアップされました。
#######################################################################

############# ORACLE DEINSTALL TOOL END #############



スタートボタンをクリックし、Oracleがなくなっていることを確認



## パッチ適用

環境変数を定義

ORACLE_HOME

E:\app\oracle\install\WINDOWS.X64_193000_db_home

Path

%ORACLE_HOME%\OPatch



コマンドプロンプトを管理者権限で起動



以下のコマンドを実行

opatch lsinventory

コマンドが認識されてオプション出力されることを確認

インストールされた最上位製品(1):

Oracle Database 19c                                                  19.0.0.0.0
このOracleホームには1の製品がインストールされています。

このOracleホームには仮パッチがインストールされていません。



サービスを起動

「ora」と付くサービスを停止する



パッチファイルを解凍

※本来は製品版を購入しOracle Support IDを入手しないと手に入らない。お客様から頂いた。

p30901317_190000_MSWIN-x86-64.zip



コマンドプロンプトで解凍したフォルダへ移動

cd /d

dir

README.htmlファイルが直下にある事を確認



以下のコマンドを実行

opatch apply

パッチが適用されることを確認



OSを再起動



コマンドプロンプトを起動



sqlplus を実行

バージョンが19.7になっている事を確認



参考

https://docs.oracle.com/cd/E26854_01/doc.121/e49737/patch_application.htm





## Oracle設定構築

### ログイン

コマンドプロンプトを起動

以下コマンドを実行

sqlplus

ユーザー名を入力してくださいと出たら以下を入力

sys/abridge2020 as sysdba

SQL> プロンプトが出る事を確認



### ブロック・サイズを変更

show parameter db_16k_cache_size
0になっている事を確認

alter system set db_16k_cache_size = 16777216;



### 表領域作成

CREATE TABLESPACE USER10
DATAFILE 'E:\app\oracle\MVBASE\MVBASE_data\USER10.dbf' SIZE 60G REUSE AUTOEXTEND ON MAXSIZE UNLIMITED
LOGGING
ONLINE
BLOCKSIZE 16K
EXTENT MANAGEMENT LOCAL AUTOALLOCATE
SEGMENT SPACE MANAGEMENT AUTO
/

しばらく待つ

表領域が作成されました。
と出たらOK



### ユーザー作成

CREATE USER MVBASE IDENTIFIED BY MVBASE
DEFAULT TABLESPACE USER10
TEMPORARY TABLESPACE TEMP
PROFILE DEFAULT;

ユーザーが作成されました。
と出たらOK



GRANT CONNECT TO MVBASE;
GRANT CTXAPP TO MVBASE;
GRANT EXP_FULL_DATABASE TO MVBASE;
GRANT IMP_FULL_DATABASE TO MVBASE;
GRANT RESOURCE TO MVBASE;
GRANT CREATE MATERIALIZED VIEW TO MVBASE WITH ADMIN OPTION;
GRANT EXPORT FULL DATABASE TO MVBASE;
GRANT IMPORT FULL DATABASE TO MVBASE;
GRANT UNLIMITED TABLESPACE TO MVBASE;
ALTER USER MVBASE QUOTA UNLIMITED ON USER10;
GRANT IMP_FULL_DATABASE TO MVBASE;
grant write on directory DATA_PUMP_DIR to MVBASE;
grant READ on directory DATA_PUMP_DIR to MVBASE;
GRANT IMP_FULL_DATABASE TO MVBASE;

CREATE OR REPLACE DIRECTORY DATA_PUMP_DIR AS 'E:\app\oracle\install\20201126_bri';

grant write on directory DATA_PUMP_DIR to MVBASE;
grant READ on directory DATA_PUMP_DIR to MVBASE;







## インポート

以下のファイルを元にインポート処理を行う。

20201126_bri.tgz

解凍

20201126_bri.dmp ファイルができる事を確認



あらかじめフォルダ作成
E:\app\oracle\MVBASE\MVBASE_data\



コマンドプロンプトを起動する。

cd /d E:\app\oracle\install\20201126_bri

impdp MVBASE/MVBASE parfile='para_in_sgmvuser.txt'