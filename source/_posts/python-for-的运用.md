title: "python for 的运用"
date: 2015-07-01 23:00:07
tags: [python,for,python语法]
---
#一、[enumerate](#001)
#二、[dict items iteritems](#002)

##<a name="001">一、enumerate:</a>

<pre><code>
dict_a = {"a":1,"b":2}
for k,v in enumerate(dict_a):
    print k,v 
结果:
0 a
1 b


sli = ["a","b","c"]
for k,v in enumerate(sli):
    print k,v
结果:
0 a
1 b
2 c

结论:enumerate是每个元素的k返回的是每个元素的位置,v是元素的值
</code></pre>


##<a name="002">二、dict items iteritems:</a>
<pre><code>
dict_a = {"a":1,"b":2}
for (k,v)in dict_a.items():
     print k,v
结果:
a 1
b 2

for k,v in dict_a.iteritems():
    print k,v
结果:
a 1
b 2

items和iteritems 都可以遍历出 键和值，
items函数返回的是键值对的元组的列表，而iteritems使用的是键值对的generator。 
</code></pre>

