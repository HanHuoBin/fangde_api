# 资金流水

## 新增

	POST /fund/flow/add

**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金id|int|是|
|occurrence_time|发生时间|String|是|
|info|资金说明|String|是|
|category|类别|String|是|
|money|金额|float|是|
|type|类型|int|是|
|crm_id|会员ID|int|否|
|project_id|项目ID|int|否|

说明：category：类别->1/收入,2/支出
type:1/用户,2/项目
选用户传crm_id，选项目传project_id


**返回参数:**



## 详情

	GET /fund/flow/detail
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|用户id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|资金id|int|是|
|occurrence_time|发生时间|String|是|
|info|资金说明|String|是|
|category|类别|String|是|
|money|金额|float|是|
|type|类型|int|是|
|crm_id|会员ID|int|否|
|project_id|项目ID|int|否|

	
## 编辑

	POST /fund/flow/edit
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|用户id|int|是|
|name|姓名|String|是|
|head_image|头像|String|是|
|position|职位|String|是|
|content|内容|String|是|	


**返回参数:**

	
## 列表

	GET /fund/flow/list
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|资金ID|int|是|
|name|姓名|String|是|
|head_image|头像|String|是|
|position|职位|String|是|
|content|内容|String|是|