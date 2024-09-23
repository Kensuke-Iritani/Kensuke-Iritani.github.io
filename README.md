# Kensuke-Iritani.github.io
pagesへのreflexアプリのデプロイ検証用

## setup 1
[reflexのインストール](https://reflex.dev/docs/getting-started/installation/)を行う
1. `python -m venv .venv`
1. `.venv\Scripts\activate.bat`
1. `python -m pip install --upgrade pip setuptools`
1. `pip install reflex`
1. `reflex init`

## setup 2
1. `reflex export --frontend-only`