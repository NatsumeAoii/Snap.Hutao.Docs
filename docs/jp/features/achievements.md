---
headerDepth: 2
category: [機能, チュートリアル]
tag: [アチーブメント]
order: 6
comment: false
description: Snap Hutaoは、原神のアチーブメント管理機能を提供し、すべてのアチーブメントの状態の閲覧と管理をサポートし、強力なフィルターシステムで特定のアチーブメントを簡単に検索できます。
---

# アチーブメント管理

::: important
この翻訳はGoogle Geminiモデルによって作成されたものであり、PRによる修正を歓迎します。
:::

Snap Hutaoは、原神の包括的なアチーブメント管理機能を提供し、すべてのアチーブメントの状態の閲覧と管理をサポートします。ユーザーは、さまざまなフィルタリング方法を使用して、アチーブメントをすばやく見つけ、管理エクスペリエンスを最適化できます。

<!-- more -->

![アチーブメント管理インターフェース](https://img.alicdn.com/imgextra/i1/1797064093/O1CN01fApvim1g6e0xyGQvS_!!1797064093.png_.webp)

初めて使用するときは、プロンプトに従って「新規アーカイブを作成」ボタンをクリックして、アチーブメントアーカイブを作成し、名前を付けます。最初のアーカイブを作成した後、ユーザーは右上隅の「新規アーカイブを作成」ボタンをクリックして、異なるアカウント用に独立したアチーブメントアーカイブを作成できます。

## アチーブメントのフィルタリング

Snap Hutaoは、さまざまな柔軟なアチーブメントフィルタリング方法をサポートしています。

- 右上隅の隠しメニューをクリックし、`デイリー依頼のアチーブメントのみ` オプションを選択して、デイリー依頼で完了する必要がある隠されたアチーブメントをフィルタリングします。
- 検索ボックスにバージョン番号（例：`5.3`）を入力して、対応するバージョンのアチーブメントを検索します。
- 関連するモンスター名（例：`無相の炎`）を入力して、関連するアチーブメントをすばやく見つけます。
- アチーブメントの一部名（例：`四風`）を入力して、あいまい検索を実行します。
- 完全なアチーブメント番号（例：`84575`）を入力して、目的のアチーブメントを正確に検索します。

## アチーブメントのインポート <Badge text="UIAF" type="info" />

Snap Hutaoは、[UIAF 統一交換可能アチーブメント標準](https://uigf.org/zh/standards/uiaf.html)を介したアチーブメントデータのインポートをサポートしています。

- ユーザーは、URLプロトコルまたはクリップボードを介して、**サードパーティのアチーブメントエクスポートツール**からデータをインポートできます。
- アチーブメントページの右上隅にある隠しメニューの「インポート」ボタンをクリックし、「UIAFファイルからインポート」を選択して、UIAFデータ形式に準拠したアチーブメントデータをロードします。

::: tip
複数のバージョンのSnap Hutao（Alpha版や正式版など）をインストールしている場合、`URL:hutao`リンクのデフォルトのターゲットアプリケーションを変更する必要があります。「Windows設定」-「アプリ」-「デフォルトアプリ」-「プロトコル別のデフォルトアプリを指定」で`URL:hutao`項目を見つけ、アイコンをクリックして変更できます。
:::

## アチーブメントのエクスポート <Badge text="UIAF" type="info" />

アチーブメントページの右上隅にある隠しメニューの「エクスポート」ボタンをクリックし、ディレクトリを選択してファイル名を指定すると、アチーブメントデータはUIAF形式でエクスポートされ、指定された場所に保存されます。

## アーカイブの削除

ユーザーは、右上隅の隠しメニューの「現在のアーカイブを削除」オプションを使用して、現在のアチーブメントアーカイブを削除できます。

## 推奨されるアチーブメント認識ツール

- [YaeAchievement](https://github.com/HolographicHat/YaeAchievement) <Badge text="ワンクリックでアチーブメントをエクスポート" type="tip" />
- [椰羊 cocogoat](https://cocogoat.work/) <Badge text="アチーブメント攻略" type="tip" />