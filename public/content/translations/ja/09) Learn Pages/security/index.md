---
title: イーサリアムのセキュリティと詐欺対策
description: イーサリアムにおける安全対策
lang: ja
---

# イーサリアムのセキュリティと詐欺対策 {#introduction}

暗号通貨への関心が高まるにつれ、詐欺師やハッカーによるリスクも高まっています。 この記事では、被害に遭うリスクを軽減するためのベストプラクティスをご紹介します。

<Divider />

## 仮想通貨セキュリティ入門 {#crypto-security}

### 知識のレベルアップ {#level-up-your-knowledge}

暗号通貨の仕組みを誤解していると、被害を大きくしてしまう間違いを犯してしまうかもしれません。 例えば、誰かがカスタマーサービスエージェントを装って、あなたの秘密鍵と引き換えに失ったETHを戻せると言った場合、詐欺師らはイーサリアムの分散型ネットワークにそのような機能は無いことを知らない人々を食い物にしています。 イーサリアムの仕組みについての知識を得ることは大切です。

<DocLink to="/what-is-ethereum/">
  イーサリアムとは
</DocLink>

<DocLink to="/eth/">
  イーサとは
</DocLink>
<Divider />

## ウォレットのセキュリティ {#wallet-security}

### 絶対に秘密鍵を他人に教えない {#protect-private-keys}

**どんな理由があっても、秘密鍵は絶対に他人に教えないでください!**

ウォレットの秘密鍵は、イーサリアムウォレットのパスワードです。 リカバリーフレーズを教えてしまうと、あなたのウォレットアドレスを知っている人が、あなたのアカウントの全資産を盗むことができます!

<DocLink to="/wallets/">
  イーサリアムウォレットとは
</DocLink>

#### シードフレーズ/秘密鍵のスクリーンショットを撮らない {#screenshot-private-keys}

シードフレーズや秘密鍵のスクリーンショットを撮ると、クラウドデータプロバイダーへ同期され、ハッカーからアクセスされる危険性があります。 クラウドから秘密鍵を取得することは、ハッカーよく行う攻撃ベクトルです。

### ハードウェアウォレットの使用 {#use-hardware-wallet}

ハードウェアウォレットは秘密鍵をオフラインで保存します。 これらは秘密鍵を保存するための最も安全なウォレットオプションと考えられています。秘密鍵はインターネットに接続されることなく、デバイス上で完全にローカルな状態に保持されます。

秘密鍵をオフラインで保存すると、たとえハッカーがコンピュータをコントロールしたとしても、秘密鍵がハッキングされるリスクを大幅に軽減します。

#### ハードウェアウォレット: {#try-hardware-wallet}

