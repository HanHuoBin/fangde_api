# 基金基本接口


## 列表

    GET /fund/list
    
**请求参数：**
无


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金id|int|是|
|name|名称|String|是|
|scale|基金规模|float|是|
|fund_manager|基金经理|String|是|
|admin|录入人|String|是|
|create_time|添加时间|int|是|


## 基金详情

	GET /fund/detail?id=1
	
说明：无
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金id|int|是|
|name|名称|String|是|
|scale|基金规模|float|是|
|small_photo|基金小图|String|是|
|big_photo|项目图片|String[]|是|
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


## 项目新增

	POST /project/add
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
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
|admin_id|添加人|int|是|




**返回参数:**


```json
{
	"code": 200
	"msg": "添加成功"
	"result": []
}
```

## 项目编辑

	POST /project/edit?id=2
	
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

## 项目删除

	POST /project/del?id=1

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