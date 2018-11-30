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
可以通过匿名的形式对老师、领导进行评价，对热点事情进行匿名评论，提出建议。

## 痛点：
学生不敢实名向老师反映教学问题、不敢实名向领导反映学校问题。
选课前学生难以了解任课老师，选课纠结。

## Background and strategic fit：
针对带有主观描述的中文文本，可自动判断该文本的情感极性类别并给出相应的置信度。情感极性分为积极、消极、中性。情感倾向分析能帮助学校了解教师教学、分析热点话题和危机舆情监控，为学校提供有力的决策支持

## Assumptions:
1. 该产品可在移动端、PC端使用。
2. 需要登陆

### 示例：情感倾向分析

<p><img src="http://aip.bdstatic.com/portal/dist/1543490900641/ai_images/technology/nlp-sentiment_classify/introduce.jpg" alt="情感倾向分析" title="" /></p>

## Requirements:
Title|User story|Importance|Notes
:--:|:--:|:--:|:--:
评论分析与决策|评论“胡老师讲课很生动有趣”，学生看到胡老师很多好评，于是很想上她的课，优先选课|⭐⭐⭐|评论分析方便决策
评论分类|“吴老师是个负责任的老师”与“吴老师讲课听不懂”自动分类成积极评论与消极评论|⭐⭐|对评论情感性分析，进行分类
舆情监控|app上同学们讨论“西区弥漫着一股屎味”，疯狂分析原因|⭐⭐⭐⭐|把握用户对热点信息的情感倾向性变化

## User interaction and design
**产品结构**
<p><img src="https://image.ipaiban.com/upload-ueditor-image-20181130-1543551433796047282.png" alt="产品结构" title="" /></p>

## Questions：
登录需绑定账号，以防止恶意煽动行为、语言不文明行为。 

## Not doing：
用学号登录、评论观点抽取

