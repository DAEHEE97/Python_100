# 문제 1. 함수작성


```python
# [1] : 함수 작성
# -------------------------------------
def a():
        print( '붕어빵' )
        
def b():
        print( '개구리빵' )
# -------------------------------------


# [2] : 함수 호출
a()
b()




```

    붕어빵
    개구리빵


# 문제 2. return



```python
# [1] : 함수 작성
# -------------------------------------
def a():
    result = '붕어빵'
    return result
        
def b():
    result = '개구리빵'
    return result
# -------------------------------------


# [2] : 함수 호출
print( a() )
print( b() )


```

    붕어빵
    개구리빵


# 문제 3. 


```python
# 변수의 메모리 주소값을 출력하여 다른 함수내 같은 변수의 값들이 어떤 주소를 가지고 있는지 출력하시오.


# [1] : 함수 작성
# ------------------------------------
def a():
    result = '붕어빵'
    result_loc = id( result )
    return result_loc
        
def b():
    result = '개구리빵'
    result_loc = id( result )
    return result_loc
# ------------------------------------


# [2] : 함수 호출
print( '[2-1] a() 함수내 result 변수의 메모리 주소 : ', a() )
print( '[2-2] b() 함수내 result 변수의 메모리 주소 : ', b() )

```

    [2-1] a() 함수내 result 변수의 메모리 주소 :  140328664397072
    [2-2] b() 함수내 result 변수의 메모리 주소 :  140328664396400



```python
print( '[2-1] a() 함수내 result 변수의 메모리 주소 : ', a() )
print( '[2-2] b() 함수내 result 변수의 메모리 주소 : ', b() )

```

    [2-1] a() 함수내 result 변수의 메모리 주소 :  140328664397072
    [2-2] b() 함수내 result 변수의 메모리 주소 :  140328664396400


# 문제 4. max( lst )



```python
# 한 반의 학생들 10명에 대한 영어 점수표가 리스트로 있다.
# 최고 점수를 출력하는 함수를 만들어 영어 점수표를 함수로 전달하면 최고 점수가 나오도록 구현해보시오.

# [1] : 함수 작성
def max_in_list( lst ):
    return max(lst)  #--- max() 함수는 전달받은 리스트내 요소중 가장 큰 숫자를 반환 --;;

# [2] : 영어 점수표 --> list
english_score = [ 35, 55, 87, 98, 48, 88, 77, 65, 91, 79 ]

# [3] : 함수 호출 및 결과 출력하기
result = max_in_list( english_score )
print( result )


```

    98


# 문제 5. return



```python
# 한 반의 학생들 10명에 대한 영어 점수표가 리스트로 있다.
# 함수를 만들어 영어 점수표를 함수로 전달하면 최고 점수와 최저 점수가 동시에 나오도록 구현해본 것이다.

# [1] : 함수 작성
def max_min_in_list(lst):
    return min(lst)
    return max(lst)

# [2]  : 영어 점수표 --> list
english_score = [ 35, 90, 58, 30, 98, 56, 89, 78, 91, 67 ]

# [3] : 함수 호출 및 결과 출력하기
result = max_min_in_list(english_score)
print( result )
```

    30


# 문제 6. 


```python
# [1] : 함수 작성 --> return을 하나로 tuple return

def max_min_in_list(lst):
    return max(lst), min(lst)


# [2]  : 영어 점수표 --> list

english_score = [ 35, 90, 58, 30, 98, 56, 89, 78, 91, 67 ]


# [3] : tuple 반환

result = max_min_in_list(english_score)
print(result, type(result))


# [4] : a, b 변수 각각에 반환 

a, b = max_min_in_list(english_score)
print(a,b)

```

    (98, 30) <class 'tuple'>
    98 30


# 문제 7. 가변길이 입력 파라미터




```python
# 가변길이 입력 파라미터 값들을 함수로 넘겨서 해당 파라미터의 갯수와 홀수들의 합을 구하는 코드를 구현하시오.
# 함수의 리턴은 항상 하나의 값을 반환한다. 

# 그러나 여러개의 값을 리턴하는 경우도 구현할 수 있는데 이러한 예제와 그때의 리턴 자료형은 무엇인지를 묻는 문제이다.
# 아래 코드의 결과로 출력되는 자료형에 대해서 말해보시오.


# [1] : 함수의 리턴 --> 하나의 tuple --> 2개의 값
```


```python
def my_func( *params ):
    
    count_ = 0
    sum_ = 0
    
    for i in params:
        count_ += 1
        
        if i % 2 != 0:  #--- 나머지연산자를 사용하여 결괏값이 0과 같지 않은 홀수들의 합만 구함 --;;
            sum_ += i
            return count_, sum_
# -----------------------------------------------------


# [2] : 함수 호출
a, b = my_func( 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 )
result = my_func( 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11 )

#--- a, b 변수 각각은 int --;;
print( '[2-1] 가변길이 입력 파라미터 갯수와 홀수 합은 : ', a, ',', b, type(a), type(b) )  

#--- 이때는 자료형이 tuple --;;
print( '[2-2] result 변수 하나로 리턴되는 결과의 값을 받으면 : ', result, type(result) )  




```

    [2-1] 가변길이 입력 파라미터 갯수와 홀수 합은 :  10 , 25 <class 'int'> <class 'int'>
    [2-2] result 변수 하나로 리턴되는 결과의 값을 받으면 :  (11, 36) <class 'tuple'>


# 문제 8. 리스트 정렬

# 문제 9. enumerate( )



# 문제 10. list 수정


# 문제 11. list.index( )



# 문제 12. list 중복제거

# 문제 13. list comprehension

# 문제 14. dictionary




```python

```
