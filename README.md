# 自用入门级初级编程错误记录
自用入门级初级编程错误记录

## 外卖小程序记录 20201125凌晨02:16

### 美团部分
在外卖推广小程序中，美团部分的难点在于需要申请到媒体appkey，此项美团已经关闭个人推广申请，最后通过挂靠群主解决。申请到appkey后，直接在源代码替换原始appkey即可。

### 饿了么部分
饿了么的难点在于申请小程序的短链接，而期间，此[链接](https://open.taobao.com/doc.htm?docId=1&docType=15&apiName=taobao.tbk.activity.info.get)又必须被使用到。
通过此页面获取饿了么推广短链接，再在源代码内替换群主原始短链接，才能发布上线，整体流程难度要稍高于美团。
此页面的 `activity_material_id` 参数申请需要提前布置好小程序的api的权限，此项是在使用google搜索 `code":11,"msg":"Insufficient isv permissions"` 后才了解到解决方法，如下[链接](https://developer.alibaba.com/docs/doc.htm?treeId=34&articleId=102617&docType=1)
初始权限赋予仅为5项，还有11项是待申请，`权限包：已获得权限包(5)|申请中权限包(0)|可申请权限包(11)|未满足条件权限包(0)`，实际上填写一百个字符以上的理由即可获取权限，此细节在开始并未注意到，浪费了很多时间。
