# 문제 1 range( )


```python
# 0부터 9까지 출력하는 for 반복문 예제를 구현하시오.


print(range(10), type(range(10)))
```

    range(0, 10) <class 'range'>



```python

# [1] : for 반복문
print( '[ 출력 결과 ]' )
print( '-' * 100 )

for i in range(10):
    print( i )

    
# 파이썬 프린트 end = '\n' 자동 널 Enter    
    
# for i in range(10):
#     print( i, end='\n' ) 
 

# for i in range(10): print( i )   
```

    [ 출력 결과 ]
    ----------------------------------------------------------------------------------------------------
    0
    1
    2
    3
    4
    5
    6
    7
    8
    9


# 문제 2 end = 


```python
# 0부터 9까지 숫자가 아래처럼 출력되도록 for 반복문 예제를 구현하시오.
# 0     1       2       3       4       5       6       7       8       9

```


```python
# [1] : for 반복문
print( '[ 결과 출력 ]' )
print( '-' * 100 )


for i in range(10):
    print( i, end='\t' )

```

    [ 결과 출력 ]
    ----------------------------------------------------------------------------------------------------
    0	1	2	3	4	5	6	7	8	9	

# 문제 3


```python
# 0부터 9까지 숫자가 아래처럼 출력되도록 for 반복문 예제를 구현하시오.

# 0부터 9까지 숫자를 가로출력 했을 때 마지막 콤마를 없애시오.

# 0, 1, 2, 3, 4, 5, 6, 7, 8, 9


```


```python
# [1] : for 반복문

print( '[ 결과 출력 ]' )
print( '-' * 100 )

n = 0

for i in range(10):
    if n < 9:
        print( i, end=', ' )
    else:
        print( i )
    
    n += 1

```

    [ 결과 출력 ]
    ----------------------------------------------------------------------------------------------------
    0, 1, 2, 3, 4, 5, 6, 7, 8, 9


# 문제 4 range( first, last+1 )


- first = f
- last = l
- for i in range( first, last+1 ):


- range(9) = range( 0, 8+1 )




```python
# for 반복문을 사용해서 4부터 21까지의 홀수들의 합을 구하는 코드를 구현하시오.

```


```python
# [1] : 변수 선언 및 초기 데이터 값 설정

first = 4
last = 21


# [2] for 반복문

sum_odd = 0
for i in range( first, last+1 ):
    #print( i )
    
    # 홀수 판단
    
    if ( i % 2 != 0 ):
        print( i )
        sum_odd += i



# [3] : 출력

print( '[ 결과 출력 ]' )
print( '-' * 100 )
print( sum_odd )



```

    5
    7
    9
    11
    13
    15
    17
    19
    21
    [ 결과 출력 ]
    ----------------------------------------------------------------------------------------------------
    117


# 문제 5 range( first, last+1, step ) 


```python
# 1부터 100까지의 수에서 짝수들만 출력하는 코드를 구현하시오.
# 두 가지 방식을 생각해서 구현해보시오.

```


```python
# [2] : range() 함수의 step(간격) 옵션 값을 이용하여 처리.

for i in range( 2, 100+1, 2 ):
    print( i, end='\t' )

```

    2	4	6	8	10	12	14	16	18	20	22	24	26	28	30	32	34	36	38	40	42	44	46	48	50	52	54	56	58	60	62	64	66	68	70	72	74	76	78	80	82	84	86	88	90	92	94	96	98	100	

# 문제 6 range( len ( lst ) )


```python
# 리스트 요소의 값을 반복문을 사용하여 모두 출력하시오.
# 이때 가로로 값을 출력시키시오.
# 값을 모두 출력한 후에는 끝에 요소의 갯수를 함께 출력시키시오.

```


```python

# [1] : 리스트
lst = [ 'dog', 'hippo', 'elephant', 'lion', 'tiger', 'alligator' ]


# [2] : 반복문 --> 출력
# range( len(lst) ) = range(6) = range(0, 5+1)

for i in range( len(lst) ):    
    print( lst[i] )

print( '총', len(lst), '개 요소' )

# [3] : for i in lst 리스트 바로 출력

for i in lst:
    print(i)

```

    dog
    hippo
    elephant
    lion
    tiger
    alligator
    총 6 개 요소
    dog
    hippo
    elephant
    lion
    tiger
    alligator


