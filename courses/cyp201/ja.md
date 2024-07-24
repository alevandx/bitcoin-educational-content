---
name: ビットコイン暗号入門
goal: 暗号の観点からビットコイン・ウォレットの作成を理解する。
objectives:
  - ビットコインに関連する暗号用語の謎を解く。
  - ビットコイン・ウォレットの作成をマスターする。
  - ビットコイン・ウォレットの構造を理解する。
  - アドレスと派生パスを理解する。
---

# 暗号学への旅

ビットコインに魅了されていますか？ビットコインウォレットの仕組みが気になりますか？暗号学への魅力的な旅に出発しましょう！Loïc（ロイック）、私たちの専門家が、ビットコインウォレットの作成の複雑さを案内し、ハッシング、キー導出、楕円曲線などの技術用語の謎を解き明かします。

このトレーニングでは、ビットコインウォレットの構造を理解する知識だけでなく、暗号学のエキサイティングな世界に深く潜る準備も整います。この旅に出発する準備はできましたか？私たちと一緒に参加して、好奇心を専門知識に変えましょう！

+++

# はじめに
<partId>32960669-d13a-592f-a053-37f70b997cbf</partId>

## 暗号学入門
<chapterId>fb4e8857-ea35-5a8a-ae8a-5300234e0104</chapterId>

### このトレーニングはあなたに向いていますか？ YES！

「Crypto 301: 暗号学とHDウォレットへの入門」という新しいトレーニングコースへようこそ、この分野の専門家であるLoïc Morel（ロイック・モレル）がリードします。このコースは、データの暗号化とセキュリティを保証する数学の基本的な分野である暗号学の魅力的な世界にあなたを没入させます。

私たちの日常生活、特にビットコインの領域では、暗号学は重要な役割を果たします。プライベートキー、パブリックキー、アドレス、導出パス、シード、エントロピーなど、暗号学に関連する概念は、ビットコインウォレットの使用と作成の核心にあります。このコースを通じて、Loïcはプライベートキーの生成方法とそれがアドレスにどのようにリンクされるかを詳しく説明します。また、楕円曲線の数学的詳細について1時間かけて説明します。さらに、ウォレットのセキュリティを保つためにHMAC SHA512の使用が重要である理由や、シードとニーモニックフレーズの違いについても理解できるようになります。
このトレーニングの最終目標は、HDウォレットの作成に関わる技術的プロセスと使用される暗号学的方法を理解することです。年月を経て、ビットコインウォレットは使用が容易で、より安全で、特定のBIPのおかげで標準化されています。LoïcはこれらのBIPを理解するのを助け、ビットコインの開発者や暗号学者によってなされた選択を把握します。私たちの大学が提供するすべてのトレーニングと同様に、このトレーニングも完全に無料でオープンソースです。つまり、自由に受講して使用することができます。このエキサイティングなコースの終わりにあなたのフィードバックを楽しみにしています。

### それでは、教授、どうぞ！

皆さん、こんにちは。私はLoïc Morel（ロイック・モレル）、ビットコインウォレットで使用される暗号学の技術的探求を通じてあなたを導くガイドです。

私たちの旅は、暗号学的ハッシュ関数の深淵への潜入から始まります。一緒に、不可欠なSHA256の内部構造を解剖し、導出に特化したさまざまなアルゴリズムを探求します。

次に、デジタル署名の神秘的な世界を解読する冒険を続けます。これらの署名に楕円曲線の魔法がどのように適用されるかを発見し、プライベートキーからパブリックキーを計算する方法を明らかにします。もちろん、デジタル署名のプロセスにも深く潜ります。

次に、ビットコインウォレットの進化を振り返り、エントロピーとランダム数の概念に冒険します。有名なニーモニックフレーズをレビューしながら、パスフレーズにも触れます。さらに、128回のサイコロのロールからシードを作成するユニークな体験もできるチャンスがあります！
これらの確かな基盤を持って、我々は重要な部分に取り組む準備が整います:ビットコインウォレットの作成です。シードとマスターキーの誕生から、拡張キーの研究、子キーペアの導出に至るまで、各ステップを詳細に解説します。また、ウォレットの構造と導出パスについても議論します。
最後に、ビットコインアドレスの検討でこの旅を締めくくります。ビットコインアドレスがどのように作成され、ビットコインウォレットの機能においてどのような重要な役割を果たすかを説明します。

この魅力的な旅に参加し、これまでにない形で暗号学の世界を探索する準備をしてください。先入観を捨て、ビットコインとその基本構造を理解する新しい方法に心を開いてください。

# ハッシュ関数
<partId>3713fee1-2ec2-512e-9e97-b6da9e4d2f17</partId>

## ビットコインに関連する暗号学的ハッシュ関数の紹介
<chapterId>dba011f5-1805-5a48-ac2b-4bd637c93703</chapterId>

本日のセッションでは、ビットコインプロトコルのセキュリティに不可欠な基石であるハッシュ関数の暗号学的世界に深く潜ることに専念します。ハッシュ関数を、任意のサイズの情報を一意で固定サイズのデジタル指紋（「ハッシュ」、「ダイジェスト」、「チェックサム」と呼ばれる）に変換する超効率的な暗号解読ロボットと想像してください。
要約すると、ハッシュ関数は任意サイズの入力メッセージを固定サイズの出力指紋に変換します。

暗号学的ハッシュ関数のプロファイルを説明するには、2つの重要な特性を理解する必要があります:その不可逆性と偽造への抵抗力。

不可逆性、またはプレイメージへの抵抗とは、入力から出力を簡単に計算できるが、出力から入力を計算することは不可能であることを意味します。
これは一方向関数です。

![image](assets/image/section1/0.webp)

偽造への抵抗は、入力のわずかな変更でも出力が大きく異なる結果となることから来ます。
これらの関数により、ダウンロードしたソフトウェアの整合性を検証することができます。

![image](assets/image/section1/1.webp)

また、衝突とセカンドプレイメージへの抵抗という、彼らが持つもう一つの重要な特性があります。衝突とは、2つの異なる入力が同じ出力を生じることです。
確かに、ハッシングの世界では衝突は避けられないものですが、優れた暗号学的ハッシュ関数はそれを大幅に最小限に抑えます。リスクは非常に低いため、無視できると考えられます。それは、各ハッシュが広大な都市の家であり、良いハッシュ関数が各家にユニークなアドレスを保証するかのようです。

セカンドプレイメージへの抵抗は、衝突への抵抗に依存します。衝突への抵抗があれば、セカンドプレイメージへの抵抗もあります。
与えられた入力情報に対して、最初の入力とは異なるセカンド入力を見つけ出し、関数の出力ハッシュで衝突を生じさせる必要があります。セカンドプレイメージへの抵抗は、衝突への抵抗と似ていますが、入力は与えられています。
さて、時代遅れのハッシュ関数の荒波を航海しましょう。SHA0、SHA1、MD5は、暗号ハッシュの海で錆びた殻と見なされています。それらは衝突への抵抗力を失ったため、しばしば推奨されません。出力サイズの制限のため、衝突回避が不可能であることを鳩の巣原理が説明しています。真に安全とみなされるためには、ハッシュ関数は衝突、セカンドプレイメージ、プレイメージに対して抵抗力を持つ必要があります。

ビットコインプロトコルにおける重要な要素であるSHA-256ハッシュ関数は、この船の船長です。他の関数、例えばSHA-512はHMACやPBKDFでの導出に使用されます。さらに、RIPMD160は指紋を160ビットに縮小するために使用されます。HASH256とHASH160に言及するとき、私たちはSHA-256とRIPMDを使用したダブルハッシングを指しています。

HASH256については、SHA256関数を使用してメッセージのダブルハッシュです。
以下は、技術的な内容を日本語に翻訳したものです。

SHA256(SHA256(メッセージ))$$
HASH160については、最初にSHA256を使用してメッセージのダブルハッシュを行い、次にRIPMD160を使用します。
$$
RIPMD160(SHA256(メッセージ))
$$
HASH160の使用は、SHA-256のセキュリティを保ちながらフィンガープリントのサイズを縮小するという利点があります。

要約すると、暗号ハッシュ関数の究極の目標は、任意のサイズの情報を固定サイズのフィンガープリントに変換することです。安全と認識されるためには、以下の強度が必要です:不可逆性、改ざん抵抗性、衝突抵抗性、および第二事前画像抵抗性。

