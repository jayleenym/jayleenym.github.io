---
layout: post
type: blog
date: 2022-05-06 22:01
category: 프로그래머스
title: Lv. 1 신규 아이디 추천
subtitle: 2021 KAKAO BLIND RECRUITMENT
post-header: true
header-img: img/programmers.png
hash-tag: [프로그래머스, 코딩테스트]
---
문제 링크 - https://programmers.co.kr/learn/courses/30/lessons/72410

---

### ✍🏻 Comment
간단하게 정규표현식으로 7단계 해결! 역시 파이썬..C로는 어떻게 할 수 있을지 감도 안잡힌다..

### ⌨️ Code
```python
import re

def solution(new_id):
    ans = re.sub("[^a-zA-Z0-9-_.]", "", new_id.lower())
    ans = re.sub("[.]{2,}", ".", ans)
    ans = re.sub("^[.]|[.]$", "", ans)
    if len(ans) == 0: ans = 'a'
    if len(ans) >= 16: ans = re.sub("[.]$", "", ans[:15])
    if len(ans) <= 2: ans += ans[-1] * (3 - len(ans))
    return ans
```