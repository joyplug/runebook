---
layout: post
title:  "[python] print() & global & list & dic"
date:   2021-11-16 09:00:00 +0900
category: python
---

```python
print('Hello', end='')
print('World')
>> HelloWorld


print('cats', 'dogs', 'mice', sep=',')
>> cats,dogs,mice


'''함수에서 전역 변수에 저장된 값을 수정하려고 한다면 그 변수에 global 문을 사용해야 한다.'''

def spam():
global eggs
egges = 'spam'

eggs = 42
spam()
print(eggs)
>> spam



listItem.index('Pooka')
listItem.append('Moose')
listItem.insert(1, 'chickken')
listItem.remove('bat')
listItem.sort()
listItem.sort(reverse=True)
listItem.sort(key=str.lower)



spam = {'color':'red', 'age':42}
for v in spam.values():
    print(v)

for k in spam.keys():
    print(k)

for i in spam.items():
    print(i)

for k, v in spam.items():
    print('Key:' + k + ' Value:' + str(v))


>>> picnicItems = {'apple':5, 'cups':2}

>>> 'I am bringing' + str(picnicItems.get('cups', 0) + ' cups.'
'I am bringing 2 cups.'

>>> 'I am bringing' + str(picnicItems.get('eggs', 0) + ' eggs.'
'I am bringing 0 eggs.'



>>> 'ABC'.join(['My', 'name', 'is', 'Simon'])
'MyABCnameABCisABCSimon'

>>> 'My name is Simon'.split()
['My', 'name', 'is', 'Simon']

>>> spam = '''Dear Alice,
How have you been? I am fine.

Bye
Sincerely,
Bob'''

>>> spam.split('\n')
['Dear Alice', 'How hava you been? I am fine', '', 'Bye', 'Sincerely', 'Bob']

```