![image](assets/image/section1/2.webp)

この探求の終わりに、暗号ハッシュ関数の謎を解明し、ビットコインプロトコルでの使用法を強調し、その具体的な目的を詳述しました。ハッシュ関数が安全と見なされるためには、事前画像、第二事前画像、衝突、および改ざんに対して抵抗性がなければならないことを学びました。また、ビットコインプロトコルで使用されるさまざまなハッシュ関数の範囲についても説明しました。次のセッションでは、SHA256ハッシュ関数の核心に迫り、その独特な特性を生み出す魅力的な数学について探求します。

## SHA256の内部構造
<chapterId>905eb320-f15b-5fb6-8d2d-5bb447337deb</chapterId>

暗号ハッシュ関数の複雑な迷路を通じた魅力的な旅の続きへようこそ。今日は、以前に紹介したSHA256の謎を解き明かします。この複雑で巧妙なプロセスを詳しく見ていきましょう。

SHA256ハッシュ関数の目的を思い出してください。それは、任意のサイズの入力メッセージを取り、256ビットのハッシュを出力として生成することです。

### 前処理

この迷路をさらに進むために、SHA256の前処理から始めましょう。

#### パディングビット

この最初のステップの目的は、メッセージを512ビットの倍数に等しくすることです。これを達成するために、メッセージにパディングビットを追加します。

Mを初期メッセージサイズとします。
1を区切りのためのビットとします。
Pをパディングのために使用されるビット数、64を第二前処理段階のために確保されたビット数とします。
合計は512ビットの倍数でなければならず、これはnで表されます。

![image](assets/image/section1/3.webp)

950ビットの入力メッセージの例:

```
ステップ1: サイズを決定します。最終的に必要なビット数。
(M + 64 + 1) (M = 950の場合) > 512の最初の倍数は1024です。
1024 = 2 * 512
したがって、n = 2です。

ステップ2: 最終的に必要なビット数に達するために必要なP、パディングビット数を決定します。
-> M + 1 + P + 64 = n * 512
-> M + 1 + P + 64 = 2 * 512
-> 940 + 1 + P + 64 = 1024
-> P = 1024 - 1 - 64 - 950
-> P = 9

したがって、メッセージを512の倍数に等しくするために9つのパディングビットを追加する必要があります。
```

そして次に？
初期メッセージの直後に、この例では9つの0が続く区切りの1とPを追加する必要があります。

```
メッセージ + 1 000 000 000
```

#### サイズパディング
私たちは現在、前処理の第二段階に移行しており、これには初期メッセージのビット数のバイナリ表現を追加する作業が含まれます。
950ビットの入力を例に再考してみましょう:

```
数字950のバイナリ表現は:11 1011 0110

前のステップから予約された64ビットを使用します。64ビットを均等にするためにゼロを追加します。その後、初期メッセージ、パディングビット、サイズパディングを統合して均等化された入力を得ます。
```

こちらが結果です:

![image](assets/image/section1/4.webp)

### 処理

#### 理解の前提条件

##### 定数と初期化ベクトル

現在、SHA-256関数の処理の初期段階の準備をしています。どんな良いレシピにも基本的な材料が必要なように、私たちはこれを定数と初期化ベクトルと呼びます。

初期化ベクトルは、最初の8つの素数の平方根の小数部分の最初の32ビットから、AからHまでです。これらは初期処理ステップの基本値として機能します。その値は16進数形式です。

定数Kは、最初の64個の素数の立方根の小数部分の最初の32ビットを表し、0から63まであります。これらは圧縮関数の各ラウンドで使用されます。その値も16進数形式です。

![image](assets/image/section1/5.webp)

##### 使用される操作

圧縮関数内では、XOR、AND、NOTなどの特定の演算子を使用します。ビットはその位置に応じて一つずつ処理され、XOR演算子と真理値表を使用します。AND演算子は、両方のオペランドが1に等しい場合にのみ1を返し、NOT演算子はオペランドの反対の値を返すために使用されます。また、選択した数だけビットを右にシフトするSHR操作も使用します。

真理値表:

![image](assets/image/section1/6.webp)

ビットシフト操作:

![image](assets/image/section1/7.webp)

#### 圧縮関数

圧縮関数を適用する前に、入力を512ビットのブロックに分割します。各ブロックは他のブロックとは独立して処理されます。

各512ビットブロックはさらに32ビットのチャンクであるWに分割されます。このように、W(0)は512ビットブロックの最初の32ビットを表し、W(1)は次の32ビットを表し、512ビットのブロックに達するまで続きます。

すべての定数KとチャンクWが定義されたら、各ラウンドで各チャンクWに対して以下の計算を実行します。

圧縮関数では64ラウンドの計算を実行します。最後のラウンドでは、「関数の出力」レベルで、圧縮関数の初期状態に追加される中間状態が得られます。

次に、これらの圧縮関数のステップを次の512ビットブロックに対して繰り返し、最後のブロックまで続けます。

圧縮関数内のすべての加算は、常に32ビットの合計を保つために2^32の加算で行われます。

![image](assets/image/section1/9.webp)

![image](assets/image/section1/8.webp)

##### 圧縮関数の1ラウンド

![image](assets/image/section1/11.webp)

![image](assets/image/section1/10.webp)

圧縮関数は64回実行されます。私たちは入力として定義済みの定数KとピースWを持っています。
赤い四角/十字は2^32ビットの加算を表します。
入力 A, B, C, D, E, F, G, H はそれぞれ32ビットの値と関連付けられ、合計で 32 * 8 = 256 ビットとなります。また、出力として新しいシーケンス A, B, C, D, E, F, G, H があります。この出力は次のラウンドの入力として使用され、64ラウンドの終了まで続けられます。

圧縮関数の最初のラウンドの入力シーケンスの値は、以前に述べた事前定義された初期化ベクトルに対応します。
念のために述べておくと、初期化ベクトルは、最初の8つの素数の平方根の小数部分の最初の32ビットを表します。

以下はラウンドの例です:

![image](assets/image/section1/12.1.webp)

##### 中間状態

メッセージは512ビットのブロックに分割され、それぞれが32ビットのピースに分割されます。各512ビットブロックに対して、圧縮関数の64ラウンドが適用されます。
中間状態は、ブロックの64ラウンドの終了時に対応します。この64ラウンドの出力シーケンスの値は、次のブロックの最初のラウンドの入力シーケンスの初期値として使用されます。

![image](assets/image/section1/12.2.webp)

#### ハッシュ関数の概要

![image](assets/image/section1/13.webp)

最初の512ビットメッセージピースの出力が、次の512ビットメッセージピースの入力としての初期化ベクトルに対応していることがわかります。

最後のピースの最後のラウンドの出力は、SHA256関数の最終結果に対応します。

最後に、CH、MAJ、σ0、σ1ボックスで行われる計算の重要な役割を強調したいと思います。これらの操作は、他のものとともに、SHA256ハッシュ関数の攻撃に対する堅牢性を保証する守護者であり、特にBitcoinプロトコル内で多くのデジタルシステムのセキュリティを確保するための選択肢として好まれます。SHA256の美しさは、その複雑さにもかかわらず、ハッシュから入力を見つけ出す能力にあり、与えられた入力のハッシュを検証することは機械的に単純な行動です。

## 導出に使用されるアルゴリズム
<chapterId>cc668121-7789-5e99-bf5e-1ba085f4f5f2</chapterId>

HMACおよびPBKDF2導出アルゴリズムは、Bitcoinプロトコルのセキュリティメカニズムの重要な要素です。これらは様々な潜在的な攻撃を防ぎ、Bitcoinウォレットの完全性を保証します。
HMACとPBKDF2は、Bitcoinで様々なタスクに使用される暗号化ツールです。HMACは主に、階層的決定論的（HD）ウォレットを導出する際の長さ拡張攻撃に対抗するために使用され、PBKDF2はニーモニックフレーズをシードに変換するために使用されます。

#### HMAC-SHA512

HMAC-SHA512ペアには2つの入力があります:メッセージ m（入力1）とユーザーによって任意に選ばれたキー K（入力2）。また、固定サイズの出力:512ビットがあります。

