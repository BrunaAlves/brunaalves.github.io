---
layout: post
title:  "Regular expression"
date:   2023-01-08 15:07:19
categories: [regular expression]
comments: true
---
A brief explanation about Regular expression.


<!--more-->

### What is Regular expression?

It is a technology for expression pattern of text using symbols.

###### Allow lower and upper case: []
```java
"cat".matches("[cC]at");
``` 
Express a range
```java
"cat".matches("[a-fA-Fw-zW-Z]at");
``` 

###### Not in: ^
```java
"cat".matches("[^c]at");
``` 
Not in a range
```java
"cat".matches("[^a-z]at");
``` 

###### Match any character: \w
One word character follow by at. Also allow numbers.
```java
"cat".matches("\wat");
``` 

###### Match any number/digits: \d
One word character follow by at. Also allow numbers.
```java
"cat2".matches("\wat\d");
```

###### Match space: \s
One word character follow by at. Also allow numbers.
```java
"cat 2".matches("\wat\s\d");
```




References:

 - 
