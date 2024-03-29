水やり機自作キットAB001 サポートページ

## 概要
KOSHINの電池式灯油ポンプ[EP-105](https://www.koshin-ltd.jp/products/1144.html)の内部にハンダ付け不要で組み込み可能な超小型 wifi コントローラー ボードです。スマホで予約が可能なタイマー式水やり機として使うことができます(**改造により灯油ポンプはメーカー保証対象外となります。自己責任でお願いします！**)。

- ベランダ菜園など、電源や水道がない場所でも使えます
- 単三電池２本を使用します（ニッケル水素充電池可）
- 数日から数週間程度の間の水やりに適します
- 水やりの時刻は1時間刻みで複数時刻に設定できます
- 時差は1日あたり15秒程度は発生するようです
- マイコン（ESP32）に詳しい方はご自分でプログラムを書き換えて単なるwifiコントローラーとして使うことも可能です。詳しくは[回路図](https://github.com/aobato/ab001/blob/master/circuite/touyu_pomp.pdf)および基盤のシルクをご覧ください。

## 注意事項
- このキットは個人がDIYを楽しむために開発したものです。植物が枯れた！などの保証には応じられません。絶対に枯らせたくない植物への水やりは人間に頼みましょう
- 組み込みには手先の器用さが必要です
- 灯油ポンプ（EP-105）を給水に使うことはメーカーは推奨していないため、錆などで故障するかもしれません
- 改造によって灯油ポンプはメーカー保証対象外となります

## 準備するもの
1. KOSHINの電池式灯油ポンプ[EP-105](https://www.koshin-ltd.jp/products/1144.html)
2. 単三電池２本（ニッケル水素充電池でも可）
3. ニッパー
4. カッターまたはワイヤーストリッパー（ビニール被覆を剥くのに使用）
5. プラスおよびマイナスドライバー
6. ピンセット
7. １５ｃｍ以上の結束バンドとアルミホイルがあるとプランターへの水やりに便利です

## 灯油ポンプへの組み込みかた
1. (**電池ケースの分解**) 灯油ポンプのスライドスイッチをオフにし、電池ケースをあけて中に電池が入っているようなら外に出します。電池ケースの内側にあるプラスチックのツメと壁のすきまにマイナスドライバーの先を当てます。ドライバーの柄の部分を壁側にあてテコの原理の要領ですきまを広げてツメを外し、電池ケースを二つに分解します。スライドスイッチのついていない方のケースはわきによけておきます。

![IMG_20190630_111006](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_111006.jpg)

![IMG_20190630_111028](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_111028.jpg)

![IMG_20190630_111040](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_111040.jpg)

2. (**電源ケーブルの切断**) ポンプとホースとが一体化した部品と、電池ケースとが２本の電源ケーブルでつながっているのがわかります。ポンプ側の部品から出たケーブルが二本にわかれた部分から1.2センチ程度はなれた場所をニッパーで切断します。切断したケーブルのビニール被覆をカッターナイフやワイヤーストリッパーなどで3ミリほど剥いておきます。切り離されたポンプ側の部分はわきによけておきます。

![IMG_20190630_111109](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_111109.jpg)

![IMG_20190630_111113](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_111113.jpg)

3. (**内部の突起の除去**)　写真をみながら電池ケース部分の右下にあるプラスチックの突起部分を二つともニッパーで切り取ります。

![IMG_20190630_112842](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_112842.jpg)

![IMG_20190630_112859](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_112859.jpg)

![IMG_20190630_112928](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_112928.jpg)

4. (**電池ボックス側ケーブルの接続**) wifiコントローラー ボードの４つのスクリューターミナルをプラスドライバーをつかってあらかじめ緩めておきます。電池ボックスのスイッチ側（電池はマイナス）から伸びているケーブルの露出された導線の先を、下の写真（や基盤のシルク）をよく見ながらスクリューターミナルへピンセットをつかって差し込み、プラスドライバーでスクリューを締め付けて固定します。つぎに電池ボックスのプラス側から出ているケーブルの先を、同じブロックの残りのターミナルの穴に同様の手順でとりつけます。固定したケーブルをピンセットでしっかり引っ張っても外れないかどうか確認します。（★***ケーブルとその取付先コネクターの位置を間違えないでください。間違ったつなぎ方をすると回路が壊れます***★）

![IMG_20190630_113048](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_113048.jpg)

![IMG_20190630_113029](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_113029.jpg)

![IMG_20190630_113100](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_113100.jpg)

![IMG_20190630_113319](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_113319.jpg)

5. (**ポンプ側ケーブルの接続**) わきによけておいたポンプとホースが一体化した部品を手にとり、写真をよく見てとなり会うスクリューターミナルの内側同士が同じ色のケーブルになるよう注意して、ポンプ側から出ているケーブルを同様の手順で固定します。写真（と基盤シルク）をよく見ながら、４本のケーブルが正しいターミナルに接続されているかどうかを再確認してください。（★***くどいですが、間違ったつなぎ方をすると回路が壊れます***★）

![IMG_20190630_113627](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_113627.jpg)

6. (**各部品の位置合わせ**) ケーブルに無理な力が入らないように注意しながら、ポンプとホースが一体化した部品をもとあったように電池ボックスの末端部にはめこみます。収まったら、写真のようにボードから出ている黒い薄い板（ESP32のアンテナ板）の位置が電池ボックスとは反対側になるようにwifiコントローラーを位置を合わせて、指で押さえます。

![IMG_20190630_113649](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_113649.jpg)

![IMG_20190630_113703](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_113703.jpg)

![IMG_20190630_113719](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_113719.jpg)

7. (**各部品のはめ込み**) わきによけてあった分解された電池ボックスの部品を上からかぶせます。wifiコントローラー全体がケース内に収まるように指などで調整しながら、ゆっくりとカバー全体を押し付けてカチッと音がするまではめ込みます。

![IMG_20190630_113741](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_113741.jpg)

![IMG_20190630_113749](https://github.com/aobato/ab001/blob/master/img/IMG_20190630_113749.jpg)

8. (**電池の挿入**) スイッチをオフにした状態で、正しい向きに電池を入れます（★***電池の向きを間違えると回路が壊れます***★）。電池ボックスのフタを閉じれば完成です。付属のシールにスマホからの接続方法が書かれているので、ポンプの取っ手部分に張り付けておくと便利です。

## タイマー設定の仕方
1. ポンプ本体のスライド スイッチをオンにします
2. スマホの設定を開き、モバイルデータ通信をオフにします
3. スマホのwifi設定を開き、"ESP32-WiFi"というアクセスポイントに接続します
4. スマホのブラウザを起動します（付属シールのQRコードを読み取ってもかまいません）
5. 以下のurlを開きます（付属シールのQRコードを読み取ってもかまいません）
http://192.168.0.2/
6. 「水やり設定」という画面が開くので、あとは指示に従って設定を行います。タイマー作動中は一定間隔でLEDが点滅します。LEDが点滅しなくなったら電池切れです。
7. スマホの設定を開き、モバイルデータ通信をオンにもどします
8. 使い終わないときは電池の液漏れを防ぐため電池は抜いてください。また、ポンプは錆びをさけるためにしっかり乾燥させることをお勧めします。

## 水やりのコツ
- プランターの中に適当に穴をあけたアルミホイルを敷き、その上に水を出すようにすると水が全体に行き渡りやすくなります　
- ポンプのホースの先に２本の結束バンドを切らずにVの字型に取り付け、あまった先を土にしっかり差し込んでおくと、水が出る勢いでポンプのホースが動いてしまうことを防げます。
- 水やりの際にポンプのホースの先がたまった水の中に完全に浸かってしまうと、サイフォンの原理でせっかく注水した水が逆流してしまうことがあります。ホースの先はやや空中に浮くように固定した方がよいでしょう。
- 電池がどれくらい持つのかは給水時間や使用する電池によって変わります。必要な期間だけ水やりが持続するかどうかを旅行などの本番前に実験してみることをお勧めします。　

## 回路図
 回路図はこの[リンク](https://github.com/aobato/ab001/blob/master/circuite/touyu_pomp.pdf)です。特徴は以下の通り。
- ポンプ本体の単三電池二本を3.3Vに昇圧
- ポンプのオンオフにはパワーFETを使用
- タイマー作動中の電源確認用のLEDを表面と裏面に実装
- スクリューターミナルの使用によりはんだ付け不要
- プログラム書き込み用スルーホール（GND,EN,RX,TX,3V3,IO0）あり
- 基板上のY1（32.768Khzクリスタル）、C11、C12、R7は実装してありません。自作派の方はY1のスルーホールをGPIO32,GPIO33として使ってみてはいかがでしょうか。

## プログラム
arduino IDEで開発しています。主な工夫は以下の通り。
- ソフトウェア アクセスポイント機能によりスタンドアロンでスマホと接続可能
- タイマー動作中はディープスリープで省電力化
- ディープスリープ中もULPによりLEDを点滅させ動作確認が可能
- PWMでチャージポンプを駆動することでFETに十分なゲート電圧を供給

ソースコードは[こちら](https://github.com/aobato/ab001/blob/master/arduino/ab001)。コンパイルには、
[Arduino core for ESP32 WiFi chip](https://github.com/espressif/arduino-esp32)
[ESP32 Filesystem Uploader](https://randomnerdtutorials.com/install-esp32-filesystem-uploader-arduino-ide/)
[ESPAsyncWebServer](https://github.com/me-no-dev/ESPAsyncWebServer)
[ulptool v2.3.0](https://github.com/duff2013/ulptool)
のインストールが必要です。(たぶんpythonを2.7インストールしてpathが通っていないと動きません。)

## 書き込み回路
興味のある方は[このあたり](https://ht-deko.com/arduino/esp-wroom-02.html#13_08)を参考にして作ってください。追加としてENTとGNDの間に10uFの電解コンデンサを入れた方が自動リセットが安定すると思います。このとき、基盤自体に３V電源をつけないと書き込みできません。なお書き込み用スルーホールにソケットやピンコネクタをはんだ付けしてしまうと灯油ポンプの内部に入りきれなくなってしまいます。[スルホール用テストワイヤ](http://akizukidenshi.com/catalog/g/gC-09830/)などを使ってください。

## コメントや連絡先
歓迎します。みなさまの使用体験を共有したいので、githubアカウントをお持ちの方はissueページへ書き込みをお願いします。アカウントをお持ちでない方はromanpot95＠gmail.comへどうぞ。