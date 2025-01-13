---
category: [開発ログ]
order: 1
comment: false
description: この記事の内容は、Snap Hutao **1.4.11〜1.8.4バージョン**から1.9.0以降のバージョンへのアップグレードに適用されます
---

# 1.9.0 バージョンの重大な変更点に関する詳細な解説

この記事の内容は、Snap Hutao **1.4.11〜1.8.4バージョン**から1.9.0以降のバージョンへのアップグレードに適用されます

::: important
この翻訳はGoogle Geminiモデルによって作成されたものであり、PRによる修正を歓迎します。
:::

## 前書き

Snap Hutao は、MSIX形式のWindowsサンドボックスアプリケーションであり、インストールの利便性とAppXアプリケーションの安全性を提供します。インストールパッケージに対する強制的なコード署名は、安全性を保証する重要な要素の一つです。インストールパッケージが改ざんされた場合、Windows App Installerは署名が破損しているためにエラーを表示し、ユーザーがインストールすることを禁止します。これは、主要なモバイルOSではすでに普及しています。Windowsプラットフォームでは、厳格な身元審査制度のため、コード署名証明書の価格は常に高額に維持されています。

Snap Hutaoは、1.4.11バージョン以前は、自己署名証明書の方法を使用していました。このモードでは、ユーザーは手動でDGP-Studioの証明書をインストールして、オペレーティングシステムがDGP-Studio証明書で署名されたアプリケーションをコンピューターにインストールできるようにする必要がありました。1.4.11バージョン以降、Snap HutaoはMicrosoft Storeに掲載され、Microsoftは胡桃の開発者アカウントにGUID `35C8E923-85DF-49A7-9172-B39DC6312C52`を提供し、このGUIDをユーザー名としてSnap Hutaoに無料の署名を提供しました。msixインストールパッケージを使用してSnap Hutaoを更新することに慣れている場合は、常に発行者欄にこのGUIDが表示されるはずです。

Microsoft Storeでの公開により、Snap Hutaoのユーザーは手動で署名証明書をインストールする必要がなくなり、Snap Hutaoインストールパッケージの配布もサポートされ、開発チームのコストを大幅に削減できました。しかし、面倒で冗長な審査プロセスがSnap Hutaoの開発計画を頻繁に妨害するため、開発チームは過去半年間、解決策を探し続けていました。SignPathは、オーストリアのウィーンに拠点を置く、コード署名統合ソフトウェアを提供する企業です。2023年12月初旬、Snap Hutaoの開発チームは、SignPath Foundationの支援をなんとか得て、提供されるコード署名証明書をSnap Hutaoの署名に無料で使用することが許可されました。これはSnap Hutaoプロジェクトを大いに助けました。Snap HutaoがMicrosoft Storeの束縛から解放されることを許可しただけでなく、毎年高額な証明書費用も回避できました。

**新しい証明書への移行により、パッケージ名の競合問題が発生するため、Snap Hutaoはすべてのユーザーが1.9.0以降のバージョンに更新できるように、以下に詳細な説明を提供します。**

## 1.9.0 バージョンへのアップグレード

### バージョンリリース

Snap Hutao 1.9.0バージョンは、2023年クリスマスの前の週末にリリースされる予定です。GitHub、極狐GitLab、公式サイト、およびコミュニティを通じて、インストールパッケージのダウンロードアドレスを公開します。

> 1.9.0 バージョンはすでにリリースされています。[クイックスタート](../quick-start.md#全新安装)ページで入手してください

### 旧バージョンのアンインストール

パッケージ名と署名の競合により、このインストールパッケージを直接インストールすると、システムバージョンに応じて問題が発生します。

| システムバージョン |                                         予想される問題                                          |
| :----------------: | :---------------------------------------------------------------------------------------------: |
|     Windows 10     |                           インストール不可；署名とパッケージ名が競合                            |
|     Windows 11     | インストール成功；<br/>旧バージョンのSnap Hutaoと同名で共存し、プログラムの実行エラーが発生する |

上記の問題のため、まず旧バージョンのSnap Hutaoをアンインストールしてから、1.9.0バージョンのインストールパッケージをインストールする必要があります。

> **Snap Hutaoをアンインストールする方法**：スタートメニューでSnap Hutaoを見つけ、右クリックしてアンインストールします。Windowsアプリ設定で見つけてアンインストールを選択することも簡単な方法です。

**重要なデータ（ログイン済みのmiHoYoアカウント、祈願履歴、アチーブメントデータ、深境螺旋挑戦記録、自分のキャラクターキャッシュデータ、育成計画を含む）は失われず、ローカルコンピューターのSnap Hutaoデータディレクトリに保存されたままになります。**ただし、以下のデータはリセットされます。

1. Snap Hutaoの実行回数カウント
2. データフォルダーのパス **（以前にデータディレクトリを変更した場合は、データディレクトリのパスを覚えておいてください）**
3. Snap Hutaoアカウントのログイン状態
4. 閉じられたSnap Hutaoのお知らせマーク
5. 育成計画のプリセットレベル情報
6. ホームページのダッシュボードカードの状態
7. 自動連打機能の状態

### 新バージョンのインストール

![1.8.5バージョンインストールファイル](/images/202312/1-8-5-installer.png)

ダウンロードした1.9.0バージョンのインストールパッケージを実行します。インストール画面で発行者が `SignPath Foundation` であることを確認できたら、インストールをクリックすると、新しいバージョンのSnap Hutaoをインストールできます！

**旧バージョンでデータディレクトリの場所を変更した場合は、起動後に設定でデータディレクトリのパスを再度選択してデータを復元する必要があります。データディレクトリを一度も設定したことがない場合、データは直接ロードされるため、追加の設定は必要ありません。**

## 今後の計画

> Microsoft Store、今後のリリース、ソフトウェアの安全性...

Microsoft Storeで公開されたアプリケーションの発行者名は、Microsoftが指定したGUIDである必要があり、`SignPath Foundation`のような「カスタム」の名前は使用できません。異なる署名パッケージ間の共存問題を解決するためのより良い方法がない限り、今後はMicrosoft Storeで更新バージョンを公開する予定はありません。Snap HutaoはMicrosoftの認証を受けなくなりますが、SignPathの制限により、Snap HutaoはGitHubコードリポジトリから直接コンパイルおよびビルドされたリリースパッケージのみを使用できます。これは、ユーザーのインストールパッケージ内のコードが100％私たちのGitHubコードリポジトリからのものであることを意味し、誰もがコードをレビューして開発に参加する権利があります。

1.9.0バージョン以降のクライアントには、新しいリリース方法に対応するためのソフトウェア更新モジュールが組み込まれます。ユーザーが更新に必要な操作をできる限り減らすように努めます。この機能はまったく新しい機能であるため、現在も展開中です。プログラム内のお知らせとコミュニティを継続して確認し、情報を入手してください！