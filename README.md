# PRD 


item|content
--|:--:
Target release|2018/11/25
Epic| 匿语APP
Document status|进行中
Document owner|钟嘉孜

## API：
<p><a href="http://ai.baidu.com/tech/nlp/sentiment_classify">百度API-情感倾向分析接口技术文档</a></p>   
<p><a href="https://www.shenjianshou.cn/index.php?r=market/product&product_id=500532&app_id=1803747#stack-info-1">神箭云-评论观点抽取</a></p>
<p><a href="http://dun.163.com/trial/text">网易云-易盾文本检测API</a></p>   

## user：
中山大学南方学院师生群体

## Goals：
* 可以通过匿名的形式对老师、领导进行评价，对热点事情进行匿名评论，提出建议
* 情绪天气表可以反映该用户与全部用户一周内的情绪天气，进行建议提醒。
* 校师生可以对热点事件进行评论（百度贴吧类型） 

## 痛点：
1. 学生不敢实名向老师反映教学问题、不敢实名向领导反映学校问题。
2. 选课前学生难以了解任课老师，选课纠结。
3. 学校难以了解师生观念（通常通过问卷进行信息收集）

## Background and strategic fit：
针对带有主观描述的中文文本，可自动判断该文本的情感极性类别并给出相应的置信度。情感极性分为积极、消极、中性。情感倾向分析能帮助学校了解教师教学、分析热点话题和危机舆情监控，为学校提供有力的决策支持

## Assumptions:
1. 该产品可在移动端、PC端使用。
2. 需要登陆

## 产品需求分析
中大南方暂时没有其他平台、软件专属于校内交流（例：广大华软有内网可以供上传、下载文件，但没有交流，也没有软件）

## Input & Output
#### 情感分析
* input：文本（评论）
* output：该文本的情感极性类别并给出相应的置信度   
#### 评论观点抽取
* input：文本（评论）   
* output：抽取评论关键词   

### 示例：情感倾向分析（作用于热点和评论）

<p><img src="http://aip.bdstatic.com/portal/dist/1543490900641/ai_images/technology/nlp-sentiment_classify/introduce.jpg" alt="情感倾向分析" title="" /></p> 

### 示例：评论观点抽取（作用于评论）

<p><img src="https://image.ipaiban.com/upload-ueditor-image-20181217-1545007271136046335.png" alt="评论观点抽取" title="" /></p>

### 文本检查反垃圾（作用于评论、话题）
<p><img src="https://image.ipaiban.com/upload-ueditor-image-20181223-1545541293499092658.png" alt="文本检测反垃圾" title="" /></p>

## Requirements:
Title|User story|Importance|Notes
:--:|:--:|:--:|:--:
评论分析与决策|评论“胡老师讲课很生动有趣”，学生看到胡老师很多好评，于是很想上她的课，优先选课|⭐⭐⭐|评论分析方便决策
情绪分析|
评论分类|“王老师是个负责任的老师”与“王老师讲课听不懂”自动分类成积极评论与消极评论|⭐⭐|对评论情感性分析，进行分类
舆情监控|app上同学们讨论“西区弥漫着一股恶臭”，疯狂分析原因|⭐⭐⭐⭐|把握用户对热点信息的情感倾向性变化
评论观点抽取|学生们对某位老师评价一段话，说的很委婉让人看不太懂|⭐⭐|观点抽取，容易看懂

## User interaction and design

**产品结构**   
![Aaron Swartz](https://github.com/Kazeeeee/API_ML_AI/blob/master/images/jiegou.png)

**产品原型**   
![Aaron Swartz](https://github.com/Kazeeeee/API_ML_AI/blob/master/images/jiemian.png)

## Questions：
登录需绑定账号，以防止恶意煽动行为、语言不文明行为。 

## Not doing：
校友APP、普及到其他学校、

## 恶意内容监控
通过对消极内容进行排序（对恶意内容，消极程度越高，就把把他们放在更显眼的地方进行监控）

## API示例:
```python
{   
    "text": "苹果是一家伟大的公司"    
}    
```
### 返回示例
```python

 {     "text":"苹果是一家伟大的公司",   
     "items":[   
         {   
            "sentiment":2,    //表示情感极性分类结果   
            "confidence":0.40, //表示分类的置信度   
            "positive_prob":0.73, //表示属于积极类别的概率   
            "negative_prob":0.27  //表示属于消极类别的概率   
        }   
    ]   
}   
 ```
## API比较分析
* （评论观点抽取）百度API与神箭云对比，神箭云API能分析评论情感搭配极性（0消极1中性2积极），还能分析评论情感搭配出现结束位置，能更精确的分析评论观点
<p><a href="https://www.shenjianshou.cn/index.php?r=market/product&product_id=500532&app_id=1803747#stack-info-1">神箭云-评论观点抽取</a></p>
<p><a href="http://ai.baidu.com/docs#/NLP-API/57b9b630">百度API-评论观点抽取</a></p>

## 产品原型下载地址
<p><a href="https://github.com/Kazeeeee/API_ML_AI/blob/master/%E4%B8%AD%E5%A4%A7%E5%8D%97%E6%96%B9APP.rp">产品原型</a></p>   
