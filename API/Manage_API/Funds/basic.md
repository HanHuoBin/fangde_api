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
|fund_manager|基金经理|float|是|
|adder|添加者|String|是|
|create_time|添加时间|int|是|