新生网站 <https://rebirthjournal.cn>。

# 上传指导

## 这些文件是什么？

所有的文章都在`_articles/`文件夹之内、图片在`img/`内。除了这两个文件夹之外都是代码。要上传新的文章，可以直接上传到`_articles/`和`img/`。

## 如何上传新的文章？

`_articles`文件夹排版如下：

          _articles/
    (1)     index.md
    (2)     [第一期]/
    (3)       index.md
    (4)       [假真實與真夢境]/
    (5)         index.md
    (6)         [今天是张肝的好日子].md

`index.md`均为设置文件。

### 更改期刊顺序

文件(1) `_articles/index.md`是所有期刊的顺序。内容如下：

```
---
issues:
  - [期刊1]
  - [期刊2]
  - ...
---
```

例如：

```
---
issues:
  - 第一期
  - 第二期
  - 小说特刊
  - ...
---
```

### 添加期刊

在`_articles/`下有多个文件夹，分别是每一期期刊。若要添加期刊：

1. 新建一个文件夹，如(2) `_articles/[期刊名称]/`；
2. 如上，更改上方的文件(1) `_articles/index.md`，末端加上`  - [期刊名称]`；
3. 如下，新建一个期刊设置文件(3) `_articles/[期刊名称]/index.md`，填入期刊里面所有板块。

### 更改每一期板块/章节顺序

文件(3) `_articles/[期刊名称]/index.md`是所有板块的顺序。内容如下：

```
---
chapters:
  - [板块1]
  - [板块2]
  - ...
---
```

例（第一期）：

```
---
chapters:
  - 序言
  - 假真實與真夢境
  - 車輪滾滾
  - 詩從八方來
  - 光與影
  - 驪歌悠揚
  - 後記
  - ...
---
```

### 添加板块/章节

在(2) `_articles/[期刊名称]/.`下有多个文件夹，分别是每一期期刊。若要添加期刊：

1. 新建一个文件夹，如(4) `_articles/[期刊名称]/[板块名称]/`；
2. 如上，更改上方的(3) `_articles/[期刊名称]/index.md`，末端加上`  - [板块名称]`；
3. 如下，新建一个板块设置文件(5) `_articles/[期刊名称]/[板块名称]/index.md`，填入这个板块里面所有文章。

### 更改板块中的文章顺序

文件(5) `_articles/[期刊名称]/[板块名称]/index.md`是一个板块中所有文章的顺序。内容如下：

```
---
subtitle:
  - [副标题行1]
  - [副标题行2]
  - ...
subtitle_cite: [副标题引用自] (此行可选)
articles:
  - [文章文件名1]
  - [文章文件名2]
  - ...
---

[正文内容（即板块标题之后、第一篇文章之前的内容）]
```

例一（第一期/序言）：

```
---
subtitle:
  - 凡是人，不分地位、宗教信仰、年龄、性别、教育程度、家庭环境，都可以在写作上一试身手，甚至疯子、舞台艺术爱好者、被褫夺公权的人要写作，也不犯禁。
subtitle_cite: 契诃夫
articles:
  - 郭文瀚序言
  - 张云起序言
  - 胡臻杰序言
---

![](/img/Eric Tang.jpg)
{:.caption-bottom-right-outside caption="Eric Tang 唐宇澄"}
```

例二（第一期/假真实与真梦境）：

```
---
subtitle:
  - 化生活为神奇的能力
  - 是文字工作者赖以生存的土壤
articles:
  - 今天是张肝的好日子
  - 清晨的阳光
  - 怪圈
  - 宿梦
  - 四月的春雪
  - 希区柯克是如何满足观众的
---

![](/img/sophisticated.jpg)
{:.caption.bottom.left.inside caption="Danny Guo 郭文瀚"}
```

### 添加文章

在(4) `_articles/[期刊名称]/[板块名称]/.`下有多个文件，除了`index.md`外分别是每一篇文章。若要添加文章：

1. 新建一个文件，如(6) `_articles/[期刊名称]/[板块名称]/[文章文件名].md`；
2. 在这个文件中填入以下内容：

```
---
title: [文章标题]
author: [文章作者]
heading:
  - [显示的标题]
  - [显示的标题]
entry: [目录条目]
poem: true
---

[文章正文]
```

其中，`title`为文章的标题（如`title: 今天是张肝的好日子`），可选，若没有写`title`行则使用文件名为标题；

`author`为文章的作者（如`author: 吕枨予`），若多个作者，直接写“author: 作者一 & 作者二”就可以；

`heading`为行文中显示的文章标题（如`heading:↵  - 今天是张肝的好日子↵  - 吕枨予`），可选，若没有写`heading`则使用上方的`title`和`author`作为显示标题，若`heading: false`则不显示标题；

