## 滋賀大学夏期講習「ビジネスで戦うための　Python画像分類塾」へようこそ  Day3

#Practice over the Theory!! せっかくの夏休みに自己研鑽って素敵です。楽しくやりましょう！！  

備忘：リモートワークについて
備忘２：画像分類 パンのレジ きゅうりの仕分け

##Day3  
・さて、最終日です。昨日まで実施してきた技術で、大抵のQiitaやその他WebのPythonCodeは  
  colaboratry で実装できるかと思います。  
  
  初日に、画像のクローラーを検索していただきましたが、実際そんな感じでやっています。  
  使えそうな処理を探して部分的に切り出して実装し、最適化します  
  
  気づきましたか？？ colaboratry 凄いですね opencv も keras も インストールしていません。  
  ローカルで環境作ると、あの時間では厳しかったかもしれません。  
  
  ・昨今の開発でCodeをパクるのは常套手段です。そして、よくできたソリューションは  
  大抵良質なコードで書かれています  
  
  お題：下記に良記事やサンプルをまとめてみました。こちらを読んでいただき、
  　　　まずは感想をディスカッションしましょう。１人１分で11分
  　　　30分程度で読んでみましょう。
  　　　
  それから、実習の実装（10分）にすすみます。
  
  
  良いコードを書く技術  
  https://qiita.com/NoriakiOshita/items/e60ab5bb01b90d927ae5  
  
  読み物；「美しいコード」という概念のない世界で  
  https://enterprisezine.jp/article/detail/9352  
  
  サンプル；open cv のソースコード
  https://github.com/opencv/opencv_contrib/blob/master/samples/python2/common.py
  
  説明向けでやりすぎ。用途は違う
  https://qiita.com/wwacky/items/98d8be2844fa1b778323
  
  一般的と言われる書き方ではない
  https://qiita.com/skyfish20ch/items/781407972c84de05af60
  
  こっちは一般的でした
  https://qiita.com/neet-AI/items/2b3d7f743e4d6c6d8e10
  
  Google Python Style Guide
  http://works.surgo.jp/translation/pyguide.html
  
  【Pythonコーディング規約】PEP 8 vs Google Style
  https://qiita.com/hi-asano/items/f43ced224483ea1f62f4
  
  VSCodeの話ですが：
  https://qiita.com/firedfly/items/00c34018581c6cec9b84
  
  余談ですが、エクストリーム・プログラミング
  https://it-trend.jp/development_tools/article/32-0023
  
  おすすめ本： https://amzn.to/2Quk2mP https://amzn.to/3lkajhn
  
  --ここまで
  
  実習：
  https://oishi-kenko.hatenablog.com/entry/2019/07/05/192425
  
##Day3-2
  GoogleFunction でやりたかったところですが、これは応用編でやってみてください。

  Google Functions  
  https://qiita.com/kai_kou/items/dca21cdfd8375a247c2f  
  ※無料３万円の枠があるもののカードの入力が必要  
  

  手順：実業務レベルです。割と重いです。やり方考えます。
  
  やりたいこと
  ・colaboratryのサーバー化をして、画像を受け取って分類結果をHttpResponseで返却する。
  
  やり方
  ・testprocessで、ic に画像を送信している。これと同じことを受け取るサーバー側で実施する形にする。
  ・下記画像の送受信モジュールを参考にして、ic_module.py をimport し、ic.TestProcess(imgname) を呼び出す。※
  ・※ ic.TestProcess(imgname)は、ファイルに保存された画像を処理しているので、
    image を受け渡す形式のImageTestProcessを追加して ic_module.py に実装する。
  ・TestProcess は保存されたファイルから、ImageTestProcessは、PIL Imageからテストできる形にする。
  
  ・修正前にブランチを作成するとよいです。

        ヒント：
        img = load_img(imgname, target_size=(hw["height"], hw["width"]))    
        ここで、 A PIL Image instance. を返している（https://www.tensorflow.org/api_docs/python/tf/keras/preprocessing/image/load_img?hl=ja）
  
  colaboratryのサーバー化
  https://qiita.com/k_0214/items/dcf14c74779eb9839577
  
  画像の送受信
  https://qiita.com/Motonaga/items/8da21f52e379469d744b
  
  アンケート
  https://forms.office.com/Pages/ResponsePage.aspx?id=ElscFkSOhkquGkFS5N1vj6y-ohaR5l1FmGkaNBWEH35UOFlHNUoxMUcyV1JWWTBJN1BDVFNaRVZRMSQlQCN0PWcu
  
  予備  
  
  OpenCV のアルゴリズムに関して：  
  https://qiita.com/FukuharaYohei/items/ec6dce7cc5ea21a51a82  
  
  GitHubとlocalの連携
  https://qiita.com/Shi-nakaya/items/43c858ea707770c03b17
  
