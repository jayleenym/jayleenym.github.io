---
layout: post
type: blog
date: 2022-05-05 23:43
category: 프로그래머스
title: Lv. 1 신고 결과 받기
subtitle: 2022 KAKAO BLIND RECRUITMENT
post-header: true
header-img: img/programmers.png
hash-tag: [프로그래머스, 코딩테스트]
---
문제 링크 - https://programmers.co.kr/learn/courses/30/lessons/92334

너무 복잡하게 풀이한 것 같다..ㅠ 내일 일어나서 다시 해봐야지!

```python
from collections import Counter

def solution(id_list, report, k):
    report_dict = {id_list[i] : [] for i in range(len(id_list))}
    for r in report:
        a, b = r.split()
        report_dict[a].append(b)
        report_dict[a] = list(set(report_dict[a]))
    for_k = []
    for i in report_dict.keys(): for_k += report_dict[i]
    for_k = dict(Counter(for_k))
    
    reported = [a for a, b in for_k.items() if b>= k]
    for a, b in report_dict.items():
        for i in range(len(b)):
            if b[i] in reported: b[i] = 1
    return [i.count(1) for i in report_dict.values()]

```