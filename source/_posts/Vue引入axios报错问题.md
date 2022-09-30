---
title: Vue引入axios报错
date: 2022-09-13 21:23:58
categories: [笔记]
tags: [Vue, axios, Web]
---

# Vue 引入 axios 报错 TypeError Cannot read property protocol of undefined

### Vue 引入 axios 报错

---

### 错误信息

```c++
Uncaught (in promise) TypeError: Cannot read property 'protocol' of undefined
    at isURLSameOrigin (isURLSameOrigin.js?3934:57)
    at dispatchXhrRequest (xhr.js?b50d:109)
    at new Promise (<anonymous>)
    at xhrAdapter (xhr.js?b50d:12)
    at dispatchRequest (dispatchRequest.js?5270:52)
```

### 错误的引入方式

```js
import axios from "axios"; //引入
Vue.use(axios); //使用 正是这种使用方式导致的报错
```

### 正确的引入方式

```js
import axios from "axios"; //引入
Vue.prototype.$http = axios; //正确的使用
```

————————————————
版权声明：本文为 CSDN 博主「断风尘」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/android_app_2012/article/details/106475808
