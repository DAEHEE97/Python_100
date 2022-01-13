# 문제 1 list


```python


# [1] : 정수형
a = [ 1, 2, 3, 4, 5 ]
print( '[1] 정수형 리스트 : ', a, type(a) )


# [2] : 실수형
b = [ 1.0, 2.0, 3.0, 4.0, 5.0 ]  #--- [ 1., 2., 3., 4., 5. ] --;;
print( '[2] 실수형 리스트 : ', b, type(b) )


# [3] : 문자형
c = [ 'a', 'b', 'c', 'd', 'e' ]
print( '[3] 문자형 리스트 : ', c, type(c) )




```

    [1] 정수형 리스트 :  [1, 2, 3, 4, 5] <class 'list'>
    [2] 실수형 리스트 :  [1.0, 2.0, 3.0, 4.0, 5.0] <class 'list'>
    [3] 문자형 리스트 :  ['a', 'b', 'c', 'd', 'e'] <class 'list'>


# 문제 2

- 파이썬 리스트 생성시 서로 다른 데이터 자료형 값을 사용할 수 있습니다.


```python


# [1] : 정수 + 리스트
a = [ 1, 2, 3, 4, 5, ['a', 'b', 'c'] ]
print( '[1] 정수 + 리스트 : ', a, type(a) )


# [2] : 정수 + 실수 + 문자
b = [ 100, 3.14, 'korea', [1, 2, 3] ]
print( '[2] 정수 + 실수 + 문자 : ', b, type(b) )


# [3] : 정수 + 리스트 + 튜플
c = [ 1, 2, 3, [1, 2, 3], (1, 2, 3) ]
print( '[3] 정수 + 리스트 + 튜플 : ', c, type(c) )


# [4] : 정수, 실수, 문자, 리스트(list), 튜플(tuple), 집합(set), 딕셔너리(dict)
d = [ 100, 3.14, 'kroea', [1, 2, 3, 3], (1, 2, 3, 3), {1, 2, 3, 3}, { 'a': 100, 'b': 200, 'c': 300 } ]
print( '[4] 주요 타입 7개 모두 : ', d, type(d) )





```

    [1] 정수 + 리스트 :  [1, 2, 3, 4, 5, ['a', 'b', 'c']] <class 'list'>
    [2] 정수 + 실수 + 문자 :  [100, 3.14, 'korea', [1, 2, 3]] <class 'list'>
    [3] 정수 + 리스트 + 튜플 :  [1, 2, 3, [1, 2, 3], (1, 2, 3)] <class 'list'>
    [4] 주요 타입 7개 모두 :  [100, 3.14, 'kroea', [1, 2, 3, 3], (1, 2, 3, 3), {1, 2, 3}, {'a': 100, 'b': 200, 'c': 300}] <class 'list'>


# 문제 3. empty list

- lst = []
- lst = list()



```python
# 파이썬 리스트 생성시 빈 리스트를 생성하는 코드를 2가지로 구현해보시오.


# [1] : 빈 리스트 생성 --> 첫 번째 방식
a = []
print( '[1] 빈 리스트 첫 번째 방식 : ', a, type(a) )


# [2] : 빈 리스트 생성 --> 두 번째 방식
b = list()
print( '[2] 빈 리스트 두 번째 방식 : ', b, type(b) )



```

    [1] 빈 리스트 첫 번째 방식 :  [] <class 'list'>
    [2] 빈 리스트 두 번째 방식 :  [] <class 'list'>


# 문제 4 indexing



```python

a = [ 100, 200, 300, 400, 500 ]

print( '[1] 인덱스를 이용한 a 리스트의 요소 값 출력 : ', a[3] )



b = [ 100, 3.14, 'korea', [1, 2, 3, 3], (1, 2, 3, 3), { 1, 2, 3, 3 }, { 'a': 100, 'b': 200, 'c': 300 } ]

print( '[2] 요소 값 : ', b[5] )
print( '[2] len() : ', len(b) )  #--- 7


                

```

    [1] 인덱스를 이용한 a 리스트의 요소 값 출력 :  400
    [2] 요소 값 :  {1, 2, 3}
    [2] len() :  7


