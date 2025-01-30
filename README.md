# myProfileTemplate-Svelte

## 概要

sveltekitを使って、自己紹介サイトを作るレポジトリです。
とりあえずフォークして、GitHub PagesとGitHub Actionの設定をすれば https://{自分のGitHubアカウント名}.GitHub.io/{フォークした時のレポジトリ名}/ で自己紹介サイトを公開することができます。

## 手順(初回)

1. GitHubのアカウントを作成
1. GitHub Educationの申請
1. 公開鍵の作成・登録
1. myProfileTemplate-Svelte レポジトリのfork
1. GitHub Pages の設定
1. GitHub Action の設定
1. svelte.config.jsを修正する

### GitHubのアカウントを作成

後日追記

### GitHub Educationの申請

後日追記

### 公開鍵の作成・登録

```bash
$ ssh-keygen -t rsa -b 4096 -C "自分のメールアドレス"
# エンターを連打
$ cat ~/.ssh/id_rsa.pub
# 出てきた文字列をコピーする
```

1. GitHubをブラウザで開いてアイコンをクリックする。
1. Setting を押す。
1. SSH and GPG keys をクリックする。
1. New SSH Key を押して、タイトルを設定、コピーした内容を貼り付けて保存する。

### myProfileTemplate-Svelte レポジトリのfork

後日追記

### GitHub Pages の設定

1. 上部のメニューから　Settings へ移動する。
1. 左のメニューから、Pages へ移動する。
1. Build and deployment の下のセレクトボックスを GitHub Actions に変更する。

### GitHub Actions の設定

1. 上部のメニューから　Actions へ移動する。
1. 緑のボタンを押す。

### aaa

svelte.config.js のレポジトリのパスを自身がフォークの際に設定したレポジトリ名に修正する。

```js
// svelte.config.js
// 例は、レポジトリ名は myProfileTemplate-Svelte となっている。
paths: {
            base: production ? '/myProfileTemplate-Svelte' : '',
        }
```

GitHubにプッシュする。

```bash
$ git add .
$ git commit -m "feat: change base path"
$ git push origin main
```

## 手順(開発)

```bash
$ git pull origin main
$ git add .
$ git commit -m "コミットメッセージ"
$ git push origin main
```
