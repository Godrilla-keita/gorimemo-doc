<!-- Generator: Widdershins v4.0.1 -->

<h1 id="-">サンプル v0.1.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

ゴリラサンプル

Base URLs:

* <a href="http://hopgn.godrilla.com/v1">http://hopgn.godrilla.com/v1</a>

<h1 id="--default">Default</h1>

## get__{user_id}_posts

`GET /{user_id}/posts`

*投稿されたメモのリストを取得する*

メモは要約レベルで全件取得し、フロントエンドでソートや検索を行う

> Example responses

> 200 Response

```json
[
  {
    "id": "85932a90-17dc-20ba-d20b-40fcf748b8b8",
    "title": "カズヤの即死コンボ解説",
    "description": "回避が遅いキャラに対して、掴みからワンターンキルする方法を解説します",
    "param_name_1": "難易度",
    "param_name_2": "安定度",
    "param_name_3": "気持ちよさ",
    "param_name_4": "平均火力",
    "param_name_5": "最大火力",
    "param_name_6": "コントローラへの被害",
    "param_val_1": 50,
    "param_val_2": 70,
    "param_val_3": 100,
    "param_val_4": 100,
    "param_val_5": 100,
    "param_val_6": 100
  }
]
```

<h3 id="get__{user_id}_posts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|メモデータの取得に成功|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|ユーザーが見つからなかった場合のエラー|[ErrorResponse](#schemaerrorresponse)|

<h3 id="get__{user_id}_posts-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[MemoSummary](#schemamemosummary)]|false|none|none|
|» id|string|false|none|メモID|
|» title|string|false|none|エラーメッセージ|
|» description|string|false|none|説明文|
|» param_name_1|number|false|none|パラメータ名|
|» param_name_2|number|false|none|パラメータ名|
|» param_name_3|number|false|none|パラメータ名|
|» param_name_4|number|false|none|パラメータ名|
|» param_name_5|number|false|none|パラメータ名|
|» param_name_6|number|false|none|パラメータ名|
|» param_val_1|number|false|none|パラメータ値|
|» param_val_2|number|false|none|パラメータ値|
|» param_val_3|number|false|none|パラメータ値|
|» param_val_4|number|false|none|パラメータ値|
|» param_val_5|number|false|none|パラメータ値|
|» param_val_6|number|false|none|パラメータ値|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_ErrorResponse">ErrorResponse</h2>
<!-- backwards compatibility -->
<a id="schemaerrorresponse"></a>
<a id="schema_ErrorResponse"></a>
<a id="tocSerrorresponse"></a>
<a id="tocserrorresponse"></a>

```json
{
  "code": "sample-0001",
  "message": "画面に表示するメッセージ"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|string|false|none|エラーコード|
|message|string|false|none|エラーメッセージ|

<h2 id="tocS_MemoSummary">MemoSummary</h2>
<!-- backwards compatibility -->
<a id="schemamemosummary"></a>
<a id="schema_MemoSummary"></a>
<a id="tocSmemosummary"></a>
<a id="tocsmemosummary"></a>

```json
{
  "id": "85932a90-17dc-20ba-d20b-40fcf748b8b8",
  "title": "カズヤの即死コンボ解説",
  "description": "回避が遅いキャラに対して、掴みからワンターンキルする方法を解説します",
  "param_name_1": "難易度",
  "param_name_2": "安定度",
  "param_name_3": "気持ちよさ",
  "param_name_4": "平均火力",
  "param_name_5": "最大火力",
  "param_name_6": "コントローラへの被害",
  "param_val_1": 50,
  "param_val_2": 70,
  "param_val_3": 100,
  "param_val_4": 100,
  "param_val_5": 100,
  "param_val_6": 100
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|false|none|メモID|
|title|string|false|none|エラーメッセージ|
|description|string|false|none|説明文|
|param_name_1|number|false|none|パラメータ名|
|param_name_2|number|false|none|パラメータ名|
|param_name_3|number|false|none|パラメータ名|
|param_name_4|number|false|none|パラメータ名|
|param_name_5|number|false|none|パラメータ名|
|param_name_6|number|false|none|パラメータ名|
|param_val_1|number|false|none|パラメータ値|
|param_val_2|number|false|none|パラメータ値|
|param_val_3|number|false|none|パラメータ値|
|param_val_4|number|false|none|パラメータ値|
|param_val_5|number|false|none|パラメータ値|
|param_val_6|number|false|none|パラメータ値|

