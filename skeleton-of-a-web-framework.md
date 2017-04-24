---
title: SKELETON OF A WEB FRAMEWORK
date: 2017-04-23 00:41:57
tags:
---

### Main components

1. __router__ route from uri to request handler
1. __request__ access request parameters
1. __controller__ handle reqeust, run business logic, produce response
1. __response__ build response construct


### Optional components

1. __middleware injection interface__ interfaces for injecting middlewares
1. __data access tool__ tools for access multiple tyle of data types(sql and no sql)
1. __config loader__ load config vars for different env
1. __template engine__ render html with template and data
1. 
