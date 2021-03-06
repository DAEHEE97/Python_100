# 문제 1 Data type


```python
# 파이썬 프로그래밍 언어에서 자료형이란 무엇인지 설명하시오.

# 자료형이 무엇인지 확인할 때 사용하는 함수는 무엇인가?

# 자료형을 보여주는 함수를 사용하여 자료형 출력 예제를 만들어보시오.
```

* [1] a 변수값의 자료형 : 100 <class 'int'>
* [2] b 변수값의 자료형 : 3.14 <class 'float'>
* [3] c 변수값의 자료형 : korea <class 'str'> 
* [3] d 변수값의 자료형: 010-1234-5678 <class'str'> 
* [4] lst 변수값의 자료형 : [1, 2, 3, 4, 5] <class 'list'> 
* [5] tpl 변수값의 자료형 : (1, 2, 3, 4, 5) <class 'tuple'> 
* [6] s 변수값의 자료형 : {1, 2, 3, 4, 5} <class 'set'>
* [7] d 변수값의 자료형 : {'a': 97, 'b': 98} <class 'dict'>
    
    


```python
# [ ! ] : 자료형이란 무엇인가?
# 자료형 또는 데이터 타입이라고 부른다.

# 즉, 프로그램 코드를 작성하는 과정에서 여러 종류의 데이터 값을 사용하여 정보처리를 하게 된다.
# 이때, 여러 종류의 데이터를 구분할 필요가 있는데 자료형을 통해서 이러한 데이터 종류를 분류한다.


# 자료형이 무엇인지 확인하는 방법은 type() 함수를 사용하면 된다.


# [1] : 숫자형 - 정수
a = 100
print( '[1] a 변수값의 자료형 : ', a, type(a) )


# [2] : 숫자형 - 실수
b = 3.14
print( '[2] b 변수값의 자료형 : ', b, type(b) )


# [3] : 문자형 - 따옴표 안 숫자는 문자열 
c = 'korea'  #--- 문자 또는 문자열은 작은따옴표(')나 큰따옴표(")로 감싸줘야 한다 --;;
print( '[3] c 변수값의 자료형 : ', c, type(c) )

d = '010-1234-5678'
print( '[3] d 변수값의 자료형 : ', d, type(d) )


# [4] : 리스트형
lst = [ 1, 2, 3, 4, 5, 500, 500 ]
print( '[4] lst 변수값의 자료형 : ', lst, type(lst) )


# [5] : 튜플형
tpl = ( 1, 2, 3, 4, 5 )
print( '[5] tpl 변수값의 자료형 : ', tpl, type(tpl) )


# [6] : 집합형 --> 중복 X
s = { 1, 2, 3, 4, 5, 500, 500 }
print( '[6] s 변수값의 자료형 : ', s, type(s) )


# [7] : 딕셔너리(사전)형
dic = { 'a' : 97, 'b' : 98 }
print( '[7] dic 변수값의 자료형 : ', dic, type(dic) )
```

    [1] a 변수값의 자료형 :  100 <class 'int'>
    [2] b 변수값의 자료형 :  3.14 <class 'float'>
    [3] c 변수값의 자료형 :  korea <class 'str'>
    [3] d 변수값의 자료형 :  010-1234-5678 <class 'str'>
    [4] lst 변수값의 자료형 :  [1, 2, 3, 4, 5, 500, 500] <class 'list'>
    [5] tpl 변수값의 자료형 :  (1, 2, 3, 4, 5) <class 'tuple'>
    [6] s 변수값의 자료형 :  {1, 2, 3, 4, 5, 500} <class 'set'>
    [7] dic 변수값의 자료형 :  {'a': 97, 'b': 98} <class 'dict'>


# 문제 2 Tuple


```python
# python100_type_002
# 아래 코드를 실행하면 자료형이 무엇으로 나오는지 말해보시오.
```