# 문제 5. list in list

- 리스트 내 리스트 또는 튜플 요소에 접근


```python
#  아래의 리스트에서 korea, 365, 400 이라는 값이 출력되도록 작성하시오.


a = [ 100, 3.14, 'korea', [1, 2, 3, 365], (100, 200, 300, 400, 500) ]

print( a[2] )
print( a[3][3] )
print( a[4][3] )


```

    korea
    365
    400


# 문제 6. 역인덱싱 슬라이싱 


```python
# 역인덱스를 사용하여 리스트 요소의 마지막 부터 거꾸로 출력되도록 구현하시오.



# [1] : 역인덱스

a = [ 100, 200, 300, 400, 500]


print( '역 인덱스를 이용한 출력 : ', a[-1],a[-2],a[-3],a[-4],a[-5] ) 

print( '리스트 역순 출력 : ', a[::-1] ) 

print( '역 인덱스를 이용한 출력 : ', a[-1:len(a)*-1-1:-1] ) # -1,-6,-1
print( '역 인덱스를 이용한 출력 : ', a[-1:-6:-1] )


```

    역 인덱스를 이용한 출력 :  500 400 300 200 100
    리스트 역순 출력 :  [500, 400, 300, 200, 100]
    역 인덱스를 이용한 출력 :  [500, 400, 300, 200, 100]
    역 인덱스를 이용한 출력 :  [500, 400, 300, 200, 100]



```python
# 역인덱스를 사용하여 영어 점수를 오름차순과 내림차순으로 출력시키시오.
# 영어 점수는 리스트로 구성한다.


# 점수
scores = [ 100, 40, 70, 90, 60, 55, 45, 85, 95, 25 ]

# 정렬 내림차순
scores.sort( reverse=True )

# 역순 출력 인덱싱
start = -1*len( scores ) # list 시작 -1*len(scores)
last = -1 # list 끝


# for i in range(start, last+1) 똑같음
for i in range(start, last+1):
    print( scores[i], '(', i, ')' )





```

    100 ( -10 )
    95 ( -9 )
    90 ( -8 )
    85 ( -7 )
    70 ( -6 )
    60 ( -5 )
    55 ( -4 )
    45 ( -3 )
    40 ( -2 )
    25 ( -1 )


# 문제 7. list for

- range( len(lst) ) = range(6) = range(0, 5+1)



```python

lst = [ 'dog', 'hippo', 'elephant', 'lion', 'tiger', 'alligator' ]


# range(len(lst)) 

for i in range( len(lst) ):    
    print( lst[i] )


# for i in lst 리스트 바로 출력

print()
for i in lst:
    print(i)


# 거꾸로 출력

print()
for i in lst[ : : -1]:
    print( i )
    
```

    dog
    hippo
    elephant
    lion
    tiger
    alligator
    
    dog
    hippo
    elephant
    lion
    tiger
    alligator
    
    alligator
    tiger
    lion
    elephant
    hippo
    dog


# 문제 8. 리스트 정렬


```python


eng_scores = [ 100, 30, 80, 90, 50 ]


# 정렬 --> sort() 또는 sorted() 함수 사용 --> 정렬은 디폴트가 오름차순.
eng_scores.sort()
#eng_scores.sort( reverse=True )  #--- 오름차순 --> 내림차순 --;;


# [3] : 반복문을 사용해서 출력하기
for i in range( len(eng_scores) ):
    print( eng_scores[i], end='\t' )


```

    30	50	80	90	100	

# 문제 9. enumerate( )

- enumerate 를 사용하면 **인덱스 번호와 값**을 함께 가져올 수 있다.

- type(enumerate(lst)) = enumerate



```python
lst = ['a','s','k']

for i,val in enumerate(lst):
    print(i,val)
```

    0 a
    1 s
    2 k


