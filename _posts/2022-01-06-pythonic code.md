---
layout : single
title : "파이썬 스타일 코드"
---

# 문자열 분리 및 결합


```python
# split : 문자열 분리
example = 'python,jquery,javascript'
a, b, c = example.split(',') # 언패킹
result = example.split(',')  # 언패킹 x
print(a, b, c)
print(result)
```

    python jquery javascript
    ['python', 'jquery', 'javascript']
    


```python
# join : 문자열 결합
colors = ['red', 'blue', 'green', 'yellow']
result = ''.join(colors)
print(result)
```

    redbluegreenyellow
    


```python
result = ', '.join(colors)
print(result)
```

    red, blue, green, yellow
    

# 리스트 컴프리헨션


```python
# 10 이하의 짝수 생성
result = [i for i in range(10) if i % 2 == 0]
print(result)
```

    [0, 2, 4, 6, 8]
    


```python
# if를 앞으로 보내고, else와 함께 사용
result = [i if i % 2 == 0 else 10 for i in range(10)]
print(result)
```

    [0, 10, 2, 10, 4, 10, 6, 10, 8, 10]
    


```python
# 중첩 반복문
word1 = 'ABC'
word2 = 'DEA'
result = [i + j for i in word1 for j in word2]
print(result)
```

    ['AD', 'AE', 'AA', 'BD', 'BE', 'BA', 'CD', 'CE', 'CA']
    


```python
# 중첩 반복문 with filtering
result = [i + j for i in word1 for j in word2 if not(i == j)]
print(result)
```

    ['AD', 'AE', 'BD', 'BE', 'BA', 'CD', 'CE', 'CA']
    


```python
# 이차원 리스트 - word2의 j가 고정(*주의)
result = [[i + j for i in word1] for j in word2]
print(result)
```

    [['AD', 'BD', 'CD'], ['AE', 'BE', 'CE'], ['AA', 'BA', 'CA']]
    


```python
# 이차원 리스트 - word1의 i가 고정(*주의)
result = [[j + i for i in word2] for j in word1]
print(result)
```

    [['AD', 'AE', 'AA'], ['BD', 'BE', 'BA'], ['CD', 'CE', 'CA']]
    


```python
# 벡터와 스칼라의 곱
# 8-1 Loop(일반 반복문 + 리스트)
import time

start = time.time()

def scalar_vector_product(scalar, vector) :
    result = []
    for value in vector:
        result.append(scalar * value)
    return result

iteration_max = 10000

vector = list(range(iteration_max))
scalar = 2

for _ in range(iteration_max): # [0~9999]까지 리스트 배열 * 2를 10000번 반복
    scalar_vector_product(scalar, vector)
    
end = time.time()
print(end - start)
```

    8.903713703155518
    


```python
# 벡터와 스칼라의 곱
# 8-2 리스트 컴프리헨션
import time

start = time.time()

iteration_max = 10000

# vector = list(range(iteration_max))
scalar = 2

for _ in range(iteration_max):  # [0~9999]까지 리스트 배열 * 2를 10000번 반복
    [scalar * value for value in range(iteration_max)] # 리스트 컴프리헨션
    
end = time.time()
print(end - start) # 일반 반복문보다 리스트 컴프리헨션이 결과값 출력시간 더 빠름
```

    7.1373069286346436
    

# enumerate
인덱스를 붙여 리스트 값 추출


```python
for i, v in enumerate(['tic', 'tac', 'toe']):
    print(i, v)
```

    0 tic
    1 tac
    2 toe
    


```python
dic = {i:j for i, j in enumerate('TEAMLAB is an academic institute located in Korea'.split())}
print(dic)
```

    {0: 'TEAMLAB', 1: 'is', 2: 'an', 3: 'academic', 4: 'institute', 5: 'located', 6: 'in', 7: 'Korea'}
    

# zip
두 그룹의 요소들을 서로 엮음


```python
alist = ['a1', 'a2', 'a3']
blist = ['b1', 'b2', 'b3']

for a, b in zip(alist, blist):
    print(a, b)
```

    a1 b1
    a2 b2
    a3 b3
    


```python
ablist = list(zip(alist, blist))
print(ablist)
```

    [('a1', 'b1'), ('a2', 'b2'), ('a3', 'b3')]
    


```python
a, b, c = zip((1, 2, 3), (10, 20, 30), (100, 200, 300))
print(a, b, c)
```

    (1, 10, 100) (2, 20, 200) (3, 30, 300)
    


```python
[sum(x) for x in zip(a, b, c)]
```




    [6, 60, 600]




```python
for i, (a, b) in enumerate(zip(alist, blist)):    # 2개 섞기
    print(i, a, b)
```

    0 a1 b1
    1 a2 b2
    2 a3 b3
    


