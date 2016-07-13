# 基金项目

## 列表
	
	GET /project/financing/list
	
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
|id|融资ID|int|是|
|title|项目名称|String|是|
|type|融资类型|int|是|
|round|融资是轮次|String|是|
|finance_value|融资时估值|float|是|
|finance_target|融资目标|float|是|
|shares|出让股份|float|是|
|finance_time|融资时间|int|否|
|fund_name|投资该项目基金|String|否|
|fund_invest|基金投资金额|float|否|
|start_time|认投开始时间|int|否|
|end_time|认投结束时间|int|否|
|all_money|认投总金额|float|否|
|minimum_money|认投最小金额|float|否|
|max_money|认投最大金额|float|否|
|manage_fee|投资管理比率|float|否|
|manage_company|投资管理公司|int|否|
|project_evaluation|项目评价|String|否|
|recommended_id|推荐人ID|int|否|
|recommended_info|推荐人介绍|String|否|

说明：type:1/内部融资,2/基金融资,3/外部融资
	如果类型为内部融资，不返回融资时间字段
	如果类型为基金融资或外部融资，融资时间以下的字段不返回


## 融资编辑
	
	POST /project/financing/edit
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|融资ID|int|是|
|project_id|项目ID|String|是|
|type|融资类型|int|是|
|round|融资是轮次|String|是|
|finance_value|融资时估值|float|是|
|finance_target|融资目标|float|是|
|shares|出让股份|float|是|
|finance_time|融资时间|int|否|
|fund_name|投资该项目基金|String|否|
|fund_invest|基金投资金额|float|否|
|start_time|认投开始时间|int|否|
|end_time|认投结束时间|int|否|
|all_money|认投总金额|float|否|
|minimum_money|认投最小金额|float|否|
|max_money|认投最大金额|float|否|
|manage_fee|投资管理比率|float|否|
|manage_company|投资管理公司|int|否|
|project_evaluation|项目评价|String|否|
|recommended_id|推荐人ID|int|否|
|recommended_info|推荐人介绍|String|否|


说明：type:1/内部融资,2/基金融资,3/外部融资
	如果类型为内部融资，融资时间字段不需要传
	如果类型为基金融资或外部融资，融资时间以下的字段不需要传
	
**返回参数：**


## 融资新增
	
	POST /project/financing/add
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|project_id|项目ID|int|是|
|type|融资类型|int|是|
|round|融资是轮次|String|是|
|finance_value|融资时估值|float|是|
|finance_target|融资目标|float|是|
|shares|出让股份|float|是|
|finance_time|融资时间|int|否|
|fund_name|投资该项目基金|String|否|
|fund_invest|基金投资金额|float|否|
|start_time|认投开始时间|int|否|
|end_time|认投结束时间|int|否|
|all_money|认投总金额|float|否|
|minimum_money|认投最小金额|float|否|
|max_money|认投最大金额|float|否|
|manage_fee|投资管理比率|float|否|
|manage_company|投资管理公司|int|否|
|project_evaluation|项目评价|String|否|
|recommended_id|推荐人ID|int|否|
|recommended_info|推荐人介绍|String|否|
|adder|添加人id|int|否|



说明：type:1/内部融资,2/基金融资,3/外部融资
	如果类型为内部融资，融资时间字段不需要传
	如果类型为基金融资或外部融资，融资时间以下的字段不需要传
	
**返回参数：**



## 融资删除
	
	POST /project/financing/del
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|融资ID|int|是|

**返回参数:**


## 委任

	POST /project/appoint
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|
|member|被委任对象|int|是|


**返回参数:**

```json
{
	"code": 200
	"msg": "委任成功"
	"result": []
}
```