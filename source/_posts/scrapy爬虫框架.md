title: "scrapy爬虫框架介绍"
date: 2015-05-10 15:56:29
tags: [python,scrapy,架构]
---
之前用scrapy来抓取东方财富网的研报信息,现在来总结下！
1.文档:<a href="http://doc.scrapy.org/en/latest/">scrapy</a> 一定要看英文官方文档,翻译的更新都不及时
2.分布式:主要配合<a href="https://github.com/darkrho/scrapy-redis">scrapy-redis</a>,通过redis来实现简单的分布式,这里面还要注意几个事项

