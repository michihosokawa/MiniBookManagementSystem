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
#### Flask起動  
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
CTRL+Cが入力されるまで、Flaskが動作し続けます

#### アプリへのアクセス
- ブラウザで次のURLにアクセスしてください
    - http://localhost:8080

次のような画面が出れば成功です
![start](https://user-images.githubusercontent.com/37906793/48470990-3d5a3480-e836-11e8-9a8e-7190090894dc.png)


### アプリを使う
1. isbnを入力して「登録」ボタンを押します
![regist](https://user-images.githubusercontent.com/37906793/48471080-6ed30000-e836-11e8-8f78-f446eec11e52.png)
    - この時、isbnには「-」を入れないでください
    - 現在は、登録が成功/失敗のメッセージが出ません

2. 「書籍検索」ボタンで「書籍検索」画面に映ります
![search](https://user-images.githubusercontent.com/37906793/48471097-75fa0e00-e836-11e8-8711-f0129d999c63.png)

3. 例えば、タイトルに「Python」と入力して「検索」ボタンをクリックすると、結果が表示されます
![result](https://user-images.githubusercontent.com/37906793/48471113-7db9b280-e836-11e8-8920-9aba5d1b0d89.png)

4. タイトルをクリックすると詳細が表示されます
![book](https://user-images.githubusercontent.com/37906793/48471803-1d2b7500-e838-11e8-8416-935d5dc07c4e.png)


## Authors
- [michihosokawa](https://github.com/michihosokawa)
