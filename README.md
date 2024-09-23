# Reflexアプリのデプロイ検証

オススメは方法２

## 方法１: フロントをGitHub Pagesにしたい場合
[reflexのインストール](https://reflex.dev/docs/getting-started/installation/)を行う
1. `python -m venv .venv`
1. `.venv\Scripts\activate.bat`
1. `python -m pip install --upgrade pip setuptools`
1. `pip install reflex`
1. `reflex init`

次に、[Self Hosting](https://reflex.dev/docs/hosting/self-hosting/)を行う
1. `reflex export --frontend-only`
1. `frontend.zip`を解凍し、中身をgitリポジトリに入れる

-> とりあえずフロントエンドについてはデプロイできた。[こんな感じ](https://kensuke-iritani.github.io/)

### バックエンドもどこかでホスティングする場合
- 上のドキュメント曰く、`rxconfig.py`を編集して接続できるらしい
- バックエンド側はrender.com かなぁ、無料らしいし(使ったことない)


## 方法２: [Reflex Hosting Service](https://reflex.dev/docs/hosting/deploy-quick-start/)
-  バックエンド込みで簡単に無料でデプロイ可能
    - カスタムドメインを使う場合、(https://redirect.pizza/)を使うのがおすすめらしい（これはまだ使ってない）
- この方法ならバックエンドもまとめてホスティングできる。[こんな感じ](https://reflex-trial001.reflex.run/)
    - 簡単、手軽
        - githubリポジトリも作成不要
    - コードも一般公開する必要ない
    - ただ機密情報とかを扱うページはデプロイしたくない
- デプロイしたものを消す場合とかはこちら
    - (https://reflex.dev/docs/hosting/hosting-cli-commands#reflex-deployments-delete-)



