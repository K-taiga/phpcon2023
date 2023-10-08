## Laravelの便利な機能
![picture 0](images/fb5b848e6eccef84003eec0afa98d8e38e424854fcccc256cba49bbc5e260642.png)  

![picture 1](images/bc6b722488800f9e245728b6554302ee7f16f1dde6cf9bebd622cd8e99ea68f2.png)  

![picture 2](images/d095ae9452d8cee9acc93b96f05addfef5db55d95909082c6a8484c32c6290d9.png)  

・Laravel Wayにどっぷりつかるのもいいけど、バージョンアップへの追従が大変

・依存のリスクをしっかり考えておくのが大事

## Laravelとわたしたちのコードの距離を保つために

![picture 3](images/ce489f5fbc0b4352cb5dd736061a3170bd8de72de8bd702ba5ac8a8c790287b0.png)  

![picture 4](images/89b34afcc310d35e26cc9d125f4e5f81c65cacf9af07e146992fec8c68e375af.png)  

![picture 5](images/1debe4650e51fd026851b91eff5bbbb44815c2f1582c1c30fa6e5c0aca8c76ec.png)  

・Mailerに依存しないようにinterfaceに依存するようにする

・interfaceと具象クラスの紐づけはService Providerで行う

![picture 6](images/e072bb24079dbbffe79dcea383dddc4cdb22c4fcec32d0e191d561119be9a3c3.png)  

・Eloquentも同様にinterfaceに依存するようにする

![picture 7](images/a4011aa7f44d1b2093af5f9e8ab89e83b04e2fd1f6ef53176e806b245a4f8e6f.png)  

![picture 8](images/a882767b0d946d3c0e58a83997242e9319425b5572a1a4e494bfd9a46ec20930.png)  

・外部のサービスに依存している部分はinterfaceに依存するようにすることでドメインロジックを安全にするいい例

![picture 9](images/26654a5405814a80accba0be40432ad5c88e9123adc6e145df73174c871f7c53.png)  

・どこまでinterfaceを設けるかはフェーズに寄る

・PoCの場合は早くがいいが後戻りはできない可能性があるのでどの段階に入れておくのがいいかを考える

![picture 10](images/b0dd215696ea16c3f4abb0c1bda9345a22de1fce229e88a2e2c8050033017c6a.png)  


