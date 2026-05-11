# french-learning-vault
---

# 一. 快捷键

## 1. A-Z:

- **Command/Ctrl + A** : 快速启动 QuickAdd
- **Command/Ctrl + B** : 加粗，取消加粗
- **Command/Ctrl + C** : 复制
- **Command/Ctrl + D** ：删除光标行
- **Command/Ctrl + E** ：预模式与编辑模式切换
- **Command/Ctrl + F** ：查找功能
- **Command/Ctrl + G** : 打开关系图谱
- **Command/Ctrl + H** : 最小化窗口
- **Command/Ctrl + I** : 倾斜，取消倾斜
- **Command/Ctrl + J** : 
- **Command/Ctrl + K** ：选中快速插入链接 
- **Command/Ctrl + L** ：从原始的文字，依次切换到todo，todo done
- **Command/Ctrl + M** : 打开思维导图
- **Command/Ctrl + N** ：新建一个卡片，或者笔记
- **Command/Ctrl + O** ：搜索文件的名字
- **Command/Ctrl + P** ：打开命令面板
- **Command/Ctrl + Q** ：退出窗口，关闭
- **Command/Ctrl + R** : 
- **Command/Ctrl + S** : 保存当前文件
- **Command/Ctrl + T** : 新标签页
- **Command/Ctrl + U** : 
- **Command/Ctrl + V** : 粘贴
- **Command/Ctrl + W** : 关闭当前标签页
- **Command/Ctrl + X** : 剪切
- **Command/Ctrl + Y** : 
- **Command/Ctrl + Z** : 撤销操作
- ~~**Command/Ctrl + Z** : 文字宏，补全~~ （Text Snippets）

## 2. Others 1:

- **Command/Ctrl + Left** ：隐藏/展开左侧栏
- **Command/Ctrl + Right** ：隐藏/展开右侧栏
- **Command/Ctrl + ,** : 打开设置面板 
- **Command/Ctrl + Enter** ：在连接处直接打开链接到网页或者到tab页
- **Command/Ctrl + 点击编辑书页图标** ：切换编辑和只读模式在新tab中建立
- **Command/Ctrl + Shift + D** ：新建日记
- **Command/Ctrl + 鼠标滚轮** ：字体大小（要提前设置）
- **Command/Ctrl + "+"/"-"** ：同理
- **Command/Ctrl + /** ：注释或者取消注释

## 3. Others 2:

- **"---,---"** : 包裹的是文件的属性；里面可以添加 alias 设置文件的别名
- **/ + 其他** : 可以调出命令
- **Option/Alt + 鼠标单击** ：多光标编辑
- **Tab** ：缩进
- **Shift + Tab** ：退回缩进
- **幻灯片用法** ：把文字用“---，---包裹就可以实现”

--- 


# 二. 标签

## 1. 用法

- **一级标签** ：#标签名
- **二级标签** ：#标签名/二级标签（例：#提示词/源码）
- **说明** : 文件分类做总体归纳，标签做细致归纳

## 2. 名称汇总：

- #语法
- #词汇
- #发音 

---

# 三. 语法

## 1. Markdown 语法

- **“# 标题”** ：一级标题
- **“## 标题”** ：二级标题
- **“### 标题”** ：三级标题
- **“#### 标题”** ：四级标题
- **“##### 标题”** ：五级标题
- **“###### 标题”** ：六级标题
- **“\#标签”** : 添加标签 

- **“\*\*内容\*\*”** ：加粗
- **“\*内容\*”** ：斜体
- **“\_内容\_”** ：斜体
- **“\=\=内容\=\=”** ：高亮
- **“\~\~内容\~\~”** ：删除
- **“\%\%内容\%\%”** ：注释

- **“- + 空格”** ：无序列表
- **“+ + 空格”** ：无序列表
- **“* + 空格”** ：无序列表
- **“数字 + .”** ：有序列表

- **“- + 空格 + \[ 空格 \] + 空格”** ：todo列表项
- **“\[显示文字\]\(链接\)”** ：超链接
- **“> + 文字区域”** ：引用快，文字展示区域
- **“内嵌\>”** : 做多行引用 
- **“\[^1\]”** ：脚注，“:”后为脚注的内容
- **“\-\-\-”** ：分隔符

