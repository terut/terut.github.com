SocialCoding 
---

\- the beginnig -

<br/>
Togo Terunori (@terut)

どう、最近<br/>SocialCodingしてる？
---


ご清聴ありがとうございました
---

SocialCodingとは何か？
---

<br/>
---
<img src="img/octocat.png" />

<br />
---
<img src="img/GitHub_Logo.png">

<br />
---

つまるところ、ぎっはぶ

<br/>
That's all.

<br/>
英語覚えられるし、ぎっはぶすごい

RubyでSocialCoding
---
 
ソーシャルコーディングの世界 (a\_matsudaさん)

http://speakerdeck.com/u/a\_matsuda/p/social-coding

<br/>
Rubyはキメると気持ちいい (Matz)

みんなでキメると集団トランス状態

どう、最近トランスしてる？
---

<img src="img/3hg.th.jpg" />

宣伝
---

最近、ぎっとは部作りました
---

先生、ゴットハンド、僕が強制的にメンバーになりました

<br/>
---

だがしかし、何をするのかよく分かりません

なぜSocialCodingなのか？ 
---

<br />
---

ライブラリを公開してる人はすごい

<br/>
pull requestを送る = コードレビュー

<br/>
すごい人からアドバイスをもらえる

<br/>
---

同じバグ踏み、同じ作業を繰り返すのはDRYですか？

<br/>
Railsやってるなら DRY! DRY!!

<br/>
pull requestで救われる人がいる

<br/>
---

I used to wanna be a GitHubber, Then i took an arrow in the knee.

(超訳) やってみたいんだけど、膝に矢を受けてしまってな…

<img src="img/arrow.jpg" />

pull requestできる技術力がないんですが？
---

僕もないよ？
---

できることをやればいんじゃないのん？

Issueをあげるだけならできませんか？

Wikiを書くだけでもいいんだよ？

英語できませんですし、おすし？
---

勉強しろ
---

SocialCodingではヘタな英語とCodeで会話する

最悪、Codeさえあれば会話できる

僕は英語できませんけど、Naver辞書はすごい

僕のクソな英語でも<br/>typoとか誰かが直してくれる
---

<img src="img/github1.png" />

SocialCodingとは何か？
---

a\_matsudaさんは言った

<br/>
人間讃歌!!

自由、友愛、平等!!

僕らは基本的人権と参政権を手に入れた!!!

<br/>
であると!

pull request 取り扱い説明書
---

fork
---

<img src="img/fork.png" />

fork
---

<img src="img/fork3.png" />


clone & create branch
---

    $ git clone git@github.com:terut/Shogi.git
    $ cd Shogi
    $ git checkout -b urawaza

clone & create branch
---

masterにpushをするのは邪道

変更を表す作業用branchを作成

edit & pull request
---

    $ vim README.md
    $ git add -A
    $ git commit -m 'Write README.md.' 

rebase before push
---

    $ git remote add upstream git://github.com/wmoai/Shogi.git
    $ git stash
    $ git checkout master
    $ git pull --rebase upstream master
    $ git checkout urawaza
    $ git rebase master urawaza

rebase before push
---

大事なのは本流の差分をpull request前に取り込むこと

メンテナは忙しいのでrebaseで追従しておくのが優しさや！

あとは git stash pop とかで作業を再開する

squash commit & push
---

    $ git rebase -i master
    $ git push origin master
    $ git push orgin urawaza

squash commit & push
---

commitを小さな変更単位にまとめる

こうすることでpull requestを送った場合に変更が追いやすい

アトミックなコミットとか言いますよね

pull request
---

<img src="img/pull_request1.png" />

<img src="img/pull_request2.png" />

pull request
---

<img src="img/pull_request3.png" />

after pull request
---

<img src="img/pull_request4.png" />

discuss about pull request
---

<img src="img/pull_request5.png" />

welcome to the contributor list
---

<img src="img/contrib1.png" />

<img src="img/contrib2.png" />

<br/>
---

<img src="img/finish1.gif" />

これが僕の技術レベルです

@上司 san!<br />Github 有料プランはよ!!
---

みんなでpull requestしてトランスしようず

GitLabは誰も食いつきませんでした

coderwall
---

そしてcoderwallのleaderboardへ

http://coderwall.com/leaderboard

<img src="img/coderwall.png" />