# 문제 7 for i in lst[ : : -1 ]


```python
# 리스트 요소의 값을 반복문을 사용하여 거꾸로 출력시키시오.

# 이 문제는 리스트의 값들을 거꾸로 출력시킬 때 필요한게 무엇인지를 아는지 묻는 문제이다.

```


```python


# [1] : 리스트
lst = [ 'dog', 'hippo', 'elephant', 'lion', 'tiger', 'alligator' ]


print(type(lst[ : : -1 ]),lst[ : : -1 ])

print()

# [2] : 반복문 --> 거꾸로 출력
for i in lst[ : : -1 ]:
    print( i )


```

    <class 'list'> ['alligator', 'tiger', 'lion', 'elephant', 'hippo', 'dog']
    
    alligator
    tiger
    lion
    elephant
    hippo
    dog


# 문제 8 Nested for

- **밖 for** : i 유지 상태로 

- **안 for** : j 증가하면서 한턴 실행, 한턴 끝나면 i 증가 



```python
# for 반복문을 사용해서 구구단 전체(2단~9단)를 출력하는 코드를 구현하시오.
# 이 문제는 이중 반복문을 사용할 수 있는지를 묻는 문제이다.
```


```python

# [1] : 구구단
for i in range( 2, 9+1 ):
    
    print( i, '단' )
    print()
    
    for j in range( 1, 9+1 ):
        print( i, 'x', j , '=', i*j )
        print()
        
# j 1 ~ 9 한턴이 
```

    2 단
    
    2 x 1 = 2
    
    2 x 2 = 4
    
    2 x 3 = 6
    
    2 x 4 = 8
    
    2 x 5 = 10
    
    2 x 6 = 12
    
    2 x 7 = 14
    
    2 x 8 = 16
    
    2 x 9 = 18
    
    3 단
    
    3 x 1 = 3
    
    3 x 2 = 6
    
    3 x 3 = 9
    
    3 x 4 = 12
    
    3 x 5 = 15
    
    3 x 6 = 18
    
    3 x 7 = 21
    
    3 x 8 = 24
    
    3 x 9 = 27
    
    4 단
    
    4 x 1 = 4
    
    4 x 2 = 8
    
    4 x 3 = 12
    
    4 x 4 = 16
    
    4 x 5 = 20
    
    4 x 6 = 24
    
    4 x 7 = 28
    
    4 x 8 = 32
    
    4 x 9 = 36
    
    5 단
    
    5 x 1 = 5
    
    5 x 2 = 10
    
    5 x 3 = 15
    
    5 x 4 = 20
    
    5 x 5 = 25
    
    5 x 6 = 30
    
    5 x 7 = 35
    
    5 x 8 = 40
    
    5 x 9 = 45
    
    6 단
    
    6 x 1 = 6
    
    6 x 2 = 12
    
    6 x 3 = 18
    
    6 x 4 = 24
    
    6 x 5 = 30
    
    6 x 6 = 36
    
    6 x 7 = 42
    
    6 x 8 = 48
    
    6 x 9 = 54
    
    7 단
    
    7 x 1 = 7
    
    7 x 2 = 14
    
    7 x 3 = 21
    
    7 x 4 = 28
    
    7 x 5 = 35
    
    7 x 6 = 42
    
    7 x 7 = 49
    
    7 x 8 = 56
    
    7 x 9 = 63
    
    8 단
    
    8 x 1 = 8
    
    8 x 2 = 16
    
    8 x 3 = 24
    
    8 x 4 = 32
    
    8 x 5 = 40
    
    8 x 6 = 48
    
    8 x 7 = 56
    
    8 x 8 = 64
    
    8 x 9 = 72
    
    9 단
    
    9 x 1 = 9
    
    9 x 2 = 18
    
    9 x 3 = 27
    
    9 x 4 = 36
    
    9 x 5 = 45
    
    9 x 6 = 54
    
    9 x 7 = 63
    
    9 x 8 = 72
    
    9 x 9 = 81
    

