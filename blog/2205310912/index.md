---
layout: post
type: blog
date: 2022-05-31 09:12
category: 딥러닝
title: 트랜스포머 Transformer
subtitle: KAIST AI대학원 서민준 교수님
post-header: true
header-img: img/GSAI.png
hash-tag: [pytorch, transformer, 트랜스포머, 딥러닝, NLP]
---

## Attention
- 내가 어떤 단어를 봐야 잘 처리할 수 있을까
### Query, Key, Value
- Query: **요구사항**, DB에서 어떤 내용을 가져왔으면 좋겠어!   
    - ex. key가 x인 value들을 가져왔으면 좋겠어!
- Key:
- Value:

I
go
home
을 각각 선형변환을 통해 q,k,v로 변환 (가중치: w_q, w_k, w_v)

|x||y|cos_seta = x _dot y  
F: feature dimension != vocab size
큰 블럭하나에 - 선형변환 5개, norm 2개

query, key: 가중치를 구하는 도구  
value: attention 값을 구함  