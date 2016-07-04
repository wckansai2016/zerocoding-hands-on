Jetpack はインストール・有効化した直後では使用することができません。
WordPress.com アカウントを使用し「WordPress.com と連携」させる必要があります。

しかし、今回のハンズオンでは MAMP や XAMPP といったいわゆるローカル環境で使用するので、「WordPress.com と連携」することができません。
そこで、ローカル環境で Jetpack を使用するには、以下の作業が必要となります。

- WordPress をインストールしたディレクトリ直下の wp-config.php ファイルに以下コードを一行を追加

```php
define( 'JETPACK_DEV_DEBUG', true);
```

例: `http://example.com/wp/` に WordPress をインストールした場合は、`http://example.com/wp/wp-config.php` になります。

#### テキストエディターを使用し、wp-config.php ファイルにコードを追加してみよう

追加する場所は、wp-config.php ファイルに書かれた以下文章の手前がいいでしょう。

英語ならこちら
```php
/* That's all, stop editing! Happy blogging. */
```

日本語ならこちら
```php
/* 編集が必要なのはここまでです ! WordPress でブログをお楽しみください。 */
```

ここに追加

英語ならこちら

```php
define( 'JETPACK_DEV_DEBUG', true);
/* That's all, stop editing! Happy blogging. */
```

日本語ならこちら

```php
define( 'JETPACK_DEV_DEBUG', true);
/* 編集が必要なのはここまでです ! WordPress でブログをお楽しみください。 */
```

[Development Mode &#8212; Jetpack for WordPress](https://jetpack.com/support/development-mode/)

wp-config.php ファイルにコードを追加し、Jetpack 設定画面に以下の文章が表示されれば準備完了です。

> 開発モードで、wp-config.php または他の場所に定義される JETPACK_DEV_DEBUG 定数を経由します。

**注意**

Jetpack の開発モードはあくまで開発中に使用する機能です。
本番環境では、Jetpack の開発モードを使用しないようにしましょう。
