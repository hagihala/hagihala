Jenkins で何ができるか
======================

-   任意のコマンドの実行をジョブ管理

-   様々なイベントをトリガにして実行

    -   リポジトリの push

    -   HTTP API

        -   webhook (GitHub の操作とか。基本的になんでも)

        -   スクリプトから叩く

        -   他のジョブから呼び出す

    -   定期実行

        -   cron ライクなフォーマットで指定

        -   要するにリッチな cron として使える

-   git リポジトリとの連携が充実

    -   上記 webhook と組み合わせて、 push されたタイミングで実行など

    -   リポジトリから同期してきて実行など、常に最新のコードを実行することができる

-   master - slave (executor) 構成を組んで分散処理

    -   オートスケールもプラグインにより可能

ビルド・テストツールではないのか？
----------------------------------

-   もちろんビルドやテストもできるけど、その枠にとどまらず、もっと汎用的なジョブ管理ツールだと思う

-   CI/CD ツールという呼ばれ方もしてる。といってもそれ系の本を読んだこと無いし
    CI/CD の世間一般の定義を hagihala はあまり知らない

なぜ本番環境やデプロイなどに使わないのか？
------------------------------------------

-   デプロイには使えばいいと思う

-   開発補助用のバッチも、 cron の代わりに使ってよさそう

-   本番環境のバッチに使うには、少々リッチすぎるのと、動かなくなった時の対処が厄介な気がする

    -   パフォーマンス上の懸念、可用性・メンテナンス性の懸念

-   相応に複雑なシステムなので、何かうまく動かなかった時に素早く対処できる体制・人がないと怖い
