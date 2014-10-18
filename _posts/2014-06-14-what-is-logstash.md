---
layout: post
title:  "What Is Logstash?"
date:   2014-06-18 12:39:45
categories: logstash
---

Not too long ago I spent an afternoon trying to wrap my head around Logstash and what it actually is and how to get it to work. This post is what I perceive it to be in hopes that it might help someone else out there.

Logstash is an adapter, router and parser/transformer for logs, all built into one. Actually it's two adapters, one in and one out. In other words what logstash does is it consumes logs from a source (the first adapter), transforms them (if necessary) and then routes them to a target (the second adapter).

```
Adapter -> Transform -> Route -> Adapter
```


Logstash has many different adapters available so that many different sources and targets can be specified (but surprisingly non for JMS). It seems to be mostly built in JRuby on the JVM.

The advantages as I see it is that you get out of the box functionality for managing your logging events and transporting them from sources to targets.

The disadvantages are that you have to learn new technology, including how you deploy, configure and monitor it.