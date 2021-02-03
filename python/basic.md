# Python 기초

## Jupyter Notebook 사용법

- REPL(read-eval-print loop) 
- command 
  - m : 마크다운 문법 사용
  - b: below - 아래 cell 추가
  - a: above - 위 cell 추가
  - h: 키보드 단축키 참고 가능
  - command mode(명령 모드): ESC <-> edit mode(수정 모드): Enter

## Python 기초 문법(Syntax)

### 주석

1. 한 줄 주석은 `#`으로 표현한다.

2. 여러 줄의 주석은

   1) 한 줄 씩 `#`을 사용해서 표현하거나,

   2) `"""` 또는 `'''` (여러줄 문자열, multiline string)으로 표현할 수 있다.

   -> 주로 함수/클래스를 설명하기 위해 활용된다.

### 코드 라인

1. 파이썬 코드는 **'1줄에 1문장'**이 원칙이다. (T/F 문장으로 출제 가능)

2. 문장이란 파이썬이 실행 가능한 최소한의 코드 단위이다. 

3. 기본적으로 파이썬에서는 `;`을 작성하지 않는다. 

4. 한 줄로 표기할 때는 `;`을 작성하여 표기할 수 있다. 

5. 줄을 여러줄 작성할 때는 역슬래시`\`를 사용하여 작성할 수 있다.

   ```python
   print('hello
   world')
   ```

   ```python
   print('hello\
   world')
   ```

   하지만, 잘 사용하지는 않는다.

6. 아래와 같이 작성하는게 관례이다.

   ```python
   print('''hello
   world''')
   ```

## 변수(Variable)

### 변수  ![변수](basic.assets/변수.png)

- **할당 연산자** 
- 변수는 `=`을 통해 할당된다.
  - 해당 데이터 타입을 확인하기 위해서는 type()을 활용한다.
  
- 예제) 변수 x와 y의 값을 바꿔보기

```python
x = 10
y= 100

#임시변수 활용
temp = x
x = y
y = temp
print(x, y) #파이썬 외의 언어

#파이썬 
x = 10 
y = 100
x, y = y, x
print(x, y) #파이썬은 가능
```

- **식별자**: 파이썬에서 식별자는 변수, 함수, 모듈, 클래스 등을 식별하는데 사용되는 이름(name)
  - **키워드 쓸 수 없음**: `False, None, True, and, as, assert, async, await, break, class, continue, def, del, elif, else, except, finally, for, from, global, if, import, in, is, lambda, nonlocal, not, or, pass, raise, return, try, while, with, yield`
  - **이름 짓는 법**: 숫자 먼저 올 수 x (T/F 문제로 출제 가능)
  - 길이에 제한이 없다. 
  - 대소문자를 구별한다.

## 데이터 타입(Data Type)

: dust(식별자) = 60(Data Type)

1. 숫자(number) 타입
   - int(정수, integer)
   - 8진수: `0o` / 2진수: `0b` / 16진수: `0x`
   - 파이썬은 정수 자료형에서 오버플로우가 있다. (x)
   - 파이썬은 정수 자료형에서 오버플로우가 없다. 임의 정밀도 산술을 사용하기 때문이다. 

2. 글자(string) 타입

   - 문자열은 `''` 나 `""`을 활용하여 표현 가능하다. 

   - **따옴표 사용**:

     문자열 안에 문장부호(`'`, `"`)가 사용될 경우 이스케이프 문자(`\`)를 활용 가능하다. 

   - **이스케이프 시퀀스**:

     ```python
     \n: 줄바꿈
     \t: 탭
     \r: 캐리지리턴
     \0: 널(Null)
     \\: \
     \': 단일인용부호
     \": 이중인용부호
     ```

   - end 옵션:

     ​	한 줄 문자에 이용

3. 참/거짓(Boolean) 타입

### 형변환(Type conversion) 타입

: 문자열 안에 변수의 값 자체를 넣는 방법

### 표현식 & 문장

표현식

- 표현식 => `evaluate` => 값

  1) 하나의 값으로 환원될 수 있는 문장

  2) **식별자**, 값(리터럴), **연산자**로 구성됨

문장

- 파이썬이 실행 가능한 최소한의 코드 단위

**표현식이 문장 안에 포함되는 관계**

```python
표현식: area < 100
문장:
  greeting = 'Bye' + '!' * 3
```