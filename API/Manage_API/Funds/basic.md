# 基金基本接口


## 列表

    GET /fund/list
    
**请求参数：**
无


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金id|int|是|
|name|名称|String|是|
|scale|基金规模|float|是|
|fund_manager|基金经理|String|是|
|admin|录入人|String|是|
|create_time|添加时间|int|是|


## 基金详情

	GET /fund/detail?id=1
	
说明：无
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金id|int|是|
|name|名称|String|是|
|scale|基金规模|float|是|
|small_photo|基金小图|String|是|
|large_photo|基金大图|String[]|是|
|logo|基金logo图|String|是|
|explain|基金说明|String|是|
|tag|投资领域|String|是|
|number_years|基金年限|String|是|
|management_fees|管理费用|String|是|
|excess_returns|超额收益|String|是|
|executing_transaction_partner|执行事务合伙人|int|是|
|executing_transaction_money|执行事务合伙人投资金额|float|是|
|fund_manager|基金经理|int|是|




## 基金新增

	POST /project/add
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|name|名称|String|是|
|scale|基金规模|float|是|
|small_photo|基金小图|String|是|
|large_photo|基金大图|String[]|是|
|logo|基金logo图|String|是|
|explain|基金说明|String|否|
|tag|投资领域|String|是|
|number_years|基金年限|String|是|
|management_fees|管理费用|String|是|
|excess_returns|超额收益|String|是|
|executing_transaction_partner|执行事务合伙人|int|是|
|executing_transaction_money|执行事务合伙人投资金额|float|是|
|fund_manager|基金经理|int|是|
|admin_id|添加人|int|是|




**返回参数:**


```json
{
	"code": 200
	"msg": "添加成功"
	"result": []
}
```

## 基金编辑

	POST /project/edit?id=2
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金ID|int|是|
|name|名称|String|是|
|scale|基金规模|float|是|
|small_photo|基金小图|String|是|
|large_photo|基金大图|String[]|是|
|logo|基金logo图|String|是|
|explain|基金说明|String|是|
|tag|投资领域|String|是|
|number_years|基金年限|String|是|
|management_fees|管理费用|String|是|
|excess_returns|超额收益|String|是|
|executing_transaction_partner|执行事务合伙人|int|是|
|executing_transaction_money|执行事务合伙人投资金额|float|是|
|fund_manager|基金经理|int|是|

**返回参数:**

```json
{
	"code": 200
	"msg": "编辑成功"
	"result": []
}
```

## 基金删除

	POST /project/del?id=1

**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|基金id|int|是|


**返回参数:**

```json
{
	"code": 200
	"msg": "删除成功"
	"result": []
}
```