以下の点に注意しましょう:
- m: ユーザーによって選ばれた任意サイズのメッセージ（入力1）
- K: ユーザーによって選ばれた任意のキー（入力2）
- K': サイズBのブロックに調整されたキー K。
- ||: 連結操作。
- opad: バイト0x5cがB回繰り返された定数。
- ipad: バイト0x36がB回繰り返された定数。
- B: 使用されるハッシュ関数のブロックのサイズ。

![image](assets/image/section1/14.webp)
HMAC-SHA512は、メッセージとキーを入力として受け取り、固定サイズの出力を生成します。一貫性を保つために、キーはハッシュ関数で使用されるブロックのサイズに基づいて調整されます。HDウォレットの導出の文脈では、HMAC-SHA-512が使用されます。これは1024ビット（128バイト）のブロックで動作し、キーをそれに応じて調整します。セキュリティを強化するために必要に応じて繰り返されるOPAD（0x5c）とIPAD（0x36）の定数を使用します。
HMAC-SHA-512のプロセスには、キーXOR OPADとキーXOR IPADにSHA-512を適用した結果とメッセージを連結する作業が含まれます。1024ビット（128バイト）のブロックで使用される場合、入力キーは必要に応じてゼロでパディングされ、その後IPADとOPADでXORされます。変更されたキーはその後メッセージと連結されます。

![image](assets/image/section1/15.webp)

文字列コードに塩を含めることで、導出されたキーのセキュリティが向上します。それがなければ、攻撃によってウォレット全体が危険にさらされ、すべてのビットコインが盗まれる可能性があります。

ニーモニックフレーズをシードに変換するためにPBKDF2が使用されます。このアルゴリズムはHMAC SHA512を使用して2048ラウンドを実行します。これらの導出アルゴリズムを通じて、異なる入力が一意で固定された出力を生成することができ、SHA-2ファミリー関数に対する可能な長さ拡張攻撃の問題を軽減します。
長さ拡張攻撃は、特定の暗号ハッシュ関数の特定の特性を悪用します。このような攻撃では、未知のメッセージのハッシュを既に持っている攻撃者が、元のメッセージの拡張であるより長いメッセージのハッシュを計算することができます。これは元のメッセージの内容を知らなくても可能であり、このタイプのハッシュ関数が整合性検証などのタスクに使用される場合、重大なセキュリティの脆弱性につながる可能性があります。

![image](assets/image/section1/16.webp)

結論として、HMACおよびPBKDF2アルゴリズムは、ビットコインプロトコルにおけるHDウォレット導出のセキュリティにおいて重要な役割を果たします。HMAC-SHA-512は長さ拡張攻撃から保護するために使用され、PBKDF2はニーモニックフレーズをシードに変換することを可能にします。文字列コードはキー導出における追加のエントロピー源として機能し、システムの堅牢性を保証します。

# デジタル署名
<partId>76b58a00-0c18-54b9-870d-6b7e34029db8</partId>

## デジタル署名と楕円曲線
<chapterId>c9dd9672-6da1-57f8-9871-8b28994d4c1a</chapterId>

これらの有名なビットコインはどこに保存されているのでしょうか？一般に考えられるビットコインウォレットにはありません。実際には、ビットコインウォレットはビットコインの所有権を証明するために必要な秘密キーを保存します。ビットコイン自体は、すべての取引をアーカイブする分散型データベースであるブロックチェーンに記録されています。

ビットコインシステムでは、アカウントの単位はビットコイン（小文字の「b」に注意）です。それは8小数点まで分割可能で、最小単位はサトシです。UTXO、または「Unspent Transaction Outputs」は、秘密キーに数学的にリンクされた公開キーに属する未使用のトランザクション出力を表します。これらのビットコインを使用するには、トランザクションの支払い条件を満たす必要があります。典型的な支払い条件には、ユーザーがUTXOに関連付けられた公開キーの正当な所有者であることをネットワークの他の参加者に証明することが含まれます。これを行うには、ユーザーは各UTXOにリンクされた公開キーに対応する秘密キーを持っていることを示す必要がありますが、秘密キーを明らかにすることなくこれを行います。

ここでデジタル署名が登場します。これは、特定の公開キーに関連付けられた秘密キーの所持を数学的に証明するものです。このデータ保護技術は、主に楕円曲線暗号学（ECC）という魅力的な暗号学の分野に基づいています。

署名は、ビットコインネットワークの他の参加者によって数学的に検証することができます。
ビットコインの取引のセキュリティを確保するために、ビットコインは2つのデジタル署名プロトコルに依存しています:ECDSA（楕円曲線デジタル署名アルゴリズム）とシュノア。ECDSAは2009年のビットコインの開始時から組み込まれている署名プロトコルであり、シュノア署名は最近の2021年11月に追加されました。これらのプロトコルはどちらも楕円曲線暗号に基づいており、類似の数学的メカニズムを使用していますが、主に署名構造の点で異なります。

このコースでは、ECDSAアルゴリズムについて紹介します。

### 楕円曲線とは何ですか？

楕円曲線暗号は、暗号文脈でその様々な幾何学的および数学的特性を利用する一連のアルゴリズムで、離散対数の計算の難しさに基づいてセキュリティが確保されています。

楕円曲線は、鍵交換から非対称暗号化、デジタル署名に至るまで、ビットコインプロトコルのさまざまな暗号化アプリケーションで役立ちます。

楕円曲線には興味深い特性があります:

- 対称性:楕円曲線上の2点を交差する非垂直線は、必ず曲線と第三の点で交差します。
- 曲線上の点に接する任意の非垂直線は、常に曲線と一意の第二の点で交差します。

ビットコインプロトコルでは、Secp256k1と呼ばれる特定の楕円曲線を暗号化操作に使用しています。

これらの署名メカニズムをより深く掘り下げる前に、楕円曲線が何であるかを理解することが重要です。楕円曲線は、方程式 y² = x³ + ax + b によって定義されます。この曲線上の各点は、暗号化において重要な特有の対称性を持っています。

最終的に、さまざまな楕円曲線が暗号化用途に安全と認識されています。最もよく知られているのは、secp256r1曲線かもしれません。しかし、ビットコインにおいては、サトシ・ナカモトは異なる曲線を選択しました:secp256k1。

この曲線は、パラメータ a=0 および b=7 によって定義され、その方程式は y² = x³ + 7 modulo n です。ここで、n は曲線の位数を決定する素数を表します。

最初の画像は実数体上のsecp256k1曲線とその方程式を表しています。
2番目の画像は、素数 p で割った正の自然数の体 ZP 上のsecp256k1曲線を表しており、点の雲のように見えます。近似を避けるために、この正の自然数の体を使用します。
pは素数であり、使用される曲線の位数です。
最後に、ビットコインプロトコルで使用される方程式は次のとおりです:$$
y^2 = (x^3 + 7) mod(p) $$
ビットコインの楕円曲線の方程式は、前の画像の最後の方程式に対応します。

次のセクションでは、理解を容易にするために実数体上の曲線を使用します。

## 私鍵から公開鍵を計算する
<chapterId>fcb2bd58-5dda-5ecf-bb8f-ad1a0561ab4a</chapterId>

まず、楕円曲線デジタル署名アルゴリズム（ECDSA）の世界に深く潜りましょう。ビットコインはこのデジタル署名アルゴリズムを使用して、プライベートキーとパブリックキーをリンクします。このシステムでは、プライベートキーはランダムまたは擬似ランダムな256ビット数です。理論上、プライベートキーの総数は2^256ですが、実際にはそれよりわずかに少ないです。正確に言うと、ビットコインには有効でない一部の256ビットプライベートキーが存在します。
Bitcoinと互換性を持たせるためには、プライベートキーは1からn-1の間でなければなりません。ここで、nは楕円曲線の位数を表します。これは、Bitcoinのプライベートキーの総可能性が約1.158 x 10^77であることを意味します。これを視覚的に理解するために、これは観測可能な宇宙に存在する原子の数とほぼ同じです。
![image](assets/image/section2/3.webp)

このユニークなプライベートキーはkと表され、公開キーを決定するために使用されます。

公開キーは、Kと表され、プライベートキーからECDSAのような不可逆アルゴリズムを使用して導出される楕円曲線上の点です。プライベートキーを知っている場合、公開キーを取得するのは非常に簡単ですが、公開キーのみを持っている場合、プライベートキーを取得することは不可能です。この不可逆性はBitcoinウォレットのセキュリティの基盤です。