`entry`为目录里面显示的文章名（如`三首转瞬即逝的诗与歌`），可选，若没有写`entry`则使用上方的`title`作为目录条目，若`entry: false`则此文章将不会在目录里；因为是网页视图，目录里不显示作者；

`poem: true`表示此文章是一个诗歌，如果有此行，程序将取消段落首行缩进，可选；

文章正文排版见下。

例一（第一期/假真实与真梦境/今天是张肝的好日子，`今天是张肝的好日子.md`）：

```
---
author: 吕枨予
---

> ——“张肝永远无法忘记那晚的风。风大得很，他甚至感到风把发际线吹后面去了。
...
```

例二（第一期/诗从八方来/李思逸的第一首无题，`李思逸无题1.md`）：

```
---
title: 无题
author: 李思逸
entry: 三首转瞬即逝的诗与歌
poem: true
---

我闭上双眼
...
```

例三（第一期/序言/胡臻杰写的最后一个序言，`胡臻杰序言.md`）：

```
---
title: 序言
author: 胡臻杰
heading:
  - 胡臻杰
entry: false
---

很久没有看书了，更长的时间没有写过什么。
...
```

## 如何排版文章？

可以先参考已有的文章。一般情况下，只要输入正文即可，每一段用双换行隔开。一些特殊的排版如下：

```markdown
第一段正文。

第二段正文。

**粗体**

*着重*（效果是下面加点）

~~删除线~~

> 引用一段话。

# 大副标题

## 小副标题

[链接](https://rebirthjournal.cn)

![插入图片](/img/图片.jpg)
{:.caption.bottom.right.outside caption="作者"}
```

注意：图片要另起一段；需要跟一个`{:.caption.* caption="作者"}`，这里`.*`是说明文字的位置，里面可以是`.top`/`.right`/`.bottom`/`.left`，如果某个方向没写这个`.*`的话默认居中。使用`caption="说明文字"`来注明图片。

# 待实现的功能/修复

- [x] 插图
  - [x] 记得支持直接使用`![](){::.caption-top-left caption="作者"}`
  - [x] 记得使用`img[caption]::after { content: attr(caption) }`这种东西
  - [x] README添加插图文档
  - [x] 好像safari的caption会换行
- [ ] 期刊首章上方的期刊名+日期
- [ ] 在`window`的`load.bs.scrollspy.data-api`之前scrollspy都不能用；而现在`window`的`load`慢得像胡臻杰补作业一样
  - [x] 因为字体文件太大了，试一试subsetting
  - [x] 或者看一下字体加载有什么别的方法，可以FOUT之前直接触发`load`
  - [x] 实在不行可以不用自定义字体
  - [ ] 或者直接手动触发`Event`
- [x] 标题应为`display: flex; flex-wrap: wrap; some-kind-of-gap: 2em;`或者这类的基于`gap`或者`margin`的空白
- [x] scrollspy的`data-offset`好像需要比`:target`的`height`大那么一两个，不能都是`100`（不改了）
  - [x] 说到scrollspy，文章最上方根本不在`header > h1:target::before`范围内，而且这个`::before`对`#[板块名称]`的url根本没用，还是那样卡在navbar里面
    - [x] 这次改了标题之后现在所有的`:target`都不对了，我觉得最好直接在`<header>`和`<article>`前用一个ghost element `<span id="[名称]"></span>`；否则就revert之前的东西并且把所有`display: flex`去掉，这好像是个chrome的bug
- [x] 主页的大引号应该用`opacity`而不是`color: rgba()`
- [ ] `#contents`里面的`.active`和`:hover`的效果应该有点细微的不一样，比如一个`color: $color-primary`一个`text-decoration`或者后者比前者`color`更浅
- [x] 对`<main>`下面所有`<a>`都进行`a, a:hover { text-decoration: underline .2em }`而不是只是`<article>`
- [x] 适当将风格代码转移到`main`或`main > *`下，毕竟都是正文，格式应该相像
- [x] 看一下`MingLiU`是啥样的——太细了，不好看，去掉了
- [x] `a.footnote:target`会换行
- [ ] 应丹尼要求：
  - [ ] `poem`应该归为板块的front matter而不是单独文章的
  - [ ] 通过这个`poem`可以使得一个诗歌板块变窄（20em左右）
    - [ ] 所以不需要`max-width:`只要`width`就可以了
  - [ ] `poem`在`min-width`之下可以整个板块排成2列，到时候看一下是小还是大breakpoint好
    - [ ] 使用CSS grid做别用flex
  - [ ] 忙完这个之后看一下单独的poem文章怎么弄
- [x] 图片压缩
  - [ ] 最好可以写个程序
- [ ] 404页
- [ ] 管一下中文URL escape和relative URL

快了快了，别急别急
