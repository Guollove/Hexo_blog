---
title: 手机正则效验
date: 2022-09-13 21:23:58
categories: [笔记]
tags: [Vue, elemuntui, Web]
---

# vue+[elementui](https://so.csdn.net/so/search?q=elementui&spm=1001.2101.3001.7020)手机号正则校验

```js
1. /^1(3|4|5|7|8|9)\d{9}$/
2. /^1[3456789]\d{9}$/
// 在表单rules中可以这样写规则验证
rules:[
  mobile: [
    {
       required: true,
         message: '请输入手机号',
         trigger: 'blur'
    },
    {
      required: true,
        pattern: /^1[3456789]\d{9}$/,
        message: '手机号格式不正确',
        trigger: 'blur'
    }
  ]
]
```
