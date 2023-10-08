## Lambdaのベストプラクティス
- コールドスタートを最小限にする
  - 最初の起動時にLambdaの環境を用意するため起動時に時間がかかる
  - それ以降は

- 関数の依存関係を最小限にする
  - 最後のパッケージを小さくするため

- 関数の実行時間を短くする
  - これはLambdaの制限によるもの

## WebフレームワークとLambda
- BrefというPHPのフレームワークをLambdaに適用する事ができる
  - カスタムランタイムを共有できる

- BrefはAPI GatewayとLambdaの間で橋渡しをしており、Lambdaが理解できるようにリクエストを変換している

- LambdaはPHPは非対応

- Lambdaは処理がなくなったら環境ごと消え、そのtemplateも消えてしまうのでそこらへんは考慮すべき

- Lambdaは関数のパッケージを可能な限り小さくするのがベストプラクティスなのでLaravelのような全部入りのフレームワークを使うのは適していない

- なぜこのようなデメリットが有るなか使ったのか！！

## 技術スタックの一貫性と共有地

- フルサーバーレス(Lambda,API Gateway, DynamoDB, S3)などで構築することでメンテナンスがかなり楽になる

- ゼロスケールはコスト面でお客さんに営業をかけやすい

- Brefを使わなくてもLambda Web Adapterを使えばLaravelを使うことができる

https://aws.amazon.com/jp/builders-flash/202301/lambda-web-adapter/?awsf.filter-name=*all

- Laravelは集合知なので、Laravelを使うことで使えるエンジニアが増える