- [Ledger](https://www.ledger.com/)
- [Trezor](https://trezor.io/)

### 送信前にトランザクションを再確認 {#double-check-transactions}

誤ったウォレットアドレスに仮想通貨を送信してしまうことはよくある間違いです。 **イーサリアム上でトランザクションを送ると取り消しができません。**送信先のアドレスの所有者を知っていて、あなたが送金した額を返金してくれるように説得することができなければ、失ったお金を取り戻すことはできません。

トランザクションを送信する前に、送信先アドレスが、意図する受信者のアドレスと正確に一致することを常に確認してください。 また、スマートコントラクトを使ってやり取りする場合にも、署名する前にトランザクションメッセージを読むことが良い方法です。

### スマートコントラクトの使用限度額を設定 {#spend-limits}

スマートコントラクトとやり取りする際は、出金限度額を無制限にしないでください。 出金限度額を無制限にすると、スマートコントラクトがあなたのウォレットの資産をゼロにしてしまう可能性があります。 トランザクションに必要な金額のみを限度額に設定してください。

多くのイーサリアムウォレットは、アカウントの資産が空になってしまうことを防ぐため、利用限度額の設定ができます。

[暗号資金へのスマートコントラクトのアクセスを無効にする方法](/guides/how-to-revoke-token-access/)

<Divider />

## 代表的な詐欺 {#common-scams}

詐欺を完全に阻止することは不可能ですが、最も使用されている手法に注意を向けることで、手口の有効性を抑えることができます。 詐欺には多くのバリエーションがありますが、一般的には同じようなパターンです。 少なくとも、次のことにご留意ください。

- 常に警戒を怠らない
- 無料または割り引かれたETHを誰かがくれるはずはない
- 秘密鍵や個人情報を教えない

### Twitter 広告フィッシング {#ad-phishing}

![Twitter 広告フィッシング](./twitterPhishingScam.png)

Twitter (Xとも知られています) のリンクプレビュー機能 (アンファール) を偽装して、ユーザーが正規のウェブサイトにアクセスしていると思い込ませる可能性のある方法があります。 この技術は、ツイートで共有されたURLのプレビューを生成するTwitterの仕組みを悪用し、例えば_ethereum.org_からのものと表示されます (上に示されています) が、実際には悪意のあるサイトにリダイレクトされています。

特にリンクをクリックした後は、正しいドメインにいるかどうかを常に確認してください。

[詳細はこちら](https://harrydenley.com/faking-twitter-unfurling).

### プレゼント詐欺 {#giveaway}

暗号通貨の最も一般的な詐欺の1つは、プレゼント詐欺です。 プレゼント詐欺は多くの手口がありますが、一般的な手法は、指定されたウォレットアドレスにETHを送金すると、ETHが2倍になって返ってくるというものです。 *口座確認のために仮想通貨を送ると、2倍にしてプレゼントするなどの手口です。*

通常、これらの詐欺は、無料のプレゼントに対して時間制限を設け、偽りの緊急性を装います。

### ソーシャルメディアのハッキング {#social-media-hacks}

この種の詐欺で注目を集めたのは、2020年7月に著名な有名人や組織のTwitterアカウントがハッキングされ、 ハッカーが著名人を騙りハッキングしたアカウントでビットコインのプレゼント告知を投稿した事件です。 詐欺のツイートはすぐに気づかれて削除されましたが、ハッカーは11ビットコイン(2021年9月時点で50万ドル)を持ち逃げしました。

![Twitterでの詐欺行為](./appleTwitterScam.png)

### 著名人からのプレゼント {#celebrity-giveaway}

著名人からのプレゼントもよくある詐欺の手法の1つです。 詐欺師は、著名人のビデオインタビューや講演会を使い、YouTubeでライブ配信します。著名人があたかもライブで暗号通貨のプレゼントのインタビューをしているかのように見せかけます。

この詐欺で最も頻繁に利用されるのはVitalik Buterinですが、暗号通貨に関わるElon Musk氏やCharles Hoskinson氏など他の多くの著名人も利用されています。 著名人を関与させることで、詐欺のライブ配信が正当なものであるかのように見せかけます(怪しそうだけれど、Vitalikが関与しているので大丈夫に違いないと信用性を高めます)。

**プレゼントは常に詐欺です。 これらのアカウントに資金を送ると、永久に戻ってきません。**

![YouTubeでの詐欺行為](./youtubeScam.png)

### サポート詐欺 {#support-scams}

暗号通貨は比較的歴史が浅く、誤解されやすい技術です。 この点を悪用した詐欺が、人気のあるウォレット、取引所、またはブロックチェーンのサポート担当者をかたる、なりすましサポート詐欺です。

イーサリアムについての議論の多くはディスコードで行われます。 サポート詐欺師はディスコードのパブリックチャンネルで質問をしているターゲットを探し、「サポートを提供します」というようなプライベートメッセージを送信します。 信頼を築くことによって、詐欺師はあなたを騙して、秘密鍵を公開させたり、詐欺師のウォレットに資金を送らせようとしたりします。

![ディスコードでのサポート詐欺](./discordScam.png)

原則、プライベートな非公式チャネルを介して、スタッフから連絡を取ることはありません。 サポートを受ける際は、次の基本的なことにご注意ください。

- 秘密鍵、シードフレーズ、パスワードを共有しない
- あなたのコンピュータへのリモートアクセスを許可しない
- 組織の指定されたチャネル外では連絡しない

<InfoBanner emoji=":lock:">
  <div>
    注: サポート詐欺はよくディスコードで起きていますが、暗号通貨に関する議論が行われているチャットアプリケーションや電子メールなどでも起きる可能性があります。
  </div>
</InfoBanner>

### 「ETH2」トークン詐欺 {#eth2-token-scam}

[マージ](/roadmap/merge/)の準備段階で、「ETH2」という用語の混乱を悪用し、ユーザーにETHを「ETH2」トークンとして取引させようとする詐欺が横行しました。 マージにより導入された「ETH2」や他の新しいトークンなどはありません。 マージ前に所有していたETHは、現在も何も変わることなく、同じETHです。 **ETHに関しては、プルーフ・オブ・ワークからプルーフ・オブ・ステークへの移行によって必要となる対応は一切ありません**。

ETHを入金すれば「ETH2」が戻ってくるという「サポート担当」を偽る詐欺があります。 [公式のイーサリアムサポート](/community/support/)というものはなく、新しいトークンも存在しません。 また、ウォレットのシードフレーズは誰にも教えないようにしてください。

_注: ステークされたETHを表す、Rocket PoolのrETH、LidoのstETH、CoinbaseのETH2などデリバティブトークン/ティッカーがありますが、これらは「移行」が必要なものではありません。_

### フィッシング詐欺 {#phishing-scams}

フィッシング詐欺もまた、ウォレットの資金を盗む手法として一般的になっています。

フィッシングメールを送ってユーザーにリンクをクリックさせて、偽のウェブサイトへ誘導し、 シードフレーズを入力させようとしたり、パスワードをリセットさせようとしたり、ETHを送金させようとしたりします。 また、マルウェアを知らないうちにインストールさせて、コンピュータのファイルに詐欺師がアクセスできるようにするフィッシングメールもあります。

もし差出人不明のメールを受け取った場合は、次のことにご注意ください。

- 知らないメールアドレスから送られたリンクや添付ファイルを開かない
- 個人情報やパスワードを誰にも漏らさない
- 差出人不明のメールは削除する

[フィッシング詐欺の回避策の詳細](https://support.mycrypto.com/staying-safe/mycrypto-protips-how-not-to-get-scammed-during-ico)

### 暗号通貨取引ブローカー詐欺 {#broker-scams}

暗号通貨取引ブローカー詐欺師は、暗号通貨ブローカーの専門家を名乗って、あなたの代わりにお金を運用すると言って近づきます。 詐欺師は資金を受け取った後、さらなる投資利益を見逃さないように追加の資金を送るよう求めたり、時には忽然と姿を消す場合もあります。

こうした詐欺師達はしばしば、偽のYouTubeアカウントを使い、「ブローカー」に関して自然さを装った対話を始めて、ターゲットを探します。 通常、これらの動画には正当性を高めるために高評価が付けられていますが、それらはすべてボットアカウントによるものです。

**あなたに代わって投資をしようとするインターネット上の他人を信用しないようにしてください。 暗号通貨を失うことになってしまいます。**

![YouTubeでの取引ブローカー詐欺](./brokerScam.png)

### 暗号通貨マイニングプール詐欺 {#mining-pool-scams}

2022年9月現在、イーサリアムのマイニングはできなくなりましたが、 マイニングプール詐欺は依然として存在しています。 マイニングプール詐欺では、一方的に連絡をよこし、イーサリアムのマイニングプールに参加することで大きな利益が得られると勧誘してきます。 詐欺師は勧誘を続け、たとえどれだけ時間がかかっても連絡を取り続けます。 詐欺師は「イーサリアムのマイニングプールに参加すると、ETHを作るためにあなたの暗号通貨が使用され、配当金はETHで支払われる」と説得してきます。 そして、あなたの暗号通貨が小さなリターンを生み出していることが確認できます。 これはより多額の投資をさせるための手口にすぎません。 最終的に、あなたの資金は見知らぬアドレスに送金され、詐欺師は姿を消します。一方、最近の事件では連絡を取り続けるケースも見られます。

要するに、SNS上でマイニングプールへの参加を呼びかける人には注意が必要です。 一度暗号通貨を失うと、取り戻すことはできません。

留意事項:

- あなたの暗号通貨でお金を稼ぐ方法について連絡してくる人には、注意してください。
- ステーキング、流動性プール、または他の暗号通貨の投資方法について、ご自身で調べてください。
- 詐欺に見られるスキームが正当なものであることは、ほとんどありません。 もし仮に適正なものであったならば、おそらくそれが主流になっていて、すでに聞いたことがあるはずです。

[マイニングプール詐欺で20万ドル損失](https://www.reddit.com/r/CoinBase/comments/r0qe0e/scam_or_possible_incredible_payout/)

### エアドロップ詐欺 {#airdrop-scams}

エアドロップ詐欺は、詐欺プロジェクトがあなたのウォレットに資産(NFTやトークン)をエアドロップし、エアドロップされた資産を受け取るために詐欺ウェブサイトに誘導するという手法です。 受け取ろうとすると、イーサリアムウォレットでサインインし、トランザクションを「承認 」するよう促されます。 このトランザクションによって、公開鍵と秘密鍵が詐欺師に送信されてしまい、あなたのアカウントが危険な状態に晒されてしまいます。 この種の詐欺の別の手口として、詐欺師のアカウントに送金するトランザクションを承認させるものもあります。

[エアドロップ詐欺の詳細](https://www.youtube.com/watch?v=LLL_nQp1lGk)

<Divider />

## ウェブセキュリティ入門 {#web-security}

### 強力なパスワードの使用 {#use-strong-passwords}

[アカウントのハッキングの80%以上は、パスワードの脆弱さ、またはパスワードが盗まれることにより起こっています](https://cloudnine.com/ediscoverydaily/electronic-discovery/80-percent-hacking-related-breaches-related-password-issues-cybersecurity-trends/) 。 文字、数字、記号の長い組み合わせを用いると、アカウントを安全に保つことに役立ちます。

よくある間違いとしては、一般的で関連のある用語をいくつか組み合わせることです。 このようなパスワードは、辞書攻撃と呼ばれるハッキングの攻撃に遭いやすく危険です。

```md
脆弱なパスワード例: CuteFluffyKittens!

強力なパスワード例: ymv\*azu.EAC8eyp8umf
```

もう1つのよくある間違いは、[ソーシャルエンジニアリング](https://wikipedia.org/wiki/Social_engineering_(security))を通して簡単に推測または発見できるパスワードを使用することです。 パスワードに母親の旧姓、子供やペットの名前、生年月日を含めることはハッキングされるリスクが大きくなります。

#### パスワードのグッド・プラクティス: {#good-password-practices}

- パスワードジェネレータや入力フォームで許可される最長のパスワードを使用
- 大文字、小文字、数字、記号を組み合わせる
- パスワードに家族名などの個人情報を使用しない
- よく使われる言葉を避ける

[より強力なパスワードの作成の詳細](https://terranovasecurity.com/how-to-create-a-strong-password-in-7-easy-steps/)

### パスワードの使い回しをしない {#use-unique-passwords}

データ侵害によって明らかになってしまった強力なパスワードは、もはや強力ではありません。 [Have I Been Pwned](https://haveibeenpwned.com)というウェブサイトで、公になっているデータ侵害において、あなたのアカウントが含まれているかどうかを調べることができます。 検索の結果、もしそのデータベースにあなたのアカウントがあれば、**パスワードをすぐに変更してください**。 すべてのアカウントで異なるパスワードにしておくと、いずれかのパスワードが漏洩してもハッカーにすべてのアカウントにアクセスされるリスクを低減します。

### パスワードマネージャーの使用 {#use-password-manager}

<InfoBanner emoji=":bulb:">
  <div>
    パスワードマネージャーを利用すると、強力で一意のパスワードを作成し、それらを覚えておくことができます! パスワードマネージャーの利用を<strong>強く推奨します</strong>(多くは無料で利用可能)。
  </div>
</InfoBanner>

すべてのアカウントで固有の強力なパスワードを覚えておくことは理想的とはいえません。 パスワードマネージャーは、すべてのパスワードを安全に暗号化して保存し、強力なマスターパスワードを利用してそれらにアクセスすることができます。 また、新しいサービスに登録する際、強力なパスワードを提案するため、自分自身でパスワードを作成する必要がなくなります。 また、情報漏洩が起こった場合は、多くのパスワードマネージャーには通知機能があるため、悪意のある攻撃の前にパスワードを変更することができます。

![パスワードマネージャーの使用例](./passwordManager.png)

#### パスワードマネージャー: {#try-password-manager}

- [Bitwarden](https://bitwarden.com/)
- [KeePass](https://keepass.info/)
- [1Password](https://1password.com/)
- または、他の[推奨パスワードマネージャー](https://www.privacytools.io/secure-password-manager)を確認してください

### 二要素認証の使用 {#two-factor-authentication}

あなたのアイデンティティを一意な証明を通して認証することが求められることがあります。 このことを**要素**と呼びます。 3つの主要な要素は次になります。

- 自分自身が知っていること(パスワードやセキュリティ質問など)
- 生体認証(指紋や虹彩/顔認証など)
- 所有しているもの(スマートフォンのセキュリティキーまたは認証アプリ)

**二要素認証(2FA)**を使用することで、追加の*セキュリティ要素*をあなたのオンラインアカウントに提供できます。 2FAにより、パスワードだけではアカウントへアクセスできないことが保証されます。 最も一般的には、二つ目の要素は**時間ベースのワンタイムパスワード (TOTP)**として知られる、ランダム化された6桁のコードを使用します。このコードはGoogle AuthenticatorやAuthyなどの認証アプリからアクセスします。 時間制限のあるコードを生成するシードがあなたのデバイスに保存されているため、この要素は「所有しているもの」です。

<InfoBanner emoji=":lock:">
  <div>
    注: SMSベースの2FAを使用すると<a href="https://www.vice.com/en/article/3kx4ej/sim-jacking-mobile-phone-fraud">SIMハイジャック</a>に遭う恐れがあり、安全ではありません。 最大限に安全を確保するためには、{" "} 
   <a href="https://mashable.com/article/how-to-set-up-google-authenticator">Google Authenticator
</a>
または<a href="https://authy.com/">Authy</a> のようなサービスを利用してください。
  </div>
</InfoBanner>

#### セキュリティキー {#security-keys}

より高度で安全なタイプの二要素認証として、セキュリティキーがあります。 セキュリティキーは、認証アプリに似た機能を持つ物理的なハードウェア認証デバイスです。 セキュリティキーの使用は、二要素認証(2FA)で最も安全な方法です。 これらのキーの多くは、FIDOユニバーサル第二認証要素(U2F)規格を利用しています。 FIDOユニバーサル第二認証要素(U2F)についての詳細は[こちら](https://www.yubico.com/authentication-standards/fido-u2f/)をご覧ください。

二要素認証の説明動画:

<YouTube id="m8jlnZuV1i4" start="3479" />

### ブラウザ拡張機能のアンインストール {#uninstall-browser-extensions}

Chrome拡張機能やFirefoxのアドオンなどのブラウザ拡張機能は、ブラウザの機能を向上しますが、リスクが伴います。 デフォルトでは、ほとんどのブラウザ拡張機能は「サイトデータの読み取りと変更」の権限を要求し、データに対してほとんど何でもできるようにします。 Chrome拡張機能は常に自動的に更新されるため、以前は安全であった拡張機能であっても、悪意のあるコードを含むように更新されてしまう可能性があります。 ほとんどのブラウザ拡張機能は、データを盗もうとしていませんが、それらができるということを認識しておく必要があります。

#### 安全性を確保するためのヒント: {#browser-extension-safety}

- 信頼できるソースからのみブラウザ拡張機能をインストール
- 未使用のブラウザ拡張機能を削除
- 自動更新を無効にするため、ローカルからChrome拡張機能をインストールします (上級者向け)

[ブラウザ拡張機能に関するリスクの詳細](https://www.kaspersky.co.uk/blog/browser-extensions-security/12750/)

<Divider />

## 参考文献 {#further-reading}

### ウェブセキュリティ {#reading-web-security}

- [マルウェアが含まれるChromeとEdgeの悪質なアドオンにより最大300万台のデバイスが感染](https://arstechnica.com/information-technology/2020/12/up-to-3-million-devices-infected-by-malware-laced-chrome-and-edge-add-ons/) - _Dan Goodin_
- [忘れない強力なパスワードを作成する方法](https://www.avg.com/en/signal/how-to-create-a-strong-password-that-you-wont-forget) - _AVG_
- [セキュリティキーとは](https://help.coinbase.com/en/coinbase/getting-started/verify-my-account/security-keys-faq) - _Coinbase_

### 暗号資産のセキュリティ {#reading-crypto-security}

- [自分自身と資金の保護](https://support.mycrypto.com/staying-safe/protecting-yourself-and-your-funds) - _MyCrypto_
- [一般的なクリプトコミュニケーションソフトウェアのセキュリティに関する問題](https://docs.salusec.io/untitled/web3-penetration-test/risks-in-social-media) - _Salus_
- [超初心者とそうでない人のためのセキュリティガイド](https://medium.com/mycrypto/mycryptos-security-guide-for-dummies-and-smart-people-too-ab178299c82e) - _MyCrypto_
- [暗号通貨のセキュリティ: パスワードと認証](https://www.youtube.com/watch?v=m8jlnZuV1i4) - _Andreas M. Antonopoulos_

### 詐欺被害にあわないために {#reading-scam-education}

- [ガイド: 詐欺トークンの見分け方](/guides/how-to-id-scam-tokens/)
- [安全に利用: よくある詐欺](https://support.mycrypto.com/staying-safe/common-scams) - _MyCrypto_
- [詐欺の回避](https://bitcoin.org/en/scams) - _Bitcoin.org_
- [一般的な暗号通貨フィッシングメールとメッセージ](https://twitter.com/tayvano_/status/1516225457640787969) - _Taylor Monahan_

<QuizWidget quizKey="security" />