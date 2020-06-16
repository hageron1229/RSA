*これは情報系の大学に通う大学生が勉強のために実装したものです
*これらを使用したことで損害が発生したとしても一切関知しません

RSA暗号という暗号化アルゴリズムを実装してみました。
仕組みは非常にシンプルであるので、最初にやるのには適切と考え選びました。

作成したプログラムの使い方を一応書いておきます。

このプログラムはクラスを通して実行します。

-インスタンスの作成
・RSA()でインスタンスを作成します。
・RSA()の引数にRSA().pub_key()とRSA().pri_key()をとると、公開鍵、秘密鍵がそれで初期化されます。

-暗号化
・RSA().enc(target,key)で暗号化します。
・targetは暗号化したい英数字を文字列として入力します。
・keyは公開鍵を指定して暗号化したいときに指定できます。

-複号
・RSA().dec(target,key)で復号します。
・targetは復号したい文字列をとります。（想定外のエラー処理はしていません。）
・keyは秘密鍵を指定して復号したいときに指定できます。

-実装したメソッドの説明
product()
--素数の積を返します。

pub_key()
--公開鍵を返します。（実態は整数を２つ持つタプルです。）

pri_key()
--秘密鍵を返します。（実態は整数を２つ持つタプルです。）

keys()
--秘密鍵、公開鍵、素数の積を返します。（確認用です。）


pythonで作っておいてなんですが、public,privateをfiled変数にもメソッドにも適応できないのは、なかなかいただけないと思うんですが、勉強のために作ったので目を瞑りました。

Reference
「RSA暗号の仕組みと安全性」（https://mathtrain.jp/rsaango）
「Python で公開鍵暗号アルゴリズム RSA を実装してみる」(https://qiita.com/QUANON/items/e7b181dd08f2f0b4fdbe)