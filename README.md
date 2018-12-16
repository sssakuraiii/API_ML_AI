### product requirements

| 发布日期 | 18/11/25 |
|----|----|
| 更新日期 | 18/12/17 |
| 史诗名称 | 语音输入笔记本 |
| 文件现状 | 未起头 |
| 文件主人 |啊诗本诗 |
| 领头的设计师 | |
| 领头的开发者 | |
| 领头的测试者| |

### 产品介绍
- 语音笔记本是一款兼顾长语音输入、文字输入语音朗读、识别图片文字输入与文章自动分类的笔记本APP。在方便用户快速输入输出的同时加上待办事项提醒、密码锁、悬浮记事、推荐文章等功能，致力于为用户打造不费时不费力的使用体验。

### 目标

- 帮助用户解放双手和双眼，用语音输入与带有文字的图片记录文字，标签功能快速记录与获取信息。为用户带来更便捷快速的体验，构建一个帮助用户提升技能，快速记录与思考的工具。


### 背景
- 在高速发展的社会下，人们总面对着瞬息万变的信息。为了不与世界脱节，便需要更快地行动与更好的节省时间和精力。但单靠文字输入输出已经无法满足用户的多样化需求。

 
### 战略契合处
加值宣言：使用百度长语音输入API、百度通用文字识别API、百度文章标签API为本产品核心功能语音输入、图片识别、文章标签加值。
最小可用产品为可进行长语音输入、图片识别的语音笔记本。

1. 本产品在编辑时，用户可以直接选择使用长语音输入，由系统在文档中转换成文字进行记录，大幅提升了用户的录入效率，方便后期的文字处理和内容存档，省去记录的人力和时间成本。
2. 用户上传或现拍一张带有文字的图片，由系统识别后在文档中转换成可编辑的文档文字。
3. 当用户完成一篇文章的编辑后，系统对文章的标题和内容进行深度分析，输出能够反映文章关键信息的主题、话题、实体等多维度标签，方便用户日后寻找。
4. 用户登录后可以将文章上传云端实现同步，也可以实现跨平台分享给其他社交平台上的朋友。
5. 待办事项的提醒可以在忙碌的日子里提醒用户不要忘记重要的事项
6. 密码锁帮助用户锁住所有的私密文档
7. 悬浮在手机其他界面的语音输入小按钮，可以帮助用户随时随地记录
8. 每日根据用户常用标签推荐的业内新闻与其他类型文章可以帮助用户更便捷地获取感兴趣的内容

### 情境假设
- 用户需要在手机上联网使用。
- 用户使用语音输入功能时，需要给出麦克风权限。
- 用户使用图片上传功能时，需要给出存储与摄像头功能。

### 用户画像
- 针对有长语音转化文字需求，拍照/上传图片转化文字需求，记录频繁、对文章分类头疼的15-35岁用户，如作家、学生、公司职员等。

###  用户需求
|#| 使用场景 | 问题需求 |重要程度 |对应功能|对应API|
|----|----|----|----|----|----|
|1| 在需要快速记录一大段讲话时，既无法手打快速输入，也无法依赖输入法的短语音输入 | 快速、准确录入长语音 |最重要 |长语音输入| 百度长语音识别|
|2| 当只有一张满是文字的图片时，对慢慢手打感到心累 | 需要一种方法快速获取图片上的文字转化为可编辑的文字 | 重要|图片转文字 | 百度通用文字识别|
|3| 在面对一大堆杂乱无章排列的文章时，无法快速找到自己想要的部分或一篇 |需要用一种方法让文章被快速分类 |次重要|文章标签 | 百度文章标签|
|4| 忙手忙脚时总是忘了接下来要干什么，没有明确规划或总是忘记时间 |需要一个能提醒自己待办事项的功能 |次重要|待办事项提醒 | 无|
|5| 文档中写着自己的私密笔记，不愿被人轻易看到 |需要一个密码锁来帮助封锁 |次重要|密码锁| 无|
|6| 当在手机其他页面忙碌时，赶不及重新点开笔记本进行记录 |需要用一种方法能随时快速进入语音输入界面 |次重要|悬浮记事窗口 | 无|
|7| 想要快速获取自己兴趣所向的文章 |需要用一种方法快速获取资讯 |次重要|美文推荐| 无|


<!-- ### 人工智能概率性
/1. 百度官方宣布百度语音开放平台自 2013 年 10 月上线以来每日在线语音识别请求已经达到了 1.4 亿次，开发者数量超过 14 /万。在如此庞大的数据支撑下，百度语音在“安静条件下”的识别准确率达到了 97%。 /[新闻网址](https://blog.csdn.net/snow2know/article/details/53858131) -->


### 产品功能架构
![产品功能架构.jpg](https://upload-images.jianshu.io/upload_images/14325233-2fbcaa25c2d706bb.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 流程图
![流程图.jpg](https://upload-images.jianshu.io/upload_images/14325233-32aa30edc7c7f097.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


### 全局说明
1. 功能权限分为登录/未登录两个状态。

&emsp;（1）登录：登录状态下可进行app内所有操作。

&emsp;（2）未登录：只能使用编辑文章，文章列表视图设置，标签，分享文章至其他平台功能。不能使用云端，账号功能。
 2. 激活编辑界面时自动弹出tab，再次点击编辑界面空白地区时弹出输入法。

### 使用者交互及设计
[流程图&功能构架&交互原型](https://sssakuraiii.github.io/API_ML_AI/. )
![交互.jpg](https://upload-images.jianshu.io/upload_images/14325233-2e7eeecef0c34c2d.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 迭代功能
- 搜索功能

