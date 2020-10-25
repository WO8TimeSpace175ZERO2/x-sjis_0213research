# 文字コード Shift_JSI  リンク集

第3水準と第4水準などの字をWebブラウザで表示できるか確認

https://kind-hodgkin-b70c94.netlify.app/

https://kind-hodgkin-b70c94.netlify.app/docs/UTF-8sample.html

https://kind-hodgkin-b70c94.netlify.app/docs/Shift_JISsample.html

https://kind-hodgkin-b70c94.netlify.app/docs/Shift_JISsample0.html


[]()

[jisx0213 infocenter JIS X 0213:2000 関連データです。ご自由に（利用したり加工したり配布したりして）お使いください。データは、死にたい程度にはチェックしていますが、保証しろといわれても困ります。](http://www.jca.apc.org/~earthian/aozora/0213.html)

[JIS X 0213 漢字集合第1面](https://www.itscj.ipsj.or.jp/iso-ir/233.pdf)

[JIS X 0213 漢字集合第2面](https://www.itscj.ipsj.or.jp/iso-ir/229.pdf)

[JIS X 0213の代表的な符号化方式 ～2004年改正 (JIS2004) 対応版～ 2000年11月初版公開、2017年8月最終更新 矢野啓介](http://www.asahi-net.or.jp/~wq6k-yn/code/enc-x0213.html)

## コード値の算出
面区点番号からShift_JIS-2004の第1・第2バイトは以下の通り求められます。

面番号を m、区番号を k、点番号を t とする。また、記号 ÷ は整数除算 (小数点以下切捨て)を表す。

第1バイト(S1)は、以下による:

### m = 1 で 1 ≦ k ≦ 62 のとき, S1 = (k + 0x101) ÷ 2.

### m = 1 で 63 ≦ k ≦ 94 のとき, S1 = (k + 0x181) ÷ 2.

### m = 2 で, k = 1, 3, 4, 5, 8, 12, 13, 14, 15 のとき, S1 = (k + 0x1df) ÷ 2 － (k ÷ 8) × 3.

### m = 2 で, 78 ≦ k ≦ 94 のとき, S1 = (k + 0x19b) ÷ 2.

第2バイト(S2)は、以下による:

k が奇数の場合:

### 1 ≦ t ≦ 63 のとき, S2 = t + 0x3f.

### 64 ≦ t ≦ 94 のとき, S2 = t + 0x40.

k が偶数の場合, S2 = t + 0x9e.

2バイトコードの見分け方
2バイトコードの第1バイトになるのは以下の範囲です。

0x81～0x9f, 0xe0～0xfc

それ以外のバイトは1バイトコードおよび保留域です。

保留域となるバイト は0x80、0xa0、0xfd、0xfe、0xffです。

なお、2バイトコードの2バイト目になる範囲は以下の通りです。1バイトコー ドの範囲と重なっているので注意が必要です。バイト列の途中の1バイトだけ取 り出しても1バイトコードか否かを判断できません。

0x40～0x7e, 0x80～0xfc




[JIS X 0213のコード対応表](http://x0213.org/codetable/)

[JIS X 0213 Wiki](http://x0213.org/wiki/wiki.cgi)

[面区点から ISO-2022-JP-2004、EUC-JIS-2004、Shift JIS-2004 におけるバイト列を求める](https://blog.sarabande.jp/post/36118776898)

[文字コード表 シフトJIS(Shift_JIS)](http://charset.7jp.net/sjis.html)

[JIS第１水準の漢字（２９６５字）](https://kanji.jitenon.jp/cat/jisdai1.html)

[JIS第２水準の漢字（３３９０字）](https://kanji.jitenon.jp/cat/jisdai2.html)

[JIS第３水準の漢字（１２５９字）](https://kanji.jitenon.jp/cat/jisdai3.html)

[JIS第４水準の漢字（２４３６字）](https://kanji.jitenon.jp/cat/jisdai4.html)

[行政情報処理用漢字コードの現状 第1回 漢字コードの基礎、JISコード](https://xtech.nikkei.com/it/article/COLUMN/20140616/564463/)

[行政情報処理用漢字コードの現状 第2回 住民基本台帳ネットワーク統一文字](https://xtech.nikkei.com/it/article/COLUMN/20140621/565782/)

[行政情報処理用漢字コードの現状 第3回 戸籍統一文字](https://xtech.nikkei.com/it/article/COLUMN/20140621/565783/)

[行政情報処理用漢字コードの現状 第4回 入国管理局正字](https://xtech.nikkei.com/it/article/COLUMN/20140621/565784/)

[行政情報処理用漢字コードの現状 第5回 文字情報基盤](https://xtech.nikkei.com/it/article/COLUMN/20140621/565785/)

[情報処理推進機構（IPA）の文字情報基盤](https://mojikiban.ipa.go.jp/)

[マイクロソフトなど6社が参加、異体字を取り扱う「IVS」促進協議会が発足](https://xtech.nikkei.com/it/article/NEWS/20101206/354916/)

[ASH multimedia lab 文字コードについて](http://ash.jp/code/code.htm)

[ウィキペディア Unicode](https://ja.wikipedia.org/wiki/Unicode)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編18 JIS X 0213の改正は、文字コードにどんな未来をもたらすか（1）　改正の概要1：そのポイントを整理する](https://internet.watch.impress.co.jp/www/column/ogata/sp18.htm)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編19 JIS X 0213の改正は、文字コードにどんな未来をもたらすか（2）　改正の概要2：JIS X 0208が改正されなかった理由](https://internet.watch.impress.co.jp/www/column/ogata/sp19.htm)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編20 JIS X 0213の改正は、文字コードにどんな未来をもたらすか（3）　改正の概要3：例示字体が変更された168字について](https://internet.watch.impress.co.jp/www/column/ogata/sp20.htm)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編21 JIS X 0213の改正は、文字コードにどんな未来をもたらすか（4）　改正の概要4：追加された10字の「表外漢字UCS互換」について（前編）](https://internet.watch.impress.co.jp/www/column/ogata/sp21.htm)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編22 JIS X 0213の改正は、文字コードにどんな未来をもたらすか（5）　改正の概要5：追加された10字の「表外漢字UCS互換」について（後編）](https://internet.watch.impress.co.jp/www/column/ogata/sp22.htm)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編23 JIS X 0213の改正は、文字コードにどんな未来をもたらすか（6）　改正の影響：MSフォントのデザイン変更とその波紋について](https://internet.watch.impress.co.jp/www/column/ogata/sp23.htm)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編24 JIS X 0213の改正は、文字コードにどんな未来をもたらすか（7）　番外編：改正JIS X 0213とUnicodeの等価属性／正規化について（上）](https://internet.watch.impress.co.jp/www/column/ogata/sp24.htm)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編25 JIS X 0213の改正は、文字コードにどんな未来をもたらすか（8）　番外編：改正JIS X 0213とUnicodeの等価属性／正規化について（下）](https://internet.watch.impress.co.jp/www/column/ogata/sp25.htm)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編26 JIS X 0213の改正は、文字コードにどんな未来をもたらすか（9）改正の影響：フォントデザインを変更しないアップルコンピュータの真意（上）](https://internet.watch.impress.co.jp/www/column/ogata/sp26.htm)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編27 JIS X 0213の改正は、文字コードにどんな未来をもたらすか（10）改正の影響：フォントデザインを変更しないアップルコンピュータの真意（中）](https://internet.watch.impress.co.jp/www/column/ogata/sp27.htm)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編28 JIS X 0213の改正は、文字コードにどんな未来をもたらすか（11）改正の影響：フォントデザインを変更しないアップルコンピュータの真意（下）](https://internet.watch.impress.co.jp/www/column/ogata/sp28.htm)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編29 JIS X 0213の改正を総括する（1）改正を繰り返した挙げ句、78JISの字体に戻ってしまったJIS文字コード](https://internet.watch.impress.co.jp/www/column/ogata/sp29.htm)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編30 JIS X 0213の改正を総括する（2）JISが例示字体を変更せざるを得なかった、本当の理由](https://internet.watch.impress.co.jp/www/column/ogata/sp30.htm)

[小形克宏の「文字の海、ビットの舟」――文字コードが私たちに問いかけるもの 特別編31 JIS X 0213の改正を総括する（3）JIS X 0213の改正と「漢字を救え！」キャンペーン](https://internet.watch.impress.co.jp/www/column/ogata/sp31.htm)

[ウィキペディア 異体字セレクタ](https://ja.wikipedia.org/wiki/%E7%95%B0%E4%BD%93%E5%AD%97%E3%82%BB%E3%83%AC%E3%82%AF%E3%82%BF)

[図書館員のコンピュータ基礎講座 JIS X 0208およびJIS X 0213の字形・字体の変更点](http://www.asahi-net.or.jp/~ax2s-kmtn/ref/jisrev.html)

[Character Sets IANA](https://www.iana.org/assignments/character-sets/character-sets.xhtml)


# JIS X 0213の紙の規格文書は 総額 ￥19,580で購入できる。

https://www.jsa.or.jp/

https://webdesk.jsa.or.jp/books/W11M0270
規格番号 X0213 で検索

【1】
JIS X 0213:2000
７ビット及び８ビットの２バイト情報交換用符号化拡張漢字集合
7-bit and 8-bit double byte coded extended Kanji sets for information interchange

発行年月日： 2000-02-29

状態： 有効

和文
541ページ
11,550 円（税込）
本体価格：10,500円

https://webdesk.jsa.or.jp/books/W11M0090/index/?bunsyo_id=JIS+X+0213%3A2000

【2】
JIS X 0213:2000/AMENDMENT 1:2004
７ビット及び８ビットの２バイト情報交換用符号化拡張漢字集合（追補１）
7-bit and 8-bit double byte coded extended KANJI sets for information interchange (Amendment 1)

発行年月日： 2004-02-20

確認年月日： 2008-10-01

状態： 有効

和文
68ページ
4,400 円（税込）
本体価格：4,000円

https://webdesk.jsa.or.jp/books/W11M0090/index/?bunsyo_id=JIS+X+0213%3A2000%2FAMENDMENT+1%3A2004

【3】
JIS X 0213:2000/AMENDMENT 2:2012
７ビット及び８ビットの２バイト情報交換用符号化拡張漢字集合（追補２）
7-bit and 8-bit double byte coded extended Kanji sets for information interchange (Amendment 2)

発行年月日： 2012-02-20

確認年月日： 2016-10-20

状態： 有効

和文
42ページ
3,630 円（税込）
本体価格：3,300円

https://webdesk.jsa.or.jp/books/W11M0090/index/?bunsyo_id=JIS+X+0213%3A2000%2FAMENDMENT+2%3A2012


また、上記の紙文書は下記ページで無償で閲覧が可能

[日本産業標準調査会　HP](https://www.jisc.go.jp/app/jis/general/GnrJISSearch.html)

左側にJISと書かれたテキスト入力欄に「X 0213」と入力し、一覧表示ボタンをクリック後に表示される「JISX0213」リンクをクリックすると閲覧が可能。




