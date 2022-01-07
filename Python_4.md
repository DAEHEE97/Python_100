# 문제 1


```python
# 파이썬 프로그래밍 언어에서의 기본적인 if 조건문 예제를 구현한 것이다.
```


```python
# [ ! ] : 조건문
# 대부분의 프로그래밍 언어가 그러하듯이 파이썬에서도 조건문은 if문을 사용한다.

# 다른 언어와 파이썬의 차이점 
# --> if문 끝에 콜론(:)을 붙여서 if문 줄(line)의 끝을 알려줘야 한다.


# [1] : if문
a = 100

# [A]
if a <= 100:
    print( a )

# [B]
if a <= 100 :
    print( a )

# [C]
if a <= 100:print( a )


```

    100
    100
    100


# 문제 2


```python
# 파이썬의 기본적인 if .. else, if .. elif .. else 조건문 예제를 구현하시오.
```


```python
# [1] : if .. else 조건문
a = 130

if a > 120:
    print( 'a는 120보다 크다.' )
else:
    print( 'a는 120보다 작다.' )

    
print( '-' * 100 )


# [2] : if .. elif .. else 조건문 --> 청년(~39세 미만), 중년(40세~59세), 장년(60세~79세), 노년(80세~)

age = 120

if age < 40:
    print( '당신은 청년이에요..' )
elif age < 60:
    print( '당신은 중년이에요..' )
elif age < 80:
    print( '당신은 장년이에요..' )
else:
    print( '당신은 노년이에요..' )
        
```

    a는 120보다 크다.
    ----------------------------------------------------------------------------------------------------
    당신은 노년이에요..


# 문제 3


```python
# 아래는 한 카페의 메뉴 선택기를 if 조건문으로 구현한 것인데 틀린 곳을 찾아보시오.

# 커피숍의 메뉴는 1번: 아메리카노, 2번: 카페라떼, 3번_아이스 카페라떼 이렇게 3개만 있다고 가정한다.
```


```python
# [1] : 카페 메뉴 선택기

btn = int(input(" Enter the Num "))


if btn == 1:
    print( '아메리카노' )
elif btn == 2:
    print( '카페라떼' )
elif btn == 3:
    print( '아이스 카페라떼' )
else:
    print( '메뉴는 1, 2, 3번중 하나를 골라주세요!' )


```

     Enter the Num 3
    아이스 카페라떼
