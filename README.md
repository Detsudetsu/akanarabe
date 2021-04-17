# README
## これは何？
「あかならべ配列」という名称の日本語かな入力配列です。

日本語かな入力配列とは、特定のキーを入力することでひらがなを入力するためのキー配列です。

一般的な日本語かな入力配列としては、JISかな入力配列とQWERTYローマ字入力配列がよく知られています。

ややこしいですがQWERTYローマ字入力配列もひらがなを入力するための配列なので日本語かな入力配列の1つです。

## あかならべ配列の名前の由来
「AZIK」配列と「和ならべ」配列という2つの日本語かな入力配列をベースに作成したため、「AZIK」のAK、「和ならべ」の「ならべ」から取って「あかならべ」としました。

## あかならべ配列のメリット
* 入力に必要なキー数がローマ字入力と同程度であり、手の移動距離が少ない
* ローマ字入力同様、英語キーボード配列でも入力できる
* 頻出するキーはホームポジションに、頻出する組み合わせのキーは隣り合って配置されており、ローマ字入力よりも手の移動距離が少ない
* 一部の日本語かな文字（拗音・長音）はローマ字入力よりも打鍵数が少ない
* Google日本語入力のローマ字テーブル機能で実装可能なため、当該IMEがインストール可能なWindows, Mac, Linuxで利用可能

## あかならべ配列のデメリット
* 既存の日本語かな入力配列と互換性がないため、使いこなすまでに多少の学習コストが必要

とはいえ、上記デメリットを軽減すべく、学習曲線をなだらかにするために配列にはいくつか工夫をしてあります。

## インストール方法
Google日本語入力＋JIS配列キーボードの場合です。

1. このリポジトリにある akanarabe_jis.txt をダウンロードする
1. Google日本語入力のプロパティを開き、 一般タブ -> キー設定 -> ローマ字テーブル -> 編集 -> 編集 -> インポート... を選択する
1. さきほどダウンロードした akanarabe_jis.txt を選択する

USキーボードの場合はJIS版のファイルを適宜書き換えて使ってください。
なお akanarabe.txt は筆者が使っている独自のキーボード配列用のファイルです。

## あかならべ配列のチュートリアル

あかならべ配列はローマ字入力の改良を目指した配列です。

ローマ字入力同様、子音キー＋母音キーの組み合わせで日本語かな文字を入力します。

たとえば「か」を入力するためには「k」相当のキーと「a」相当のキーを組み合わせて入力します。

まずは子音キーと母音キーの配置を見てみましょう。

## 前提_チュートリアルで使用するキー配置の表記方法

一般的なQWERTYキーボードの配列の場合、以下のように表現します。

段数 | 左手 | 右手
-----|-----|-----
1段目 | Ｑ, Ｗ, Ｅ, Ｒ, Ｔ | Ｙ, Ｕ, Ｉ, Ｏ, Ｐ
2段目 | Ａ, Ｓ, Ｄ, Ｆ, Ｇ | Ｈ, Ｊ, Ｋ, Ｌ, ；
3段目 | Ｚ, Ｘ, Ｃ, Ｖ, Ｂ | Ｎ, Ｍ, `，`, `．`, `/`

## あかならべ配列の子音キー

段数 | 左手 | 右手
-----|-----|-----
1段目 | ＃, Ｚ, Ｄ, Ｇ, Ｐ | ＃, ＃, ＃, ＃, ＃
2段目 | Ｎ, Ｓ, Ｔ, Ｋ, Ｈ | ＃, ＃, ＃, ＃, ＃
3段目 | Ｍ, Ｗ, ＃, Ｒ, Ｂ | ＃, ＃, ＃, ＃, ＃

## あかならべ配列の母音キー

段数 | 左手 | 右手
-----|-----|-----
1段目 | ＃, ＃, ＃, ＃, ＃ | ＃, ＃, ｉ, ｅ, ＃
2段目 | ＃, ＃, ＃, ＃, ＃ | ＃, ａ, ｕ, ｏ, ＃
3段目 | ＃, ＃, ＃, ＃, ＃ | ＃, ＃, ＃, ＃, ＃

## 子音キーと母音キーの配置を覚える
以下にQWERTYキーボードのキー配置とあかならべ配列で入力される文字の対応の例を示します。

QWERTY配列で入力するキー | 実際の子音キーと母音キーの組み合わせ | 出力される文字
---|---|---
ｆｊ | Ｋａ | か
ｆｉ | Ｋｉ | き
ｆｋ | Ｋｕ | く
ｆｏ | Ｋｅ | け
ｆｌ | Ｋｏ | こ
ｒｊ | Ｇａ | が
ｒｉ | Ｇｉ | ぎ
: | : | :

