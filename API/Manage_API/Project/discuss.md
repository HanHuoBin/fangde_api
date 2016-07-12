# 讨论

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
|content|问题|String|是|
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