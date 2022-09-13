---
layout: post
title:  "[python] magic 8 balls"
date:   2021-11-19 09:00:00 +0900
category: python
---

```python
import random

messages = ['It is certain',
    'It is decidedly so',
    'Yes definitely',
    'Reply hazy try again',
    'Ask again later',
    'Concentrate and ask again',
    'My reply is no',
    'Outlook not so good',
    'Very doubtful']

print(messages[random.randint(0, len(messages)-1)])

```