```python
# [1] : 자료형 맞추기
a = ( 1, 2, 3, 4, 5 )
print( '[1-1] a 변수값의 자료형 : ', a, type(a) )

b = 1, 2, 3, 4, 5, 6, 7, 8, 9
print( '[1-2] b 변수값의 자료형 : ', b, type(b) )


```

    [1-1] a 변수값의 자료형 :  (1, 2, 3, 4, 5) <class 'tuple'>
    [1-2] b 변수값의 자료형 :  (1, 2, 3, 4, 5, 6, 7, 8, 9) <class 'tuple'>


# 문제 3 아스키 코드


```python
# python100_type_003
# 아스키 코드란 무엇인지 설명하시오.

```


```python
# [1] : 아스키 코드란?

# 컴퓨터는 내부에서 숫자 또는 문자에 대한 정보처리를 이진수로 처리한다. 
# 0과 1 두개로만 처리 --> 즉, 문자도 숫자로 기억한다.
# 이때, 문자를 숫자로 대응시켜줘야 하는데 여러 방법중 아스키 코드 방식을 사용한다.

# 영어 알파벳(Alphabet)각각의 문자에 번호를 붙여서 처리 --> 번호를 붙일 때 ASCII(아스키) 규약에 따라 붙임 --> 아스키 코드


# 대문자 A --> 65  ( 이후부터는 하나씩 증가하므로 B --> 66 )
# 소문자 a --> 97 ( 하나씩 증가하므로 100은 소문자 d )

# 숫자 0 --> 48 ( 하나씩 증가하므로 57은 숫자 9 )


# 엔터(Enter) --> 아스키 코드 13
# NULL --> 아스키코드 0번 
# \n --> 아스키코드 10번 



```

# 문제 4 ord( ) 함수 

- ordinal number 문자 -> 아스키 코드(#) 으로 변환



```python
# python100_type_004

# 대문자 A, B, C 3개 문자에 대해서 아스키 코드로 출력하는 코드를 작성하시오.

```


```python
# [1] : 대문자 A --> 넌 정체가 뭐냐?
print( 'A', type('A') )

print( ord('A') )  #--- ord() 함수는 문자를 입력받아 해당 문자에 해당하는 아스키코드 값을 반환(ordinal number) --;;
print( ord('B') )
print( ord('C') )
print( ord('Z') )  #--- A(65) + 알파벳문자(26개-1) = Z(90) --;;


# [2] : 소문자 a --> 넌 또 정체가 뭐냐?
print( 'a', type('a') )

print( ord('a') )  #--- 97
print( ord('b') )
print( ord('c') )
print( ord('z') )  #--- a(97) + 알파벳문자(26개-1) = z(122) --;;




```

    A <class 'str'>
    65
    66
    67
    90
    a <class 'str'>
    97
    98
    99
    122


# 문제 5 chr( ) 함수, input( ) 함수, print 출력

- Number( ASCII ) -> 문자 로 변환

- input( ) 함수 -> 터미널로 부터 입력을 받아서 문자열로 반환 > 데이터 타입 변환 해줘야 합니ㅏㄷ.



```python
# python100_type_005

# 사용자로 부터 숫자(아스키 코드)를 입력받아 그에 해당하는 문자를 출력하는 프로그램을 구현하시오.


```


```python

# [1] : 사용자 입력
a = input( '숫자를 입력하면 해당하는 문자를 출력해드려요 = ' )
print( a, type(a) )  #--- 타입이 str --;;


# [2] : 정수형으로 자료형을 변환
a = int(a)
print( a, type(a) )  #--- 타입이 int --;;


# [3] : 해당하는 값을 출력하기 --> chr() 함수 사용
chr_ = chr(a)

print( '당신이 입력한 숫자의 문자는 : ', chr_ )

print( f'당신이 입력한 숫자의 문자는 {chr_} 입니다.' )




```

    숫자를 입력하면 해당하는 문자를 출력해드려요 = 65
    65 <class 'str'>
    65 <class 'int'>
    당신이 입력한 숫자의 문자는 :  A
    당신이 입력한 숫자의 문자는 A 입니다.



```python
chr_
```




    'A'




```python

```
