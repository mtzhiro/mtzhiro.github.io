# OSC京都にどれくらいの企業・コミュニティが来てるのかの統計をとってみる・ω・
https://mtzhiro.github.io/opensource/kyoto/staticskyotogroup

まずは単純コピペ作業

http://www.ospn.jp/osc2007-kansai/（あるいは -kyoto）からコピペしてくる簡単なお仕事です。

次に、表計算に「いい感じ」にします。私はXyzzy（Emacsみたいなもん＠Windows）のキーボードマクロでやりました。

企業、コミュニティ名前が載ってるバッファ、年度が載ってるバッファ、組織の種類が載ってるバッファを用意して、それぞれを行ったり来たりするかんたんなキーボードマクロです。
C-X（（キーボードマクロ開始）、C-D（行頭の「・」を消してる）、C-A、C-E、TAB、C-XO（バッファ移動）、C-A、C-@（マークセット）、C-E、E-W（リージョンコピー））、C-XO、C-XO、もとのバッファに戻る、C-Y（貼り付け）、TAB・・的なことを繰り返します。
キリの良いところでC-X）（キーボードマクロ終了）して、あとはC-XEで繰り返していくとこういうリストができます。

    企業名１  年度  組織種類
    企業名２  年度  組織種類
    ：
    コミュニティ名１  年度  組織種類
    ：

できた表計算ファイルがこちら（Googleドライブ上）

https://docs.google.com/spreadsheets/d/1f7suX4Ze01t22F2PAUXUhZsY6FTqAaXkqPnXsKUqnZk/edit#gid=0

イレギュラーな例をさがしてみます。おやおや、１団体で２行も消費している団体があります。。 opennotebook.org[改行](オープンノートブックドットオルグ)...いったいどんな団体でしょうか？まったく、主催者の顔が見てみたいですね！！←すんません、ボケてます、この記事を書いている本人の団体です ^^;;; すいません・・

COUNFIFを使って、かぞえてみます。ドキュメント開いたたびに、COUNTIF走ってたら大変なので、計算結果の「値だけ」を隣の列に貼り付けました。計算式のサンプル=COUNTIF($C$6:$C$1152,C3)　（このサンプルは、セルC3にある団体名を12年分の団体名リスト$C$6:$C$1152から探そうとしています。）

おお！　協賛~後援~参加数 「12」の団体がたくさんあります！　OSC京都は2018年(この記事を書いてる年)で12回目なので、「12」は満点ですね！

書き出しておきましょう。

    日本仮想化技術株式会社 協賛
    株式会社オライリー・ジャパン 協賛
    株式会社技術評論社(Software Design) 協賛
    株式会社翔泳社 協賛
    ソフトバンク クリエイティブ株式会社 協賛
    株式会社日経BP - 日経Linux 協賛
    日本UNIXユーザ会  後援
    Ubuntu Japanese Team
    日本NetBSDユーザーグループ
    日本Sambaユーザ会

さて、この時点ですでに、実は本筋から外れてるのですが^^;;;・・この「カウントプロジェクト」の当初の目的は「OSC京都参加の「老舗」を探そう[特にコミュニティ]」でした・・ここまでの計算・作業結果で、若い年度ですでに、多くの参加回数の数字を重ねている団体は「老舗」と言えそうです。抜き出してみます。だいたい「6」回以上が目安になりそうです。

はじめのころ、3回　2007-2009年を調べてみます。

    Ubuntu Japanese Team	12
    日本NetBSDユーザーグループ	12
    日本Sambaユーザ会	12
    Firebird日本ユーザー会	7
    Geeklog Japanese	7
    Momonga Project	7
    小江戸らぐ	7
    Firebird日本ユーザー会	7
    オープンソースビジネス推進協議会	7
    LILO	6

だいたいこんな感じですね－。回数順、登場早い（参加早い）順です。

まずは、このリストをもとに、当初の目的である、「OSC京都参加の「老舗」を探したら[特にコミュニティ]、そこのブログに当時の写真があるんちゃうか」プロジェクトに戻ってみます。

【ベースになってる活動の趣旨的に、perlとかのone-linerで数え上げたらいいんちゃう？んで、そのコードを公開したらーー？】というツッコミがあるかと思いますが、少々お待ちくだされ・・ ^^;



