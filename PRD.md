# PRD 


item|content
--|:--:
Target release|2018/11/25
Epic| 易懂
Document status|进行中
Document owner|钟嘉孜

## API：
调用百度API-对话情绪识别

## user：
各大商家客服（如：T宝、拼DD、mei团、e了么等）

## Goals：
服务商家、便捷回复、节约没必要的时间

## Background and strategic fit：
通过对对话中的话语进行情绪识别，使得用户更容易理解对话者的情绪，从而进行对自身语言表达方式、内容的改变。在人工客服场景下，也可用于监控客服人员的服务态度

## Assumptions:
1. 联网使用

## Requirements:
Title|User story|Importance|Notes
:--:|:--:|:--:|:--:
客服对话|智能客服对话中，客户：“**你们这是什么垃圾产品啊?这么垃圾的东西都敢拿出来卖？**”|⭐⭐⭐|触发人工客服介入或选择出更匹配用户情绪的文本进行回复
任务型对话|客户：“帮我把地址改为xxx”，客服：“**收到，您的收货地址已改为xxx**”或“**抱歉，您的商品已送出请联系xxx（快递\送货员）进行更改**”|⭐⭐|提高人效


### 示例：智能客服对话

<p><img src="http://aip.bdstatic.com/portal/dist/1542890330398/ai_images/technology/nlp-emotion_detection/introduce.png" alt="智能客服示例" title="" /></p>

## User interaction and design：
容易使用、上传图片、查找图片、身份配对

## Questions：
可以完成话语情绪分析进行改进用户表达行为、内容。

## Not doing：
对话语进行自动反馈
挑出着重点、关键词进一步分析
拍照选取文字、文字识别等

