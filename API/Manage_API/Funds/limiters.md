# 有限合伙人

## 新增

	POST /fund/limit/add

**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|会员id|int|是|
|funds_id|基金id|int|是|
|investment_amount|合伙人投资金额|String|是|


**返回参数:**



## 成员详情

	GET /fund/limit/detail
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|合伙人id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|合伙人id|int|是|
|member_id|会员id|int|是|
|investment_amount|姓名|String|是|

	
## 成员编辑

	POST /fund/limit/edit
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|合伙人id|int|是|
|member_id|会员id|int|是|
|investment_amount|合伙人投资金额|String|是|


**返回参数:**

	
## 成员删除

	POST /fund/limit/del
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|合伙人id|int|是|


**返回参数:**

	
## 成员列表

	GET /fund/limit/list
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|成员ID|int|是|
|mobile|手机|String|是|
|name|姓名|String|是|
|truename|真实姓名|String|是|
|investment_amount|投资金额|String|是|
|create_time|添加时间|int|是|