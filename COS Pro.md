# COS Pro

- 

## 정수,실수,복소수


```python
# 2진수: 숫자 앞에 0b를 붙이며 0과 1을 사용합니다.

0b110
```




    6




```python
# 8진수: 숫자 앞에 0o(숫자 0과 소문자 o)를 붙이며 0부터 7까지 사용합니다.

0o10
```




    8




```python
# 16진수: 숫자 앞에 0x 또는 0X를 붙이며 0부터 9, A부터 F까지 사용합니다(소문자 a부터 f도 가능).

0xF
```




    15




```python
# 실수 float()는 부동소수점(floating point)에서 유래

float(1 + 2)
```




    3.0




```python
# 실수부와 허수부로 이루어진 복소수(complex number)
# 허수부는 숫자 뒤에 j를 붙이거나 ,  complex( , ) 함수 사용
# 공학에서는 j를 사용 // 수학에서는 허수를 i로 표현하지만 


1.2+1.3j
complex(1.2, 1.3)
```




    (1.2+1.3j)




```python
# 빈 변수 / 타 언어에서는 널(null)이라고 표현

x = None
print(x)
```

    None



```python
# 변수 삭제

del(x)

```


```python
# multiline string

hello = '''Hello, world!
안녕하세요.
Python입니다.'''

print(hello)
```

    Hello, world!
    안녕하세요.
    Python입니다.



```python
# escape sequence

print('Hello, \'Python\'')
print("""Hello, 'Python'""")
```

    Hello, 'Python'
    Hello, 'Python'



```python
# UTF-8에서 한글 글자 하나는 3바이트로 표현

hello = '안녕하세요'
length = len(hello.encode('utf-8')) # UTF-8로 인코딩 했을 때 바이트 수를 구함
length
```




    15




```python
# 제어 문자는 화면에 출력되지는 않지만 출력 결과를 제어한다고 해서 제어 문자라 부릅니다. 
# 또한, 제어 문자는 \로 시작하는 이스케이프 시퀀스입니다(부록 ‎47.2 이스케이프 시퀀스' 참조).
# ₩n: 다음 줄로 이동하며 개행이라고도 부릅니다.
# ₩t: 탭 문자, 키보드의 Tab 키와 같으며 여러 칸을 띄웁니다.
# ₩₩: ₩ 문자 자체를 출력할 때는 ₩를 두 번 써야 합니다.

print(1,2,3, sep='\n')
```

    1
    2
    3



```python
print('1\n2\n3')
```

    1
    2
    3



```python
print(1,end='')    # end에 빈 문자열을 지정하면 다음 번 출력이 바로 뒤에 오게 됨
print(2, end='')
print(3)
```

    123



```python
year = 2000
month = 10
day = 27
hour = 11
minute = 43
second = 59
 
print(year, month, day, sep='-',end=' ')
print(hour, minute, second, sep=':')
```

    2000-10-27 11:43:59



```python
5 / 2 
```




    2.5




```python
# //
# 버림 나눗셈, 결과에서 소수점 이하는 버림

print(5/2, 5 // 2)  
print(int(5/2))


```

    2.5 2
    2



```python
print(1 == 1.0, 1!=1.0)
```

    True False



```python
# is
# is, is not은 객체(object)를 비교합니다.

1 is 1.0
```

    <>:1: SyntaxWarning: "is" with a literal. Did you mean "=="?
    <>:1: SyntaxWarning: "is" with a literal. Did you mean "=="?
    <ipython-input-7-2ebf4c947f31>:1: SyntaxWarning: "is" with a literal. Did you mean "=="?
      1 is 1.0





    False




```python
# not false

if not 0:
    print('참')    # not 0은 참
    
if not None:
    print('참')    # None은 참
    
if not '':
    print('참')    # not 빈 문자열은 참
```

    참
    참
    참



```python
for _ in range(3):
    print("hello")
```

    hello
    hello
    hello



```python
# range(역순)
for i in range(3, 0, -1):     # 3에서 1까지 역순으로 숫자 생성
    print('Hello, world!', i)
```

    Hello, world! 3
    Hello, world! 2
    Hello, world! 1



```python
# reversed(range())

for i in reversed(range(3)):    # 3에서 1까지 역순으로 숫자 생성
    print('Hello, world!', i)
```

    Hello, world! 2
    Hello, world! 1
    Hello, world! 0



```python
count = int(input('반복할 횟수를 입력하세요: '))
 
while count > 0:     # count가 0보다 클 때 반복
    print('Hello, world! %d' % count)
    count -= 1       # count를 1씩 감소시킴
```

    반복할 횟수를 입력하세요: 3
    Hello, world! 3
    Hello, world! 2
    Hello, world! 1



```python
# 3의 배수

for i in range(1, 101):    # 1부터 100까지 100번 반복
    if i % 3 == 0:         # 3의 배수일 때
        print(i, end=' ')
```

    3 6 9 12 15 18 21 24 27 30 33 36 39 42 45 48 51 54 57 60 63 66 69 72 75 78 81 84 87 90 93 96 99 


