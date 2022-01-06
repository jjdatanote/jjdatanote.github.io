---
layout : single
title : "파이썬 자료구조"
---

# stack


```python
a = [1, 2, 3, 4, 5]
a.append(10)
a
```




    [1, 2, 3, 4, 5, 10]




```python
a.append(20)
a
```




    [1, 2, 3, 4, 5, 10, 20]




```python
a.pop()
```




    20




```python
a.pop()
```




    10




```python
# 7-1 stack
word = input("Input a word:")
word_list = list(word)
print(word_list)

result = []
for _ in range(len(word_list)):
    result.append(word_list.pop())

print(result)
print(word[::-1])
```

    Input a word:PYTHON
    ['P', 'Y', 'T', 'H', 'O', 'N']
    ['N', 'O', 'H', 'T', 'Y', 'P']
    NOHTYP
    

# Queue


```python
a = [1, 2, 3, 4, 5]
a.append(10)
a.append(20)
a
```




    [1, 2, 3, 4, 5, 10, 20]




```python
a.pop(0)
```




    1




```python
a.pop(0)
```




    3



# tuple
* 리스트와 유사하지만 변경 불가능한 자료 구조
* ( ) 를 사용하여 정의


```python
t = (1, 2, 3)
print(t + t, t * 2)
len(t)
```

    (1, 2, 3, 1, 2, 3) (1, 2, 3, 1, 2, 3)
    




    3




```python
t[1]
```




    2




```python
t[1] = 5  # 아이템 할당 불가 오류 발생
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-27-1c5b8e2c8180> in <module>
    ----> 1 t[1] = 5  # 아이템 할당 불가 오류 발생
    

    TypeError: 'tuple' object does not support item assignment


## tuple indexing


```python
print(t[0], t[-2])
```

    1 2
    

## nested tuple indexing


```python
t = (1, 2, 3, ('One', 'Two', 'Three'))
print(t)
print(t[3])
print(t[3][1])
```

    (1, 2, 3, ('One', 'Two', 'Three'))
    ('One', 'Two', 'Three')
    Two
    

# set
* 데이터 중복을 허용하지 않는 자료 구조
* 순서가 없는 데이터 집합 
* 인덱싱 불가


```python
s1 = set([1, 2, 3, 1, 2, 3]) # 집합형태 1
s2 = {4, 5, 6}               # 집합형태 2
print(s1)
print(s2)
```

    {1, 2, 3}
    {4, 5, 6}
    


```python
s1.add(1)   # 추가
s1          # 이미 있기 때문에 그대로 출력
```




    {1, 2, 3}




```python
s1.remove(1) # 제거
s1
```




    {2, 3}




```python
s1.update([1, 4, 5, 6, 7]) # 수정
s1
```




    {1, 2, 3, 4, 5, 6, 7}




```python
s1.discard(3) # 제거
s1
```




    {1, 2, 4, 5, 6, 7}




```python
s1.clear()      # 모두 삭제
s1
```




    set()



## set operations, methods
* 교집합 : &, intersection()
* 합집합 : |, union()
* 차집합 : -, difference()
* 대칭차집합 : ^, symmetric_difference()


```python
s1 = {10, 20, 20 ,30}
s2 = {30, 30, 40, 50}
print(s1)
print(s2)
```

    {10, 20, 30}
    {40, 50, 30}
    


```python
print(s1 & s2)
print(s1 | s2) # 중복된 것 1개만 출력
print(s1 - s2)
print(s1 ^ s2)
```

    {30}
    {50, 20, 40, 10, 30}
    {10, 20}
    {40, 10, 50, 20}
    


```python
print(s1.intersection(s2))
print(s1.union(s2)) # 중복된 것 1개만 출력
print(s1.difference(s2))
print(s1.symmetric_difference(s2))
```

    {30}
    {50, 20, 40, 10, 30}
    {10, 20}
    {40, 10, 50, 20}
    

# dictionary
* key, value의 쌍으로 구성된 자료 구조
* 순서가 없는 데이터
* key를 이용하여 value 검색
* 동일한 key가 있을 경우 덮어씀


```python
student_info = {20140012:'Sungchul', 20140059:'Jiyoung', 20140058: 'JaeHong'}
print(student_info)
```

    {20140012: 'Sungchul', 20140059: 'Jiyoung', 20140058: 'JaeHong'}
    


```python
student_info[20140012]
```




    'Sungchul'




```python
student_info[20140012] = 'Janhyeok'
student_info[20140039] = 'Wonchul'
student_info
```




    {20140012: 'Janhyeok',
     20140059: 'Jiyoung',
     20140058: 'JaeHong',
     20140039: 'Wonchul'}



## dictionary methods


```python
country_code = {'America': 1 , 'Korea': 82, 'China': 86, 'Japan': 81}
country_code
```




    {'America': 1, 'Korea': 82, 'China': 86, 'Japan': 81}




```python
print(country_code.keys())   # *결과값 형태 주의
print(country_code.values()) # *결과값 형태 주의
print(country_code.items())  # *결과값 형태 주의
```

    dict_keys(['America', 'Korea', 'China', 'Japan'])
    dict_values([1, 82, 86, 81])
    dict_items([('America', 1), ('Korea', 82), ('China', 86), ('Japan', 81)])
    


```python
'Korea' in country_code.keys() # True
'German' in country_code.keys() # False
82 in country_code.values() # True
49 in country_code.values() # False
```




    False



# collections
* 컨테이너 데이터형


```python
from collections import deque, OrderedDict, defaultdict, Counter, namedtuple
```

## deque
* 양쪽 끝에서 빠르게 추가와 삭제를 할 수 있는 리스트형 컨테이너


```python
deque_list = deque()           # deque 선언

