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

# 代码
`package bin

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
`

# 分割线
***