```python
# 3으로 끝나는

i = 0
while True:
    
    if i % 10 != 3:
        i += 1
        continue
    
    if i > 73:
        break
    
    print(i, end=' ')
    i += 1
```

    3 13 23 33 43 53 63 73 


```python
# append(값)은 이름 그대로 리스트의 맨 뒤에 값을 추가
# append(리스트)처럼 리스트를 넣으면 리스트 안에 리스트 추가

lst = [10, 20]
lst.append(30)
lst


```




    [10, 20, 30]




```python
# extend(리스트)는 리스트의 맨 뒤에 다른 리스트를 연결합니

lst = [10]
lst.extend([20, 30])
lst

```




    [10, 20, 30]




```python
# insert(idx, value)

lst = [10, 20, 30]
lst.insert(2, 500)
lst
```




    [10, 20, 500, 30]




```python
# remove(value)

lst = [10, 20, 30]
lst.remove(20)
lst
```




    [10, 30]




```python
# pop()

lst = [10, 20, 30]
lst.pop()
```




    30




```python
lst
```




    [10, 20]




```python
# index(value)

lst = [10, 20, 30, 10, 25, 40]
lst.index(20)
```




    1




```python
lst = [10, 20, 30]
lst.clear()
lst
```




    []




```python
# count(value)

lst = [10, 20, 30, 10, 25, 40]
lst.count(10)
```




    2




```python
# lst[] 값 추가

lst = [1, 2, 3]
lst[len(lst):] = [10]
lst
```




    [1, 2, 3, 10]




```python
# lst[] 값 추가

lst = [1, 2, 3]
lst[len(lst):] = [10, 20]
lst
```




    [1, 2, 3, 10, 20]




```python
# lst[] 값 추가

lst = []
lst[:] = [10]
lst[:] = [20]
lst
```




    [20]




```python
lst = [0, 10, 20, 30, 40, 50, 60, 70, 80, 90]
lst[0:len(lst)]
# lst[0:]
```




    [0, 10, 20, 30, 40, 50, 60, 70, 80, 90]




```python
lst[0:-1]
```




    [0, 10, 20, 30, 40, 50, 60, 70, 80]




```python
# b = a와 같이 리스트를 다른 변수에 할당하면,
# 리스트는 b,a 가 될 것 같지만 하나의 리스트 객체입니다.

a = [0, 0, 0, 0, 0]
b = a

b[2] = 99
```


```python
print(a, b, a == b, a is b )
```

    [0, 0, 99, 0, 0] [0, 0, 99, 0, 0] True True



```python
a = [0, 0, 0, 0, 0]
b = a.copy()
b[2] = 99
```


```python
print(a, b, a == b, a is b )
```

    [0, 0, 0, 0, 0] [0, 0, 99, 0, 0] False False



```python
# 리스트 덧셈

a = [10, 20, 30]
b = [1, 2, 3]

c = a + b
c

```




    [10, 20, 30, 1, 2, 3]




```python
index,value in enumerate(a)
```




    (4, False)




```python
lst = [38, 21, 53, 62, 19]

```


```python
# in    
for i in lst:
    print(i)


```

    38
    21
    53
    62
    19



```python
# in idx
for i in range(len(lst)):
    print(lst[i])


```

    38
    21
    53
    62
    19



```python
# while
i = 0
while i < len(a):
    print(a[i])
    i+=1
```

    38
    21
    53
    62
    19



```python
a = [38, 21, 53, 62, 19]
for index, value in enumerate(a):
    print(index, value)
```

    0 38
    1 21
    2 53
    3 62
    4 19


## 최소 최대


```python
# min value

lst = [38, 21, 53, 62, 19]

# smallest idx0 초기화
smallest = lst[0]

for i in lst:
    if i < smallest:
        smallest = i
        
smallest
```




    19




```python
# max value
lst = [38, 21, 53, 62, 19]

# largest idx0 초기화
largest = lst[0]

for i in lst:
    if i > largest:
        largest = i
largest
```




    62




```python
# max idx
lst = [38, 21, 53, 62, 19]

# largest idx = 0
largest_idx = 0

for i in range(len(lst)):
    if lst[largest_idx] > lst[i]:
        largest_idx = i
        
largest_idx
```




    4




```python
# min max sort

lst = [38, 21, 53, 62, 19]
print(min(lst),max(lst))

lst.sort()
print(lst[0])

lst.sort(reverse=True)
print(lst[0])


```

    19 62
    19
    62


## List comprehension

- 리스트 안에 식, for 반복문 등을 지정하여 리스트를 생성하는 것


```python
lst = [i for i in range(10)]    # 0부터 9까지 숫자를 생성하여 리스트 생성
lst = list(i for i in range(10))
lst
```




    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]




```python
lst = [i + 5 for i in range(10)]    # 0부터 9까지 숫자를 생성하면서 값에 5를 더하여 리스트 생성
lst
```




    [5, 6, 7, 8, 9, 10, 11, 12, 13, 14]




```python
lst = [i * 2 for i in range(10)]    # 0부터 9까지 숫자를 생성하면서 값에 2를 곱하여 리스트 생성
lst
```




    [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]