for i in range(5) : 
    deque_list.append(i)       # append
    
print(deque_list)    
```

    deque([0, 1, 2, 3, 4])
    


```python
deque_list.pop()
```




    4




```python
deque_list.pop()
```




    3




```python
deque_list.pop()
```




    2




```python
deque_list
```




    deque([0, 1])




```python
deque_list = deque()

for i in range(5) :
    deque_list.appendleft(i)    # appendleft : 요소를 왼쪽으로 추가
    
print(deque_list)  
```

    deque([4, 3, 2, 1, 0])
    


```python
deque_list.rotate(2) # 값의 위치 오른쪽으로 2칸씩 이동
deque_list
```




    deque([1, 0, 4, 3, 2])




```python
deque(reversed(deque_list))   # 역순 출력(원래 데이터 보존됨)
```




    deque([2, 3, 4, 0, 1])




```python
deque_list.extend([5, 6, 7]) # 새로운 요소 추가
deque_list
```




    deque([1, 0, 4, 3, 2, 5, 6, 7])




```python
deque_list.extendleft([8, 9])   # 주의
deque_list
```




    deque([9, 8, 1, 0, 4, 3, 2, 5, 6, 7])



## OrderedDict
* 항목이 추가된 순서를 기억하는 딕셔너리 서브 클래스 


```python
d = {} 
d['x'] = 100
d['l'] = 500
d['y'] = 200
d['z'] = 300

for k, v in d.items() :
    print(k, v)
```

    x 100
    l 500
    y 200
    z 300
    


```python
d = OrderedDict() # OrderedDict 선언
d['x'] = 100
d['y'] = 200
d['z'] = 300
d['l'] = 500

for k, v in d.items() :
    print(k, v)
```

    x 100
    y 200
    z 300
    l 500
    


```python
def sort_by_key(t) :       
    return t[0]            # key값 기준 정렬 -> t[0] 
                           # value값 기준 정렬 -> t[1]
d = dict()
d['x'] = 100
d['y'] = 200
d['z'] = 300
d['l'] = 500

for k, v in OrderedDict(sorted(d.items(), key = sort_by_key)).items():
        print(k ,v) # default : 오름차순
```

    l 500
    x 100
    y 200
    z 300
    


```python
sorted(d.items(), key = sort_by_key)
```




    [('l', 500), ('x', 100), ('y', 200), ('z', 300)]



## defaultdict
* 누락된 값을 제공하기 위해 팩토리 함수를 호출하는 딕셔너리 서브 클래스


```python
d = dict()
print(d['first'])   # 비어있기 때문에 오류
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    <ipython-input-45-0a831f038353> in <module>
          1 d = dict()
    ----> 2 print(d['first'])   # 비어있기 때문에 오류
    

    KeyError: 'first'



```python
d = defaultdict(lambda: 0)   # 비어있는 것을 lambda함수를 통해 초기 0 생성
print(d['first'])
```

    0
    


```python
# 7-7 : list를 default_factory로 사용. 키-값 시퀀스를 리스트의 딕셔너리로 그룹화
s = [('yellow', 1), ('blue', 2), ('yellow', 3), ('blue', 4), ('red', 1)]
d = defaultdict(list) # d를 list로 선언

for k, v in s :
    d[k].append(v)     # 리스트는 append

print(d.items()) # *결과값 형태 주의(숫자값 리스트 형태)
```

    dict_items([('yellow', [1, 3]), ('blue', [2, 4]), ('red', [1])])
    


```python
# set를 default_factory로 사용. 집합의 딕셔너리가 생성됨
s = [('yellow', 1), ('blue', 2), ('yellow', 3), ('blue', 4), ('red', 1)]
d = defaultdict(set) # d를 set으로 선언

for k, v in s :
    d[k].add(v)      # 집합은 add

print(d.items()) # *결과값 형태 주의(숫자값 딕셔너리 형태)
```

    dict_items([('yellow', {1, 3}), ('blue', {2, 4}), ('red', {1})])
    

## Counter
* 시퀀스 자료형의 데이터 값의 개수를 세는 딕셔너리 서브 클래스


