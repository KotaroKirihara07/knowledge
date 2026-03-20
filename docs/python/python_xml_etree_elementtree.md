# [Python](python_index.md)
## xml.etree.ElementTree
[xml.etree.ElementTree](https://docs.python.org/ja/3/library/xml.etree.elementtree.html)はXMLデータを解析および作成するためのモジュール

---

### モジュールの読み込み
```
import xml.etree.ElementTree as ET
```

---

### ファイルの操作
#### ファイルを読み込み、Elementオブジェクトを取得する
```
tree = ET.parse("data/example_data.xml")
root = tree.getroot()
```

#### 子ノードを取得する
```
element = root[0]
```

|attribute|description|
|-----|-----|
|element.tag|elementのタグ名|
|element.attrib|elementの属性名とその値|
|element.text|タグで囲まれた値|

|method|description|
|-----|-----|
|element.find("tag_name")|特定のタグ名のElementオブジェクトを一つ返す|
|element.findall("tag_name")|特定のタグ名のElementオブジェクトをすべて返す (引数にXPath式を限定的にサポートしている)|
|element.get("attr_name")|タグ内の指定した属性の値を返す|
|element.set("new_attr_name", "new_attr_value")|タグ内に新しい属性と属性値を追加する|
|element.remove("attr_name")|タグ内の指定した属性と属性値を削除する|
|element.append("tag_name")|新しい子ノードを追加する|

---