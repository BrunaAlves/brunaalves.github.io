---
layout: post
title:  "Basic syntax of regular expression"
date:   2023-01-11 17:07:19
categories: [regular expression]
comments: true
---
A brief explanation about the basic of regular expression.


<!--more-->

### What is Regular expression?
It is a technology for expression pattern of text using symbols.

#### Allow lower and upper case: []
```java
"cat".matches("[cC]at");
``` 
Express a range
```java
"cat".matches("[a-fA-Fw-zW-Z]at");
``` 

#### Not in: ^
```java
"cat".matches("[^c]at");
``` 
Not in a range
```java
"cat".matches("[^a-z]at");
``` 

#### Match any character: \w
One word character follow by at. Also allow numbers.
```java
"cat".matches("\\wat");
``` 

#### Match any number/digits: \d
One word character follow by at. Also allow numbers.
```java
"cat2".matches("\\wat\\d");
```

#### Match space: \s
One word character follow by at. Also allow numbers.
```java
"cat 2".matches("\\wat\\s\\d");
```

#### Match group of digits:
###### Digit and space repeatable at n times {}
```java
"321-333-7652".matches("\\d{3}-\\d{3}-\\d{4}");
```

###### Group od different characters []
```java
"321-333.7652".matches("\\d{3}[-,.\\s]\d{3}[-,.\\s]\\d{4}");
```

###### One or more what there is before(One or more space in that case): +
```java
"321-333    7652".matches("\\d{3}[-,.\\s]+\d{3}[-,.\\s]+\\d{4}");
```

###### Possibility of zero or more: *
```java
"321-3337652".matches("\\d{3}[-,.\\s]*\d{3}[-,.\\s]*\\d{4}");
```

###### Zero or just one: ?
```java
"321-3337652".matches("\\d{3}[-,.\\s]?\d{3}[-,.\\s]?\\d{4}");
```

###### Min and max range: {n,n}
```java
"321-333-652".matches("\\d{3}[-,.\\s]?\d{3}[-,.\\s]?\\d{3,4}");
```

###### Specify one or the other(min 3 digit with no upper limit): {n,}
```java
"321-333-652".matches("\\d{3}[-,.\\s]?\d{3}[-,.\\s]?\\d{3,}");
```

###### Reduce repeatable chars:

Before
```java
"321-333-652".matches("\\d{3}[-.,\s]?\\d{3}[-.,\s]?\\d{4}");
```

After(group repeatable 2 times)
```java
"321-333-652".matches("(\\d{3}[-.,\\s]?){2}\\d{4}");
```


References:
 - https://www.udemy.com/course/neutrino-java-foundations