公開キーは512ビットの長さで、x座標が256ビット、y座標が256ビットの曲線上の点に対応しています。しかし、264ビットの数値に圧縮することができます。

![image](assets/image/section2/4.webp)

生成点（G）は、Bitcoinプロトコルですべての公開キーが生成される曲線上の点です。通常、16進数で表される特定のxおよびy座標を持っています。secp256k1の場合、Gの座標は以下の通りです:

- `Gx = 79BE667E F9DCBBAC 55A06295 CE870B07 029BFCDB 2DCE28D9 59F2815B 16F81798`
- `Gy = 483ADA77 26A3C465 5DA4FBFC 0E1108A8 FD17B448 A6855419 9C47D08F FB10D4B8`

この点は、すべての公開キーを導出するために役立ちます。公開キーKを計算するには、単純に点Gをプライベートキーkで乗算します。すなわち:K = k.G

これから、楕円曲線上での点の加算と乗算について学びます。

#### 楕円曲線上の点の加算と倍加

##### 二つの点M + Lの加算

楕円曲線の顕著な特性の一つは、非垂直線が曲線と二点で交差する場合、第三の点、この例では点Oと呼ばれる点でも交差するということです。この特性を利用して点Uを決定します。点Uは点Oの反対の点です。

M + L = U

![image](assets/image/section2/5.webp)

##### 点の自己加算 = 点の倍加

点Gを自身に加算することは、その点で曲線に接線を引くことによって行われます。楕円曲線の特性により、この接線は曲線と第二のユニークな点-Jで交差します。この点の反対、Jが点Gを自身に加算した結果です。
G + G = J

実際に、点GはBitcoinシステムのユーザーのすべての公開キーを計算するための出発点です。

![image](assets/image/section2/6.webp)

#### 楕円曲線上のスカラー乗算

点にnを乗算することは、その点を自身にn回加算することと同等です。

点の倍加と同様に、点Gに点nをスカラー乗算することは、点Gで曲線に接線を引くことによって行われます。この接線は、楕円曲線の特性により、曲線と第二のユニークな点-2Gで交差します。この点の反対、2Gが点Gを自身に加算した結果です。
n = 4 の場合、操作は 4G に到達するまで繰り返されます。
![image](assets/image/section2/7.webp)

3G の計算例は以下の通りです:

![image](assets/image/section2/8.webp)

これらの楕円曲線上の点に対する操作は、公開鍵を計算する基礎です。秘密鍵を知っていれば、公開鍵を導出するのは非常に簡単です。
公開鍵は楕円曲線上の点であり、点 G を k 回加算および倍加した結果です。ここで k = 秘密鍵です。

この例では:

- 秘密鍵 k = 4
- 公開鍵 K = kG = 4G

![image](assets/image/section2/9.webp)

秘密鍵 k を知っていれば、公開鍵 K を計算するのは簡単です。しかし、公開鍵に基づいて秘密鍵を取得することは不可能です。これは点の加算または倍加の結果ですか？

次のレッスンでは、ビットコインを使用するために秘密鍵を使って ECDSA アルゴリズムを使用してデジタル署名がどのように作成されるかを探ります。

## 私の鍵で署名する
<chapterId>bb07826f-826e-5905-b307-3d82001fb778</chapterId>

デジタル署名のプロセスは、秘密鍵の保持者であることを明かさずに証明するための重要な方法です。これは ECDSA アルゴリズムを使用して行われ、一意の nonce の決定、特定の数 V の計算、および二部構成のデジタル署名 S1 と S2 の作成を含みます。
セキュリティ攻撃を避けるためには、常に一意の nonce を使用することが重要です。このルールに従わなかった場合に何が起こるかの悪名高い例は、nonce の再利用が原因で PlayStation 3 がハッキングされたことです。

![](assets/image/section2/10.webp)

手順:

- nonce v を決定します。これは一意のランダム数です。
  Nonce = Number Only Used Once.
  署名を行う者によって決定されます。
- 楕円曲線上の点 G から点 V の楕円曲線上の位置を加算および倍加して計算します。
  その結果 V = v.G
  x と y は平面上の V の座標です。
- S1 を計算します。
  S1 = x mod n ここで n = 曲線の位数、x は平面上の V の座標です。
  注:可能な公開鍵の数は Bitcoin で使用される有限体の楕円曲線上の点の数よりも多いです。
  曲線の位数は公開鍵が曲線上で取り得る可能性にのみ対応します。
- S2 を計算します。
  H(Tx) = トランザクションのハッシュ
  k = 秘密鍵
- 署名を計算します:S1 + S2 の連結。
- 署名検証計算 P を計算します。
  K = 公開鍵

例えば、公開鍵 3G を得るために、点 G に接線を引き、-G の反対を計算して 2G を得て、G と 2G を加算します。トランザクションを行うためには、公開鍵 3G に関連付けられたビットコインを解除するために数字 3 を知っていることを証明する必要があります。

公開鍵 3G に関連付けられた秘密鍵を知っていることを証明するためにデジタル署名を作成するには、まず nonce を計算し、この nonce に関連付けられた点 V（上記の例では 4G）を計算します。次に、公開鍵 3G と点 V を加算して点 T を計算し、これにより 7G が得られます。

![image](assets/image/section2/11.webp)

デジタル署名のプロセスを簡素化しましょう。
前の画像では、秘密鍵 k = 3 です。
このプライベートキーに関連付けられた公開キーKを簡単に計算できます:K = 3G。次に、nonceを擬似ランダムに生成します:v = 4。
このnonceから、次のようにVを計算できます:V = v.G = 4G。

この点Vから、次のように点Tを計算します:
T = t.G = 7G（t = 7の場合）。

これで、デジタル署名の検証に進む時が来ました。

デジタル署名を検証することは、ECDSAアルゴリズムを使用する際の重要なステップであり、送信者のプライベートキーを必要とせずに署名されたメッセージの真正性を確認することができます。詳細は以下の通りです:

この例では、tとVという2つの重要な値があります。
tは数値（この例では7）、Vは楕円曲線上の点（ここでは4Gで表されます）。これらの値はデジタル署名の作成中に生成され、メッセージと共に送信されて検証を可能にします。

検証者がメッセージを受け取ると、これらの2つの値、tとVも受け取ります。

検証者が署名を検証するために従う手順は次のとおりです:

1. まず、メッセージのハッシュを計算します。これをHと呼びます。
2. 次に、u1とu2を計算します。これを行うために、次の式を使用します:
   - u1 = H /\* (S2)^-1 mod n
   - u2 = T /\* (S2)^-1 mod n
     ここで、S2はデジタル署名の第二部分、nは楕円曲線の位数、(S2)^-1はS2のmod nにおける逆数です。
3. 検証者は次に、式 P' = u1 _ G + u2 _ K を使用して楕円曲線上の点P'を計算します。
   - Gは曲線の生成点
   - Kは送信者の公開キー
4. 検証者は次に、点P'のx座標をnで割った余りであるI'を計算します。
5. 最後に、検証者はI'がtに等しいかを確認します。もしそうなら、署名は有効と見なされます。そうでなければ、署名は無効です。
この手順により、対応するプライベートキーを持つ送信者のみがこの検証プロセスを通過する署名を生成できたことが保証されます。

簡単に言うと:
署名を生成する人は、検証する人に数値t（この例ではt = 7）と点Vを提供します。

数値7と点Vから公開キーまたはプライベートキーを特定することは不可能です。

デジタル署名を検証する手順は次のとおりです:

- 曲線上で、検証者は公開キーの点と点Vを加算して点T'を取得します。
- 検証者は数値t.Gを計算します。
- 検証者はt.Gの結果が数値T'と等しいかを確認します。

結論として、デジタル署名の検証はBitcoin取引において不可欠な手続きです。これにより、送信中に署名されたメッセージが変更されていないこと、そして送信者が実際にプライベートキーの保持者であることが保証されます。このデジタル認証技術は、楕円曲線算術を含む複雑な数学的原理に基づいており、プライベートキーの機密性を維持しながら、暗号取引のための堅固なセキュリティ基盤を提供します。