- **“\`\`\`代码块\`\`\`”** ：代码块；（可以在第一行指定语言名）
- **“\`代码\`”** : 行内代码
- **“\|title 1\|title 2\|title 3”** : 表格制作法
- **“加\:,左，右，左右”** : 表格的对齐方式 

- **“行位+两个空格”** : 换行
- **“\<br\>”** : 用 html 标签换行

- **“\!\[图片说明\]\(图片链接\)”** ： 图片引用
- **“\\” :** 转义字符

## 2. Obsidian 语法

- **“\[\[内容\]\]”** ：obsidian 双链
- **“! + 双链”** ：引用展示，嵌入笔记，可用于文本和多媒体素材
- **“\[\[#标题内容\]\]”** ：文本内跳转相应的标题项内容
- **“\[\[文件名|别名\]\]”** ：Alias别名，给文件创建别名，让名字更有意思，搜索更快捷；可以在metadata里应用，作为aliases项


## 3. Cite 语法

- **\[\[\]\]** ：双链引用
- **!\[\[\]\]** ：展示引用内容
- **\[\[\#引用标题\]\]** ：当前文本内标题引用
- **\[\[^引用块\]** ：当前文本内内容块引用
- **!\[\[^引用块\]\]** ：展示当前文本块内容
- **\[\[^^引用块\]\]** ：所有笔记的块内容 

## 3. Callout 语法

- **语法**：
- \>空格\[\!标注类型\] name（可选择，修改名字）
- \>标注文字

- **分为可折叠(有“-”)/不可折叠(无“-”)**:
- \>空格\[\!标注类型\]\- name（可选择，修改名字）
- **例子**:
> [!note]- FOLD
> 
> This is an example... 
> This is an example...
> This is an example...

> [!tip] UNFOLD
> This is an example...
> This is an example...
> This is an example...

- **可嵌套**：
> [!info] INFO
>> [!check] CHECK
>> Check the information

- **自带类型**：
> [!note] Note, Seealso

> [!abstract] Abstract, Summary, tldr

> [!info] Info, Todo

> [!tip] Tip, Hint, Important

> [!success] Success, Check, Done

> [!question] Question, Help, Faq

> [!warning] Warning, Caution, Attention

> [!failure] Failure, Fail, Missing

> [!danger] Danger, Error

> [!bug] Bug

> [!example] Example
> 

> [!quote] Quote, Cite

## 4. CardView 语法 (选用)

- 是一个卡片视图，可以折叠或者展开，标题卡片会显示为单独的一列
- 里面的内容是列表，有序/无序都可以；也可以是多个列表
- 不可以是多维列表
- 用来放置一些并列，琐碎的信息
- 只是修改了展示方式，笔记中依然是 callout 的格式
- 有序列表可以，但是不能显示序号
- 因为是新的\%\% \%\%列表，所以会从新的一行开始
- 超长文字也可以，滚动条会影响体验，将内容控制在合适长度
- 卡片的数量是动态的，不同窗口大小，手机上也可以显示

- **语法**：
- \> [!cards-show]- \*\*无序列表\*\* 第一张卡片内容
- \> \- 第二张
- \> \- 第三章
- ……
- 例子：

> [!cards-show]- 无序列表 第一张
> - 第二张
> - 第三张
> - 第四张
> - 第五张
> - 第六张


## 4. LaTex 数学公式

- **待更新**

## 5. Mermaid 图表语法

- **待更新**

## 6. Yaml/Property 语法

metadata
- \---- + \----：三个包裹起来
- 

---

# 四. 用到的插件

- Git：云端同步方案
	- 用法：跟 Github 仓库建立连接，多设备共享
- Calendar：日历插件
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
- Export Image：把笔记导出为图片
- Waypoint：在每个目录下建立一个索引文档，实时更新
	- 用法：\%\% waypoint \%\%
- Text Snippets：文件快捷输入，宏设定
	- 用法：快捷键 - Command + Z



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
- List outline：列表的层级线条


# PDF阅读以及标记

# Mermaid语法
 
| column1 | column2 | column3 |     |
| ------- | ------- | ------- | --- |
|         |         |         |     |
|         |         |         |     |
|         |         |         |     |

# AI 设置


# 主题设置

## Border 主题

### Todo List (List Style)
 
- [ ]     <-> To do \- \[ \]
- [/]     <-> In Progress \- \[/\]
- [x]     <-> Done \- \[x\]
- [-]     <-> Cancelled \- \[-\]
- [>]     <-> Rescheduled \- \[>\]
- [<]     <-> Scheduled \- \[<\]
- [!]     <-> Important \- \[!\]
- [?]     <-> Question \- \[?\]
- [i]     <-> Information \- \[i\]
- [S]     <-> Amount \- \[S\]
- [*]     <-> Star \- \[\*\]
- [b]     <-> Bookmark \- \[b\]
- ["]     <-> Quote \- \["\]
- [n]     <-> Note \- \[n\]
- [l]     <-> Location \- \[l\]
- [I]     <-> Idea \- \[I\]
- [p]     <-> Pro \- \[p\]
- [c]     <-> Con \- \[c\]
- [u]     <-> Up \- \[u\]
- [d]     <-> Down \- \[d\]


## Obsidian Web Clipper 剪藏

AI + claude or codex，or kimi or chatgpt

