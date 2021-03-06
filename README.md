﻿## スクリーンリーダーNVDAのLiblouisで日本語を六点漢字または漢点字(6点式)で表示するためのテーブルファイル

### NVDAで六点漢字または漢点字(6点式)を表示させる設定

ここには下記の2つのliblouis用テーブルファイルがあります。

* ja-rokutenkanji.utb - 六点漢字で表示するためのファイル
* ja-kantenji6dot.utb - 漢点字で表示するためのファイル(ただし8点式ではなく、6の点と2 3の点で囲む形の6点式で表したもの)

githubのページの中の「Clone or download」ボタンを押して、「Download ZIP」でダウンロードすることができます。

このファイルを使ってスクリーンリーダーNVDAで点字の漢字を点字ディスプレイに表示するには次のようにします。

たとえばNVDAの設定の点字の出力テーブルで「統一英語点字1級」を選んだときに日本語を六点漢字で表示するには次のような操作をします。

1. ja-rokutenkanji.utbをNVDAのインストールフォルダ内のlouisの中のtablesフォルダにコピーします。(管理者権限でないとコピーできません)
2. 同じくtablesフォルダ内のen-ueb-g1.ctbファイルの「include en-ueb-math.ctb」の行の下に「include ja-rokutenkanji.utb」と書いた行を追加して上書き保存します(元のファイルはバックアップしておいてください)。
3. NVDAを再起動して、出力テーブルを「統一英語点字1級」に設定すると、六点漢字が表示されます。

漢点字(6点式)で表示したい場合は、上記の「ja-rokutenkanji.utb」の代わりに「ja-kantenji6dot.utb」にします。

また、出力テーブルの「アメリカ英語1級点字」に漢点字(6点式)を追加したい場合は、tablesフォルダの「en-us-g1.ctb」ファイルの一番最後の行に、「include ja-kantenji6dot.utb」の行を追加します。

「統一英語」に六点漢字、「アメリカ英語」に漢点字と設定しておくと、NVDAの点字設定の出力テーブルで「統一英語」か「アメリカ英語」を切り替えることで、六点漢字/漢点字の切り替えができます。

また1級点字にincludeしておくと、2級点字の方では1級点字のファイルがincludeされているので、2級点字を選んでも六点漢字や漢点字表示が有効になっています。

### 著作権について

日本語の漢字を表す点字は2種類の方式が考案されています。

長谷川貞夫氏による「六点漢字」と、川上泰一氏による「漢点字」です。

「六点漢字」はコンピュータで漢字を入力するために考えられたもので、「漢点字」は点字で漢字を読むために考えられたものです。

これらの漢字の点字に関する著作権はそれぞれの方に帰属します。

私がここに作成しているデータは個人的学習のためのものです。

私が作成している部分については、作者の表示をせずに、どのような形で使用してもかまいませんが、その結果について私は責任を負いません。

仕様する際は自己責任でお願いします。

### 点字の漢字「六点漢字」と「漢点字」について

日本点字は分かち書きされた仮名だけで書かれたもので、漢字は使われていませんが、点字で漢字を表す方式として「六点漢字」と「漢点字」の２つがあります。

六点漢字は主に音読み+訓読みのペアで１つの漢字を記号にしたものです。

たとえば「山」という漢字は「サン」という音読みと「やま」という訓読みの「や」を組み合わせて「サン+や」で表します。

同じように「川」は「セン+か」、「新」は「シン+あ」などとなります。

ただし音読みの部分は仮名と区別するための漢字符号を兼ねて、仮名点字とは異なる書き方になっています。

たとえば「サン」という音読みは「4 5 6の点+サ⠸⠱」、「セン」は「4 5 6の点+セ⠸⠻」、他にも「2 6の点+ア」で「アツ」、「2 6の点+カ」で「カツ」という音読みになります。

もう一つの「漢点字」では、主に部首の組み合わせで1つの漢字を表します。

たとえば「木」という漢字は仮名点字の「き⠣」で表され、「目」という漢字は仮名点字の「め⠿」で表されます。

そしてこの２つの組み合わせでできている「相」は「きめ⠣⠿」で表されます。

「田」は「た⠕」で、「力」は「ぬ⠍」、そして「男」は「たぬ⠕⠍」などです。

ただし漢点字では仮名と区別するための漢字符号を点字6点の上に点を付ける形で表します。

たとえば仮名点字の「き」は「1 2 6の点⠣」ですが、漢字の「木」は「1 2 6の点の上に0の点と7の点⢏」となります。

「相」は「きめ⠣⠿」の上に0の点と7の点がついた形「0 1 2 6の点、1 2 3 4 5 6 7の点⢇⣾」となります。

### 参考サイト

下記の、福野泰介さん、@uhyo_さんのサイトでテキストデータをそれぞれ六点漢字や漢点字のデータに変換できます。

また下記の『やむ６点』を使うとパソコンのキーボードを使って六点漢字方式または漢点字方式で入力して漢字を入力することができます。

- [(福野泰介さん) tenji converter - 点字変換 日本語点字体系対応版(六点漢字に変換できます)](https://code4sabae.github.io/tenji/converter-jp.html)
- [(@uhyo_さん) Unicode点字変換 (漢点字に変換できます)](https://uhyo.github.io/tenji-web/)
- [６点入力ソフト『やむ６点』](http://www.pcyam.com/game2/yam6ten/hp/index.htm)

六点漢字と漢点字について詳しくは:

* [点字の漢字 | ひらせ鍼灸院、平瀬徹のホームページ](http://www.yoihari.com/tenji/kanji.htm)
* [漢字の点字 | ロービジョン相談と光学(六点漢字について詳しい解説があります。元のサイトは終了していますが、Internet Archive: Wayback Machineでの過去のアーカイブで読むことができます)](https://web.archive.org/web/20040415111009/http://www.geocities.co.jp/Technopolis/4819/body28kanten.html)
* [名古屋点訳ネットワーク(漢点字の点訳図書がダウンロードできます)](http://www.n-braille.net/index.html)
* [横浜漢点字羽化の会(無料/有料の漢点字の読み物を郵送してもらって読むことができます)](http://www.ukanokai-web.jp/)
