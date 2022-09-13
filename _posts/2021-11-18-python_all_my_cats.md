---
layout: post
title:  "[python] all my cats"
date:   2021-11-18 09:00:00 +0900
category: python
---

```python
catNames = []
while True:
    print('Enter the name of cat' + str(len(catNames)+1) + ' (Or enter nothing to stop.): ')
    name = input()
    if name == '':
        break
    catNames = catNames + [name]

print('The cat names are: ')
for name in catNames:
    print(' ' + name)

'''
Enter the name of cat1 (Or enter nothing to stop.): 
Zophie
Enter the name of cat2 (Or enter nothing to stop.): 
Pooka
Enter the name of cat3 (Or enter nothing to stop.): 
Simon
Enter the name of cat4 (Or enter nothing to stop.): 
Lady Macbeth
Enter the name of cat5 (Or enter nothing to stop.): 
Fat-tail
Enter the name of cat6 (Or enter nothing to stop.): 
Miss Cleo
Enter the name of cat7 (Or enter nothing to stop.): 

The cat names are: 
 Zophie
 Pooka
 Simon
 Lady Macbeth
 Fat-tail
'''

```
