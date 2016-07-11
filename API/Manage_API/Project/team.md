# 团队

## 成员新增

	POST /project/team/add

**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|
|name|姓名|String|是|
|head_image|头像|String|是|
|position|职位|String|是|
|description|描述|String|是|
|content|内容|String|是|


**返回参数:**



## 成员详情

	GET /project/team/detail
	
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
|description|描述|String|是|
|content|内容|String|是|

	
## 成员编辑

	POST /project/team/edit
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|用户id|int|是|
|name|姓名|String|是|
|head_image|头像|String|是|
|position|职位|String|是|
|description|描述|String|是|
|content|内容|String|是|	


**返回参数:**

	
## 成员删除

	POST /project/team/del
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|用户id|int|是|


**返回参数:**

	
## 成员列表

	GET /project/team/list
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|name|姓名|String|是|
|head_image|头像|String|是|
|position|职位|String|是|
|description|描述|String|是|
|content|内容|String|是|