# 常见问题

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