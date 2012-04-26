AWSでのデプロイの話
---

Terunori Togo (@terut)

デプロイといえば
---

Capistrano
---

多分に偏見が入っています

デプロイするには
---

deploy.rb書いて

    $ bundle exec cap production deploy

capistrano_extは使ってるよね、ね

簡単ですね
---

ある日
---

某PHPプロジェクト降臨

AWS使ってた
---

簡単ですね
---

僕等にはCapistranoあるし、PHPでの採用実績も<br/>
色々あるっぽい

AWSは簡単じゃなかった
---

<img src="img/freeza.jpg" width="45%"/>

Auto Scaling
---

ELB（ロードバランサ）にぶらさがってるインスタンスの<br/>
CPU使用率の平均が50%以上だったらインスタンス追加<br/>
とかできる

Capistranoによるデプロイ
---

デプロイ先は固定であり、勝手に増殖するインスタンスの<br/>
面倒は見れない

<img src="img/nandatte--.jpg" />

かくして僕の切り札は<br/>やぶれたやばい
---

先人の知恵
---

某PHPプロジェクトはよく考えられてた<br/>

説明しよう
---

<img src="img/svn-deploy.png" width="90%"/>

頭よい
---

僕にはセンスなんてなかったんやー

Batch散らばりすぎやばい
---

集約したいよね、ね
 
セイヤーッ！
---

<img src="img/aws-desigin.png" width="90%"/>

http://aws.clouddesignpattern.org

クラウドデザインパターン
---

センスのない僕とー、AWSクラウドデザインパターンがー、<br/>
出会ったー

Clone Server Pattern
---

<img src="img/clone-server.png" />

俺たちのrsync
---

そうやrsyncやrsyncなんやー

NEW アプローチ
---

<img src="img/owl.jpeg" width="45%"/>

owlsync
---

<img src="img/owlsync.png" width="90%" />

仕組み
---

Deploy ServerにAuto Scalingであがってきたインスタンスを
監視するデーモンを立てて新しく立ち上がってきたらrsync

既に同期したものは同期しない

<br/>
https://github.com/terut/owlsync

動作確認して本番投入
---

できませんでした
---

<img src="img/hammer.jpeg" width="45%" />

言い訳
---

* Twigがowner apacheではいて発狂
* cronの設定ファイルはowner rootじゃないと動かない発狂
* つまりdeploy用のユーザとrootとapacheが入り乱れて発狂 
* rsyncがsudoで動くように各サーバにrsync用のスクリプトを置く必要があって発狂
* owlsyncみたいなテストないgemは使うなってばあちゃんが言ってた
* 設計固まってなかったので試してみて成功したらテスト書くつもりだったけど言い訳
* テスト書きますすいません

先人の知恵は偉大
---

さっさと安定させたかったので、svnのデプロイを<br/>
gitにリプレイスした

かっー、安定運用いいわー、かっー
---

Shibuya.rbでヒント得た
---

* user scriptで起動時にrsync
* s3syncを使って同期(できるのかしら)
* もっと良い方法あれば教えて

<br/>
NFSは止まると処理がブロックされてアボーンするので<br/>やりたくない

AWSこわくない
---

AWSで楽しいデプロイライフを！

間違ってもrootでシステムを運用するんじゃないぞ！
