# 附件

## 附件新增

	POST /fund/file/add
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|文件id|int|是|
|fund_id|基金id|int|是|
|name|附件标题|String|是|
|path|附件url|String|是|
|description|附件描述|String|是|
|admin_id|添加人|int|是|

说明:status：0/否，1/是

**返回参数:**


## 附件详情

	GET /fund/file/detail
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|附件id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|附件id|int|是|
|name|附件标题|String|是|
|path|文件url|String|是|
|description|附件描述|String|是|


## 附件编辑

	POST /fund/file/edit
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|附件id|int|是|
|fund_id|基金id|int|是|
|name|附件标题|String|是|
|path|附件url|String|是|
|description|附件描述|String|是|


**返回参数:**

	
## 附件删除

	POST /fund/file/del


**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|附件id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|

## 附件列表

	GET /fund/file/list?id=1
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目ID|int|是|

**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|附件id|int|是|
|name|附件标题|String|是|
|size|文件大小|int|是|
|admin|添加人|String|是|
|create_time|添加时间|int|是|

说明:status：0/否，1/是
