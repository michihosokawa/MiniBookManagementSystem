# Mini Book Management System

簡易的な書籍管理システムです。  
Flask＋Elasticsearchで動作しています

## Requirement
- Elasticsearch6.3
    - 事前にインストールし、http://localhost:9200 でアクセスできることを確認しておいてください
    - 次の2つのプラグインをインストールしておいてください
        - ICU Analysis
        - Japanese (Kuromoji) Analysis

## Usage

### Elasticseachの初期化
- ElasticsearchのINDEXを定義します。（RDBでのTable作成に相当）
    - python initialize.py
    - 「setting.json」「mapping.json」を参照しています
    - すでに、INDEXが作成されていた場合には、該当するINDEXは削除されます

### Flask＋アプリの実行
- python app.py

次のような画面が出れば、成功です
```
 * Serving Flask app "app" (lazy loading)
 * Environment: production
   WARNING: Do not use the development server in a production environment.
   Use a production WSGI server instead.
 * Debug mode: off
 * Running on http://0.0.0.0:8080/ (Press CTRL+C to quit)
```  
CTRL+Cが入力されるまで、アプリが動作し続けます

## Authors
- [michihosokawa](https://github.com/michihosokawa)
