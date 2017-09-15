## Liblouisで日本語を六点漢字と漢点字に変換するためのテーブルファイル

### 著作権について

日本語の漢字を表す点字は2種類の方式が考案されています。

長谷川貞夫氏による「六点漢字」と、川上泰一氏による「漢点字」です。

「六点漢字」はコンピュータで漢字を入力するために考えられたもので、「漢点字」は点字で漢字を読むために考えられたものです。

これらの漢字の点字に関する著作権はそれぞれの方に帰属します。

私がここに作成しているデータは個人的学習のためのものです。

利用する場合、それぞれの責任でお願いします。

### 各ファイルの説明

* ja-rokutenkanji.utb - 六点漢字に変換するためのファイル
* ja-kantenji.utb - 漢点字に変換するためのファイル

上記の２つがメインのファイルで、下記のファイルはこのメインのファイルから読み込むファイルになっています。

- ja-alphabet-digit.uti - 全角のアルファベットと数字
* ja-punctuation.uti - 句読点と記号
* ja-hiragana.uti - ひらがな
* ja-katakana-rokutenkanji.uti - 六点漢字のカタカナ符号をつけたカタカナ
* ja-katakana-kantenji.uti - 漢点字のカタカナ符号をつけたカタカナ
* ja-kanji-rokutenkanji.uti - 六点漢字の漢字
* ja-kanji-kantenji.uti - 漢点字の漢字
* ja-unicode78top.dis - 感点字の6点の上に2点付く形に変更したunicode.dis

これら以外に、Liblouis付属の下記のファイルも読み込んでいます。アルファベット、数字、半角の句読点、記号などは下記のファイルでの変換になります。

* en-ueb-g1.ctb - このファイルから以下のファイルが読み込まれている
* braille-patterns.cti
* en-ueb-chardefs.uti
* en-ueb-math.ctb
* latinLetterDef8Dots.uti
* unicode.dis

### 使い方

Liblouisに含まれるlou_translateを使う場合、コマンドプロンプトで:

> lou_translate -f ja-rokutenkanji.utb <input.txt >output.txt

のようにします。

ja-rokutenkanji.utbは六点漢字に変換するためのファイルです。

input.txtは変換したいテキストファイルで、文字コードがutf8のものです。

output.txtは出力ファイル名です。


ja-rokutenkanji.utbの代わりに、ja-kantenji.utbを指定すると漢点字に変換できます。





