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
print(int(5/2))
print(5 // 2)   # 버림 나눗셈, 결과에서 소수점 이하는 버림
```

    2
    2



```python
'Python' == 'Python'
```




    True




```python
'Python' != 'Python'
```




    False




```python
# is is not 
# is, is not은 객체(object)를 비교합니다.

1 == 1.0

```




    True




```python
1 is 1.0
```

    <>:1: SyntaxWarning: "is" with a literal. Did you mean "=="?
    <>:1: SyntaxWarning: "is" with a literal. Did you mean "=="?
    <ipython-input-20-2ebf4c947f31>:1: SyntaxWarning: "is" with a literal. Did you mean "=="?
      1 is 1.0





    False


