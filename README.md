# Sphinx テンプレート

sphinxで文章を書くためのテンプレートです。

[Read the Doc](https://github.com/readthedocs/readthedocs.org)を利用しています。

## 使い方

### 必要なパッケージのインストール
```sh
sudo apt install pandoc
git clone git@github.com:m0hashi/sphinx-template.git your-project-dir
cd your-project-dir
virtualenv -p python3.7 .venv 
source .venv/bin/activate
pip install -r requirements.txt
```

### ドキュメントのビルド
下記コマンドの実行でsourceディレクトリ以下に配置されたリソースがビルドされ、 docs/htmlフォルダ配下にビルド成果物が配置されます。

デフォルトでは docs/index.htmlがドキュメントのルートとなります。
```sh
# your-project-dir
source .venv/bin/activate
make build
```


### ドキュメントのライブプレビュー
sphinx-autobuildモジュールを利用すると、ファイル変更後に自動的にビルドをすることができます。

このテンプレートでは下記コマンドで実行可能です。
```sh
make preview
```

このコマンドは自動ビルド後のドキュメントをローカルにWebサーバを立ててホストします。

ブラウザから下記URLにアクセスして生成されたドキュメントを見ることができます。

```sh
http://localhost:8000
```

## githubへの公開
作成したドキュメントは Github Pagesで公開することができます。

このテンプレートのサンプルも下記GighubPagesでホストされています。

### 手順
masterブランチの/docsを公開する手順を記載します。/docs直下にindex.htmlを始めとするドキュメントが配置されている必要があります。

1. レポジトリのSettingsのタブを選択
   
   ![](/source/_static/readme_pict/settings.png)


2. GitHub PagesのセクションのSourceで、master /branch/docsを選択
   
   ![](/source/_static/readme_pict/github_pages.png)

3. 成功するとホストしたGitHub PagesのURLが表示されます。
   
   ![](/source/_static/readme_pict/published.png)


## 参考
このテンプレートを作成する際に、下記サイトを参考にしました。

- [SphinxとGitHub Pagesで技術ノートを公開しよう！](https://qiita.com/tutuz/items/88a32d94d700b33dc3ea)
- 


