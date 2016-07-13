# 有限合伙人

## 新增

	POST /fund/team/add

**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|会员id|int|是|
|investment_amount|合伙人投资金额|String|是|


**返回参数:**



## 成员详情

	GET /fund/team/detail
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|用户id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|用户id|int|是|
|member_id|用户id|int|是|
|investment_amount|姓名|String|是|

	
## 成员编辑

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

	
## 成员删除

	POST /fund/team/del
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|用户id|int|是|


**返回参数:**

	
## 成员列表

	GET /fund/team/list
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|成员ID|int|是|
|name|姓名|String|是|
|head_image|头像|String|是|
|position|职位|String|是|
|content|内容|String|是|