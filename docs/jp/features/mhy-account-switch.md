---
headerDepth: 2
category: [機能, チュートリアル]
tag: [米游社, HoYoLAB, 複数アカウント, チェックイン]
order: 14
comment: false
description: 米游社（miHoYo BBS）の複数アカウントパネル機能を使用すると、Snap Hutaoに複数の米哈游フォーラムアカウントをログインして自由に切り替えることができ、ツールボックス内で異なるアカウントを使用してさまざまな機能を利用できます。
banner: https://opengraph.snapgenshin.cn/generate?url=https://hut.ao/zh/features/mhy-account-switch.html
---

# 米游社（miHoYo BBS）複数アカウント切り替え

::: important
この翻訳はGoogle Geminiモデルによって作成されたものであり、PRによる修正を歓迎します。
:::

::: tip
Snap Hutaoは、中国大陸版のmiHoYo BBSである**米游社**と、国際版フォーラムである**HoYoLAB**のアカウントをサポートしています。HoYoLABは、中国大陸からのネットワーク接続をデフォルトでブロックするため、Snap Hutaoソフトウェアは、この制限を回避することができません。

- このドキュメントで説明するアカウントの切り替えは、ゲームデータを取得するための**米游社 / HoYoLABアカウント**であり、**原神ゲーム内のアカウント**ではありません。
- この機能を使用する前に、公式の米游社アプリを使用してアカウントにログインし、米游社機能を初期化する必要があります。
  - Snap Hutaoにログインしたアカウント名が「user_123456789」のような形式である場合、初期化されていない可能性があります。

:::

![多アカウント管理サンプル](https://img.alicdn.com/imgextra/i4/1797064093/O1CN01ZhnkRl1g6e0tz18y9_!!1797064093.png.png_.webp)

プログラムのメインインターフェースの左下、設定ボタンの上にアカウントメニューがあり、Snap Hutaoにログインした米游社アカウントを管理できます。表示されるパネルでは、米游社またはHoYoLABアカウントを追加できます。ログイン方法は類似しています。

:::: tabs

@tab 米游社（miHoYo BBS）携帯電話認証コードログイン

::: warning
米游社アカウントが中国大陸版サーバーアカウントにバインドされていることを確認してください。
:::

1. 「携帯電話認証コード」ボタンをクリックし、携帯電話番号を入力して認証コードを送信します。
2. 認証コードを入力して確認すると、しばらくしてアカウントが追加されます。

@tab 米游社（miHoYo BBS）QRコードログイン

::: warning
米游社アカウントが中国大陸版サーバーアカウントにバインドされていることを確認してください。
:::

1. 「QRコードログイン」ボタンをクリックし、QRコードの読み込みを待ちます。
2. 米游社アプリでQRコードをスキャンし、ログインを確認します。
3. しばらくすると、Snap Hutaoにアカウントが追加されます。

@tab HoYoLAB パスワードログイン

::: warning
HoYoLABアカウントが国際版サーバーアカウントにバインドされていることを確認してください。
:::

1. 「パスワードログイン」ボタンをクリックし、アカウントパスワードを入力して確認します。
2. しばらくすると、アカウントが追加されます。

@tab HoYoLAB ソーシャルメディアアカウントログイン

この方法はWebView2ランタイムコンポーネントに依存しています。

::: warning
HoYoLABは、中国大陸からのネットワーク接続をデフォルトでブロックします。
:::

1. 「サードパーティログイン」ボタンをクリックし、WebView2を通じてログインします。
2. しばらくすると、アカウントが追加されます。

@tab Cookieログイン

::: warning
Cookie情報を適切に保管し、アカウントのリスクを回避してください。
:::

STokenを手動で入力してCookieを送信してログインします。

1. 目的のアプリのアイコンをクリックして「手動入力」を選択します。
2. 有効なCookieを入力して確認すると、しばらくしてアカウントが追加されます。
   ::::

- 完了すると、アカウント管理パネルでログインした米游社アカウントを切り替えることができます。
  - 新しく米游社アカウントを追加した後、メインインターフェースの左下にあるアカウント切り替え機能で、新しくログインしたアカウントを手動で1回クリックして、使用状態に設定する必要があります。
  - アカウント管理メニューで、対応するアカウントのCookieをコピーしたり、Snap Hutaoからそのアカウントを削除したりできます。
  - プログラムが管理者モードで実行されていない場合は、アカウントをドラッグして並べ替えることができます。
  - ログインアカウントを選択した後、次のことができます。
    - 「Cookieを更新」ボタンをクリックして、現在保存されているCookieを更新します。
    - 「チェックイン」ボタンをクリックして、miHoYo BBSのチェックインを実行します。米游社アカウントの場合、チェックインを正常に実行するには、まずリスクコントロール状態を解除する必要があります。

::: info セキュリティに関する注意

- `SToken`はセキュリティ上機密性の高いCookieフィールドであり、`SToken`フィールドを含むCookieを、クラウド上やその他のデータセキュリティが保証されていないデバイスに保存すべきではありません。
- Snap HutaoからコピーしたCookieにはこのフィールドが含まれているため、Cookieを受け取る側に`SToken`フィールドを提供するかどうかを慎重に検討してください。
- **Snap HutaoでパスワードまたはCookieを使用して米游社にログインする際、あなたのデータは米游社サーバーとローカルのSnap Hutaoのみで処理され、Snap Hutaoサーバーを含む第三者のサービスを経由することはありません。**

:::

## よくある質問

### 米游社アカウントのログイン状態が頻繁に無効になり、追加したアカウントが消えるのはなぜですか？

- アカウントの米游社Cookieを保存することでログイン状態を維持しています。
- しかし、ユーザーがブラウザやその他のデバイスで**アカウントをログアウト**すると、ログイン状態を維持するCookieが**無効**になります。
- これにより、Snap Hutao上の米游社アカウントが起動後に自動的に削除されます。
- この状況は、ネットワーク接続の問題によりCookieの有効性を確認できないことが原因である可能性もあるため、この状況が発生した場合は、まずSnap Hutaoを再起動してください。
- 2022年10月から、米游社はアカウントが危険と判断される確率を大幅に高めており、[アカウントが危険な状態](../advanced/exceptions.md#状態1034-検証失敗)の場合も、Cookieが有効な状態として認識されなくなります。
- バージョン1.4.15以降では、アカウントパネルでCookieを更新することにより、ログイン状態を更新できます。
