# 资金流水

## 新增

	POST /fund/flow/add

**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金id|int|是|
|name|姓名|String|是|
|head_image|头像|String|是|
|position|职位|String|是|
|content|内容|String|是|


**返回参数:**



## 详情

	GET /fund/team/detail
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|用户id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|用户id|int|是|
|name|姓名|String|是|
|head_image|头像|String|是|
|position|职位|String|是|
|content|内容|String|是|

	
## 编辑

	POST /fund/team/edit
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|用户id|int|是|
|name|姓名|String|是|
|head_image|头像|String|是|
|position|职位|String|是|
|content|内容|String|是|	


**返回参数:**

	
## 删除

	POST /fund/team/del
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|用户id|int|是|


**返回参数:**

	
## 列表

	GET /fund/team/list
	
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