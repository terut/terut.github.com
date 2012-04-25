AWSでのデプロイの話
---

Terunori Togo (@terut)

デプロイといえば
---

Capistrano

＊多分に偏見が入っています

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

僕等にはCapistranoあるし、PHPでの採用実績も色々あるっぽい

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

かくして僕の切り札はやぶれたやばい
---

先人の知恵
---

某PHPプロジェクトはよく考えられてた<br/>

説明しよう
---


