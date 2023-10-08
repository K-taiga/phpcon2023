## readonly property

・コンストラクタでのみ値を代入できそのプロパティは読み取り専用になる

・protected readonlyのように記述する

・そのプロパティのみをもったクラスがreadonly Class

## Immutable

・Carbonだとしたら今日の日付を取得しようとするがインスタンにaddDays(1)していたら明日の日付が取得できてしまう

・CarbonでImmutableをするにはCarbonImmutable

・Mutableだといつどこでプロパティが書き換えられる可能性がある、すべての実装を見て書き換わっていないか確認する必要がある

・readonly Classならそのクラスのみを見ればよい

・Immutableにすると複雑さを減らしシンプルに目の前の実装のみを見れば良くなる

## readonly Classをいつ使うのか

・小規模なプロジェクトでは使わなくても良くCRUDのみのばあいはスピードが落ちる可能性がある

・中〜大規模でビジネスロジックが複雑になりそうな場合は効果が多い


## readonly Classのつらさ

・ORMからの変換が面倒

・Eloquentはテーブルのレコードを抽象的にしたもので、フロントなどに持ち込むから複雑になる

・Eloquentからreadonly Classに変換している

・RepositoryパターンでEloquentの処理を閉じている

・readonlyの一部の値を変更する場合は一部の値を変更したインスタンスを作成してそれを使って処理をするようにしないといけない

→ その場合は自家製のCopyメソッドを作成する

→ 型情報まではコピーできないのでそこがつらい

→ withHogeメソッドでそのプロパティのみを書き換えるようにする

## まとめ