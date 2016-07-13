# 项目投后
## 投后列表

	GET  /after/project/list

**请求参数：**
无


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|
|title|标题|String|是|
|att_number|关注用户|int|是|
|adder|添加者|String|是|
|create_time|添加时间|int|是|



## 投后详情

	GET /after/project/detail?id=1
	
说明：无
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|
|title|标题|String|是|
|description|一句话描述|String|是|
|introduction|项目介绍|String|是|
|image|项目图片|String[]|是|
|logo|项目logo图|String|是|
|tag|标签|String|是|
|province|省份|int|是|
|city|城市|int|是|
|website|网址|String|是|
|business_license|工商资质|String|是|
|invest_process|认投流程|String|是|
|development|发展历程|String|是|

说明：1.项目图片为多张
	 2.工商资质，认投流程都为图片

```json
{
	waiting...
}
```


## 投后新增

	POST /after/project/add
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|project_id|项目id|int|是|
|description|一句话描述|String|是|
|introduction|项目介绍|String|是|
|image|项目图片|String[]|是|
|logo|项目logo图|String|是|
|tag|标签|String|是|
|province|省份|int|是|
|city|城市|int|是|
|website|网址|String|是|
|business_license|工商资质|String|是|
|invest_process|认投流程|String|是|
|development|发展历程|String|是|
|admin_id|添加人|int|是|




**返回参数:**


```json
{
	"code": 200
	"msg": "添加成功"
	"result": []
}
```

## 投后编辑

	POST /after/project/edit?id=2
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|
|title|标题|String|是|
|description|一句话描述|String|是|
|introduction|项目介绍|String|是|
|image|项目图片|String[]|是|
|logo|项目logo图|String|是|
|tag|标签|String|是|
|province|省份|int|是|
|city|城市|int|是|
|website|网址|String|是|
|business_license|工商资质|String|是|
|invest_process|认投流程|String|是|
|development|发展历程|String|是|

**返回参数:**

```json
{
	"code": 200
	"msg": "编辑成功"
	"result": []
}
```

## 投后删除

	POST /after/project/del?id=1

**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|


**返回参数:**

```json
{
	"code": 200
	"msg": "删除成功"
	"result": []
}
```
