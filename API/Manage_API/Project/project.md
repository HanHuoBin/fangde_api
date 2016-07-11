#项目管理API

## 全部项目->项目相关基本接口


```

## 操作->讨论

## 讨论列表
	
	get /project/discuss/list
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|ID|int|是|
|content|评论内容|String|是|
|commenter|评论人|String|是|
|comment_time|评论时间|int|是|
|replyer|回复人|String|是|
|reply_time|回复时间|String|是|
|status|是否公开|int|是|

说明：status:0/不公开，1/公开

## 讨论详情

	get /project/discuss/detail
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|评论id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|ID|int|是|
|content|评论内容|String|是|
|status|是否为公开|int|是|

说明：status:0/不公开，1/公开

	
## 讨论删除

	POST /project/discuss/del
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|评论id|int|是|


**返回参数:**



## 讨论回复

	POST /project/discuss/reply
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|评论id|int|是|
|content|回复内容|String|是|
|status|是否公开|int|是|

说明：status:0/不公开，1/公开


**返回参数:**


## 设为公开

	POST /project/discuss/set_public

**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|评论id|int|是|

说明：status:0/不公开，1/公开

**返回参数:**

## 操作->团队

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

## 操作->附件

## 附件新增

	POST /project/file/add
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|
|title|附件标题|String|是|
|file_url|文件url|String|是|
|status|是否设为BP|int|是|

说明:status：0/否，1/是

**返回参数:**


## 附件详情

	GET /project/file/detail
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|附件id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|附件id|int|是|
|title|附件标题|String|是|
|file_url|文件url|String|是|
|status|是否设为BP|int|是|

说明:status：0/否，1/是


## 附件编辑

	POST /project/file/edit
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|附件id|int|是|
|title|附件标题|String|是|
|file_url|文件url|String|是|
|status|是否设为BP|int|是|

说明:status：0/否，1/是

**返回参数:**

	
## 附件删除

	POST /project/file/del


**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|附件id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|

## 附件列表

	GET /project/file/list?id=1
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目ID|int|是|

**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|附件id|int|是|
|title|附件标题|String|是|
|file_size|文件大小|int|是|
|adder|添加人|String|是|
|create_time|添加时间|int|是|
|status|是否设为BP|int|是|

说明:status：0/否，1/是

## 附件设为BP

	GET /project/file/set_bp			
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|附件id|int|是|


**返回参数:**

	
## 操作->常见问题

## 常见问题新增

	POST /project/problem/add
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|
|problem|问题|String|是|
|reply|回答|String|是|
|status|是否设为常见问题|int|是|

说明:status：0/否，1/是（默认是）

**返回参数:**



## 常见问题详情

	GET /project/problem/detail
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|常见问题id|int|是|

**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|常见问题id|int|是|
|problem|问题|String|是|
|reply|回答|String|是|
|status|是否设为常见问题|int|是|

说明:status：0/否，1/是（默认是）
	
## 常见问题编辑

	POST /project/problem/edit

**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|常见问题id|int|是|
|problem|问题|String|是|
|reply|回答|String|是|
|status|是否设为常见问题|int|是|

说明:status：0/否，1/是（默认是）

**返回参数:**


	
## 常见问题删除

	POST /project/problem/del
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|常见问题id|int|是|


**返回参数:**


## 常见问题列表

	GET /project/problem/list
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|

**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|常见问题id|int|是|
|problem|问题|String|是|
|adder|添加人|String|是|
|create_time|添加时间|int|是|
|status|是否设为常见问题|int|是|

说明:status：0/否，1/是（默认是）
	


## 设为常见问题

	GET /project/problem/common	
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|问题id|int|是|

**返回参数:**






	