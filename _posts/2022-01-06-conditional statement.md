---
layout : single
title : "파이썬 조건문(if)
---

```python
# 코드 4-1
print("Tell me your age")
myage = int(input())

if myage < 30 :
    print("Welcome to the club")
else :
    print("Oh No, Yor are not accepted")
```

    Tell me your age
    55
    Oh No, Yor are not accepted
    


```python
# 코드 4-2
score = int(input("Enter your score:"))

if score >= 90 :
    grade = 'A'
if score >= 80 :
    grade = 'B'
if score >= 70 :
    grade = 'C'
if score >= 60 :
    grade = 'D'
if score < 60 :
    grade = 'F'

print(grade)
```

    Enter your score:55
    F
    


```python
# 코드 4-3 
score = int(input("Enter your score:"))

if score >= 90 : grade = 'A'
elif score >= 80 : grade = 'B'
elif score >= 70 : grade = 'C'
elif score >= 60 : grade = 'D'
else : grade = 'F'
    
print(grade)
```


```python
# 코드 4-4(Lab)
print("당신이 태어난 연도를 입력하세요.")
birth_year = input()
age = 2021 - int(birth_year)

if age <= 26 and age >= 20 :
    print("대학생")
elif age <= 20 and age >= 17 :
    print("고등학생")
elif age <= 17 and age >= 14 :
    print("중학생")
elif age <= 14 and age >= 8 :
    print("초등학생")
else :
    print("학생이 아닙니다.")
```

    당신이 태어난 연도를 입력하세요.
    1998
    대학생
    
