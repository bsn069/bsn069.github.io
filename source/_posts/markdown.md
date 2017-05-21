---
title: markdown
tags:
  - unknown
categories:
  - unknown
date: 2017-05-21 20:51:11
---
摘要
<!--more-->

# 标题1
## 标题2
### 标题3
####  标题4
##### 标题5
###### 标题6

# 有序表
1. 这是1
2. 这是2
    1. 这是1
    2. 这是2
        1. 这是1
        2. 这是2
        4. 这是4
        6. 这是6
    4. 这是4
    6. 这是6
3. 这是3

# 无序表
- 这是1
- 这是2
    - 这是1
    - 这是2
    - 这是3
- 这是3
    1. 这是1
    2. 这是2
        - 这是1
        - 这是2
        - 这是3
    4. 这是4
    6. 这是6

* 这是4
* 这是5
* 这是6
    - 这是7
    - 这是8
    - 这是9
        - 这是
            - 这是
                * 这是
                    * 还是

# 图片
![图片](https://www.baidu.com/img/baidu_jgylogo3.gif)

> 这里是引用

# 链接
[baidu](https://www.baidu.com)

# **粗体** *斜体*

# 表格
| Tables    | Are           | Cool  |
| -------------:|:-------------:| :-----|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

| 姓名     | 年龄| 性别|
|:--------|---------:|:-------:|
| 张三| 18| 女      |
| 小明| 23| 男      |

Name | Academy | score
- | :-: | -:
Harry Potter | Gryffindor| 90
Hermione Granger | Gryffindor | 100
Draco Malfoy | Slytherin | 90

| 参数 |详细解释|备注|
| - | - | - |
| -l | use a long listing format |以长列表方式显示（显示出文件/文件夹详细信息） |
| -t | sort by modification time |按照修改时间排序（默认最近被修改的文件/文件夹排在最前面） |
|-r | reverse order while sorting |逆序排列|


<table>
  <tr>
    <th width=10%, bgcolor=yellow >参数</th>
    <th width=40%, bgcolor=yellow>详细解释</th>
    <th width="50%", bgcolor=yellow>备注</th>
  </tr>
  <tr>
    <td bgcolor=#eeeeee> -l </td>
    <td> use a long listing format  </td>
    <td> 以长列表方式显示（显示出文件/文件夹详细信息）  </td>
  </tr>
  <tr>
    <td bgcolor=#00FF00>-t </td>
    <td> sort by modification time </td>
    <td> 按照修改时间排序（默认最近被修改的文件/文件夹排在最前面） </td>
  <tr>
    <td bgcolor=rgb(0,10,0)>-r </td>
    <td> reverse order while sorting </td>
    <td>  逆序排列 </td>
  </tr>
</table>

# 代码
    package bin

    import (
      "sync"
    )

    var g_bins map[uint64]IBin
    var g_binMutex sync.Mutex
    var g_waitQuit sync.WaitGroup
    var g_cmd map[string]func(strParam string, bHelp bool) bool
    var g_lastBin IBin

    func init() {
      cmdReg()
      g_bins = make(map[uint64]IBin)
      go inputThread()
    }


# 分割线
***

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

> ## 这是一个标题。
> 
> 1.   这是第一行列表项。
> 2.   这是第二行列表项。
> 
> 给出一些例子代码：
> 
>     return shell_exec("echo $input | $markdown_script");

*   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
*   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

*   A list item with a blockquote:

    > This is a blockquote
    > inside a list item.    

This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.

See my [About](/t1.md) page for details.

This is [an example][foo] reference-style link.

[Google][]

[foo]: http://example.com/  "Optional Title Here"
[foo]: http://example.com/  'Optional Title Here'
[foo]: http://example.com/  (Optional Title Here)
[Google]: http://google.com/

I get 10 times more traffic from [Google][] than from
[Yahoo][2] or [MSN][3].

[2]: http://search.yahoo.com/  "Yahoo Search"
[3]: http://search.msn.com/    "MSN Search"


Use the `printf()` `function`.

``There is a literal backtick (`) here.``

<http://example.com/>

<address@example.com>

\*literal asterisks\*