```python
text = list('gallahad')
text
```




    ['g', 'a', 'l', 'l', 'a', 'h', 'a', 'd']




```python
c = Counter(text) # *결과값 형태 주의(딕셔너리)
c 
```




    Counter({'g': 1, 'a': 3, 'l': 2, 'h': 1, 'd': 1})




```python
c['a']
```




    3



## Counter methods


```python
# elements() : 각 요소의 개수만큼 리스트형의 결과 출력. 요소가 1보다 작으면 무시
c = Counter(a = 4, b = 2, c = 0, d = -2)
print(list(c.elements())) # *주의 (c,d는 출력 x)
```

    ['a', 'a', 'a', 'a', 'b', 'b']
    


```python
# most_common(n) : 빈도수가 가장 높은 n개의 요소 반환.
### 만약 n을 생략하면 모든 요소 출력. 개수가 같은 요소는 처음 발견된 것 순서로 출력.
Counter('abracadabra').most_common(3)
```




    [('a', 5), ('b', 2), ('r', 2)]




```python
Counter('abracadabra').most_common()
```




    [('a', 5), ('b', 2), ('r', 2), ('c', 1), ('d', 1)]




```python
# subtract : 요소의 개수 빼는 메서드
c = Counter(a = 4, b = 2, c = 0, d = -2)
d = Counter(a = 1, b = 2, c = 3, d = 4)
c.subtract(d)
c
```




    Counter({'a': 3, 'b': 0, 'c': -3, 'd': -6})




```python
# *주의 (+, -, &, | : 결과값 0 이하는 결과에서 제외)
c = Counter(a = 4, b = 2, c = 0, d = -2)
d = Counter(a = 1, b = 2, c = 3, d = 4)

print(c + d)
print(c - d)
print(c & d) # 둘 중 최솟값 선택됨(c, d는 각각 0, -2 선택되지만 0이하이므로 결과에서 제외)
print(c | d) # 둘 중 최댓값 선택됨 
```

    Counter({'a': 5, 'b': 4, 'c': 3, 'd': 2})
    Counter({'a': 3})
    Counter({'b': 2, 'a': 1})
    Counter({'a': 4, 'd': 4, 'c': 3, 'b': 2})
    

## namedtuple
* 이름 붙은 필드를 갖는 튜플 서브 클래스를 만드는 팩토리 함수


```python
Point = namedtuple('Point', ['x', 'y'])
p = Point(11, y = 22)
p # 결과값 기억하기
```




    Point(x=11, y=22)




```python
p[0] + p[1]
```




    33




```python
x, y = p # 언패킹
x, y
```




    (11, 22)




```python
p.x + p.y
```




    33



# lab: textmining


```python
text = """A press release is the quicktest and easiest way to get free publicity.
If well written, a press release can result in multiple published articles about
your firm and its products. And that can mean new propects contacting you asking you
to sell to them. ...""".lower().split() # 소문자로 변경 + 단어 단위 구분

from collections import defaultdict # defaultdict 호출

word_count = defaultdict(lambda: 0) # 비어있는 것을 lambda함수를 통해 초기 0 생성

for word in text :                  # text 단어 모두 탐색
    word_count[word] += 1           # 단어별 등장 횟수 증가시킴

from collections import OrderedDict # OrderedDict 호출

for i, v in OrderedDict(sorted(word_count.items(), key = lambda t:t[1],
    reverse = True)).items(): # 횟수 기준(t[1]) 내림차순으로 key, value값 출력
    
    print(i, v)
```

    and 3
    to 3
    a 2
    press 2
    release 2
    can 2
    you 2
    is 1
    the 1
    quicktest 1
    easiest 1
    way 1
    get 1
    free 1
    publicity. 1
    if 1
    well 1
    written, 1
    result 1
    in 1
    multiple 1
    published 1
    articles 1
    about 1
    your 1
    firm 1
    its 1
    products. 1
    that 1
    mean 1
    new 1
    propects 1
    contacting 1
    asking 1
    sell 1
    them. 1
    ... 1
    


```python
c = Counter(text)     # Counter 적용하면 쉽다.
c
```




    Counter({'a': 2,
             'press': 2,
             'release': 2,
             'is': 1,
             'the': 1,
             'quicktest': 1,
             'and': 3,
             'easiest': 1,
             'way': 1,
             'to': 3,
             'get': 1,
             'free': 1,
             'publicity.': 1,
             'if': 1,
             'well': 1,
             'written,': 1,
             'can': 2,
             'result': 1,
             'in': 1,
             'multiple': 1,
             'published': 1,
             'articles': 1,
             'about': 1,
             'your': 1,
             'firm': 1,
             'its': 1,
             'products.': 1,
             'that': 1,
             'mean': 1,
             'new': 1,
             'propects': 1,
             'contacting': 1,
             'you': 2,
             'asking': 1,
             'sell': 1,
             'them.': 1,
             '...': 1})




```python
c['and']
```




    3


