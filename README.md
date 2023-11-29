## 本项目实现的最终作用是基于JSP新闻发布网站系统
## 分为2个角色
### 第1个角色为管理员角色，实现了如下功能：
 - 友情链接管理
 - 新闻管理
 - 新闻类别管理
 - 新闻评论管理
 - 管理员登陆
### 第2个角色为用户角色，实现了如下功能：
 - 查看新闻详情
 - 查看某一类目新闻
 - 用户发表评论
 - 用户首页
## 数据库设计如下：
# 数据库设计文档

**数据库名：** news_fabu

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [t_comment](#t_comment) |  |
| [t_link](#t_link) |  |
| [t_news](#t_news) |  |
| [t_newstype](#t_newstype) |  |
| [t_user](#t_user) | 用户表 |

**表名：** <a id="t_comment">t_comment</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | commentId |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | newsId |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  3   | content |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 内容  |
|  4   | userIP |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  5   | commentDate |   datetime   | 19 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_link">t_link</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | linkId |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | linkName |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | linkUrl |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | linkEmail |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  5   | orderNum |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_news">t_news</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | newsId |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | title |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | content |   text   | 65535 |   0    |    Y     |  N   |   NULL    | 内容  |
|  4   | publishDate |   datetime   | 19 |   0    |    Y     |  N   |   NULL    |   |
|  5   | author |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 作者  |
|  6   | typeId |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  7   | click |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  8   | isHead |   tinyint   | 4 |   0    |    Y     |  N   |   NULL    |   |
|  9   | isImage |   tinyint   | 4 |   0    |    Y     |  N   |   NULL    |   |
|  10   | imageName |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  11   | isHot |   tinyint   | 4 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_newstype">t_newstype</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | newsTypeId |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | typeName |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_user">t_user</a>

**说明：** 用户表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | UserId |   int   | 10 |   0    |    N     |  Y   |       | 用户ID  |
|  2   | userName |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户名  |
|  3   | password |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 密码  |

**运行不出来可以微信 javape 我的公众号：源码码头**
