# 문제 1. func list

- input list > 리스트 내부 변경 > output list


```python
import random


def add_power_level( c_id ):
    c_id[2] = random.choice([1, 2, 3, 4, 5, 6, 7, 8, 9])
    return c_id


person1 = [ 'p1', 20, 7 ]
person2 = [ 'p2', 30, 9 ]

print( person1[0], person1[1], person1[2] )
print( person2[0], person2[1], person2[2] )


add_power_level(person1)
add_power_level(person2)

print(person1)
print(person2)

```

    p1 20 7
    p2 30 9
    ['p1', 20, 6]
    ['p2', 30, 5]


# 문제 2. class

- 클래스를 사용하면 변수와 함수를 하나로 묶어서 데이터를 굉장히 효율적이면서 더 체계적으로 핸들링 할 수 있다.

- 클래스 내부에서 여러 다양한 변수나 함수가 정의되고 사용되는데 이를 --> 클래스 멤버 --> 변수, 메서드

- 메서드(method) : 클래스의 행위나 동작을 구현 (함수)  클래스에서는 메서드라고 호칭하는 것 뿐임.


- (1) 클래스 작성 --> class 키워드로 선언하고 클래스명 지정.
- (2) 클래스 이름 --> 관례적으로 CamelCase --> 파이썬은 보통 단어 사이에 _를 넣는 편이나 클래스명은 카멜케이스를 따른다.


- __naming__


class CamelCase:


def snake_case():



```python
# test
# class PersonInfo:
#     pass


class PersonInfo:
    def hello(self):
        print( 'hello' )
                
                
```


```python
p = PersonInfo()
print( p, type(p) )
p.hello()

```

    <__main__.PersonInfo object at 0x7fc8386cf2e0> <class '__main__.PersonInfo'>
    hello


# 문제 3. \__init__

__init__ 생성자 메서드란?

- 생성자 메서드를 통해서 객체가 생성될 때 해당 객체의 여러 초기 값을 셋팅할 수 있다.

- Person() 객체를 생성하는 순간 __init__ 메서드는 바로 호출



```python
class Person:
    def __init__( self ):
        print( 'initalize' )

```


```python
p1 = Person()
```

    initalize


# 문제 4. return func( lst )



```python
class Person:
    
    def __init__( self, name, age ):
        self.name = name
        self.age = age
                
    def print_info( self ):
        print( 'Name : ', self.name )
        print( 'Age : ', self.age )
        
```


```python

p1 = Person( 'P1', 20 )
p1.print_info()

p2 = Person( 'P2', 30 )
p2.print_info()

p3 = Person( 'P3', 40 )
p3.print_info()


```

    Name :  P1
    Age :  20
    Name :  P2
    Age :  30
    Name :  P3
    Age :  40


# 문제 5.  \__del__


```python
class SmartPhone:
        
        # 생성자
        def __init__( self, name, price ):
                self.name = name
                self.price = price
                print( self.name + " 객체 init " )
                
        def a_method( self ):
                print( self.name, self.price )

        # 소멸자
        def __del__( self ):
                print( self.name + " 객체 del " )
```


```python
s1 = SmartPhone( '엘지', 500000 )
s1.a_method()
del s1

```

    엘지 객체 init 
    엘지 500000
    엘지 객체 del 


# 문제 6. method, func


```python
class Person:
    
    def a_method( self ):
        print( 'a_method 호출' )
                
    def b_method( self ):
        print( 'b_method 호출' )
        
        print('')
        a_func()  #--- self 사용해서 a_method 호출 --;;

def a_func():
        print( '클래스 외부 정의 함수' )
        
        
p1 = Person()
p1.a_method()  #--- 바로 a_method를 호출하는건 당연히 가능 --;;


p1.b_method()  #--- b_method를 통해서 a_method를 호출하는 것도 가능 --;;


```

    a_method 호출
    b_method 호출
    
    클래스 외부 정의 함수


# 문제 7. class variable, object variable

- 클래스 내부 변수는 클래스 외부에서 "클래스명.변수명" 으로 접근
- 클래스 내부에서 접근시 마찬가지로 "클래스명.변수명" 으로 접근



```python
class MyClass:
    
    a_var = 0                  # 클래스 변수
    
    def __init__(self):
        self.var = 10          # 객체 변수
        print("생성")
    
    def a_method( self ):      # 클래스 메서드


        MyClass.a_var = 6000


print( MyClass.a_var ) # 클래스 생성 X / 클래스 변수 호출

MyClass.a_var = 3000 # 클래스 변수 외부에서 변경

print( MyClass.a_var ) # 클래스 생성 X / 클래스 변수 호출

```

    0
    3000



```python
m1 = MyClass() # m1 객체 생성 
m1.a_method()  # m1 객체의 method 호출

print( MyClass.a_var,m1.var ) # 클래스 변수 호출, m1 객체의 변수 호츌

m1.var = 3000 # m1 객체 변수 외부에서 변경
print( MyClass.a_var,m1.var ) #  클래스 변수 호출, m1 객체의 변수 호츌
```

    생성
    6000 10
    6000 3000


# 문제 8. isinstance( )

- 특정 클래스의 인스턴스 객체인지 아닌지를 확인


```python

class Person:
        pass
        
class Monster:
        pass


p1 = Person() # 객체 생성

result = isinstance( p1, Person ) 
print( result ) 

result2 = isinstance( p1, Monster )
print( result2 )  


```

    True
    False


# 문제 9. __init__ method()

- __init__ 에서 method 호출
- 같은 내용으로 객체 계속해서 생성 ( 다른 주소 )
- 클래스 변수 method 안에서 접근, ClassName.class_variable



```python
class Person:
        
        # 클래스 변수
        count_class_var = 0
        
        # 생성자
        def __init__( self, name, age, power ):
            
                self.name = name
                self.age = age
                self.power = power
                
                self.increase_obj() # __init__ 에서 method 호출

        # 클래스 메서드
        def increase_obj( self ):
            Person.count_class_var += 1 # 클래스 변수 
                
```


```python
print(Person.count_class_var)  

p1 = Person('P1', 20, 9)
print(Person.count_class_var)  

p2 = Person('P2', 30, 8 )
print(Person.count_class_var) 

p3 = Person('P3', 40, 7)
print(Person.count_class_var)  



```

    0
    1
    2
    3



```python
isinstance(p3,Person)
```




    True


