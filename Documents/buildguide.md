# tks4ビルドガイド
## はじめに
![000](https://user-images.githubusercontent.com/58157342/235360931-86d49395-396d-4aa8-b1cb-5759324c4791.jpg)

このたびはご購入いただきありがとうございます。<br>
本製品は組み立てが必要なキットです。<br>

tks4は4キーマクロパッドキットです。<br>
使用するキーキャップすべて1Uになります。<br>

写真は作成見本であり商品内容と同一ではありません。<br>
また仕様は予告なく変更されることがあります。<br>

Boothや遊舎工房など自分が販売または委託している以外での購入されたものに対しての<br>
同梱品の不足や不良品の対応などの各種サポートが厳しいため、<br>
ヤフオク!やメルカリなどのフリマアプリでの転売は禁止しております。<br>
ご理解のほどよろしくお願いいたします<br>

ファームウェアに[qmk_firmware](https://github.com/qmk/qmk_firmware)を採用しています。<br>
QMKにtks4のコードはまだマージされていませんのでこの[ブランチ](https://github.com/kushima8/qmk_firmware/tree/tks4)を使用してください。<br>
動作確認の為の[HEXファイル](https://github.com/kushima8/tks4/tree/main/HEX)を用意しています。<br>

キット作成前にPro Microの書き込み環境の構築を行ってください。<br>
ファームウェアの書き込み環境の構築については下記のサリチル酸さんのサイトを参考にしてください。<br>
[（初心者編）自作キーボードにファームウェアを書き込む](https://salicylic-acid3.hatenablog.com/entry/qmk-toolbox)<br>

キー割り当ての変更方法などはご自身でお調べいただくようお願いします。<br>

GUIから簡単にキー割り当てを変更できる[VIA](https://caniusevia.com/)と[Remap](https://remap-keys.app/)に対応しております。<br>
各種キー割り当ても含めLEDの光度などの設定できますのでご活用ください。<br>
VIAとRemapについては下記のサリチル酸さんのサイトを参考にしてください。<br>
[（初心者編）VIAを使ってキーマップを書き換えよう](https://salicylic-acid3.hatenablog.com/entry/via-manual)<br>
[（初心者編）Remapを使ってキーマップを書き換えよう](https://salicylic-acid3.hatenablog.com/entry/remap-manual)<br>

以下の部品リストを参考に欠品がないか確認をお願いします。<br>

## 部品

### キットに付属しているもの

|名称|数量|備考|
|----|:---:|----|
|PCB|1枚||
|ボトムプレート|1枚|
|M2 7.5mmスペーサー(ARB-2007.5E)|4個|丸型両メネジ|
|M2 4mmネジ|8本|
|ダイオード(1N4148W)|4個|
|タクトスイッチ|1個|

### 別途、購入が必ず必要なもの
以下の部品はキットに付属していない場合、別途購入してください。

|名称|数量|備考|
|----|:---:|----|
|キースイッチ(Cherry MX互換)|4個|
|キーキャップ(Cherry MX互換)|4個|
|Pro Micro|1個|※|
|コンスルーピンヘッダ(3.5mm 12PIN)|2個||

※動作確認しているPro Microは以下の通りになります。  
　下記以外のPro Microを使用する場合は動作しないことがあります。  
　使用する場合はご自身で調整してください。  
　Pro Micro（単体）黒基盤/青基盤  
　https://shop.yushakobo.jp/products/pro-micro?variant=42225070768359

### オプション
以下の部品はオプション品です。  
キーボードを光らせたいなどの場合のみ別途購入してください。

|名称|数量|備考|
|----|:---:|----|
|LEDチップ(YS-SK6812MINI-E)|4個|

### 組み立てに必要な道具
|名称|数量|備考|
|----|:---:|----|
|はんだごて|1台|HAKKO FX600など
|はんだ|1個|goot SE-06008など
|ピンセット|1台|HOZAN P880など
|プリント基板用のフラックス|1本|goot BS-75Bなど
|はんだ吸い取り線|1個|goot CP-3015など
|ドライバー(M2用)|1個|Gグリップドライバー No.990(+00×75) など
  

## 組み立て
* 表面<br>
  ![001](https://user-images.githubusercontent.com/58157342/235360224-d3ab0b6a-ac5e-4151-8779-4350c20a6f92.JPG)
* 裏面<br>
  ![002](https://user-images.githubusercontent.com/58157342/235360225-cf9ded58-cb48-4b82-8174-1075ea0cfe5f.JPG)
* 1.ヤスリがけ
  * 製造の都合上PCBにバリが存在します。
  * 市販されている紙ヤスリなどで研磨してください。
* 2.Pro Microのはんだ付け
  * チップが載っている面が内側になるようにし、コンスルーピンヘッダを取り付けはんだ付けをしてください。
  * コンスルーピンヘッダには取り付け方向があるため気をつけてください。
  * [コンスルー - Self-Made Keyboards in Japan - ](https://scrapbox.io/self-made-kbds-ja/%E3%82%B3%E3%83%B3%E3%82%B9%E3%83%AB%E3%83%BC)<br>
  ![006](https://user-images.githubusercontent.com/58157342/89108152-21b31980-d471-11ea-9df6-11b106120852.JPG)
* 3.ファームウェアの書き込み
  * [tks4_default.hex](https://github.com/kushima8/tks4/tree/main/HEX)を指定してファームウェアを書き込んでください。
* 4.LEDチップのはんだ付け(オプション)
  * 高い温度ではんだ付けを行うとLED破損の可能性がありますので、約270℃に設定してはんだ付けをするようにしてください。
  * 基板裏面のL字のシルクのマークの位置にLEDの足が欠けている箇所が来るように設置し、はんだ付けを行ってください。
  * はんだ付けが完了したら一度Pro Microを取り付け、LEDが光るかどうかテストを行ってください。<br>
  ![007](https://user-images.githubusercontent.com/58157342/235360227-9ae2e79e-8005-4e76-8742-a7096b25e1c3.JPG)
* 5.ダイオードのはんだ付け
  * PCB裏面のダイオード取り付け箇所の片側に予めはんだを盛ります。<br>
  ![009](https://user-images.githubusercontent.com/58157342/235360243-bfc40e10-30d9-4994-87cf-078354c576b4.JPG)
  * その後、線が書いてある方を右(三角形の頂点の先に縦棒がある方)にセットします。
  * ダイオードをピンセットで持ちつつ、予めはんだを盛った箇所をはんだごてで加熱して片側だけはんだ付けを行います。<br>
  ![011](https://user-images.githubusercontent.com/58157342/235360251-b26b8efe-c72d-428e-8cc0-990c22dbf68e.JPG)
  * 片側のはんだ付けが完了後、もう片方もはんだ付けを行ってください。
* 6.タクトスイッチはんだ付け
  * PCB表面から取り付け、裏面からはんだ付けを行ってください。
* 7.キースイッチのはんだ付け
  * PCB前面にキースイッチを配置してください。
  ![011](https://user-images.githubusercontent.com/58157342/235360288-98f008f9-d8a4-4de0-8fba-d6ea96a2dd9f.JPG)
  * マスキングテープなどで仮止めします。
　![032](https://user-images.githubusercontent.com/58157342/235360292-c9b83281-dff0-407e-bba3-ceadd6de76cd.JPG)
  * 裏返してキースイッチの足をはんだ付けしてください。
  ![032](https://user-images.githubusercontent.com/58157342/235360297-13337094-9f2b-4b52-a28d-bc7d27b29fbe.JPG)
  ![032](https://user-images.githubusercontent.com/58157342/235360303-a8471405-7e8c-49c1-8d3b-a353d31c4dd3.JPG)
* 8.Pro Microの取り付け
  * Pro Microを取り付け、PCと接続しREMAPなどを用いてキースイッチの入力の確認を行ってください。
* 9.ボトムプレートの取り付け。
  * スペーサーとボトムプレートのネジ穴の位置を合わせ、M2 4mmネジで固定してください。
* 10.キーキャップの取り付け
  * キースイッチにキーキャップを取り付けてください。

組み立ての手順は、以上です。
