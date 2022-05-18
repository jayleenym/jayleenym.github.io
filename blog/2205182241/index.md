---
layout: post
type: blog
date: 2022-05-18 22:41
category: 프로그래머스
title: Lv. 1 숫자 문자열과 영단어
subtitle: 2021 카카오 채용연계형 인턴십
post-header: true
header-img: img/programmers.png
hash-tag: [프로그래머스, 코딩테스트]
---
[문제 링크](https://programmers.co.kr/learn/courses/30/lessons/81301)

---

### ✍🏻 Comment
영단어를 숫자로 바꾸는 간단한 작업. python의 replace로 쉽게 해결할 수 있었다. 

### ⌨️ Code
```python
def solution(s):
    num = {'one':'1', 'two':'2', 'three':'3',
            'four': '4', 'five':'5', 'six':'6', 'seven':'7', 'eight':'8', 'nine':'9', 'zero':'0'}
          # 대응되는 영단어 dictionary로 만들기 
    for n in num: 
        s = s.replace(n, num[n]) # 영어 문자열 숫자로 바꾸기

    return int(s)
```