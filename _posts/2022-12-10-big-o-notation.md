---
layout: post
title:  "Big O notation"
date:   2022-12-10 15:07:19
categories: [data structure]
comments: true
---
On my path learning data structure, I thought It'd be nice to make a post with a quick explanation about Big O notation with Java examples.


<img alt="Light" src="{{ site.url }}/img/big-o-graph.png" width="55%">


<!--more-->

### What is Big O?

Big O is used for measure the time complexity of an algorithm. It helps to understand how efficient is the code, dealing with the worst scenario, as the good scenario does not tell us much.

### O(n)

```java
public static void printItems(int n) {
    for (int i = 0; i < n; i++) {
        System.out.println(i);
    }
}
``` 

Drop Constants

```java
public static void printItems(int n) {
    for (int i = 0; i < n; i++) {
        System.out.println(i);
    }

    for (int j = 0; j < n; i++) {
        System.out.println(i);
    }
}
``` 

###  O(n^2)

```java
public static void printItems(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            for (int k = 0; k < n; k++) {
                System.out.println(String.format("%s, %s, %s",i,j,k));
            }
        }
    }
}
``` 

### O(1) 

```java
public static int printItems(int n) {
    return n + n + n;
}
``` 


### (log n)

```java
public static void printItems(int n) {
    for (int i = 1; i < n; i = i * 2){
        System.out.println(i);
    }
}
``` 


References:

 - https://www.baeldung.com/java-algorithm-complexity
 - https://www.freecodecamp.org/news/big-o-notation-why-it-matters-and-why-it-doesnt-1674cfa8a23c/