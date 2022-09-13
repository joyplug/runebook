---
layout: post
title:  "[python] print picnic"
date:   2021-11-21 09:00:00 +0900
category: python
---

```python
def printPicnic(itemDict, leftWidth, rightWidth):
    print('PICNIC ITEMS'.center(leftWidth + rightWidth, '-'))
    for k, v in itemDict.items():
        print(k.ljust(leftWidth, '.') + str(v).rjust(rightWidth))

picnicItems = {'sandwitches':4, 'apples':12, 'cups':4, 'cookies':8000}

printPicnic(picnicItems, 12, 5)
printPicnic(picnicItems, 20, 6)

"""
---PICNIC ITEMS--
sandwitches.    4
apples......   12
cups........    4
cookies..... 8000
-------PICNIC ITEMS-------
sandwitches.........     4
apples..............    12
cups................     4
cookies.............  8000
"""

```