このルールに基づくといくつか入力できない文字があることに気付くと思いますが、そうした文字の入力方法は後述します。

子音キーと母音キーの配置におけるポイントは以下です。

* 子音キーは左手、母音キーは右手に配置されている。そのため左右の手で交互に打鍵しやすく効率良く手を動かせる
* 日本語で頻出する子音である S, K, T, N, H, R がホームポジションと動かしやすい左手人差し指近辺に配置されている
  * QWERTYローマ字配列と比較してTとNが特に入力しやすいはず
* 濁音、半濁音は各清音の上下に配置されている。「が行」「ざ行」「だ行」は上段、「ば行」のみ下段となっている
  * 清音と横の位置を揃えているので、濁音の位置が覚えられていない状態でも、基本は清音の指を上にずらした先のキーを入力すれば濁音を入力できる
  * 濁音は「ば行」のみ下段だが、薬指、中指は上段の方が動かしやすく、人差し指は下段の方が動かしやすいことによるもの
  * QWERTYキーボードでもTよりBの方が楽に指を動かせると感じるはず
  * 「ば行」と「ぱ行」だと前者の方が入力頻度が高いため、入力しやすい人差し指下段にBを配置した
* 母音は日本語で頻出する「ai」「ei」「ou」といった二重母音が入力しやすい配置にしてある
  * 日本語の熟語は上記の組み合わせを含むことがとても多い
  * 例えば「製造工程」といった単語はQWERTYローマ字入力だと指があちらこちらに飛ぶが、あかならべ配列だとQWERTYキーボードで soi wlk flk doi で入力できる
* 「D+i」の組み合わせのみ、「ぢ」は殆ど使われないので「でぃ」が入力できるようにしてあります。

## その他の単打キー
右手には母音以外にも単打で入力可能なキーがいくつか存在します。

段数 | 左手 | 右手
-----|-----|-----
1段目 | ＃, ＃, ＃, ＃, ＃ | や, っ, い, え, ＃
2段目 | ＃, ＃, ＃, ＃, ＃ | ゆ, あ, う, お, ん
3段目 | ＃, ＃, ＃, ＃, ＃ | よ, ー, 、, 。, ー

単打キーのポイントは以下です。

* 「ん」をローマ字のNNではなく単打キーかつ母音の近くのキーで入力できるように
  * 日本語で頻出する「an」「in」「un」「en」「on」をスムーズに入力できます。
  * たとえば「新幹線」といった単語はQWERTYキーボードでは si; fj; so; で入力できます。
* 「やゆよ」を子音キーＹと母音キーの組み合わせでなく単打キー化
* 長音をローマ字入力より入力しやすい位置に配置

## 拗音母音、長音母音キー
右手には通常の母音に加えて拗音と長音を母音として入力可能な拡張母音キーも存在します。

段数 | 左手 | 右手
-----|-----|-----
1段目 | ＃, ＃, ＃, ＃, ＃ | ya, i-, i, e, ＃
2段目 | ＃, ＃, ＃, ＃, ＃ | yu, a, u, o, e-
3段目 | ＃, ＃, ＃, ＃, ＃ | yo, a-, u-, ＃, o-

拡張母音キーのポイントは以下です。

* 「ゃゅょ」が母音キーとして使える
  * 「きゅ」は「K+yu」で入力できます。QWERTYキーボードだと fh で入力可能です。
  * QWERTYキーボードでYのキーから縦に並んでいるので覚えやすい
* 長音付き母音が母音キーとして使える
  * 「かー」は「K+a-」で入力できます。QWERTYキーボードだと fm で入力可能です。
  * 「カードケース」をQWERTYキーボードで入力する場合 fm el f; sk で入力できます。
  * 通常母音のaiueoの近くに配置しているため覚えやすくなっています。
  * 長音母音は必ずしも覚えなくても長音単打キーで代替可能です。最後に覚えましょう。

## 小文字・外来音レイヤ
「ぁ」などの小文字や、「ヴぃ」などの外来音を入力するためのレイヤと、レイヤ切り替えキーが存在します。

段数 | 左手 | 右手
-----|-----|-----
1段目 | ☆, Ｗ, ＃, ＃, Ｔ | ゃ, ＃, ぃ, ぇ, ＃
2段目 | ＃, Ｓ, Ｄ, Ｆ, Ｊ | ゅ, ぁ, ぅ, ぉ, ＃
3段目 | ＃, ＃, Ｃ, Ｖ, ＃ | ょ, ＃, ＃, ＃, ＃

小文字・外来音レイヤのポイントは以下です。

