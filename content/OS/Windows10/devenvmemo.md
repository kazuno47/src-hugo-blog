---
title: "Devenvmemo"
date: 2019-01-07T15:49:04+09:00
draft: false
---

# Windows10 setup memo

## WiFi接続

ネットワークの一覧に接続先が存在しない場合（SSIDが非表示の場合？）設定→ネットワークとインターネット→新しい接続またはネットワークのセットアップ

## ドメイン参加

1. 設定→アカウント→職場または学校にアクセスする
2. ＋接続ボタン
3. ウィンドウ下部にある、ローカルActiveDirectoryうんぬんをクリック
4. ドメイン名を設定
5. ドメインアカウントで認証

## Windows Update

更新プログラムの確認を実施

## ファンクションキー

HP ELITEBOOK は Shift + Fn で function key をロックできる。

## アプリケーションのインストール

- yappa
  - スタートアップに登録する場合、ファイル名を指定して実行から「shell:startup」を実行すると、エクスプローラが開くので、そこにショートカットをコピペする。
- Chrome
- Office2016
- git
  - username, email, sslVerify, keygen あたり。別途、Gitの項目を書く。
- Visual Studio Code
  - C:\Users\{username}\AppData\Roaming\Code\User\ で git-hub に上げている設定を持ってくる。
  - plugin
    - Git History
    - GitLens
    - Japanese Laguage Pack for VisualStudio Code
    - Markdown PDF
    - markdownlint
    - PlantUML
  - これも別途 VSCode の項目を書く
- JetBrains toolbox
- rlogin
- Hugo
- Microsoft To-Do
  - スタートアップに登録する場合、ファイル名を指定して実行から「shell:appsfolder」を実行すると、エクスプローラが開くので、そこにショートカットを作成し、yappa と同じくスタートアップフォルダに配置する。
