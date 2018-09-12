# intelligence-analysis-api

### 隐性涉毒对象列表

```
GET /warning/list
```

参数

```
keywords: "510103"
tag: "多次犯案"
level: "一级预警"
```

返回

```
{
    "code": 0,
    "msg": "成功",
    "data": [
        {
            "name": "张晓红",
            "idCard": "51010319952653123",
            "head": "http://xxx.com",
            "level": "一级预警",
            "total": 56.15,
            "integrals": [
                {
                    "name": "通联",
                    "icon": "http://xxx.com",
                    "detail": [
                        {
                            "name": "号码在涉毒人员通讯录(人数)",
                            "score": 10,
                            "icon": "http://xxx.com"
                        },
                        {
                            "name": "通讯录中存在涉毒人员(人数)",
                            "score": 7.5,
                            "icon": "http://xxx.com"
                        }
                    ]
                },
                {
                    "name": "旅馆",
                    "icon": "http://xxx.com",
                    "detail": [
                        {
                            "name": "与涉毒人员同住旅馆",
                            "score": 2.3,
                            "icon": "http://xxx.com"
                        },
                        {
                            "name": "后半夜入住旅馆",
                            "score": 1.36,
                            "icon": "http://xxx.com"
                        }
                    ]
                }
            ],
            "tags": [
                {"name": "暴力"},
                {"name": "多次犯案"}
            ]
        },
        {
            "name": "梁亦玉",
            "idCard": "510103199207081567",
            "head": "http://xxx.com",
            "level": "二级预警",
            "total": 86.75,
            "integrals": [
                {
                    "name": "通联",
                    "icon": "http://xxx.com",
                    "detail": [
                        {
                            "name": "号码在涉毒人员话单(人数)",
                            "score": 12.36,
                            "icon": "http://xxx.com"
                        },
                        {
                            "name": "话单中存在涉毒人员(人数)",
                            "score": 2.3,
                            "icon": "http://xxx.com"
                        }
                    ]
                },
                {
                    "name": "旅馆",
                    "icon": "http://xxx.com",
                    "detail": [
                        {
                            "name": "本地户籍入住旅馆",
                            "score": 1.5,
                            "icon": "http://xxx.com"
                        },
                        {
                            "name": "同时段多次更换旅馆",
                            "score": 2.3,
                            "icon": "http://xxx.com"
                        }
                    ]
                }
            ],
            "tags": [
                {"name": "涉黄"},
                {"name": "多次犯案"}
            ]
        }
    ]
}
```

### 隐性涉毒对象积分详情

```
GET /warning/detail
```

参数

```
idCard: "51010319952653123"
date: "2018-09-12"
```

返回
```
{
    "code":0,
    "msg":"成功",
    "data":[
        {
            "name":"通联模型",
            "score":27,
            "detail":[
                {
                    "name": "号码在涉毒人员通信录",
                    "score": 12,
                    "detail":[
                        {
                            "phone": "18281995890",
                            "belongPlace": "绵阳 移动",
                            "name": "周志明",
                            "idCard": "513174246141312354",
                            "remark": "黑狐",
                            "score": 9
                        },
                        {
                            "phone": "18381515581",
                            "belongPlace": "乐山 移动",
                            "name": "范忆文",
                            "idCard": "532128199904061382",
                            "remark": "孤狼",
                            "score": 3
                        }
                    ]
                },
                {
                    "name": "通讯录中存在涉毒人员",
                    "score": 5,
                    "detail":[
                        {
                            "phone": "18281995890",
                            "belongPlace": "绵阳 移动",
                            "name": "周志明",
                            "idCard": "513174246141312354",
                            "remark": "黑狐",
                            "score": 3
                        },
                        {
                            "phone": "18381515581",
                            "belongPlace": "乐山 移动",
                            "name": "范忆文",
                            "idCard": "532128199904061382",
                            "remark": "孤狼",
                            "score": 2
                        }
                    ]
                }
            ]
        },
        {
            "name":"资金模型",
            "score":31,
            "detail":[
                {
                    "name": "与吸毒人员交易",
                    "score": 12,
                    "detail":[
                        {
                            "cardNo": "554566665841",
                            "belongPlace": "绵阳建行",
                            "name": "周志明",
                            "idCard": "513174246141312354",
                            "mode": "支付宝",
                            "score": 9
                        },
                        {
                            "cardNo": "554566664273",
                            "belongPlace": "绵阳建行",
                            "name": "范忆文",
                            "idCard": "532128199904061382",
                            "mode": "微信",
                            "score": 3
                        }
                    ]
                },
                {
                    "name": "资金流入高危地区",
                    "score": 5,
                    "detail":[
                        {
                            "place": "四川绵阳",
                            "cardNo": "554566665841",
                            "belongPlace": "绵阳 移动",
                            "name": "周志明",
                            "idCard": "513174246141312354",
                            "mode": "支付宝",
                            "score": 3
                        },
                        {
                            "place": "四川绵阳",
                            "cardNo": "554566664273",
                            "belongPlace": "绵阳 移动",
                            "name": "范忆文",
                            "idCard": "532128199904061382",
                            "mode": "微信",
                            "score": 2
                        }
                    ]
                },
                {
                    "name": "资金来自高危地区",
                    "score": 5,
                    "detail":[
                        {
                            "place": "四川绵阳",
                            "cardNo": "554566665841",
                            "belongPlace": "绵阳 移动",
                            "name": "周志明",
                            "idCard": "513174246141312354",
                            "mode": "支付宝",
                            "score": 3
                        },
                        {
                            "place": "四川绵阳",
                            "cardNo": "554566664273",
                            "belongPlace": "绵阳 移动",
                            "name": "范忆文",
                            "idCard": "532128199904061382",
                            "mode": "微信",
                            "score": 2
                        }
                    ]
                },
                {
                    "name": "资金漫游高危地区",
                    "score": 5,
                    "detail":[
                        {
                            "place": "四川绵阳",
                            "cardNo": "554566665841",
                            "belongPlace": "绵阳 移动",
                            "name": "周志明",
                            "idCard": "513174246141312354",
                            "mode": "支付宝",
                            "score": 3
                        },
                        {
                            "place": "四川绵阳",
                            "cardNo": "554566664273",
                            "belongPlace": "绵阳 移动",
                            "name": "范忆文",
                            "idCard": "532128199904061382",
                            "mode": "微信",
                            "score": 2
                        }
                    ]
                },
                {
                    "name": "后半夜交易",
                    "score": 5,
                    "detail":[
                        {
                            "cardNo": "554566665841",
                            "belongPlace": "绵阳 移动",
                            "name": "周志明",
                            "idCard": "513174246141312354",
                            "mode": "支付宝",
                            "time": "2018-01-05  13:12:45",
                            "score": 3
                        },
                        {
                            "cardNo": "554566664273",
                            "belongPlace": "绵阳 移动",
                            "name": "范忆文",
                            "idCard": "532128199904061382",
                            "mode": "微信",
                            "time": "2018-09-05  08:17:41",
                            "score": 2
                        }
                    ]
                }
            ]
        }
    ]
}
```
