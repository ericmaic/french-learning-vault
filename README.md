# french-learning-vault

# 一. 快捷键列表：

- Command/Ctrl + Enter：在连接处直接打开链接到网页或者到tab页
- Command/Ctrl + L：从原始的文字，依次切换到todo，todo done
- Command/Ctrl + 点击编辑书页图标：切换编辑和只读模式在新tab中建立
- Command/Ctrl + P：打开命令面板
- Command/Ctrl + Shift + D：新建日记
- Command/Ctrl + D：删除光标行
- Command/Ctrl + N：新建一个卡片，或者笔记
- Command/Ctrl + O：搜索文件的名字
- Command/Ctrl + ，：打开设置面板 
- Command/Ctrl + Left：隐藏/展开左侧栏
- Command/Ctrl + Right：隐藏/展开右侧栏
- Command/Ctrl + E：预模式与编辑模式切换
- Command/Ctrl + F：查找功能
- Command/Ctrl + 鼠标滚轮：字体大小（要提前设置）
- Command/Ctrl + "+"/"-"：同理
- Command/Ctrl + K：选中快速插入链接 
- Command/Ctrl + /：注释或者取消注释
- Command/Ctrl + M: 打开思维导图
- "---,---": 包裹的是文件的属性
- / + 其他: 可以调出命令
- Option/Alt + 鼠标单击：多光标编辑
- Tab：缩进
- Shift + tab：退回缩进
- 幻灯片用法：把文字用“---，---包裹就可以实现”

# 二. 标签用法

- 一级标签：#标签名
- 二级标签：#标签名/二级标签（例：#提示词/源码）
- 文件分类做总体归纳，标签做细致归纳

## 1. 标签名称汇总：

- #语法
- #词汇
- #发音 

# 三. Markdown & Obsidian 语法

## 基本语法

- “# 标题”：一级标签
- “## 标题”：二级标签
- “### 标题”：三级标签
- “#### 标题”：四级标签
- “##### 标题”：五级标签
- “###### 标题”：六级标签
- “两个* + 两个*”：加粗
- “一个* + 一个*”：斜体
- “一个_ + 一个_”：斜体
- “两个= + 两个=”：高亮
- “两个~ + 两个~”：删除
- “两个% + 两个%”：注释
- “- + 空格”：无序列表
- “数字 + .”：有序列表
- “- + 空格 + [] + 空格”：todo列表项
- “\[+名字\]\(+链接\)”：超链接
- “\[\[+内容\]\]”：obsidian双链
- “! + 双链”：引用展示
- "> + 文字区域"：文字展示区域
- "\[^\]"：标注
- “\[\[#+标题内容\]\]”：文本内跳转相应的标题项内容
- “\[\[+文件名|+别名\]\]”：Alias别名，给文件创建别名，让名字更有意思，搜索更快捷；可以在metadata里应用，作为aliases项
- “\`\`\`+语言名称+内容\`\`\`”：代码
- “\-\-\-”：分隔符
- jixu

## 进阶语法

### %% 引用 %%

- \[\[\]\]：双链引用
- !\[\[\]\]：展示引用内容
- \[\[\#引用标题\]\]：当前文本内标题引用
- \[\[^引用块\]：当前文本内内容块引用
- !\[\[^引用块\]\]：展示当前文本块内容
- \[\[^^引用块\]\]：所有笔记的块内容 

### Callout
- Obsidian 新语法
- ```
  > []
  ```


```javascript
let hideMap = [];
and 
```


%%  %%

## Yaml用法

metadata
- \---- + \----：三个包裹起来
- 


# 四. 用到的插件

- Git：云端同步方案
	- 用法：跟 Github 仓库建立连接，多设备共享
- Calendar：
- Tasks
- Notebook Navigator
- Style Settings
- Media Extended
- dragger？
- Dataview：抽取符合条件的笔记，筛选
	- 用法：“三个\`开始，+ dataview + 三个\`结束”，代码块
- Templater：
- Heat Map？
- Mind Map
- Admonition: 文字块风格
	- 用法：“三个\`开始，+ ad-功能标记 + 三个\`结束”
- List Callout：Callout 升级版
	- 用法：\- 空格 特俗符号
	- ! Callout 1
	- @ Callout 2
	- $ Callout 3
	- % Callout 4
	- & Callout 5
	- ~ Callout 6
	- ? Callout 7
- Banner: 题图
	- 用法：Command + P -> Banner add local image
- QuickAdd：
- Advanced Table：markdown增强表格
	- 用法：只需要\|title\|title\|title\|就可以实现表格
- Settings Search：setting里面的搜索框
- Easy Typing：对文字优化处理
- PDF++：对 PDF 进行标注的插件



```

[!]


	

```dataview
list
from ""
where contains(file.name,"Daily")
```


## 可以选配的插件
- Note refector：笔记重构，根据title的级别重构为双链笔记

# 日记或Daily


# 文件存储
- 附件存放在ATTACHMENTS文件夹中
- 

---

# 工作区布局
## 使用场景

- 书籍阅读/读书笔记：pdf，其他电子书
- 项目管理
- 日记
- todo list
- 学习笔记/视频学习：视频+记录
---

![[Pasted image 20260510000024.png]]


# 思维导图

- 通过插件Mind Map实现
- 快捷命令为Command/Ctrl + M打开
- 可以Copy Screenshot拷贝思维导图


# CSS Style
- List outline：


# PDF阅读以及标记

# Mermaid语法
 
| column1 | column2 | column3 |     |
| ------- | ------- | ------- | --- |
|         |         |         |     |
|         |         |         |     |
|         |         |         |     |


 - [/] 还没有完成呢进行中 in progress
 - [>]  



# 主题设置

## Border 主题

### Todo List




![[Pasted image 20260510232706.png]]