```python
lst = [i for i in range(10) if i % 2 == 0]    # 0~9 숫자 중 2의 배수인 숫자(짝수)로 리스트 생성
lst
```




    [0, 2, 4, 6, 8]




```python
lst = [i for i in range(10) if i % 2 == 1]    # 0~9 숫자 중 홀수에 5를 더하여 리스트 생성
lst
```




    [1, 3, 5, 7, 9]




```python
lst = [i * j for j in range(2, 10) for i in range(1, 10)]
print(lst)
```

    [2, 4, 6, 8, 10, 12, 14, 16, 18, 3, 6, 9, 12, 15, 18, 21, 24, 27, 4, 8, 12, 16, 20, 24, 28, 32, 36, 5, 10, 15, 20, 25, 30, 35, 40, 45, 6, 12, 18, 24, 30, 36, 42, 48, 54, 7, 14, 21, 28, 35, 42, 49, 56, 63, 8, 16, 24, 32, 40, 48, 56, 64, 72, 9, 18, 27, 36, 45, 54, 63, 72, 81]



```python
lst = [i * j for j in range(2, 10)
           for i in range(1, 10)]
print(lst)
```

    [2, 4, 6, 8, 10, 12, 14, 16, 18, 3, 6, 9, 12, 15, 18, 21, 24, 27, 4, 8, 12, 16, 20, 24, 28, 32, 36, 5, 10, 15, 20, 25, 30, 35, 40, 45, 6, 12, 18, 24, 30, 36, 42, 48, 54, 7, 14, 21, 28, 35, 42, 49, 56, 63, 8, 16, 24, 32, 40, 48, 56, 64, 72, 9, 18, 27, 36, 45, 54, 63, 72, 81]


## List map


```python
lst = [1.2, 2.5, 3.7, 4.6]
lst = list(map(int, lst))

print(lst)
```

    [1, 2, 3, 4]



```python
lst = [1.2, 2.5, 3.7, 4.6]
for i in range(len(lst)):
    lst[i] = int(lst[i])

print(lst)
```

    [1, 2, 3, 4]



```python
lst = list(map(str, range(10)))
print(lst)

lst = list(map(int, range(10)))
print(lst)

```

    ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]



```python
list_str = input().split()           # input().split()의 결과는 문자열 리스트
list_int = map(int, list_str)        # 리스트의 요소를 int로 변환, 결과는 맵 객체
a, b = list_int                      # 맵 객체는 변수 여러 개에 저장할 수 있음
print(a,b)
```

    10 30
    10 30



```python
a, b = map(int,input().split())
print(a,b)
```

    10 30
    10 30



```python
# 문자열 길이가 5인 단어들
a = ['alpha', 'bravo', 'charlie', 'delta', 'echo', 'foxtrot', 'golf', 'hotel', 'india']
lst = [i for i in a if len(i) == 5]
print(lst)
```

    ['alpha', 'bravo', 'delta', 'hotel', 'india']


## 2d List


```python
lst = [[10, 20], [30, 40], [50, 60]]
for x, y in lst:    # 리스트의 가로 한 줄(안쪽 리스트)에서 값 두 개를 꺼냄
    print(x, y)
```

    10 20
    30 40
    50 60



```python
lst = [[10, 20], [30, 40], [50, 60]]
 
for i in lst:        # a에서 안쪽 리스트를 꺼냄
    for j in i:     # 안쪽 리스트에서 값을 하나씩 꺼냄
        print(j)
    
```

    10
    20
    30
    40
    50
    60



```python
a = [[10, 20], [30, 40], [50, 60]]
 
for i in range(len(a)):            # 세로 크기
    for j in range(len(a[i])):     # 가로 크기
        print(a[i][j])
 
```

    10
    20
    30
    40
    50
    60



```python
a = [[10, 20], [30, 40], [50, 60]]
 
i = 0
while i < len(a):    # 반복할 때 리스트의 크기 활용(세로 크기)
    x, y = a[i]
    print(x, y)
    i += 1           # 인덱스를 1 증가시킴
```

    10 20
    30 40
    50 60



```python
a = [[10, 20], [30, 40], [50, 60]]
 
i = 0
while i < len(a):           # 가로 크기
    
    j = 0
    while j < len(a[i]):    # 세로 크기
        print(a[i][j])
        j += 1              # 가로 인덱스를 1 증가시킴
        
    i += 1                  # 세로 인덱스를 1 증가시킴
```

    10
    20
    30
    40
    50
    60



```python
a = []    # 빈 리스트 생성
 
for i in range(3):
    line = []              # 안쪽 리스트로 사용할 빈 리스트 생성
    for j in range(2):
        line.append(0)     # 안쪽 리스트에 0 추가
    a.append(line)         # 전체 리스트에 안쪽 리스트를 추가
 
print(a)
```

    [[0, 0], [0, 0], [0, 0]]



```python
lst = [[0 for j in range(2)] for i in range(3)]
lst
```




    [[0, 0], [0, 0], [0, 0]]




```python
lst = [[0] * 2 for i in range(3)]
lst
```




    [[0, 0], [0, 0], [0, 0]]




```python

```