* レイヤ切り替えキーは☆の位置、QWERTYキーにおけるQキーです。
* Q入力後は概ねQWERTYキーの配置通りのキーで外来音の子音が入力できます。
  * Q->QWERTYキーボード上の外来音の音を示すキー->あかならべ配列の子音キー の順番で入力します。
  * 「しぇ」をQWERTYキーボードで入力する場合 qso で入力できます。
  * 「ふぁ」をQWERTYキーボードで入力する場合 qfj で入力できます。
  * 「でぃ」と「ぢ」のみ通常の濁音と外来音レイヤで入力できる文字が交換されています。
  * Jのみ近い音であるQWERTYキーのGの位置で入力可能です。
  * 詳しくは後述の表をご覧ください。
* Q入力後に単打キーと同じ場所のキーを入力することで小文字が入力可能です。
  * 「ゃ」をQWERTYキーボードで入力する場合 qy で入力できます。

## その他記号
* 「・」は使われていないキーである c/ と \ で入力可能にしてありますが、好みで変更してください。

## 外来音レイヤのQWERTY対応表
* 外来音レイヤは特殊なのでQWERTYキーボードとの対応表を載せておきます。

QWERTY配列で入力するキー | 外来音レイヤにおけるキーの組み合わせ | 出力される文字
------------------|----------------|-----------------
qwi | ☆W+i | うぃ
qwo | ☆W+e | うぇ
qwl | ☆W+o | うぉ
qtj | ☆T+a | つぁ
qti | ☆T+i | てぃ
qtk | ☆T+u | とぅ
qto | ☆T+e | つぇ
qtl | ☆T+o | つぉ
qty | ☆T+ya | ちゃ
qth | ☆T+yu | ちゅ
qtn | ☆T+yo | ちょ
qtm | ☆T+a- | つぁー
qtu | ☆T+i- | てぃー
qt, | ☆T+u- | とぅー
qt\ | ☆T+e- | つぇー
qt/ | ☆T+o- | つぉー
qsj | ☆S+a | しゃ
qsi | ☆S+i | し
qsk | ☆S+u | しゅ
qso | ☆S+e | しぇ
qsl | ☆S+o | しょ
qsy | ☆S+ya | しゃ
qsh | ☆S+yu | しゅ
qsn | ☆S+yo | しょ
qsm | ☆S+a- | しゃー
qsu | ☆S+i- | しー
qs, | ☆S+u- | しゅー
qs\ | ☆S+e- | しぇー
qs/ | ☆S+o- | しょー
qdi | ☆D+i | ぢ
qdk | ☆D+u | どぅ
qdy | ☆D+ya | ぢゃ
qdh | ☆D+yu | ぢゅ
qdn | ☆D+yo | ぢょ
qdu | ☆d+i- | ぢー
qd, | ☆d+u- | どぅー
qfj | ☆F+a | ふぁ
qfi | ☆F+i | ふぃ
qfk | ☆F+u | ふゅー
qfo | ☆F+e | ふぇ
qfl | ☆F+o | ふぉ
qfh | ☆F+yu | ふゅ
qfm | ☆F+a- | ふぁー
qfu | ☆F+i- | ふぃー
qf, | ☆F+u- | ふゅー
qf\ | ☆F+e- | ふぇー
qf/ | ☆F+o- | ふぉー
qgj | ☆J+a | じゃ
qgi | ☆J+i | じ
qgk | ☆J+u | じゅ
qgo | ☆J+e | じぇ
qgl | ☆J+o | じょ
qgy | ☆J+ya | じゃ
qgh | ☆J+yu | じゅ
qgn | ☆J+yo | じょ
qgm | ☆J+a- | じゃー
qgu | ☆J+i- | じー
qg, | ☆J+u- | じゅー
qg\ | ☆J+e- | じぇー
qg/ | ☆J+o- | じょー
qcj | ☆C+a | ちゃ
qci | ☆C+i | ち
qck | ☆C+u | ちゅ
qco | ☆C+e | ちぇ
qcl | ☆C+o | ちょ
qcy | ☆C+ya | ちゃ
qch | ☆C+yu | ちゅ
qcn | ☆C+yo | ちょ
qcm | ☆C+a- | ちゃー
qcu | ☆C+i- | ちー
qc, | ☆C+u- | ちゅー
qc\ | ☆C+e- | ちぇー
qc/ | ☆C+o- | ちょー
qvj | ☆V+a | ヴぁ
qvi | ☆V+i | ヴぃ
qvk | ☆V+u | ヴ
qvo | ☆V+e | ヴぇ
qvl | ☆V+o | ヴぉ
qvh | ☆V+yu | びゅー
qv, | ☆V+u | びゅー
qvm | ☆V+a- | ヴぁー
qvu | ☆V+i- | ヴぃー
qv, | ☆V+u- | びゅー
qv\ | ☆V+e- | ヴぇー
qv/ | ☆V+o- | ヴぉー
