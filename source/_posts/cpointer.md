---
title: C语言的指针
date: 2023-09-30 22:12:00
tags:
- ideas
categories: 趣谈
---

>“你完全说不清楚话......，可以来我们学校当大学老师了。” ——匿名人士

## 要抓住男人的心，就要抓住男人的胃

如果你学过C语言，那么这句话有没有让你想到指针呢？
```C
struct stomach {
    // 胃里的一大堆东西（e.g.胃酸）
}

struct stomach mans_stomach = struct stomach { /* ... */ };
struct stomach *mans_heart = &mans_stomach;
```

现在如果我们要抓住男人的心，那么相当于
```C
*mans_heart = \* ... *\;
```
也就是说我们抓住了他的胃。

那么有没有更好的解决方案呢？比如下面这样
```C
void *mans_heart;
```

这样要抓住男人的心，不必再以胃作为前提条件，只要你愿意你抓他哪里都可以。下面是一个例子。
```C
// 假设struct eye已经定义
struct eye mans_eye = INIT_EYE;
mans_heart = (void *)&mans_eye;
```
这样，要抓住男人的心，就要抓住男人的眼睛。

## 说明
- 事实上，这是对Peter Van Der Linden《C专家编程》第三章分析《爱丽丝梦游记》庸俗的模仿。
- 你看的出来吗？以比喻来描述问题的方式根本不是在**解释**问题，而仅仅是在理解问题的基础上获得乐趣。