# 문제 10. list 수정



```python
# 학생들의 영어 점수 리스트에 새 전학생의 영어 점수를 추가해보시오.
# 추가외에도 수정, 삭제도 모두 구현한다.
# 이 문제는 기존 리스트 또는 빈리스트에 새로운 요소를 추가, 수정, 삭제하는 방법을 아는지 묻는 문제이다.


# 원본
eng_scores = [ 90, 60, 75, 100, 85 ]
print( '[1] 원본 : ', eng_scores )


# 추가 --> append() 사용.
eng_scores.append(99)
print( '[2] 추가 : ', eng_scores )


# 수정(변경) --> index 사용.
eng_scores[-1] = 37
print( '[3] 수정 : ', eng_scores )


# 삭제 --> del + index 사용.
del eng_scores[-1]
print( '[4] 삭제 : ', eng_scores )


```

    [1] 원본 :  [90, 60, 75, 100, 85]
    [2] 추가 :  [90, 60, 75, 100, 85, 99]
    [3] 수정 :  [90, 60, 75, 100, 85, 37]
    [4] 삭제 :  [90, 60, 75, 100, 85]



```python
# [1] : a, b 2개의 리스트
a = [ 0, 1, 2, 3, 4 ]
b = [ 5, 6, 7, 8, 9 ]


# a, b 리스트 --> 하나로 병합 --> 더하기(+) 연산자 사용.
ab_plus = a + b
print( '[5] a + b 병합 리스트 : ', ab_plus, len(ab_plus), '개 요소' )


# a * b X --> 리스트 * 숫자하고의 곱셈은 가능. 
# 값이 3배가 아니라 a+a+a

a_multiplication = a * 3
print( '[6] a * 3 병합 리스트 : ', a_multiplication, len(a_multiplication), '개 요소' )


```

    [5] a + b 병합 리스트 :  [0, 1, 2, 3, 4, 5, 6, 7, 8, 9] 10 개 요소
    [6] a * 3 병합 리스트 :  [0, 1, 2, 3, 4, 0, 1, 2, 3, 4, 0, 1, 2, 3, 4] 15 개 요소


# 문제 11. list.index( )

- 리스트에서 원하는 특정 요소를 검색


```python
# 코끼리(0), 하마(1), 사자(2), 호랑이(3), 악어(4)
# 이때, 동물 이름은 사용자 입력으로 처리한다 
# 예) 동물 이름을 입력하세요 = ___________


# 리스트
animals = [ 'elephant', 'hippo', 'lion', 'tiger', 'alligator' ]


# 사용자 입력
ani_name = input( '케이지를 알고 싶은 동물의 이름을 입력해주세요 = ' )

# .index() 사용하면 해당 리스트 요소 이름의 index 위치정보 반환
ani_index = animals.index( ani_name )  



print('해당 동물의 케이지는 {0} 번 입니다.'.format(animals.index(ani_name)))







```

    케이지를 알고 싶은 동물의 이름을 입력해주세요 = elephant
    해당 동물의 케이지는 0 번 입니다.


# 문제 12. list 중복제거


```python
# 리스트

lst = [ 'dog', 'hippo', 'elephant', 'lion', 'tiger', 'alligator', 'hippo', 'lion' ]


# 중복 제거 -> 리스트에서 중복을 허용하지 않는 집합으로 dtype 변환
# set() 
# 반환된 집합 dtype은 순서가 없다. 따라서 set[index] ERROR

sett = set(lst)
print( sett, type(sett) )  

# print(sett[3]) ERROR


```

    {'hippo', 'lion', 'elephant', 'dog', 'tiger', 'alligator'} <class 'set'>


# 문제 13. list comprehension


