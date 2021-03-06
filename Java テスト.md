# Java テスト

## 概要

プログラムにエラーなど動作に支障がないか検証することです。

エラーが出るたびプログラムが強制終了したり、ハングアップして操作不能になってしまうと、品質が良くないということになってせっかく作成したプログラムが使用されなくなってしまいます。

プログラムを作成したらテストを行い、良い品質のプログラムを目指しましょう。

## 種類

システムの規模や環境によっては色々と種類があります。画面単位の大きな規模から入力項目の小さな規模へと下るように種類を説明します。

画面単位で分けると、「結合テスト」と「単体テスト」の2種類あります。

### 結合テスト

既に出来上がった画面を元に画面遷移がうまく行くか、前後の画面間でデータの受け渡しがうまくいっているかどうかを検証します。

### 単体テスト

1画面もしくは1機能単体の機能が仕様通りの機能を満たしているかを検証します。本来はJavaでいうところの1クラス単体のテストを指しますが、フレームワークで開発することが多く、実際にチームで開発する時も画面単位、機能単位で作成することが多いので、1画面もしくは1機能単位のテストと考えて差し支えないと思います。

単体テストを更に細かく分けると、「相関チェック」と「単項目チェック」の2種類あります。

#### 相関チェック

複数の入力項目が論理的に正しいかを検証します。

例えば開始日と終了日という入力項目があるとして、開始日が終了日より未来の日付になっていると動作として矛盾してしまいます。

こちらはif文等の分岐処理で実装することが多いです。

#### 単項目チェック

入力項目単体で正しく入力されているかを検証します。

テキストボックスやオプションボタンなどのUIによって色々と種類がありますが、大まかには「必須チェック」と「属性チェック」と「範囲チェック」の3種類が良く実装されています。

必須チェック：必ず入力されていることを検証します。

属性チェック：数字や文字といった決まった属性になっているかを検証します。

範囲チェック：下限値もしくは上限値を超えていないかを検証します。

これらの検証はフレームワークでは「validation（バリデーション）」という機能を使用することが多いです。良く知らないと相関チェックと同様にif文で1から記述しがちですが、まずはフレームワークでこの機能が搭載されているかを確認しましょう。

フレームワークはコーディングやテストを楽にするためにありますので、出来れば積極的に取り入れていきましょう。

