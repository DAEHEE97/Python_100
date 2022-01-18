# 문제 1. no return


```python

def a():
        print( '붕어빵' )
        
def b():
        print( '개구리빵' )

a()
b()
```

    붕어빵
    개구리빵


# 문제 2. return str



```python

def a():
    result = '붕어빵'
    return result
        
def b():
    result = '개구리빵'
    return result



print( a() )
print( b(),type(b()) )


```

    붕어빵
    개구리빵 <class 'str'>


# 문제 3. memory address in function

- 다시 호출 해도 주소가 변하지 않음



```python

def a():
    result = '붕어빵'
    result_loc = id( result )
    return result_loc
        
def b():
    result = '개구리빵'
    result_loc = id( result )
    return result_loc


print( '[2-1] a() 함수내 result 변수의 메모리 주소 : ', a() )
print( '[2-2] b() 함수내 result 변수의 메모리 주소 : ', b() )

```

    [2-1] a() 함수내 result 변수의 메모리 주소 :  140636842296592
    [2-2] b() 함수내 result 변수의 메모리 주소 :  140636842295632



```python
print( '[2-1] a() 함수내 result 변수의 메모리 주소 : ', a() )
print( '[2-2] b() 함수내 result 변수의 메모리 주소 : ', b() )

```

    [2-1] a() 함수내 result 변수의 메모리 주소 :  140636842296592
    [2-2] b() 함수내 result 변수의 메모리 주소 :  140636842295632


# 문제 4. return func( lst )



```python
def max_in_list( lst ):
    return max(lst)  

english_score = [ 35, 55, 87, 98, 48, 88, 77, 65, 91, 79 ]

result = max_in_list( english_score )
print( result )


```

    98


# 문제 5. return first


```python

def max_min_in_list(lst):
    return min(lst) # return > exit
    return max(lst)

english_score = [ 35, 90, 58, 30, 98, 56, 89, 78, 91, 67 ]

result = max_min_in_list(english_score)
print( result )
```

# 문제 6. return tuple


```python

def max_min_in_list(lst):
    return max(lst), min(lst)

english_score = [ 35, 90, 58, 30, 98, 56, 89, 78, 91, 67 ]


# tuple

result = max_min_in_list(english_score)
print(result, type(result))


# int

t1, t2 = max_min_in_list(english_score)
print(t1,t2,type(t1),type(t2))

```

# 문제 7. def func( *params )

- 함수 정의 에서 입력 파라미터를 받을 때 * 표시를 해줌으로써 가변길이라는 것을 명시적으로 표시

- return tuple > int
- return tuple > tuple 



```python
def my_func( *params ):
    count_ = 0
    sum_ = 0
    
    for i in params:
        count_ += 1
        
        if i % 2 != 0:
            sum_ += i
    
    return count_, sum_

# int

a, b = my_func( 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 )
print(  a, b, type(a), type(b) )  


# tuple

result = my_func( 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11 )
print( result, type(result) )  


```

    10 25 <class 'int'> <class 'int'>
    (11, 36) <class 'tuple'>


# 문제 8. params 지정


```python
# 함수 호출시 입력 파라미터 값을 지정하여 함수를 호출
# 순서 상관 없음

def my_func( id_, name_, strength ):
    return id_, name_, strength

result = my_func( id_='batman',strength='900',name_='배트맨', )

a, b, c = my_func( id_='batman', name_='배트맨', strength = 4000 )



print( result, type(result) )

print( result[2], type(result[2]) )

print( a, b, c, type(a), type(b), type(c) )

```

# 문제 9. defalut param

- 디폴트값이 아닌 다른 값으로 함수 호출시 지정하면 그 값이 전달



```python
def calc_tax( price, operator=1.1 ):
    
    supply_value = round(price / operator)  # 공급가 = total / OP
    vat = price - supply_value              # 부가세 = total - 공급가
    total = (price / operator) * operator   # 
    
    return supply_value, vat, total

    
result1 = calc_tax( 100000 )  
result2 = calc_tax( 100000, 1.3) # defualt 값이 아닌 다른값 전달 가능 

print( result1 )
print( result2 )
```

    (90909, 9091, 100000.0)
    (76923, 23077, 100000.0)


# 문제 10. 

- tuple - *params
- list - lst


```python
# for i in tuple:
#      sum += i  

def my_func( *params ):
    sum = 0
    
    for i in params:
        sum += i
    
    return sum

def my_func_lst( lst ):
    sum = 0
    
    for i in lst:
        sum += i
    
    return sum


# a = my_func( [1, 1, 1, 1] ) ERROR
a = my_func( 1, 1, 1, 1 )
print( a )

b = my_func( 1, 2, 3, 4, 5, 6, 7, 8, 9 )
print( b )

c = my_func_lst( [1, 1, 1, 1] ) # Error list
print( c )

```

# 문제 11. 

- .sort()
- sorted()


```python
lst = [ 100, 50, 70, 88, 65 ]
print( lst )


lst.sort()
print( lst )
# print( lst.sort() ) None 


lst.sort( reverse=True ) 
print( '.sort_reverse' , lst )

asc_ = sorted( lst )  
print( 'sorted_asc' , asc_ )

reverse_ = sorted( lst, reverse=True )  
print( 'sorted_reverse' , desc_ )
```
