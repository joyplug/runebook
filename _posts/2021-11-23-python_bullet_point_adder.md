---
layout: post
title:  "[python] bullet point adder"
date:   2021-11-23 09:00:00 +0900
category: python
---

```python
#! python3
# bulletPointAdder.py - Adds Wikipedia bullet points to the start 
# of each line of text on the clipboard. 

import pyperclip
text = pyperclip.paste()

# TODO: Separate lines and add start.break
lines = text.split('\n')
for i in range(len(lines)):
    lines[i] = '*' + lines[i]

text = '\n'.join(lines)
pyperclip.copy(text)

"""
ABCD
EFGH
IJKLMN

*ABCD
*EFGH
*IJKLMN
"""

```
