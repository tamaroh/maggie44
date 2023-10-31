# maggie44
maggie42はTamarohが初めて作成した試作カスタムキーボードです。
- 左右対象、分割、カラムスタッガード
- 自然にハの字に手が配置される
- 傾けないレイアウトでキーの隙間がない
- 小指から弧を描く配列
- Pro Microに対応
- All 1Uレイアウト
## キーマップ
![keymap](./mysplit.png)
## 必要なもの
|品名|数量|備考|入手先|
|----|----|----|----|
|PCB|2枚|左右別々のデータです<br>ver1.0は一部配線の修正が必要です|当レポ内のデータから作成してください
|キープレート|2枚|左右どちらでも使えます|当レポ内のデータから作成してください
|ボトムプレート|2枚||当レポ内のデータから作成してください
|M2ネジ 4mm|20本|ボトムプレートの暑さによって長さは異なります|遊舎工房など
|M2スペーサー 7mm|10個||遊舎工房など
|Pro Micro|2個|すべての互換品については動作を保障しません*|遊舎工房など
|ピンヘッダー|12Pin x 4個|コンスルー対応|遊舎工房など
|タクトスイッチ|2個||遊舎工房など
|TRRSジャック|2個||遊舎工房など
|USBケーブル|1本||遊舎工房など
|TRRSケーブル|1本|TRSでも代用可|遊舎工房など
|ダイオード|44個|SMD/スルーホール対応|遊舎工房など
|キーソケット|44個|Cherry MX互換のみ対応|遊舎工房など
|キースイッチ|44個|Cherry MX互換のみ対応|遊舎工房など
|キーキャップ|セット|すべて1Uです|遊舎工房など

* 厚さの異なるPro Micro互換品（USB-Cコネクタのタイプ）などの場合、コンスルーでは動作を保障できません。
  確実に接続できるピンヘッダ接続をおすすめします。

## 必要な工具
- はんだごて
- コテ台、コテ先クリーナー
- はんだ
- 精密ドライバー
- ピンセット

## 必要なソフトウェア
- [qmk toolbox](https://github.com/qmk/qmk_toolbox/releases)

## 制作手順
手順は人により異なりますが、最初に動作確認をお勧めします。
1. Pro Microにファームウェアを書き込みます。
  - QMK Toolboxを起動し、書き込むファームウェア（下記参照）を選択しておきます。
  - USBをPCに接続して、リセットスイッチを押します。
  - 書き込み可能状態になったら、Flashボタンをクリックして書き込みます。
  - 書き込みが完了したらUSBケーブルを接続し直します。
  - 二つのPro Micro両方とも同じファームウェアを書き込んでください。
2. ダイオードを半田付けします。SMDの場合縦線が入っている方の端子、スルーホールの場合黒い線がある方の端子を、基板上の縦線がある側に接続してください。
3. （Ver.1.0の基板のみ）つながっていないシルクを、銅線などで半田付けしてつなぎます。
4. Pro Microを用意します。
   コンスルーを使用する場合は基板に差し込んでから、適切にPro Microに半田付けしてください。
   ピンヘッダを使用する場合は向きや表裏を間違えないようにします。
   ※USB-Cタイプなど、USBコネクタ部の場合はピンヘッダの高さが合わなかったり、コンスルーが抜けやすくなる可能性があります。
5. ソケットを半田するランドをピンセットなどで導通させて、信号に問題がないことを確認します。
6. ソケットを半田付けします。シルク印刷に合わせて、スイッチの穴を塞がないようにします。
7. TRRSジャック、リセットスイッチを半田付けします。
8. キースイッチを4個程度、先にキープレートに差し込みます。
9. 基板と接続します。スイッチのピンが曲がらないように上からまっすぐ抑えます。
10. 残りのスイッチを差し込みます。ソケットとスイッチを指で挟み込むようにして、ソケットに確実に差し込みます。
11. PCBとキースイッチを接続します。
12. キーキャップを乗せます。
13. 左右のキーボードをTRRSケーブルで接続します。
14. できあがり

## ファームウェアについて
ファームウェアは以下にあります。
https://github.com/tamaroh/maggie44/tree/main/firmware
|種別|ファイル名|備考
|----|----|----|
|QMK|maggie44_default.hex|VIA有効|
|VIA|maggie44_via.json|VIAでキーマップ設定時に使用してください|

ソースコードはこちら：https://github.com/tamaroh/qmk_firmware/tree/tamaroh/keyboards/maggie44
## 注意事項
- 自作キーボードについての知識がある方を対象としています。
- 非販売品につき、サポートは対象外としております。

