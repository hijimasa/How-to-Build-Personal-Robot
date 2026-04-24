# AIによるAIを用いたロボットの作り方入門

AI エージェントを使いこなしながら、部品を焼損させず、機械と電気の両面で自作ロボットを完成させるためのチュートリアルサイトのリポジトリです。「小中学校の理科の授業しか覚えていないが、自分でロボットを作ってみたい」個人開発者向けに設計されています。

執筆方針の詳細は [`docs/CONCEPT.md`](docs/CONCEPT.md) を参照してください。

## ローカルでサイトをプレビューする

依存ライブラリをインストールして、`mkdocs serve` で起動します。

```bash
python -m venv .venv
source .venv/bin/activate   # Windows は .venv\Scripts\activate
pip install -r requirements.txt
mkdocs serve
```

ブラウザで `http://127.0.0.1:8000/` を開くとサイトが見えます。

## サイトをビルドする

```bash
mkdocs build --strict
```

`site/` 以下に静的ファイルが生成されます。

## デプロイ

`main` ブランチへの push で GitHub Actions（`.github/workflows/deploy.yml`）が
自動的に GitHub Pages にデプロイします。手動デプロイする場合：

```bash
mkdocs gh-deploy
```

## ディレクトリ構成（v0.5 構成、全 8 Part / 31 章）

```
.
├── mkdocs.yml                       # MkDocs 設定
├── requirements.txt                 # Python 依存
├── .github/workflows/deploy.yml     # GitHub Pages デプロイ
└── docs/
    ├── CONCEPT.md                   # 編集方針書（v0.5）
    ├── index.ja.md                  # トップページ
    ├── _templates/                  # 章テンプレ
    ├── _assets/fig/                 # SVG 図版
    ├── assets/                      # MathJax 設定・CSS
    ├── getting-started/             # Part I 共通基礎 + Part II 電気の基礎
    ├── workflow-electrical/         # Part III 電気のワークフロー
    ├── topics/                      # Part IV 電気系トピック
    ├── basics-mechanical/           # Part V 機械の基礎
    ├── workflow-mechanical/         # Part VI 機械のワークフロー
    ├── topics-mechanical/           # Part VII 機械系トピック
    ├── projects/                    # Part VIII プロジェクト
    └── appendix/                    # 付録
```

## ライセンス

本文：CC BY 4.0（予定） / コード：MIT（予定）

詳細は CONCEPT.md §11 を参照。
