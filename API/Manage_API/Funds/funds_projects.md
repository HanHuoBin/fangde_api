# 基金项目

## 列表
	
	GET /fund/financing/list
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金ID|int|是|

**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|融资id|int|是|
|name|项目名称|String|是|
|financing_date|认投时间|String|是|
|funds_money|认投金额|int|是|
|sell_shares|出让股份|float|是|
|exit_earnings|退出收益|float|是|
|exit_time|推出时间|int|是|


## 项目退出详情
	
	GET /project/financing/detail
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|融资ID|int|是|

**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|融资id|int|是|
|exit_time|推出时间|int|是|
|exit_earnings|退出收益|float|是|



## 项目退出
	
	POST /project/financing/edit
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|融资id|int|是|
|exit_time|推出时间|int|是|
|exit_earnings|退出收益|float|是|

	
**返回参数：**


## 删除
	
	POST /project/financing/del
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|融资ID|int|是|

**返回参数:**