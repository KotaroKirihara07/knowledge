# Database
## basics
### DBMS(Database Management System)
- 階層型データベース (Hierarchical Database)
- 関係データベース (Relational Database : RDB)
    - Oracle Database : Oracle社のRDBMS
    - SQL Server : Microsoft社のRDBMS
    - DB2 : IBM社のRDBMS
    - PostgreSQL : オープンソースのRDBMS
    - MySQL : オープンソースのRDBMS
- オブジェクト指向データベース (Object Oriented Database : OODB)
- XMLデータベース (XML Database : XMLDB)
- キー・バリュー型データストア (Key-Value Store : KVS)

---

### SQL(Structured Query Language)の記述ルール
- 文の最後は「;」をつける
- キーワードは大文字
- テーブル名の頭文字のみ大文字
- 列名は小文字
- 文字列と日付の定数は「'」(シングルクォーテーション)で囲む。
- 単語の間は半角スペースで区切る

---

### SQLの評価順序
SQLは以下の順序で評価される。そのため、SELECTで列名に名前を付ける場合、気を付ける必要がある。

1. FROM
2. WHERE
3. GROUP BY
4. HAVING
5. SELECT
6. ORDER BY

---

### 構造
- データベース  
  インストールした直後はテンプレート用のデータベースの 「template0」、「template1」 、「postgres」 という名前のデータベースが作成される。 また、任意で新しいデータベースを作成することもできる。
- スキーマ  
  スキーマはデータベースの中に作成することができる。 スキーマはデータベース内に作成されるテーブルや関数といったオブジェクトをグループ化するものである。 スキーマが異なれば同じデータベース内であっても同じテーブル名でテーブルを作成することができる。 データベースを作成すると、自動的に「public」と呼ばれる特別なスキーマが作成されるが、任意で新しい スキーマを作成することもできる。
- テーブル  
  テーブルはスキーマの中に作成することができる。テーブル作成時にスキーマを指定しないと「public」スキーマ内に配置される。

---

### ACID特性
- 原子性 (Atomicity)  
  更新処理がすべて実行されるか、またはすべて実行されない状態で終わることを保証する性質。

- 一貫性 (Consistency)  
  トランザクションに含まれる処理はデータベースにあらかじめ設定された制約を満たすという性質。

- 独立性 (Isolation)  
  トランザクション同士が互いに干渉を受けないことを保証する性質。

- 永続性 (Durability)  
  トランザクションが終了したら、その時点でのデータの状態が保存されることを保証する性質。

---