---
title: 查找文件中 abc 出现的次数
toc: false
date: 2015-09-16 15:53:20
tags: Linux
categories: Linux

---

linux查找字符串的几种方法。

### 1.
```
grep -o abc file | wc -l
```
### 2.
```
awk -v RS='abc' 'END {print --NR}' file
```
### 3.
```
awk -v RS="@#$j" '{print gsub(/abc/,"&")}' NOTICE
```
### 4.
```
grep -c "abc" NOTICE
```
