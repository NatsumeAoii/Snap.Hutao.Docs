---
headerDepth: 2
comment: false
index: false
---

**警告：以下の内容は古い情報である可能性があります。最新の情報については[GitHub](https://github.com/DGP-Studio/Snap.Hutao)をご確認ください。**

# 第2回開発チーム座談会

[GitHubディスカッションスレッド](https://github.com/DGP-Studio/Snap.Hutao/discussions/280)からの転載、グループディスカッションからの要約

## 現在、成果エクスポートのJSON形式もUIGFですか？

A: UIAFです。

## 祈願システムデータのUEFI旧バージョンのインポートをSGのように対応できますか？

A: まず、それはUIGF形式と呼ばれています。また、ずっと対応していますが、SGのインポートとエクスポートのルールが広いため、最初から最後まで当社の製品のみを使用し、正しく使用していれば、インポートとエクスポートの異常は発生しません。

## いつになったらSGのような自動更新チェックとダウンロード機能が実装されますか？

A: 自動更新はMSIXパッケージでは実装できません。更新チェックは今後のバージョンで導入予定です。

## 同じデバイスでSGとSnap Hutaoに同時にログインすると、1つのデバイスとしてカウントされますか？それとも2つのデバイスとしてカウントされますか？

A: 2つのデバイスとしてカウントされます。理論的には、Snap Hutaoを再起動するたびにデバイスを切り替えたことになります。

## Snap Hutaoの一部のページのロードに時間がかかり、使用感に影響があるように感じます。Snap Hutaoのインターフェースが少しカクついているように感じます。

A: 深淵統計ページは1.2.6バージョン以前は確かにロードが遅い問題がありましたが、新バージョンで解決しました。他のページのカクつき問題がある場合は、通常、グラフィックカードの性能が十分ではないか、Snap Hutaoが内蔵グラフィックでレンダリングしていることが原因です。

## 属性統計が頻繁にロードに失敗します。

A: 過去からの問題です。データをバックアップした後、`userdata.db`を削除することで解決できます。

## カスタムWebページ機能は今後も計画がありますか？

A: 慌てないでください。

::: tip マイクロソフト側の問題で、私達には解決できません。

- 管理者として起動しても管理者権限を取得できない場合があります。その場合は、一度閉じてから再度起動する必要があります。
- Snap Hutaoのアイコンサイズを他のアイコンのように小さくできますか？
- 書き込まれたレジストリファイルは、更新時にインストール問題が発生した場合、すべての修復を試みても解決できず、アンインストールと再インストールによる修復の過程で、アンインストール時の残存問題が再インストールに影響を与える可能性はありますか？

:::
::: important
このドキュメントはGoogle Geminiモデルによって翻訳されたものであり、PRによる修正を歓迎します。
:::
