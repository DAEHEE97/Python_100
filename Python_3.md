# 문제 1


```python
# python100_operator_001

# 파이썬 프로그래밍 언어에서 연산자의 종류와 쓰임을 말해보시오.
# 자주 쓰는 연산자 위주로 말해보시오.
```


```python

# [1] : 산술 연산자

#       +               -               *               /               //              **              %

# 정수형까리의 연산은 결과 --> 정수형
# 실수형끼리의 연산은 결과 --> 실수형

# 정수형과 실수형의 연산은 결과가 --> 실수형


# [2] : 관계 연산자
# 대소비교를 하거나 같은지 같지 않은지 등의 비교를 할 때 사용한다.

#       >               <               >=(크거나 같다)              <=(작거나 같다)              ==              !=(같지 않다)


# [3] : 논리 연산자

# and, or, not
# and --> 양쪽 값이 모두 참인 경우에만 참.
# or --> 어느 한쪽만 참이면 참.
# not --> 참이면 거짓으로, 거짓이면 참으로.


# [4] : 부울(Boolean) 연산자

# True, False 값으로 출력.


```

# 문제 2 산술 연산자


```python
# python100_operator_002
# 산술 연산자 예제를 만들어보시오.

```


```python
# [1] : 산술 연산자
print( 10 + 10 )
print( 10 - 5 )
print( 10 * 10 )
print( 10 / 10 )  #--- 1(?)     1.0(float)

print( 3 ** 2, ' , ', 3 ** 3 )  #--- 9, 27

print( 10 // 3 )  #--- 3(몫)
print( 10 % 3 )  #--- 1(나머지)

```

    20
    5
    100
    1.0
    9  ,  27
    3
    1


# 문제 3 관계 연산자


```python
# python100_operator_003
# 관계 연산자 예제를 만들어보시오.
```


```python
# [1] : 관계 연산자

print( 10 > 5 )  #--- True

print( 10 > 11 )  #--- False

print( '-' * 100 )

print( 1 == 1 )  #--- True

print( 1 == 2 )  #--- False

print( 1 != 2 )  #--- True

print( 1 != 1 )  #--- False



```

    True
    False
    ----------------------------------------------------------------------------------------------------
    True
    False
    True
    False


# 문제 4 논리 연산자, bool 자료형


```python
# python100_operator_004
# 논리 연산자 예제를 만들어보시오.
```


```python
# [1] : 논리 연산자 
# 0 이 아닌 모든 수 = False

a = True
b = False

print( a and b )    #--- False
print( a or b )     #--- True
print( a, not(a) )  #--- True, False



if a or b:
        print( 'True' )  # -- a != b
else:
        print( 'False' )
```

    False
    True
    True False
    True



```python
# [2] : 0 이 아닌 모든 수 = False


if 0 or 0:
    print( 'True' )
else:
    print( 'False' )
```

    False


# 문제 5 = 할당 연산자


```python
# python100_operator_005
# 할당 연산자 예제를 만들어보시오.

```


```python

# [1] : 할당 연산자

a = 100
a = a * 2
print( a )  #--- 200


b = 200
b *= 2
print( b )  #--- 400





```

    200
    400


# 문제 6 in 연산자


```python
# python100_operator_006

# in(멤버쉽) 연산자 예제를 만들어보시오.
# bool 반환
```


```python

# [1] : in 연산자

lst = [ 1, 2, 3, 4, 5 ]
a = 100 in lst # bool 반환

print( lst, type(lst) )
print( a )  #--- False

tpl = 1, 2, 3, 4
b = 4 in tpl # bool 반환

print( tpl, type(tpl) )
print( b )  #--- True





```

    [1, 2, 3, 4, 5] <class 'list'>
    False
    (1, 2, 3, 4) <class 'tuple'>
    True


# 문제 7 부울(Boolean) 연산자


```python
# python100_operator_007

# 부울(Boolean) 연산자 예제를 만들어보시오.
# 그외 비트 연산자, is 연산자(동일 객체 비교) 등도 있다는 정도만 우선 참고하자!

```


```python
# [1] : 부울 연산자 --> True, False 결과가 반환

print( bool(1) )  #--- 파이썬에서 1은 참(True)을 의미 --;;
print( bool(0) )  #--- 파이썬에서 0은 거짓(False)을 의미 --;;

print( '마이너스 결과는 : ', bool(-1) )  #--- 참(True) --;;



print('-'*100)

# [2] : None 너는 대체 뭐냐? 
# --> 말 그대로 아무것도 없다는 뜻 --> 하나의 type --> 타입체크를 하면 NoneType 으로 나옴.
# 아무것도 없기 때문에 부울 연산자로 출력하면 항상 거짓(False)을 출력.



print( "None's bool is", bool(None) )  #--- 파이썬에서 None 값은 거짓(False)을 의미 --;;
# print( bool(none) )  #--- Err ---;; none X

a = None
print( "None's type is" , type(a) )
print( bool(a) )  #--- False


```

    True
    False
    마이너스 결과는 :  True
    ----------------------------------------------------------------------------------------------------
    None's bool is False
    None's type is <class 'NoneType'>
    False