```python

# 수동 리스트 생성 방식과 for 문을 사용한 list comprehension 방식을 비교해보자.


# 수동 리스트 생성 --> 1~10까지의 요소를 갖는 리스트 생성

a = [ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 ]
print( '[1] 수동으로 리스트 생성 --> ', a, type(a) )




# for 반복문 --> 빈 리스트 --> lst.append 

b = []
for aaa in range( 1, 11 ):
        b.append( aaa )  #--- 1 ~ 10까지

print( '[2] 자동으로 리스트 생성 --> ', b, type(b) )




# [3] : list comprehension

c = [ x for x in range( 1, 11 ) ]
print( '[3] 자동으로 리스트 생성 list comprehension --> ', c, type(c) )


```

    [1] 수동으로 리스트 생성 -->  [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] <class 'list'>
    [2] 자동으로 리스트 생성 -->  [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] <class 'list'>
    [3] 자동으로 리스트 생성 list comprehension -->  [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] <class 'list'>



```python
# 아래의 다양한 list comprehension 문제들을 코드로 구현하시오.




# [1] list comprehension 괄호([])를 사용하지 않고 list() 와 for 문으로 1~10까지의 리스트를 만들어보시오.

# [1] : for문 + list() --> 리스트 생성
for i in range( 1, 11 ):
        print( i, end=' ' )
print()

a = list( i for i in range(1, 11) )  #--- 이렇게도 가능하구나.. 정도만 기억.. 당연히 권장은 a = [] <-- 이걸 권장 --;;
print( '[1] for문 + list() 사용한 리스트 생성 : ', a )




# [2] 1~10까지의 수를 list comprehension으로 각 숫자를 제곱한 값을 저장하는 리스트를 만들어보시오.

# [2] : 1~10까지 수 --> 각 숫자를 제곱한 값 --> 리스트 생성
b = [ i * i for i in range( 1, 11 ) ] 
print( '[2] 1~10까지의 수를 제곱한 값 --> ', b )




# [3] 위 2번 문제에서 5의 제곱 값은 제외하고 출력시키시오. (★★★)

# [3] : 1~10까지 수 --> 제곱한 값 리스트 생성 --> 5제곱 값 제외 --> if 조건문 사용.
# 이 문제는 list comprehension에서 조건문을 사용시 어떤 순서대로 절차가 진행되면서 조건 비교가 되는지를 잘 이해해야 한다.

c = [ i * i for i in range(1, 11) if i != 5 ]
print( '[3] 1~10까지의 수를 제곱한 값에서 5제곱 값은 제외한 리스트 --> ', c )




# [4] list comprehension에서 if 조건문을 사용하여 1~50까지의 수에서 짝수, 홀수만 저장하는 리스트를 각각 만들어보시오.

# [4] : 짝수, 홀수 리스트 생성
d = [ i for i in range(1, 51) if i % 2 != 0 ]
print( '[4] 1~50까지의 수에서 홀수만 출력 --> ', d )




# [5] list comprehension에서 함수를 사용하는 것이 가능한지 예제를 작성해보시오.

# [5] : 함수 사용

def my_func( i ):
        i = i * 2
        return i
        
e = [ my_func(abs(i)) for i in [ 1, 2, -3, 4, 5, -6, 7, 8, -9, 10 ] ]

print( '[5] 함수 사용 --> ', e )


# [6] 중첩된 이중 for문에 대한 사용법과 진행 순서

# [6] : 중첩 for 반복문 --> 구구단

a = [ (i, j) for i in range(2, 4) for j in range(1, 4) ]
print( '[6] 중첩 for --> ',a )


```

    1 2 3 4 5 6 7 8 9 10 
    [1] for문 + list() 사용한 리스트 생성 :  [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    [2] 1~10까지의 수를 제곱한 값 -->  [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
    [3] 1~10까지의 수를 제곱한 값에서 5제곱 값은 제외한 리스트 -->  [1, 4, 9, 16, 36, 49, 64, 81, 100]
    [4] 1~50까지의 수에서 홀수만 출력 -->  [1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37, 39, 41, 43, 45, 47, 49]
    [5] 함수 사용 -->  [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
    [6] 중첩 for -->  [(2, 1), (2, 2), (2, 3), (3, 1), (3, 2), (3, 3)]

