
##访客系统接口变更

###1.历史来访人员查询
-方法：get
-参数：

| Field|Type|Description|Example
| :-------- ---------------| -----------------------| -------------------- |
|keyWord|string |需要进行模糊搜索的字符串|"123"|
|pageNum|int |查询的页数|5|
|pageSize|int |每页的数据条数|2|
|startDay|string |查询开始日期|"2018-10-10 00:00:00"|
|endDay|string |查询结束日期|"2018-10-11 00:00:00"|
-返回：返回值不变

-请求路径：http://[ip]:[port]/sentrycheck/getHistoryEnterPersonVisitList

###2.历史来访人员导出
-方法：get
-参数：

| Field|Type|Description|Example
| :-------- ---------------| -----------------------| -------------------- |
|keyWord|string |需要进行模糊搜索的字符串|"123"|
|startDate|string |查询开始日期|"2018-10-10 00:00:00"|
|endDate|string |查询结束日期|"2018-10-11 00:00:00"|
|gateName|string |所属大门|"正大门"|
-返回：excel文件

-请求路径：http://[ip]:[port]/sentrycheck/exportHistoryUserDetail

###3.人员来访次数排名
-方法：get
-参数：

| Field|Type|Description|Example
| :-------- ---------------| -----------------------| -------------------- |
|startDay|string |查询开始日期|"2018-10-10 00:00:00"|
|endDay|string |查询结束日期|"2018-10-11 00:00:00"|
-返回：
```javascript

{
    "success": true,
    "result": [
        {
            "id": 123,
            "visitorName": "小明",
            "visitTimes": 10
        }
        {
            "id": 456,
            "visitorName": "小乔",
            "visitTimes": 5
        }
    ]
}

```

-请求路径：http://[ip]:[port]/sentrycheck/getPersonVisitTimesPeriodRanking

###4.车辆来访次数排名
-方法：get
-参数：

| Field|Type|Description|Example
| :-------- ---------------| -----------------------| -------------------- |
|startDay|string |查询开始日期|"2018-10-10 00:00:00"|
|endDay|string |查询结束日期|"2018-10-11 00:00:00"|
-返回：
```javascript

{
    "success": true,
    "result": [
        {
            "carId": "浙A1515",
            "visitTimes": 10
        }
        {
            "carId": "浙A6544",
            "visitTimes": 5
        }
    ]
}

```

-请求路径：http://[ip]:[port]/sentrycheck/getHistoryEnterCarVisitList

###5.车辆来访次数排名导出
-方法：get
-参数：

| Field|Type|Description|Example
| :-------- ---------------| -----------------------| -------------------- |
|startDay|string |查询开始日期|"2018-10-10 00:00:00"|
|endDay|string |查询结束日期|"2018-10-11 00:00:00"|
-返回：excel文件

-请求路径：http://[ip]:[port]/sentrycheck/exportCarVisitTimesPeriodRanking

###6.人员来访次数排名导出
-方法：get
-参数：

| Field|Type|Description|Example
| :-------- ---------------| -----------------------| -------------------- |
|startDay|string |查询开始日期|"2018-10-10 00:00:00"|
|endDay|string |查询结束日期|"2018-10-11 00:00:00"|
-返回：excel文件

-请求路径：http://[ip]:[port]/sentrycheck/exportPersonVisitTimesPeriodRanking