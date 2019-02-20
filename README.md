# Django Web开发技术栈 - 面试常见问题整理

这篇内容是摘自[《Django企业开发实战》](https://www.the5fire.com/983.html)，这是这本书在让[大妈（Zoom.Quiet)](https://github.com/ZoomQuiet) Review 时，大妈给的建议。

出版物的生命周期比较短，索性放开到Github上，集众人智慧，构建一个能供所有想要学习 Python Web 开发或者 Django 的一个参考，与其说是面试参考，不如说是知识点清单，供大家查漏补缺，进一步提高自己的「战斗能力」。

目前只是可能会问到的问题或者知识点，还没有对应的答案，答案欢迎大家通过 issues 的方式来参与。

仓库地址: https://github.com/the5fire/django-interview-questions ，欢迎 star，欢迎贡献内容。

## 1. Python基础

* 基础语法是否熟悉？介绍下。
* 有哪些关键字，并且解释其作用？
* 有哪些内置方法，并且解释其作用？
* 解释下什么是动态语言？动态强类型是指什么？
* 是否有编码规范的概念？采用的是哪中编码规范？
* 解释下深拷贝和浅拷贝
* lambda的用法以及使用场景？
* 解释下什么是闭包，以及它的作用？
* 实现一个简单的装饰器，用来对某个函数的结果进行缓存？
* Python中几种容器类型的差别及使用场景？
* 列表推导式的使用和场景？
* yield的使用。
* 常用的内置库有哪些？举例他们的用法。
* 介绍下你了解的"dunder method"（魔法方法）有哪些，以及他们的作用？
* 解释下面向对象的概念，以及在编程中的作用？
* 如何实现单例模式？
* 如何对Python对象进行序列化？
* 是否能够熟练编写多线程和多进程程序？
* 使用socket编写一个简单的HTTP Server，成功返回success即可。
* 如何理解Python中的GIL？对我们日常开发有什么影响？
* 解释下协程、线程、进程之间的差别。


## 2. Django基础

#### 整体结构

* 如何理解设计模式中的MVC模式，你日常中怎么使用这种模式？
* 如何理解Django中的MTV模型？
* 介绍下Django中你熟悉的模块有哪些，分别作用是什么？
* 如何看待Django自带的Admin，以及说说你的使用经验。
* 如何理解WSGI的作用？
* 如何自己实现WSGI协议？
* 为什么正式部署时不要开启``DEBUG = True``配置？

#### Model层

* 如何理解Django Migrations的作用？
* 是否有过手动编辑Migrations文件的经历，原因是什么，有哪些需要注意的？
* 介绍下ORM的概念。
* 如何理解ORM在Django框架中的作用？
* 介绍下ORM下的N+1问题，发生的原因，以及解决方案。
* 介绍下Django中Model的作用。
* Model的Meta属性类有哪些可配置项，作用是什么，日常用到的。
* 介绍下QuerySet的作用，以及你常用的QuerySet优化措施？
* 介绍下Pagination的使用。
* 介绍下Model中Field的作用。
* 如何定制Manager？什么场景下需要定制？
* Raw SQL的效率跟ORM的效率是否进行过对比，结果如何？如何理解这种差异？
* Django内置提供的权限逻辑是什么，以及其粒度？

#### View层

* Django中function view和Class-based View的差别及适用场景？
* 如何给Class-based View添加login required装饰器？
* Middleware在Django系统中的作用？
* settings中默认配置的MIDDLEWARES有哪些？他们的作用分别是什么？是否可以移除？
* Django系统如何判断用户是否为登录用户？
* 对于无Cookie的浏览器如何实现用户登录？
* Django中的request和HttpResponse的作用是什么？
* 如何处理图片上传的逻辑，以及展示逻辑？
* 介绍下用到过的Django的缓存粒度。

#### Form层

* 介绍下Django中Form的作用。
* Form中的Field跟Model中的Field有何关联？
* 如何在Form层实现对某个字段的校验？

#### Template层

* 如何理解Django模板对设计师友好的说法？
* 日常开发中如何规划Django的模板继承和include？
* 常用的标签（tag）和过滤器（filter）有哪些？
* 在模板中如何处理静态文件？
* 在模板中如何处理系统内定义的URL？
* 如何自定义标签和过滤器？


## 3. Django进阶

* 如何排查Django项目的性能问题？
* 如何部署Django项目，以及不同的部署方式之间的差别？
* 部署时如何处理项目中的静态文件？
* 如何实现自定义的登录认证逻辑？
* 如何理解Django中Model、Form、ModelForm和Field、Widgets之间的关系？
* Paginator的原理是什么，如何自己实现分页逻辑?
* Model中Field的作用是什么？
* 什么是SQL注入，ORM又是如何解决这个问题的？
* CSRF全称是什么？Django是如何解决这个问题的？
* XSS攻击是指什么，在开发时应该如何避免这种攻击？
* Signal的作用以及实现逻辑？
* DATABASE配置中的``CONN_MAX_AGE``参数的作用，以及使用场景？
* ``CONN_MAX_AGE``的实现逻辑是什么？
* 用Django内置的User模型创建用户时是否可以直接:``User(username='the5fire', password='the5fire').save()``？
* 上面的创建方式有什么问题？应该如何处理用户密码？
* 使用Django-rest-framework如何实现用户认证登录逻辑？
* Session模块在Django中的作用是什么？
* 如何自定义Django中的权限粒度，实现自己的权限逻辑？
* 如何捕获线上系统的异常？
* 如何分析某个接口响应时间过长的问题，假设响应时间为2秒，一次请求涉及到数据库和缓存查询。


## 4. 部署相关

* 如何来自动化部署项目到生产环境，具体流程？
* 介绍下常用的自动化部署工具？
* 用到哪些监控工具，作用是什么，使用中有什么不足之处？
* Supervisor的作用是什么？为何使用它？
* Gunicorn的作用是什么？为何使用它？
* 如何对系统进行压测？以及流量预估？
* Nginx的作用是什么？是否能独立配置？有没有优化经验？
* 发版逻辑是什么，如何保证新版本发生异常时能快速回滚？


## 5. MySQL数据库

* 如何确定需要哪些字段需要设置索引？
* 什么情况下需要设定字段属性为``unique = True``？
* 如何排查某个SQL语句的索引命中情况？
* 如何排查查询过慢的SQL语句？

## 6. Redis

* 你了解的Redis的特点是什么？为什么会使用它？
* 支持的数据类型
* 如何合理的规划key？
* 比如我需要把所有的文章和分类数据写入Redis，在Django中直接读取Redis拿到分类和文章的数据，问怎么规划数据存储，如何处理分页？
* 是否支持事务？举个例子。
* 有哪些数据淘汰策略？
* 当你发现有些Redis查询响应时间太长，如何排查？可能是什么引起的？
* 你用到的或者了解的Redis的部署结构是什么？
* 是否了解Redis的持久化策略，不同的策略有什么不同？
* 说说你了解的Redis主从同步的策略。


## 7. 常用算法

* Python中字典类型的实现算法？
* 你了解的高级语言中的垃圾回收机制有哪些？Python中用的是什么？
* 介绍下你知道的缓存相关的算法？
* 介绍下你知道的负载均衡相关的算法？
* 介绍下数据库索引相关算法？


## 8. 总结

上面列的很多内容都已经超出了Django的范围，但依然是属于Web开发领域需要掌握的知识。

就Django本身来说，它只是Python众多Web开发框架中的一个，单纯的掌握Django的使用并不能让你满足企业中对Web开发的需求。因此把本书作为你开启Web开发之路的起点，在扎实地掌握Django使用之后，可以由此展开，去涉及Web开发的方方面面。


*广告*

京东：[《Django企业开发实战 高效Python Web框架指南》(胡阳)【摘要 书评 试读】- 京东图书](https://item.jd.com/12537842.html)

当当：[Django企业开发实战 高效Python Web框架指南](http://product.dangdang.com/26509799.html)
