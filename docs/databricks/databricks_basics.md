# [Databricks](databricks_index.md)
## basics
### ネームスペース
- catalog
- schema
- data-object
  - table
  - volume
  - model
  - stored function

### Databricks Lakeflow
#### Lakeflow Connect
Lakeflow Connectは幅広いソースからDatabricks Lakehouseへデータを取り込むためのシンプルで効率的なコネクタを提供する。以下の3つのデータ取り込み方法をサポートしている。
- 手動ファイルアップロード：  
    ローカルファイルを直接Databricksにアップロードする。

- 標準コネクタ：  
    さまざまなソースからのデータ取り込む。

- マネージドコネクタ：  
    SaaSプラットフォームやデータベースなどのエンタープライズアプリケーションからのデータ取り込む

##### Databricksへのデータの取り込み方法
- CREATE TABLE AS
- COPY INTO  
  手動でテーブルにデータを取り込む
- Auto Loader  
  自動的にテーブルにデータを取り込む

#### Lakeflow Spark Declarative Pipelines
build production-grade incremental batch and streaming pipelines.


#### Lakeflow Jobs
orchestration with smart triggers, real-time monitoring, and automated workloads

---

### Databricks AI/BI

- Dashboards
  ダッシュボード(自然言語でグラフの作成することも可能)
- Genie
  自然言語でクエリを発行して、結果を文章、表、ブラフで表示できる


---