```python
num = [1, 2, 3, 4]
name = ['hong', 'gil', 'dong', 'nim']
dic = {}

for num, name in zip(num, name) :
    dic[num] = name                  # 딕셔너리의 키와 값의 형태로 만들기
    
print(dic)
```

    {1: 'hong', 2: 'gil', 3: 'dong', 4: 'nim'}
    

# lambda 함수
익명의 함수



```python
f = lambda x, y: x + y
print(f(1, 4))
```

    5
    


```python
print((lambda x, y: x + y)(1, 4))
```

    5
    

# map 함수
시퀀스 자료형의 요소에 같은 함수 적용

map(함수, 시퀀스자료)


```python
ex = [1, 2, 3, 4, 5]
f = lambda x: x ** 2
print(list(map(f, ex)))
```

    [1, 4, 9, 16, 25]
    


```python
# 리스트 컴프리헨션
[x ** 2 for x in ex]
```




    [1, 4, 9, 16, 25]




```python
# 두 개 이상의 시퀀스 자료형에 적용 가능
f = lambda x, y: x + y
list(map(f, ex, ex))
```




    [2, 4, 6, 8, 10]




```python
# 리스트 컴프리헨션
[x + y for x, y in zip(ex, ex)]
```




    [2, 4, 6, 8, 10]




```python
# map함수에 필터링 적용
list(map(lambda x: x ** 2 if x % 2 == 0 else x, ex))
```




    [1, 4, 3, 16, 5]




```python
# 리스트 컴프리헨션
[x ** 2 if x % 2 == 0 else x for x in ex]
```




    [1, 4, 3, 16, 5]



# reduce 함수
시퀀스 자료형의 요소에 차례로 함수를 적용하여 결과를 누적/통합

reduce(함수, 시퀀스자료, 초기값)


```python
from functools import reduce
print(reduce(lambda x, y: x + y, [1, 2, 3, 4, 5]))
```

    15
    


```python
# 초기값(100) 부여
print(reduce(lambda x, y: x + y, [1, 2, 3, 4, 5], 100))
```

    115
    


```python
# 예제 - 최댓값 구하기
f = lambda a, b: a if (a > b) else b
print(reduce(f, [1, 100, 2, 55]))
```

    100
    

# 별표(*) 사용


```python
# 가변 매개변수
def asterisk_test(a, *args):
    print(a, args)
    print(type(args))

asterisk_test(1, 2, 3, 4, 5, 6)
```

    1 (2, 3, 4, 5, 6)
    <class 'tuple'>
    


```python
# 키워드 가변 매개변수(*주의)
def asterisk_test(a, **kwargs):
    print(a, kwargs)
    print(type(kwargs)) 
    
asterisk_test(1, b = 2, c = 3, d = 4, e = 5, f = 6)
```

    1 {'b': 2, 'c': 3, 'd': 4, 'e': 5, 'f': 6}
    <class 'dict'>
    


```python
# 언패킹
def asterisk_test(a, args):
    print(a, *args)
    print(type(args))

asterisk_test(1, (2, 3, 4, 5, 6))
```

    1 2 3 4 5 6
    <class 'tuple'>
    


```python
def asterisk_test(a, *args):
    print(a, args)
    print(type(args))

asterisk_test(1, *(2, 3, 4, 5, 6))  # 여기서 언패킹됨 
```

    1 (2, 3, 4, 5, 6)
    <class 'tuple'>
    


```python
# 튜플의 언패킹
a, b, c = ([1, 2], [3, 4], [5, 6])
print(a, b, c)
```

    [1, 2] [3, 4] [5, 6]
    


```python
# asterisk 사용으로 언패킹
data = ([1, 2], [3, 4], [5, 6])
print(*data)
```

    [1, 2] [3, 4] [5, 6]
    


```python
# zip 함수와 함께 사용 *주의!!!!!!!!! 
for data in zip(*[[1, 2], [3, 4], [5, 6]]): # 언패킹 후 [1,2],[3,4],[5,6]으로 분리
    print(data)                             # zip에 의해 (1,3,5),(2,4,6)으로 묶임
    print(sum(data))
```

    (1, 3, 5)
    9
    (2, 4, 6)
    12
    


```python
# 딕셔너리의 언패킹
def asterisk_test(a, b, c, d) :
    print(a, b, c, d)

data = {'b': 1, 'c': 2, 'd': 3}
asterisk_test(10, **data)
```

    10 1 2 3
    


```python
# 딕셔너리 언패킹 또다른 예제1
def add(a = 0, b = 0):
    return a + b

data = {'a': 2, 'b': 3}
print(add(**data))
```

    5
    


```python
# 딕셔너리 언패킹 또다른 예제2
def test(arg1, arg2, arg3):
    print('arg3:', arg3)
    print('arg2:', arg2)
    print('arg1:', arg1)
    
kwargs = {'arg3': 3, 'arg2': 'two', 'arg1': 1} # 순서가 달라도 문제 없음
test(**kwargs)
```

    arg3: 3
    arg2: two
    arg1: 1
    
