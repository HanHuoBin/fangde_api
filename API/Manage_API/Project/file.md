# 附件

## 附件新增

	POST /project/file/add
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|文件id|int|是|
|project_id|项目id|int|是|
|name|附件标题|String|是|
|path|文件url|String|是|
|is_bp|是否设为BP|int|是|
|admin_id|添加人|int|是|

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
|name|附件标题|String|是|
|path|文件url|String|是|
|is_bp|是否设为BP|int|是|

说明:status：0/否，1/是


## 附件编辑

	POST /project/file/edit
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|附件id|int|是|
|name|附件标题|String|是|
|path|文件url|String|是|
|is_bp|是否设为BP|int|是|

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

```json
{
"code": 200
"msg": "ok"
"result": [
      {
        "id": 3
        "title": null
        "file_size": null
        "adder": false
        "create_time": 0
        "status": 0
      },
      {
        "id": 2
        "title": null
        "file_size": null
        "adder": false
        "create_time": 0
        "status": 0
      },
      {
        "id": 1
        "title": null
        "file_size": null
        "adder": false
        "create_time": 0
        "status": 0
      }
    ]
}
```

## 附件设为BP

	GET /project/file/set_bp			
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|附件id|int|是|


**返回参数:**

```json
{
  "code": 200
  "msg": "设置成功"
  "result": []
}
```