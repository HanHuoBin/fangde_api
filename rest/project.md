#项目管理API

## 全部项目->项目相关基本接口
## 项目列表

	GET  /project/list

**请求参数：**
无


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|
|title|标题|String|是|
|manage|项目经理|String|是|
|att_number|关注用户|int|是|
|inputer|添加者|String|是|
|create_time|添加时间|int|是|



## 项目详情

	GET /project/detail?id=1
	
说明：无
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|


**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|
|title|标题|String|是|
|description|一句话描述|String|是|
|introduction|项目介绍|String|是|
|image|项目图片|String[]|是|
|logo|项目logo图|String|是|
|tag|标签|String|是|
|省市|地区|String|是|
|website|网址|String|是|
|evaluation|项目评价|String|是|
|business_qulity|工商资质|String|是|
|inveset_process|认投流程|String|是|
|recommend_id|推荐人ID|int|是|
|recommend|推荐人|String|是|
|recommend_intro|推荐人介绍|String|是|
|development|发展历程|String|是|

说明：1.项目图片为多张
	 2.工商资质，认投流程都为图片

```json
{
	waiting...
}
```


## 项目新增

	POST /project/add
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|title|标题|String|是|
|description|一句话描述|String|是|
|introduction|项目介绍|String|是|
|image|项目图片|String[]|是|
|logo|项目logo图|String|是|
|tag|标签|String|是|
|省市|地区|String|是|
|website|网址|String|是|
|evaluation|项目评价|String|是|
|business_qulity|工商资质|String|是|
|inveset_process|认投流程|String|是|
|recommend_id|推荐人ID|int|是|
|recommend|推荐人|String|是|
|recommend_intro|推荐人介绍|String|是|
|development|发展历程|String|是|


**返回参数:**


```json
{
	"code": 200
	"msg": "添加成功"
	"result": []
}
```

## 项目编辑

	POST /project/edit?id=2
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|
|title|标题|String|是|
|description|一句话描述|String|是|
|introduction|项目介绍|String|是|
|image|项目图片|String[]|是|
|logo|项目logo图|String|是|
|tag|标签|String|是|
|省市|地区|String|是|
|website|网址|String|是|
|evaluation|项目评价|String|是|
|business_qulity|工商资质|String|是|
|inveset_process|认投流程|String|是|
|recommend_id|推荐人ID|int|是|
|recommend|推荐人|String|是|
|recommend_intro|推荐人介绍|String|是|
|development|发展历程|String|是|

**返回参数:**

```json
{
	"code": 200
	"msg": "编辑成功"
	"result": []
}
```

## 项目删除

	POST /project/del?id=1

**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|


**返回参数:**

```json
{
	"code": 200
	"msg": "删除成功"
	"result": []
}
```

## 委任

	POST /project/appoint
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|
|crm_id|被委任对象ID|int|是|


**返回参数:**

```json
{
	"code": 200
	"msg": "委任成功"
	"result": []
}
```

## 关注用户列表

	GET /project/att_list
	
**请求参数：**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|项目id|int|是|

**返回参数:**

|参数名称|说明|类型|是否必须|
|---|---|---|---|
|id|用户id|int|是|
|nickname|昵称|String|是|
|truename|真是姓名|String|是|
|phone|电话|String|是|


```json
{
	"code": 200
	"msg": "ok"
	"result": {
			"current": 1
			"prev": 1
			"next": 2
			"last": 4
			"total": 33
			"per_page": 10
			"data": [
				{
					"id": 34,
					"nickname": "hanbin",
					"truename": "韩斌",
					"phone": "18757110824"
				},	
				{
					"id": 34,
					"nickname": "hanbin",
					"truename": "韩斌",
					"phone": "18757110824"
				},
				{
					"id": 34,
					"nickname": "hanbin",
					"truename": "韩斌",
					"phone": "18757110824"
				}
			]
		}
}
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


## 操作->融资

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



	