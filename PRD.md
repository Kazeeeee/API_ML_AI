# PRD 


item|content
--|:--:
Target release|2018/11/25
Epic| 匿语APP
Document status|进行中
Document owner|钟嘉孜

## API：
调用百度API-情感倾向分析
<p><a href="http://ai.baidu.com/tech/nlp/sentiment_classify">百度API-情感倾向分析接口技术文档</a></p>

## user：
中山大学南方学院学生群体

## Goals：
可以通过匿名的形式对老师、领导进行评价，对热点事情进行匿名评论。

## Background and strategic fit：
针对带有主观描述的中文文本，可自动判断该文本的情感极性类别并给出相应的置信度。情感极性分为积极、消极、中性。情感倾向分析能帮助学校了解教师教学、分析热点话题和危机舆情监控，为学校提供有力的决策支持

## Assumptions:
1. 该产品可在移动端、PC端使用。
2. 需要登陆
3. 

## Requirements:
Title|User story|Importance|Notes
:--:|:--:|:--:|:--:
评论分析与决策|智能客服对话中，客户：“**你们这是什么垃圾产品啊?这么垃圾的东西都敢拿出来卖？**”|⭐⭐⭐|触发人工客服介入或选择出更匹配用户情绪的文本进行回复
评论分类|客户：“帮我把地址改为xxx”，客服：“**收到，您的收货地址已改为xxx**”或“**抱歉，您的商品已送出请联系xxx（快递\送货员）进行更改**”|⭐⭐|提高人效
舆情监控|


### 示例：情感倾向分析

<p><img src="http://aip.bdstatic.com/portal/dist/1543490900641/ai_images/technology/nlp-sentiment_classify/introduce.jpg" alt="情感倾向分析" title="" /></p>

## User interaction and design
**原型、产品结构**

## Questions：
登录需绑定账号，以防止恶意煽动行为、语言不文明行为。


## Not doing：
对话语进行自动反馈
挑出着重点、关键词进一步分析
拍照选取文字、文字识别等

