# 融资

## 融资列表
	
	GET /project/financing/list
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目ID|int|是|

**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|融资id|int|是|
|title|项目名称|String|是|
|type|融资类型|int|是|
|progress|融资进度|float|是|
|target_money|目标金额（万元）|float|是|
|have_money|已筹金额（万元）|float|是|
|create_time|融资日期|int|是|


## 融资详情
	
	GET /project/financing/detail
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|融资ID|int|是|

**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
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
|all_copies|认投总份数|int|否|
|minimum_copies|认投最小份数|int|否|
|max_copies|认投最大份数|int|否|
|manage_fee|投资管理比率|float|否|
|manage_company|投资管理公司|int|否|

说明：type:1/内部融资,2/基金融资,3/外部融资
	如果类型为内部融资，不返回融资时间字段
	如果类型为基金融资或外部融资，融资时间以下的字段不返回


## 融资编辑
	
	POST /project/financing/edit
	
**请求参数：**

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
|all_copies|认投总份数|int|否|
|minimum_copies|认投最小份数|int|否|
|max_copies|认投最大份数|int|否|
|manage_fee|投资管理比率|float|否|
|manage_company|投资管理公司|int|否|


说明：type:1/内部融资,2/基金融资,3/外部融资
	如果类型为内部融资，融资时间字段不需要传
	如果类型为基金融资或外部融资，融资时间以下的字段不需要传
	
**返回参数：**


## 融资新增
	
	POST /project/financing/add
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
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
|all_copies|认投总份数|int|否|
|minimum_copies|认投最小份数|int|否|
|max_copies|认投最大份数|int|否|
|manage_fee|投资管理比率|float|否|
|manage_company|投资管理公司|int|否|


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