それにもかかわらず、これらのキーの管理や生成、さらには必要に応じての回復は、Bitcoinにおける別の重要な問題です。新しいキーペアをどのように生成するか？ 多数のキーをどのように安全かつ効率的に整理するか？ 必要に応じてそれらをどのように回復するか？
これらの質問に答え、暗号化セキュリティの理解を深めるために、次のコースでは階層的決定論的ウォレット（HDウォレット）の概念とニーモニックフレーズの使用に焦点を当てます。これらのメカニズムは、暗号通貨のキーを効果的に管理しながらセキュリティを強化するための洗練された方法を提供します。
# ニーモニックフレーズ
<partId>4070af16-c8a2-58b5-9871-a22c86c07458</partId>

## ビットコインウォレットの進化
<chapterId>9d9acd5d-a0e5-5dfd-b544-f043fae8840f</chapterId>

階層的決定論的ウォレット、一般にHDウォレットとして知られているものは、暗号通貨エコシステムにおいて重要な役割を果たしています。この分野に新しい人にとっては、「ウォレット」という用語はお金や通貨を保持することを意味するように思えるかもしれませんが、実際には暗号学的なプライベートキーの集合を指します。

初期のウォレットは、プライベートキーを擬似ランダムにグループ化するソフトウェアでしたが、それらの間には接続がありませんでした。これらのウォレットは「Just a Bunch Of Keys」（JBOK）と呼ばれています。

キー間に接続がないため、ユーザーは新しいキーペアを生成するたびに新しいバックアップを作成する必要があります。
ユーザーが常に同じキーペアを使用して機密性を損なうか、ランダムに新しいキーペアを生成して、これらのキーの新しいバックアップを作成する必要があります。

しかし、これらのキーを管理する複雑さは、Bitcoin Improvement Proposals（BIPs）と呼ばれる一連のプロトコルによって相殺されます。これらのアップグレード提案は、HDウォレットの機能性とセキュリティの核心にあります。例えば、2012年に導入された[BIP32](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki)は、キーが決定論的かつ階層的に導出されるという概念を導入することで、これらのキーの生成と保管方法を革命的に変えました。このアイデアは、すべてのキーを一意の情報、つまりシードから決定論的かつ階層的に導出することです。これにより、これらのキーのバックアッププロセスが大幅に簡素化され、セキュリティレベルが維持されます。

