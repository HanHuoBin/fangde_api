# 基金投后

## 投后列表

	GET  /after/fund/list

**请求参数：**
无


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|投后id|int|是|
|title|标题|String|是|
|number|附件个数|int|是|
|type|类型|int|是|
|name|项目标题|String|是|
|condition|状态|int|是|
|update_time|处理时间|int|是|
|dealer|处理人|String|是|
|create_time|添加时间|int|是|
|admin|添加人|String|是|

说明：condition：1/已上线,2/待审核,3/被打回,4/待提交
    type:1/简报,2/消息,3/新闻,4/互助箱


## 投后详情

	GET /after/fund/detail?id=1
	
说明：无
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|投后id|int|是|
|funds_id|基金id|int|是|
|type|类型|int|是|
|title|标题|String|否|
|description|描述|String|否|
|abouts|作者|String|否|
|content|内容|String|否|
|admin_id|添加人|int|是|
|files|附件|int[]|否|
|url|链接|String|否|

说明：type:1/简报,2/消息,3/新闻,4/互助箱

## 投后新增

	POST /after/fund/add
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|fund_id|基金id|int|是|
|type|类型|int|是|
|title|标题|String|否|
|description|描述|String|否|
|abouts|作者|String|否|
|content|内容|String|否|
|admin_id|添加人|int|是|
|files|附件|int[]|否|
|url|链接|String|否|


说明：type:1/简报,2/消息,3/新闻,4/互助箱



**返回参数:**


```json
{
	"code": 200
	"msg": "添加成功"
	"result": []
}
```

## 投后编辑

	POST /after/fund/edit?id=2
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|fund_id|基金id|int|是|
|type|类型|int|是|
|title|标题|String|否|
|description|描述|String|否|
|abouts|作者|String|否|
|content|内容|String|否|
|admin_id|添加人|int|是|
|files|附件|int[]|否|
|url|链接|String|否|

**返回参数:**

```json
{
	"code": 200
	"msg": "编辑成功"
	"result": []
}
```

## 投后删除

	POST /after/fund/del?id=1

**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|投后id|int|是|


**返回参数:**

```json
{
	"code": 200
	"msg": "删除成功"
	"result": []
}
```

## 提交

    POST  /after/fund/commit
    
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|投后id|int|是|


**返回参数:**

```json
{
	"code": 200
	"msg": "提交成功"
	"result": []
}
```


## 审核

    POST  /after/fund/check
    
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|投后id|int|是|


**返回参数:**

```json
{
	"code": 200
	"msg": "审核成功"
	"result": []
}
```


## 打回

    POST  /after/fund/refuse
    
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|投后id|int|是|


**返回参数:**

```json
{
	"code": 200
	"msg": "打回成功"
	"result": []
}
```