その後、[BIP39](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki)は重要な革新を導入しました:24語のニーモニックフレーズ。このシステムは、複雑で覚えにくい数字のシーケンスを一連の普通の単語に変換し、記憶や保管をはるかに簡単にしました。さらに、[BIP38](https://github.com/bitcoin/bips/blob/master/bip-0038.mediawiki)は個々のキーのセキュリティを強化するために追加のパスフレーズを追加することを提案しました。これらの連続した改善は、HDウォレットの構造と階層化を標準化するBIP43とBIP44の基準につながり、一般の人々にとってよりアクセスしやすく、ユーザーフレンドリーになりました。

次のセクションでは、HDウォレットの仕組みについてさらに詳しく掘り下げます。キー導出の原則について議論し、HDウォレットのセキュリティを確保するために不可欠なエントロピーと乱数生成の基本概念を検討します。

要約すると、HDウォレットの設計とセキュリティにおいてBIP32とBIP39の中心的な役割を強調することが重要です。これらのプロトコルにより、単一のシードから複数のキーを生成することが可能になります。このシードはランダムまたは擬似ランダム数であるとされています。今日、これらの基準は、単一の暗号通貨に専用されているか、複数の通貨タイプをサポートしているかにかかわらず、大多数の暗号通貨ウォレットに採用されています。

## エントロピーと乱数生成
<chapterId>b43c715d-affb-56d8-a697-ad5bc2fffd63</chapterId>
ビットコインエコシステムにおけるプライベートキーのセキュリティの重要性は否定できません。実際、これらはビットコイン取引のセキュリティを保証する基石です。予測可能性に関連する脆弱性を避けるために、これらのキーは真にランダムな方法で生成されなければなりませんが、これはすぐに手間のかかる作業になり得ます。問題は、コンピュータサイエンスでは、必ず決定論的なプロセス、つまりコードから派生するため、真にランダムな数を生成することが不可能であるということです。そのため、異なるランダムナンバージェネレーター（RNG）について学ぶことが不可欠です。RNGのタイプは、擬似ランダムナンバージェネレーター（PRNG）から真のランダムナンバージェネレーター（TRNG）、エントロピー源を取り入れたPRNGまでさまざまです。

エントロピーはシステムの「無秩序」状態を指します。外部エントロピー、つまり外部情報源から、ランダムナンバージェネレーターを使用してランダム数を得ることが可能です。

擬似ランダムナンバージェネレーター（PRNG）の動作を見てみましょう。

入力としてシードを取り、これが内部状態0に対応します。
この内部状態に変換関数が適用され、結果として得られる擬似ランダム数が内部状態1に対応します。
この内部状態1に再び変換関数が適用され、新しいランダム数 = 内部状態2が得られます。
これを繰り返します。

主な欠点は、同一のシードが常に同じ出力を生成することです。また、初期の変換関数の結果を知っていれば、プロセスの出力でランダム数を取得することができます。

変換関数の一例はPBKDF2関数です。

**要約すると、暗号学的に安全なPRNGは以下を満たす必要があります:**

- 統計的にランダムであること
- 予測不可能であること
- 結果が明らかになっても耐性を持つこと
- 十分に長い周期を持つこと

ビットコインの場合、プライベートキーはウォレットの基礎となる情報から生成されます。この情報により、決定論的かつ階層的に子キーペアが導出されます。エントロピーはすべてのHDウォレットの基盤ですが、このランダム数を生成する標準は存在しません。したがって、ランダム数の生成はビットコイン取引のセキュリティを確保する上で大きな課題です。

## ニーモニックフレーズ
<chapterId>8f9340c1-e6dc-5557-a2f2-26c9669987d5</chapterId>

ビットコインウォレットのセキュリティはすべてのユーザーにとって重大な関心事です。ウォレットのバックアップを確実にするための重要な方法の一つは、エントロピーとチェックサムに基づいてニーモニックフレーズを生成することです。

エントロピーをニーモニックフレーズに変換するには、単にエントロピーのチェックサムを計算し、エントロピーとチェックサムを連結します。

エントロピーが生成されると、SHA256関数がエントロピーに使用され、ハッシュが作成されます。
ハッシュの最初の8ビットが取得され、これがチェックサムです。
ニーモニックフレーズは、エントロピーにチェックサムが加えられた結果です。

チェックサムは、回復フレーズの正確性を検証するためにあります。このチェックサムがなければ、フレーズの誤りが異なるウォレットの作成を引き起こし、したがって資金の損失につながる可能性があります。チェックサムは、エントロピーをSHA256関数に通し、ハッシュの最初の8ビットを取得することで得られます。

ニーモニックフレーズの異なる標準が存在し、エントロピーのサイズによって異なります。24語の回復フレーズに最も一般的に使用される標準は、エントロピーが256ビットです。チェックサムのサイズは、エントロピーのサイズを32で割ることによって決定されます。
たとえば、256ビットのエントロピーは8ビットのチェックサムを生成します。エントロピーとチェックサムの連結により、それぞれのサイズは128ビット、160ビットなどになります。エントロピーのサイズに応じて、リカバリーフレーズは128ビットで12語、160ビットで15語、256ビットで24語から構成されます。
**ニーモニックフレーズのエンコーディング:**

![image](assets/image/section3/7.webp)

最後の8ビットがチェックサムに対応します。
各11ビットのセグメントは10進数に変換されます。
各10進数はBIP39の2048語のリストからの1語に対応します。最初の4文字の順序が同じ語は存在しないことに注意が必要です。

ビットコインウォレットの完全性を保つためには、24語のリカバリーフレーズをバックアップすることが不可欠です。最も一般的に使用される基準は、128ビットまたは256ビットのエントロピーと、12語または24語の連結に基づいています。パスフレーズを追加することは、ウォレットのセキュリティを強化するための追加オプションです。

結論として、ビットコインウォレットを保護するためのニーモニックフレーズを生成することは重要なプロセスです。エントロピーのサイズに基づいたニーモニックフレーズの基準に従うことが重要です。資金の損失を防ぐためには、24語のリカバリーフレーズをバックアップすることが不可欠です。

## パスフレーズ
<chapterId>6a51b397-f3b5-5084-b151-cef94bc9b93f</chapterId>

パスフレーズは、ビットコインウォレットのセキュリティを高めるために組み込むことができる追加のパスワードです。その使用はオプションであり、ユーザーの裁量によります。ニーモニックフレーズと組み合わせてウォレットのシードの計算を可能にする任意の情報を追加することで、パスフレーズはそのセキュリティを強化します。

![image](assets/image/section3/8.webp)

パスフレーズは、ユーザーが選択したサイズのオプションの暗号化ソルトです。ニーモニックフレーズと組み合わせた際にシードの計算を可能にする任意の情報を追加することで、HDウォレットのセキュリティを向上させます。

ウォレットの作成時に設定されると、ウォレットのすべてのキーの導出に必要です。パスフレーズからシードを生成するためにpbkdf2関数が使用されます。このシードにより、ウォレットのすべての子キーペアの導出が可能になります。パスフレーズが変更されると、ビットコインウォレットは完全に異なるものになります。

パスフレーズはビットコインウォレットのセキュリティを強化するための重要なツールです。たとえば、ニーモニックフレーズの複製やバックアップを容易にするために使用することができます。また、ニーモニックフレーズのランダム生成に関連するリスクを軽減することでウォレットのセキュリティを向上させることもできます。

効果的なパスフレーズは長く（20〜40文字）、多様で（大文字、小文字、数字、記号を使用）、ランダムであるべきです。ユーザーやその環境に直接関連するものではない方が安全です。単純な単語よりもランダムな文字列を使用する方が安全です。

![image](assets/image/section3/9.webp)

パスフレーズは単純なパスワードよりも安全です。理想的なパスフレーズは長く、多様で、ランダムです。それによりウォレットやホットソフトウェアのセキュリティが強化されます。また、冗長で安全なバックアップを作成するために使用することもできます。

ウォレットへのアクセスを失うことを避けるためには、パスフレーズのバックアップに注意を払うことが重要です。パスフレーズはHDウォレットのオプションです。サイコロや他の擬似ランダム数生成器を使用してランダムに生成することができます。パスフレーズやニーモニックフレーズを記憶することは推奨されません。

次のレッスンでは、シードとそれから生成される最初のキーペアの機能について詳しく調べます。このコースをフォローして学習を続けてください。またすぐにお会いできることを楽しみにしています。
# ビットコインウォレットの作成
<partId>9c25e767-7eae-50b8-8c5f-679d8fc83bab</partId>
## シードとマスターキーの作成
<chapterId>63093760-2010-5691-8d0e-9a04732ae557</chapterId>

このコースのこの部分では、プライベートキーとパブリックキーの階層的かつ決定論的な作成と管理を可能にする階層的決定論的ウォレット（HDウォレット）を導出する手順を探ります。

![image](assets/image/section4/0.webp)

HDウォレットの基盤は、ニーモニックフレーズとパスフレーズ（オプションの追加パスワード）という二つの重要な要素に依存しています。これらは合わせてシードを構成し、512ビットの英数字シーケンスであり、ウォレットのキーを導出する基盤として機能します。このシードから、ビットコインウォレットのすべての子キーペアを導出することが可能です。シードは、パスフレーズを使用するかどうかに関わらず、ウォレットに関連付けられたすべてのビットコインへのアクセスを許可する鍵です。

![image](assets/image/section4/1.webp)

シードを取得するために、ニーモニックフレーズとパスフレーズを使用してpbkdf2関数（Password-Based Key Derivation Function 2）が使用されます。pbkdf2の出力は512ビットのシードです。

シードから、HMAC SHA-512（Hash-based Message Authentication Code Secure Hash Algorithm 512）アルゴリズムを使用してマスタープライベートキーとチェーンコードを決定することができます。このアルゴリズムは、結果を生成するためにメッセージとキーを入力として必要とします。マスタープライベートキーはシードとフレーズ「Bitcoin SEED」から計算されます。このフレーズはすべてのHDウォレットのすべての導出に対して同一であり、ウォレット間の一貫性を保証します。

当初、SHA-512関数はビットコインプロトコルに実装されていなかったため、HMAC SHA-512が使用されます。「Bitcoin SEED」というフレーズを使用することで、ユーザーはビットコイン専用のウォレットを生成することが制約されます。HMAC SHA-512の結果は512ビットの数値で、左側の256ビットがマスタープライベートキーを表し、右側の256ビットがマスターチェーンコードを表します。

![image](assets/image/section4/2.webp)

マスタープライベートキーはウォレット内のすべての将来のキーの親キーであり、マスターチェーンコードは子キーの導出に関与します。親ペアの対応するチェーンコードを知らなければ子キーペアを導出することは不可能であることに注意が必要です。

ウォレット内のキーペアは、プライベートキー、パブリックキー、およびチェーンコードで構成されます。チェーンコードは子キーの導出においてランダム性の源を導入し、各キーペアを隔離して情報漏洩を防ぎます。マスタープライベートキーはシードから導出された最初のプライベートキーであり、ウォレットの拡張キーとは関連がありません。

次のレッスンでは、xPub、xPRV、zPubなどの拡張キーについて詳しく探り、それらが使用される理由と構造について理解します。

## 拡張キー
<chapterId>8dcffce1-31bd-5e0b-965b-735f5f9e4602</chapterId>

このレッスンのこの部分では、階層的決定論的ウォレット（HDウォレット）で子キーを導出する際に重要な役割を果たす拡張キー（xPub、zPub、yPub）とそのプレフィックスについて学びます。

![image](assets/image/section4/3.webp)

拡張キーはマスターキーとは異なります。HDウォレットはニーモニックフレーズとシードを生成してマスターキーとマスターチェーンコードを取得します。拡張キーは子キーを導出するために使用され、親キーと対応するチェーンコードの両方が必要です。拡張キーはこれら二つの情報を組み合わせて導出プロセスを簡素化します。

![image](assets/image/section4/4.webp)
拡張公開キーは通常の子公開キーのみを導出できますが、拡張秘密キーは通常の導出またはハード化導出を通じて、子公開キーと子秘密キーの両方を導出することができます。ハード化導出は親の秘密キーからの導出であり、通常の導出は親の公開キーからの導出に対応します。
XPUB接頭辞を持つ拡張キーを使用することで、対応する秘密キーに戻ることなく新しいアドレスを導出でき、これによりセキュリティが向上します。拡張キーに関連付けられたメタデータは、キー階層内での役割と位置についての重要な情報を提供します。

拡張キーは、それが拡張秘密キーか公開キーか、およびその特定の目的を示す特定の接頭辞（XPRV、XPUB、YPUB、ZPUB）によって識別されます。拡張キーに関連付けられたメタデータには、バージョン（接頭辞）、深さ、親キーのフィンガープリント、インデックス、およびペイロード（チェーンコードと親キー）が含まれます。

バージョンはキーのタイプに対応します:xpub、xprvなど。

深さはマスターキーから親キーと子キーの間の導出回数に対応します。

親フィンガープリントは親キーのハッシュ160の最初の4バイトです。
インデックスは同じ深さのキー（兄弟キー）の中で拡張キーを生成するために使用されるペアの番号です。例えば、私たちの3番目のアカウントのxpubを導出したい場合、そのインデックスは2になります（インデックスは0から始まるため）。

ペイロードはチェーンコード（32バイト）と親キー（33バイト）で構成されます。

圧縮公開キーは33バイトのサイズを持ち、生の公開キーは512ビットです。圧縮公開キーは生のキーと同じ情報を保持しますが、サイズが小さくなっています。拡張キーは82バイトのサイズを持ち、その接頭辞は16進数への変換を通じて基数58で表されます。チェックサムはHASH256ハッシュ関数を使用して計算されます。

強化された導出は2のべき乗（2^31）のインデックスから始まります。最も一般的に使用される接頭辞はxpubとzpubであり、それぞれレガシースタンダードとsegwit v1およびsegwit v0に対応していることが注目に値します。

次のレッスンでは、拡張キーとウォレットのマスターキーについて学んだ知識を使用して、子キーペアの導出に焦点を当てます。

## 子キーペアの導出
<chapterId>61c0807c-845b-5076-ad06-7f395b36adfd</chapterId>

思い出してください、私たちはシードとマスターキーの計算について議論しました。これらはHD（階層的決定性）ウォレットの階層的な組織と導出のための最初の重要な要素です。シードは128ビットから256ビットの長さで、ランダムに生成されるか、秘密のフレーズから生成されます。シードは他のすべてのキーの導出に決定的な役割を果たします。マスターキーはシードから導出される最初のキーであり、他のすべての子キーペアの導出を可能にします。

マスターチェーンコードはシードからのウォレット回復において重要な役割を果たします。同じシードから導出されたすべてのキーは同じマスターチェーンコードを持つことに注意してください。

HDウォレットの階層的な組織と導出は、キーとウォレット構造のより効率的な管理を提供します。拡張キーは、親キーペアから子キーペアへの導出を数学的計算と特定のアルゴリズムを使用して可能にします。
子キーペアには、強化キーと通常キーの異なるタイプがあります。拡張公開キーは通常の子公開キーの導出のみを許可し、拡張秘密キーは通常モードまたは強化モードにかかわらず、すべての子キー（公開キーと秘密キーの両方）の導出を許可します。各キーペアには、それらを互いに区別するためのインデックスがあります。
![image](assets/image/section4/8.webp)

子キーの導出には、親キーとインデックス、およびキーペアに関連付けられたチェーンコードを連結して使用するHMAC-SHA512関数が使用されます。通常の子キーは0から2の31乗マイナス1までの範囲のインデックスを持ち、強化子キーは2の31乗から2の32乗マイナス1までの範囲のインデックスを持ちます。

![image](assets/image/section4/9.webp)

![image](assets/image/section4/10.webp)

子キーペアには、強化ペアと通常ペアの2種類があります。子キーを導出するプロセスでは、公開キーを使用して支出条件を生成し、秘密キーは署名に使用されます。拡張公開キーは通常の子公開キーの導出のみを許可し、拡張秘密キーは通常モードまたは強化モードでのすべての子キー（公開および秘密）の導出を許可します。

![image](assets/image/section4/11.webp)
![image](assets/image/section4/12.webp)

強化導出では親の秘密キーを使用し、通常導出では親の公開キーを使用します。強化導出にはHMAC-SHA512関数が使用され、通常導出には512ビットダイジェストが使用されます。子公開キーは、子秘密キーを楕円曲線ジェネレーターに乗算することで得られます。

![image](assets/image/section4/13.webp)
![image](assets/image/section4/14.webp)

階層的に多くのキーペアを決定論的に導出することで、階層的導出のためのツリー構造を作成することができます。このトレーニングの次のレッスンでは、HDウォレットの構造および導出パスについて学び、特に導出パス表記に焦点を当てます。

## ウォレット構造と導出パス
<chapterId>34e1bbda-67de-5493-b268-1fded8d67689</chapterId>

この章では、階層的決定ウォレット（HDウォレット）の導出ツリーの構造について学びます。すでにシード計算、マスターキー、子キーペアの導出について探求しました。これからは、ウォレット内のキーの整理に焦点を当てます。

HDウォレットは、キーを整理するために深さレイヤーを使用します。親ペアから子ペアへの導出は、深さレイヤーに対応します。

![image](assets/image/section4/15.webp)

- 深さ0はマスターキーとマスターチェーンコードに対応します。

- 深さ1は、インデックスによって決定される特定の目的のために子キーを導出するために使用されます。目的はBIP 84およびSegwit v0/v1基準に準拠しています。

- 深さ2は、異なる暗号通貨またはネットワークのアカウントを区別するために使用されます。これにより、異なる資金源に基づいてウォレットを整理することができます。ビットコインの場合、インデックスは0になります。

- 深さ3は、ウォレットを異なるアカウントに整理するために使用され、より明確で整理された構造を提供します。

- 深さ4は、外部チェーンと内部チェーンに対応し、公に通信することを意図したアドレスに使用されます。インデックス0は外部チェーンに関連付けられ、インデックス1は内部チェーンに関連付けられます。各アカウントには2つのチェーンがあります:外部チェーン（0）と内部チェーン（1）。深さ4はまた、マルチ署名ウォレットの場合のスクリプトタイプの管理にも使用されます。
- 標準ウォレットでの受信アドレスには深度5が使用されます。次のセクションでは、子キーペアの導出についてより詳しく検討します。
![image](assets/image/section4/16.webp)

各深度層で、子キーペアを区別するためにインデックスを使用します。

アポストロフィがないインデックスは実際に使用されるインデックスに対応し、アポストロフィがあるインデックスは実際のインデックス + 2^31に対応します。ハード化された導出では、2^31から2^32-1までのインデックスが使用されます。例えば、インデックス44'は実際のインデックス2^31 + 44に対応します。

特定の受信アドレスを生成するために、マスターキーとマスターチェーンコードから子キーペアを導出します。次に、同じ深度で異なる子キーペアを区別するためにインデックスを使用します。

XPUBのような拡張キーを使用すると、複数の人とウォレットを共有できます。導出パスは、外部チェーン（共有を目的としたアドレス）と内部チェーン（おつりアドレス）を区別するために使用されます。

次の章では、受信アドレス、その使用の利点、およびその構築に関わる手順について学びます。

# ビットコインアドレスとは何ですか？
<partId>81ec8d17-f8ee-5aeb-8035-d370866f4281</partId>

## ビットコインアドレス
<chapterId>0a887ed8-3424-5a52-98e1-e4b406150475</chapterId>

この章では、ビットコインシステムで重要な役割を果たす受信アドレスについて探求します。これらは取引で資金を受け取るために使用され、プライベートキーとパブリックキーのペアから生成されます。ビットコインをパブリックキーにロックすることができるPay2PublicKeyというスクリプトタイプがありますが、ユーザーは通常、このスクリプトの代わりに受信アドレスを使用することを好みます。

![image](assets/image/section5/0.webp)

受信者がビットコインを受け取りたい場合、パブリックキーの代わりに送信者に受信アドレスを提供します。アドレスは実際にはパブリックキーのハッシュであり、特定の形式を持っています。パブリックキーは、楕円曲線上での点の加算や倍加などの数学的操作を使用して子プライベートキーから導出されます。

![image](assets/image/section5/1.webp)

アドレスからパブリックキーに逆戻りすることはできないこと、またパブリックキーからプライベートキーに逆戻りすることもできないことに注意することが重要です。アドレスを使用すると、元々は512ビットのパブリックキー情報のサイズが縮小されます。

ビットコインアドレスは使用を容易にするためにサイズが縮小されています。チェックサムがあり、誤字を検出しビットコインの喪失リスクを減らすことができます。一方で、パブリックキーにはチェックサムがないため、誤字が資金の喪失につながる可能性があります。

アドレスはまた、公開情報とプライベート情報の間にセキュリティの第二層を提供し、プライベートキーの制御をより困難にします。

各アドレスは一度だけ使用されるべきであることを強調することが不可欠です。同じアドレスの再利用はプライバシーの問題を引き起こし、避けるべきです。

ビットコインアドレスには異なるプレフィックスが使用されます。例えば、BC1QはSegwit V0アドレスに、BC1PはTaproot/Segwit V1アドレスに対応し、プレフィックス1と3はPay2PublicKeyH/Pay2ScriptH（レガシー）アドレスに関連付けられています。次のレッスンでは、パブリックキーからアドレスを導出する方法をステップバイステップで説明します。

## ビットコインアドレスの作成方法は？
<chapterId>6dee7bf3-7767-5f8d-a01b-659b95cfe0a5</chapterId>

この章では、ビットコイン取引のための受信アドレスの構築について議論します。受信アドレスは、圧縮されたパブリックキーの英数字表現です。パブリックキーを受信アドレスに変換するにはいくつかのステップが含まれます。

### ステップ1: パブリックキーの圧縮

![image](assets/image/section5/14.webp)

アドレスは子パブリックキーから導出されます。
公開鍵は楕円曲線上の点です。楕円曲線の対称性のおかげで、楕円曲線上の点は、x座標に対してyの値が2つの可能性（正または負）のみを持ちます。しかし、ビットコインプロトコルでは、実数の集合ではなく、正の整数の有限集合を扱います。yの2つの可能な値を区別するには、yが偶数か奇数かを示すだけで十分です。

公開鍵の圧縮により、そのサイズは520ビットから264ビットに削減されます。

偶数のyには接頭辞0x02を、奇数のyには0x03を使用します。これが公開鍵の圧縮形式です。

### ステップ2: 圧縮公開鍵のハッシュ化

![image](assets/image/section5/3.webp)

圧縮公開鍵のハッシュ化は、SHA256関数を使用して行われます。その後、ダイジェストにRIPEMD160関数が適用されます。

### ステップ3: ペイロード = アドレスペイロード

![image](assets/image/section5/4.webp)

RIPEMD160(SHA256(K))のバイナリダイジェストは、5ビットのグループに使用されます。各グループは16進数および/または10進数に変換されます。

### ステップ4: BCHプログラムでチェックサム計算のためのメタデータ追加

![image](assets/image/section5/5.webp)

レガシーアドレスの場合、アドレスチェックサムを生成するために二重SHA256ハッシュを使用します。しかし、Segwit V0およびV1アドレスの場合、エラー検出を保証するためにBCHチェックサム技術に依存しています。BCHプログラムは非常に低い確率でエラーを示唆および修正する能力があります。現在、BCHプログラムは修正を提案するために使用されていますが、ユーザーに代わって自動的にそれらを実行するわけではありません。

BCHプログラムには、拡張が必要なHRP（Human Readable Part）を含む複数の入力情報が必要です。HRPの拡張には、各文字をそのASCIIコードに従って2進数でエンコードすることが含まれます。その後、結果の最初の3ビットを取り、10進数に変換します（画像の青色部分）。0のセパレータを挿入します。次に、以前に10進数に変換された各文字の次の5ビットを連結します（画像の黄色部分）。

HRPを10進数で拡張することにより、各文字の最後の5ビットを隔離し、チェックサムを強化します。

Segwit V0バージョンはコード00で表され、"payload"は10進数の黒で示されます。これにはチェックサム用の6文字が予約されています。

### ステップ5: BCHプログラムでのチェックサム計算

![image](assets/image/section5/6.webp)

メタデータを含む入力は、10進数のチェックサムを取得するためにBCHプログラムに提出されます。

ここでチェックサムが得られます。

### ステップ6: アドレスの構築とBech32への変換

![image](assets/image/section5/7.webp)

バージョン、ペイロード、チェックサムの連結によりアドレスが構築されます。10進数の文字は、対応表を使用してBech32文字に変換されます。Bech32アルファベットには、混同を避けるために1、b、i、oを除くすべての英数字が含まれています。

### ステップ7: HRPとセパレータの追加

![image](assets/image/section5/8.webp)

ピンクでチェックサム。
黒でペイロード = 公開鍵のハッシュ。
青でバージョン。
すべてがBech32に変換された後、ビットコイン用に「bc」が追加され、「1」がセパレータとして使用されます。ここがそのアドレスです。
# より深く掘り下げる
<partId>58111408-b734-54db-9ea7-0d5b67f99f99</partId>

## 128回のサイコロのロールからシードを作成する！
<chapterId>0f4d40a7-cf0e-5faf-bc4d-691486771ac1</chapterId>

ニーモニックフレーズを作成することは、暗号通貨ウォレットを保護する上で重要なステップです。ニーモニックフレーズを生成する方法はいくつかありますが、ここではサイコロを使用した手動生成方法に焦点を当てます。この方法は高価値のウォレットには適していないことに注意が必要です。ニーモニックフレーズを生成するためには、オープンソースのソフトウェアやハードウェアウォレットの使用が推奨されます。ニーモニックフレーズを作成するために、サイコロを使ってバイナリ情報を生成します。このプロセスを理解することが目標です。

**ステップ1 - 準備:**
追加のセキュリティのために、Tails OSのような記憶を持たないLinuxディストリビューションをUSBキーにインストールしておくことを確認してください。このチュートリアルはメインウォレットを作成するために使用しないでください。
**ステップ2 - ランダムなバイナリ数の生成:**
サイコロを使ってバイナリ情報を生成します。サイコロを128回振り、各結果を記録します（奇数の場合は1、偶数の場合は0）。

**ステップ3 - バイナリ数の整理:**
得られたバイナリ数をさらなる計算を容易にするために11桁の行に整理します。12行目は7桁のみになります。

**ステップ4 - チェックサムの計算:**
12行目の最後の4桁がチェックサムに対応します。このチェックサムを計算するには、Linuxディストリビューションのターミナルを使用する必要があります。USBキーからブータブルな記憶を持たないディストリビューションである[TailOs](https://tails.boum.org/index.fr.html)の使用が推奨されます。ターミナルで `echo <binary number> | shasum -a 254 -0` コマンドを入力します。`<binary number>`をあなたの128個のゼロとイチのリストに置き換えてください。出力は16進数のハッシュです。このハッシュの最初の文字をメモし、バイナリに変換します。この[表](https://www.educative.io/answers/decimal-binary-and-hex-conversion-table)を参考にしてください。バイナリチェックサム（4桁）をあなたのシートの12行目に追加します。

**ステップ5 - 10進数への変換:**
各行に関連付けられた単語を見つけるためには、まず11ビットの各シリーズを10進数に変換する必要があります。これらのビットはあなたのニーモニックフレーズを表しているため、オンラインコンバーターを使用することはできません。したがって、計算機と次のようなトリックを使用して変換する必要があります:各ビットは2のべき乗に関連付けられているため、左から右に11ランクがあり、それぞれ1024、512、256、128、64、32、16、8、4、2、1に対応します。11ビットのシリーズを10進数に変換するには、1が含まれるランクのみを合計します。たとえば、シリーズ00110111011の場合、次の加算に対応します:256 + 128 + 32 + 16 + 8 + 2 + 1 = 443。各行を10進数に変換できたら、単語にエンコードする前に、すべての行に+1を加えます。なぜなら、BIP39単語リストのインデックスは1から始まるためです。

**ステップ8 - ニーモニックフレーズの生成:**
まず、[2048語のリスト](https://seedxor.com/files/wordlist.pdf)を印刷して、10進数とBIP39の単語を変換してください。このリストのユニークな点は、辞書内の他のどの単語とも最初の4文字が共有されていないことです。次に、各行の10進数に関連付けられた単語を検索します。**ステップ9 - ニーモニックフレーズテスト:**
直ちにSparrow Walletでニーモニックフレーズをテストし、それを使ってウォレットを作成します。無効なチェックサムエラーが表示された場合、計算ミスがあった可能性が高いです。ステップ4に戻ってエラーを修正し、再度Sparrow Walletでテストしてください。これで、128回のサイコロを使って新しいBitcoinウォレットを作成しました。

ニーモニックフレーズを生成することは、暗号通貨ウォレットを安全に保つための重要なプロセスです。より安全な方法、例えばオープンソースソフトウェアやハードウェアウォレットを使用してニーモニックフレーズを生成することが推奨されます。しかし、このワークショップを完了することで、ランダムな数値からBitcoinウォレットを作成する方法をより深く理解するのに役立ちます。

## ボーナス: テオ・パンタミスとのインタビュー
<chapterId>39f0ec5a-e258-55cb-9789-bc46d314d816</chapterId>

Bitcoinプロトコルで広く使用されている暗号技術の方法の一つに、デジタル署名の方法があります。

![ビデオ](https://youtu.be/c9MvtGJsEvY?si=bQ1N5NCd6op0G6nW)

## 結論と終わり
<chapterId>d291428b-3cfa-5394-930e-4b514be82d5a</chapterId>

### お礼とさらなる探求を

Crypto 301コースを完了していただき、心から感謝申し上げます。この経験が豊かで教育的なものであったことを願っています。数学から暗号学、Bitcoinプロトコルの仕組みに至るまで、多くの興味深いトピックをカバーしました。

さらに深く掘り下げたい場合は、追加のリソースを提供します。テオ・パンタミスとロイック・モレル、暗号学の分野で著名な専門家二人との独占インタビューを行いました。このインタビューでは、主題のさまざまな側面を深く探求し、興味深い視点を提供しています。

このインタビューを視聴して、暗号学の魅力的な分野をさらに探求してください。あなたの旅に役立ち、インスピレーションを与えることを願っています。再度、このコースを通じてのご参加とコミットメントに感謝します。

### 私たちをサポートしてください

このコースとこの大学のすべてのコンテンツは、私たちのコミュニティによって無料で提供されています。他の人と共有したり、大学のメンバーになったり、GitHubを通じてその開発に貢献することで、私たちをサポートできます。チーム全員を代表して、ありがとうございます！

### コースの評価

トレーニングの評価システムが新しいE-learningプラットフォームに間もなく統合されます！その間、コースを受講していただき、ありがとうございます。楽しんでいただけた場合は、他の人と共有することを検討してください。