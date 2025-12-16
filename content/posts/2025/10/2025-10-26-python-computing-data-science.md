---
title: "Data Science을 위한 Python Computing"
date: "2025-10-26"
slug: "python-computing-data-science"
description: ""
tags: ["data-science", "데이터과학", "python", "파이썬", "introduction", "개론"]
categories: ["Notes"]
draft: false
author: "Lee Deokho"
coverImage: ""
---

# 데이터과학을 위한 파이썬 컴퓨팅

## 1. 파이썬 소개 등

### 1.1. 파이썬 소개

#### 1.1.1. 개발

- 개발자: 귀도 반 로섬
- 개발철학: 간결한 문법, 쉬운 사용성, 높은 확장성

#### 1.1.2. 역사

- 버전
  - 1994 1.0
  - 2000 2.0
  - 2008 3.0
- 발전하게 된 계기
  - Data Science: NumPy, Pandas, Matplotlib 등의 라이브러리 등장
  - Web Develop: Django, Flask 등의 프레임워크 등장
  - Machine Learning: TensorFlow, PyTorch 등의 프레임워크 등장

### 1.2. 특징

#### 1.2.1. 문법

- 동일블록 들여쓰기로 처리

#### 1.2.2. 다양한 용도로 사용

- 전문적 업무처리를 위한 개발 용이

#### 1.2.3. 인터프리터 언어

- 파이썬은 C언어에 비해 71.9배의 시간, 2.8배의 메모리, 75.88배의 에너지 소비

#### 1.2.4. 동적 타이핑

- 데이터 타입을 동적으로 관리

#### 1.2.5. 풍부한 라이브러리

- 웹크롤링: Requests, BeautifulSoup, Selenium, Scrapy, lxml
- 웹개발: Django, Flask, FastAPI, Bottle, CherryPy, Tornado
- 데이터분석: NumPy, SciPy, Pandas
- 시각화: Matplotlib, Seaborn
- 인공지능: TensorFlow, PyTorch, Scikit-learn

#### 1.2.6. 다중 패러다임

- 절차지향
- 함수형
- 객체지향

#### 1.2.7. 기타특징

- 고수준 언어
- 활성화 된 커뮤니티
  - [파이썬 공식 문서](https://docs.python.org/ko/3/)
  - [Github 소스코드](https://github.com/python/)
  - [이슈트래커](https://github.com/topics/issue-tracker?l=python)
  - [PEP](https://peps.python.org/pep-0008/)
  - [커뮤니티포럼](https://www.python.org/community/forums/)
  - [파이썬소프트웨어재단](https://www.python.org/psf-landing/)
- 활성화된 호환성
- 다양한 통합기능

### 1.3. 개발환경

#### 1.3.1. 로컬

- 파이썬 설치
- 파이썬 IDE: PyCharm, VS Code, Jupyter Notebook, Spyder, Atom

#### 1.3.2. 웹

- Colaboratory

## 2. 컴퓨팅 사고

### 2.1. 기본원리

#### 2.1.1. 프로그램

- 컴퓨터에 작업지시를 하려면 일을 구성하는 단위작업을 구체적으로 제시하고, 그 단위 작업의 순서를 명확하게 제시
- 이를 컴퓨터가 이해하는 언어로 표현

#### 2.1.2. 프로그래밍의 원리

- 프로그래밍은 컴퓨터를 제대로 사용할 수 있도록 도와주는 도구

### 2.2. 컴퓨팅 사고

#### 2.2.1. 컴퓨팅 사고란

- Computational Thinking: 컴퓨터를 이용해서 문제를 해결하는 논리체계

#### 2.2.2. 컴퓨팅 사고의 기본 구조

- 순차구조: 순차적으로 코드 실행
- 선택구조: 다음에 수행할 코드를 조건식을 적용해서 결정
- 반복구조: 어떤 조건을 만족하는 동안 지정된 코드 반복

### 2.3. 프로그램의 구조

#### 2.3.1. 순차구조

- 프로그램 코드의 수행 순서는 바로 다음에 위치한 작업

#### 2.3.2. 선택구조

- 프로그램 코드의 수행 순서를 조건식에 따라 결정

  ```
  # if 구조
  if(조건식):
    코드A

  # if-else 구조
  if(조건식):
    코드A
  else:
    코드B

  # if-else-if-else 구조
  if(조건식1):
    코드A
  elif(조건식2):
    코드A
  else:
    코드B

  # switch 구조
  switch(조건)
    case'1': 코드A
    case'2': 코드B
    case'3': 코드C
    default: 코드D
  ```

### 2.3.3. 반복구조

- 조건반복: 조건을 만족시키는 동안 반복
  ```
  while(i<>조건):
    작업
    i값 변화
  ```
- 횟수반복: 반복 횟수를 설정

  ```
  for(i=0; i<2; i++):
    작업

  while(i<2):
    작업
    i++
  ```

- 원소반복: 설정된 집합의 모든 원소를 한번씩 거쳐 가는 반복
  ```
  for i in list:
    작업
  ```

## 3. 변수와 print문

### 3.1. 변수

#### 3.1.1. 컴퓨터의 원리

- 메모리의 어디에 데이터를 저장했고, 어디에 있는 데이터를 인출할지 명확하게 지정하지 않으면 메모리를 사용할 수 없음.

#### 3.1.2. 메모리의 원리

- 메모리의 첫번째 주소는 0, 마지막 셀 주소는 10<sup>9</sup>-1

#### 3.1.3. 데이터 타입

- 정수 4byte, 실수 8byte, 문자 2byte
- 정적데이터 타입과 동적데이터 타입의 구분

#### 3.1.4. 변수의 원리

- 변수: 메모리 주소를 의미있는 이름으로 대응하는 기능
- 저수준 언어: 변수 미지원, 어샘플리어

### 3.2. 기초적인 변수의 종류

#### 3.2.1. 숫자형

- 정수형, 실수형, 8진수(0o10), 16진수(0xF)

#### 3.2.2. 문자열형

```
"Truth set you free."
'Truth set you free.'
"""Truth set you free."""
"'Truth set you free.'"
```

### 3.3. 할당

#### 3.3.1. 할당문

```
val = 123
val = val2
val = val1 + val2
val = func(val1, val2)
```

#### 3.3.2. 특징

```
val1, val2 = func() // func함수가 두 개 값을 리턴하면 각 변수에 저장
val1, _ = func() // func함수가 리턴하는 값 중 하나만 필요할 경우
```

### 3.4. 출력

#### 3.4.1. print()

```
print("Hello, World")
```

#### 3.4.2. 인지를 전달받은 print()

```
name = "Tom"
height = 170
print("Name: ", name, "Height: ", height, "cm")
```

#### 3.4.3. format()을 이용한 print()

```
# {}안에 각각 값 위치
name = "Tom"
height = "170"
print("Name: {}, Height: {}".format(name, height))

# {:.4f}는 소수점 4자리까지만 출력
pi = 3.14159213
print("Pi: {:.4f}".format(pi))

# 참조값 순서 변경
name = "Tom"
height = "170"
print("Name: {1}, Height: {0}".format(name, height))
```

#### 3.4.4. f-문자열

```
# 직접 변수 참조
name = "Tom"
height = 170
print(f"Name: {name}, Height: {height}")

# 수식 포함
a, b = 5, 3
print(f"{a} + {b} = {a + b}")
```

## 4. 다양한 자료형

### 4.1. 리스트

|    구분    |  변경  |         순서         |  생성   |    구분     |
| :--------: | :----: | :------------------: | :-----: | :---------: |
| **리스트** | **유** |        **유**        | **[ ]** | **,(쉼표)** |
|    튜플    |   무   |          유          |   ( )   |   ,(쉼표)   |
|    집합    |   유   |          무          |   { }   |   ,(쉼표)   |
|  딕셔너리  |   유   | 유<sup>3.7이상</sup> |   { }   |   ,(쉼표)   |

#### 4.1.1. 정의

- 여러개의 원소를 저장하는 Container

```
my_list = [1,2,3,4,5]
```

#### 4.1.2. 특징

- 다른 프로그램에서의 배열(Array)에 대응되나, 배열과는 다르게 다양한 유형의 데이터 함께 적제 가능

```
my_mixed_list = [1, "Hello World", True, 3.14]
```

#### 4.1.3. 데이터 접근

```
# 출력
print(my_list)
# [1, 2, 3, 4, 5]

# 데이터접근
print(my_mixed_list[1]) # Hello World
print(my_mixed_list[2]) # True
print(my_mixed_list[-1]) # 3.14
print(my_mixed_list[-4]) # 1

# 데이터 원소수정
my_mixed_list[0] = 5
print(my_mixed_list[0]) # 5
```

#### 4.1.4. 관련 함수

| 함수명      | 내용                                                              |
| :---------- | :---------------------------------------------------------------- |
| append()    | 리스트에 요소 추가                                                |
| extend()    | 리스트에 다른 리스트나 이터러블의 모든 요소 추가                  |
| insert()    | 특정 위치에 요소 삽입                                             |
| remove()    | 리스트에서 특정값을 가진 첫번째 요소 제거                         |
| pop()       | 리스트에서 특정위치에 요소를 제거하고 해당 요소 반환              |
| clear()     | 리스트의 모든 요소 제거                                           |
| index()     | 리스트에서 특정값의 첫번째 인덱스 반환                            |
| count()     | 리스트에서 특정값의 개수 반환                                     |
| sort()      | 리스트의 요소 정렬                                                |
| reverse()   | 리스트의 요소 역순 정렬                                           |
| copy()      | 리스트를 복사                                                     |
| len()       | 리스트의 길이 반환                                                |
| min()       | 리스트에서 가장 작은 값 반환                                      |
| max()       | 리스트에서 가장 큰 값 반환                                        |
| sum()       | 리스트의 모든 요소를 합산하여 반환                                |
| any()       | 리스트에 하나 이상의 참값이 있는지 확인                           |
| all()       | 리스트의 모든 요소가 참값인지 확인                                |
| map()       | 리스트의 각 요소에 함수를 적용한 결과를 반환                      |
| filter()    | 리스트에서 주어진 함수의 조건을 만족하는 요소만을 필터링하여 반환 |
| enumerate() | 리스트의 인텍스와 값을 함께 반환하는 이터레이터를 생성            |

```
# append
my_list = [1, 2, 3, 4, 5]
print(my_list) # [1, 2, 3, 4, 5]
my_list.append(6)
print(my_list) # [1, 2, 3, 4, 5, 6]

# extend
my_list = [1, 2, 3, 4, 5]
ur_list = [6, 7, 8, 9]
my_list.append(ur_list)
print(my_list) # [1, 2, 3, 4, 5, 6, 7, 8, 9]

# insert
my_list = [1, 2, 3, 4, 5]
my_list.insert(3, 10)
print(my_list) # [1, 2, 3, 10, 4, 5]
```

#### 4.1.5. 슬라이싱

- 리스트의 특정 범위를 잘라내서 새로운 리스트를 만들거나 리스트의 일부분에 접근할 수 있도록 함.
- list[start, end, step]

```
# 리스트 입력
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]

# 인덱스가 2부터 4 전까지
slice1 = my_list[2:4]
print(slice1) # [3, 4]

# 인덱스가 처음부터 5 전까지
slice2 = my_list[:5]
print(slice2) # [1, 2, 3, 4, 5]

# 인덱스가 5부터 끝까지
slice3 = my_list[5:]
print(slice3) # [6, 7, 8, 9]

# 인덱스가 2부터 7까지 2칸씩 건너
slice4 = my_list[2:7:2]
print(slice4) # [3, 5, 7]

# 데이터 역순 표시
slice1 = my_list[::-1]
print(slice1) # [9, 8, 7, 6, 5, 4, 3, 2, 1]
```

### 4.2. 튜플

|   구분   |  변경  |         순서         |  생성   |    구분     |
| :------: | :----: | :------------------: | :-----: | :---------: |
|  리스트  |   유   |          유          |   [ ]   |   ,(쉼표)   |
| **튜플** | **무** |        **유**        | **( )** | **,(쉼표)** |
|   집합   |   유   |          무          |   { }   |   ,(쉼표)   |
| 딕셔너리 |   유   | 유<sup>3.7이상</sup> |   { }   |   ,(쉼표)   |

#### 4.2.1. 정의

- 리스트와 유사하지만 원소 변경 불가

```
my_tuple = (1, 2, 3, 4, 5)
```

#### 4.2.2. 특징

- 변경할 수 없는 자료구조이며, 다양한 유형의 데이터 함께 적제 가능

```
my_mixed_tuple = (1, "Hello World", True, 3.14)
```

#### 4.2.3. 데이터 접근

```
my_tuple = (1, 2, 3, 4, 5)
my_mixed_tuple = (1, "Hello World", True, 3.14)
print(my_tuple) # (1, 2, 3, 4, 5)
print(my_tuple[0]) # 1
print(my_mixed_tuple[1]) # Hello World
```

#### 4.2.4. 관련 함수

| 함수명  | 내용                                    |
| :------ | :-------------------------------------- |
| count() | 튜플에서 주어진 값의 개수 반환          |
| index() | 튜플에서 주어진 값의 첫번째 인덱스 반환 |

```
my_tuple = (1, 1, 2, 2, 2, 3, 4, 5)
print(my_tuple.count(2)) # 3
print(my_tuple.index(1)) # 0
print(my_tuple.index(6)) # error 값이 부재
```

#### 4.2.5. 패킹과 언패킹

- 패킹: 여러 개의 원소를 하나의 튜플로 묶음.
- 언패킹: 튜플의 원소를 변수에 저장

```
# 패킹
my_tuple = 1, 2, 3, 4, 5
print(my_tuple) # (1, 2, 3, 4, 5)

# 언패킹
v, w, x, y, z = my_tuple
print(v, w, x, y, z) # 1 2 3 4 5
```

#### 4.2.5. 슬라이싱

- 리스트와 동일하므로 [리스트의 4.1.5. 슬라이싱](#415-슬라이싱) 참고

### 4.3. 집합

|   구분   |  변경  |         순서         |  생성   |    구분     |
| :------: | :----: | :------------------: | :-----: | :---------: |
|  리스트  |   유   |          유          |   [ ]   |   ,(쉼표)   |
|   튜플   |   무   |          유          |   ( )   |   ,(쉼표)   |
| **집합** | **유** |        **무**        | **{ }** | **,(쉼표)** |
| 딕셔너리 |   유   | 유<sup>3.7이상</sup> |   { }   |   ,(쉼표)   |

#### 4.3.1. 정의

- 각 원소는 고유한 값을 가짐.

```
my_set = [1,2,3,4,5]
```

#### 4.3.2. 특징

- 데이터가 고유하다는 성질 때문에 중복원소는 동일한 원소로 간주

```
# 같은 집합으로 간주되는 예
my_set1 = {1, 2, 3, 4, 5}
my_set2 = {1, 2, 2, 3, 4, 4, 5, 5, 5}
```

#### 4.3.3. 데이터 접근

- 집합은 순서가 없으므로 인덱스를 이용해서 접근 불가

#### 4.3.4. 관련 함수

| 함수명                 | 내용                                                                    |
| :--------------------- | :---------------------------------------------------------------------- |
| add()                  | 집합에 요소 추가                                                        |
| extend()               | 리스트에 다른 리스트나 이터러블의 모든 요소 추가                        |
| update()               | 다른 집합이나 이터러블의 모든 요소 추가                                 |
| remove()               | 집합에서 특정값을 가진 요소 제거. 해당 요소가 없으면 KeyErrpr 발생      |
| discard()              | 집합에서 특정값을 가진 요소 제거. 해당 요소가 없어도 KeyErrpr 미발생    |
| pop()                  | 집합에서 임의의 요소를 제거하고 반환. 집합이 비어있는 경우 KeyError발생 |
| clear()                | 집합의 모든 요소 제거                                                   |
| copy()                 | 집합를 복사                                                             |
| len()                  | 집합의 요소 개수 반환                                                   |
| union()                | 두 개 이상의 집합을 합집합으로 결합                                     |
| intersection()         | 두 개 이상의 집합의 교집합 반환                                         |
| difference()           | 두 집합의 차집합을 반환                                                 |
| symmetric_difference() | 두 집합의 대칭 차집합 반환                                              |
| issubset()             | 한 집합이 다른 집합의 부분집합인지 확인                                 |
| issuperset()           | 한 집합이 다른 집합의 상위집합인지 확인                                 |
| isdisjoint()           | 두 집합이 공통된 요소를 가지고 있는지 확인                              |

### 4.4. 딕셔너리

|     구분     |  변경  |           순서           |  생성   |    구분     |
| :----------: | :----: | :----------------------: | :-----: | :---------: |
|    리스트    |   유   |            유            |   [ ]   |   ,(쉼표)   |
|     튜플     |   무   |            유            |   ( )   |   ,(쉼표)   |
|     집합     |   유   |            무            |   { }   |   ,(쉼표)   |
| **딕셔너리** | **무** | **유<sup>3.7이상</sup>** | **{ }** | **,(쉼표)** |

#### 4.4.1. 정의

- 키와 값을 쌍으로 데이터 저장

```
my_dict = {"key1":"value1","key2":"value2","key3":"value3"}
```

#### 4.4.2. 특징

- 하나의 키가 두 번 이상 나오면 마지막에 나오는 키의 값을 저장
- 데이터베이스와 유사한 용도로 사용

```
my_dict = {"Tom":"New York", "Jane":"LA", "Tom":"Boston"}
print(my_dict["Tom"]) # Boston 출력
```

#### 4.4.3. 원소 접근

- 키를 이용해서만 접근 가능

#### 4.4.4. 관련함수

| 함수명       | 내용                                                              |
| :----------- | :---------------------------------------------------------------- |
| clear()      | 딕셔너리의 모든 항목 제거                                         |
| copy()       | 딕셔너리를 Shallow Copy하여 새로운 딕셔너리 생성                  |
| fromkeys()   | 지정된 키들로부터 새로운 딕셔너리를 생성하고 값을 초기화          |
| get()        | 지정된 키에 대한 값을 반환. 키가 존재하지 않으면 기본값 반환      |
| items()      | 딕셔너리의 모든 키-값 쌍을 반환. keys() 딕셔너리의 모든 키를 반환 |
| values()     | 딕셔너리의 모든 값들을 반환                                       |
| pop()        | 지정된 키에 해당하는 값을 제거하고 반환                           |
| popitem()    | 딕셔너리에서 임의의 키-값 쌍을 제거하고 반환                      |
| setdefault() | 지정한 키에 대한 값을 반환하고, 키가 없으면 값을 추가             |
| update()     | 다른 딕셔너리의 키-값 쌍의 시퀀스로부터 딕셔너리를 업데이트       |
| len()        | 딕셔너리의 키-값 쌍의 개수를 반환                                 |

## 5. 기초 프로그래밍: 조건문과 반복문

### 5.1. 조건문

#### 5.1.1. 조건식

|  X  |  Y  | X and Y | X or Y | notX |
| :-: | :-: | :-----: | :----: | :--: |
|  T  |  T  |    T    |   T    |  F   |
|  T  |  F  |    F    |   T    |  F   |
|  F  |  T  |    F    |   T    |  T   |
|  F  |  F  |    F    |   F    |  T   |

#### 5.1.2. if문

```
if x>0:
    print("양수")
```

#### 5.1.3. if-else문

```
if x>0:
    print("양수")
else:
    print("0 또는 음수")
```

#### 5.1.4. if-else-if문

```
if x>0:
    print("양수")
elif x<0:
    print("음수")
else:
    print("0")
```

#### 5.1.5. switch문

- 파이썬에서는 미지원

### 5.2. 반복문

#### 5.2.1. while문

```
# while문 예1
num = 1 # 초기화
while num <= 100: # 조건식
    print(num) # 반복할 코드
    num += 1 # 조건변화

# while문 예2
num = 1 # 초기화
while num != 0: # 조건식
    num = int(input("숫자를 입력하세요.")) #반복할 코드 시작
    if num != 0:
        print("이 프로그램은 0이 입력될때까지 계속 반복됨.") # 반복할 코드 끝
  print("프로그램을 종료합니다.")

# 8진수 변환
n = 88 # 변환할 10진수값 변수 저장
hex = "" # 저장할 8진수값 변수 설정
while n > 0:
    k = n % 8 # 나머지값을 k에 저장
    x = ("%d" % k) # k를 문자열로 변환하여 x에 저장
    hex = x + hex #
    n = n // 8 #
print(hex) # 130

# 8진수 변환법
# 1. 대상을 8로 나눔
# 2. 나머지는 8진수의 낮은 자리에 위치
# 3. 몫은 또 8로 나눔
# 4. 나머지를 8진수의 다음 낮은 자리에 위치
# 5. 몫이 8이 될때가지 반복
```

#### 5.2.2. for문

```
# 소수판정
n = 33 # 검토대상
prime = 1 # 1이 유지되면 소수 그렇지 않으면 소수가 아님.
for i in range(2, n-1): # 1과 자기자신의 수 제외
    if n % i == 0: # 나머지가 0과 같으면
        prime = 0 # prime을 0으로 전환
if prime == 1: # prime이 1과 같으면
    print("소수입니다.")
else:
    print("소수가 아닙니다.")

# 삼각형 그리기
n = 11
if n % 2 == 0:
  bertical_number = n // 2 # 줄 수 짝수이면 n/2
else:
  bertical_number = (n // 2) + 1 # 줄 수 홀수이면 n/2 + 1
for k in range(1, bertical_number + 1):
  starting_point = n - n//2 - k + 1 # *를 찍기 시작하는 위치
  mark_number = n - 2 * (bertical_number - k)# *의 개수
  tri = ""
  for i in range(1, starting_point):
    tri = tri + " "
  for i in range(starting_point, starting_point + mark_number):
    tri = tri + "*"
  print(tri)
# 결과
     *
    ***
   *****
  *******
 *********
***********
```

## 6. 함수 정의와 호출

### 6.1. 함수의 특징

#### 6.1.1. 장점

- 코드의 재사용성 증대
- 모듈화 향상
- 가독성 개선

#### 6.1.2. 구성요소

- 이름(identifier): 다른 코드에서 함수를 호출할 때 사용
- 매개변수(parameter): 함수에 전달하는 값
- 내용(body): 함수의 기능을 정의하는 코드 블록
- 결과(return value): 함수가 수행한 결과로 반환하는 값

### 6.2. 함수의 정의

#### 6.2.1. 파이썬에서 함수의 저으이

```
# 함수의 정의
def add(a,b):
    val = a + b
    return val

# 함수의 사용
sum = add(3,4)
print(sum)
```

#### 6.2.2. 매개변수와 인수

- 매개변수와 인수의 개수는 일치해야 함.

#### 6.2.3. 전역변수와 지역변수

```
# 지역변수
def change(a):
    a = a + 10
    print(a)
a = 5
change(a) # 15
print(a) # 5

# 전역변수
def change():
    global a
    a = a + 10
    print(a)
a = 5
change() # 15
print(a) # 15
```

### 6.3. 파이썬에서의 함수 호출

#### 6.3.1. 매개변수와 출력이 없는 함수

```
day ="Sunday"
def banner():
    print("Welcom")
    print("This is ", day)
banner() # This is Sunday
```

#### 6.3.2. 매개변수만 있는 함수

```
def add(a, b):
    global sum
    sum = a + b
    print(sum)
add(10, 20) # 결과를 프린트문으로 출력
print(sum) # 전역변수에 저장된 결과 출력
```

#### 6.3.3. 출력만 있는 함수

```
from datetime import datetime

def print_current_time():
    current_time = datetime.now()
    print("현재 시간은 ", current_time, "입니다.")

print_current_time()
```

#### 6.3.4. 매개변수와 출력이 있는 함수

```
def multi(a, b):
    return a*b

print(multi(3, 4))
```

### 6.4. 파이썬의 독특한 함수 사용

#### 6.4.1. 입력의 개수가 정해져 있지 않은 함수

- 여러 개의 숫자를 받아 합을 출력하는 함수를 가정할 때, 매개변수의 개수가 정해지지 않았다면 \* 사용

```
def add_unfixed(*args):
    result = 0
    for arg in args:
        result = result + arg
    return result

print(add_unfixed(1, 2, 3, 4)) # 10
print(add_unfixed(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)) # 55
```

#### 6.4.2. 키워드 매개변수

- 함수를 호출할 때 인자의 이름을 지정하여 값을 전달하는 방식

```
# 사례1
def hello(name, age):
    print("H1, ", name, ". Are you ", age, "years old?")
hello(60, "Tom") # Hi, 60. Are you Tom years old?
hello(age=60, name="Tom") # Hi, Tom. Are you 60 years old?

# 사례2
def hello_unfixed(**kargs):
    for arg in kargs:
        print(arg, "is", kargs[arg]) # arg는 key, kargs[arg]는 value
        print("")

hello_unfixed(name="Tom")
hello_unfixed(name="Tom", age=60)
hello_unfixed(name="Tom", home="LA")
hello_unfixed(name="Tom", home="LA", age=60)
hello_unfixed(age=60, name="Tom", home="LA")
```

#### 6.4.3. 여러개의 리턴값을 갖는 함수

```
def calc(a, b):
    return a+b, a*b

sum_multi = calc(5, 2) # Tuple type
sum, _ = calc(5, 2) # Int type
_, multi = calc(5, 2)
print(type(sum))
print(multi)
print(sum_multi)
```

#### 6.4.4. 매개변수의 초기값 설정

- 여러 매개변수를 가진 함수를 정의할 때, 매개변수의 기본값(default)을 지정할 필요시 운용

```
def hello(name, home="No where"):
    print("Hi, ", name, ", You are from ", home)

hello("Tom") # Hi,  Tom , You are from  No where
hello(name="Tom") # Hi,  Tom , You are from  No where
hello("Tom", "LA") # Hi,  Tom , You are from  LA
```

#### 6.4.5. 람다구문

- 문법: 함수이름 = lambda 매개변수1, 매개변수2: 매개변수를 이용한 함수의 내용

```
def general_sum(a, b):
    return a+b
# 람다구문으로 표현
lambda_sum = lambda a,b: a+b

print(general_sum(5, 7)) # 12
print(lambda_sum(5, 7)) # 12
```

## 7. 클래스와 모듈

### 7.1. 클래스는 왜 필요한가?

- 클래스는 여러 변수의 조합으로 표현되며, 속성(attribute)은 클래스를 통해 접근할 수 있는 정보
- 클래스에 속한 정보들을 처리하는 함수를 메서드(method)라고 하며, 클래스에 속한 속성은 매서드를 이용해서만 접근가능
- 한 클래스의 속성과 매서드가 다른 클래스에 상속되므로 클래스 정의를 효율적으로 수행
- 모듈이란 내 코드 외부의 클래스나 함수를 사용하는 방법

### 7.2. 클래스 만들기

#### 7.2.1. 클래스의 속성 만들기

```
class Rectangle: # 사각형의 넓이를 구하는 클래스 생성
    def make(self, x1, x2, y1, y2): # 속성 초기화
        self.x1 = x1
        self.x2 = x2
        self.y1 = y1
        self.y2 = y2

r1 = Rectangle() # r1이라는 객체 생성
r1.make(3, 4, 5, 6) # 속성값 지정
print(r1.x1, r1.x2, r1.y1, r1.y2)
```

```
######### 생성자 사용 #########
class Rectangle: # 사각형의 넓이를 구하는 클래스 생성
    def __init__(self, x1, x2, y1, y2): # 속성 초기화. 매개변수를 전달하는 생성자 __init__ 사용
      self.x1 = x1
      self.x2 = x2
      self.y1 = y1
      self.y2 = y2

r1 = Rectangle(3, 4, 5, 6) # r1이라는 객체 생성하며 속성값 지정
print(r1.x1, r1.x2, r1.y1, r1.y2)
```

#### 7.2.1. 클래스의 매서드 만들기

```
class Rectangle:  # 사각형의 넓이를 구하는 클래스 생성
    def __init__(
        self, x1, x2, y1, y2
    ):  # 속성 초기화 메소드. 매개변수를 전달하는 생성자 __init__ 사용
        self.x1 = x1
        self.x2 = x2
        self.y1 = y1
        self.y2 = y2

    def area(self):  # 사각형의 넓이 계산 메소드
        return (self.x2 - self.x1) * (self.y2 - self.y1)

    def perimeter(self):  # 사각형의 둘레 계산 메소드
        return 2 * ((self.x2 - self.x1) + (self.y2 - self.y1))


r1 = Rectangle(0, 5, 0, 6)  # r1이라는 객체 생성하며 속성값
print(r1.area(), r1.perimeter())
```

### 7.3. 객체 생성

```
class Rectangle:  # 사각형의 넓이를 구하는 클래스 생성
    def __init__(
        self, x1, x2, y1, y2
    ):  # 속성 초기화 메소드. 매개변수를 전달하는 생성자 __init__ 사용
        self.x1 = x1
        self.x2 = x2
        self.y1 = y1
        self.y2 = y2

    def area(self):  # 사각형의 넓이 계산 메소드
        return (self.x2 - self.x1) * (self.y2 - self.y1)

    def perimeter(self):  # 사각형의 둘레 계산 메소드
        return 2 * ((self.x2 - self.x1) + (self.y2 - self.y1))


r1 = Rectangle(1, 5, 1, 5)  # r1이라는 객체 생성하며 속성값
r2 = Rectangle(3, 6, 3, 6)  # r1이라는 객체 생성하며 속성값
print("사각형 r1: ", r1.area(), r1.perimeter())
print("사각형 r2: ", r2.area(), r2.perimeter())
```

### 7.4. 클래스 상속

#### 7.4.1. 상속의 구현

```
class Rectangle:  # 사각형의 넓이를 구하는 클래스 생성
    def __init__(
        self, x1, x2, y1, y2
    ):  # 속성 초기화 메소드. 매개변수를 전달하는 생성자 __init__ 사용
        self.x1 = x1
        self.x2 = x2
        self.y1 = y1
        self.y2 = y2

    def area(self):  # 사각형의 넓이 계산 메소드
        return (self.x2 - self.x1) * (self.y2 - self.y1)

    def perimeter(self):  # 사각형의 둘레 계산 메소드
        return 2 * ((self.x2 - self.x1) + (self.y2 - self.y1))


class ColorRectangle(Rectangle):
    def __init__(self, x1, x2, y1, y2, color):
        super().__init__(x1, x2, y1, y2)
        self.color = color


r1 = ColorRectangle(1, 5, 1, 5, "red")  # r1이라는 객체 생성하며 속성값
r2 = ColorRectangle(3, 6, 3, 6, "white")  # r1이라는 객체 생성하며 속성값
print("사각형 r1: ", r1.area(), r1.perimeter(), r1.color)
print("사각형 r2: ", r2.area(), r2.perimeter(), r2.color)
```

### 7.4.2. 새로운 메서드 추가

```
class Rectangle:  # 사각형의 넓이를 구하는 클래스 생성
    def __init__(
        self, x1, x2, y1, y2
    ):  # 속성 초기화 메소드. 매개변수를 전달하는 생성자 __init__ 사용
        self.x1 = x1
        self.x2 = x2
        self.y1 = y1
        self.y2 = y2

    def area(self):  # 사각형의 넓이 계산 메소드
        return (self.x2 - self.x1) * (self.y2 - self.y1)

    def perimeter(self):  # 사각형의 둘레 계산 메소드
        return 2 * ((self.x2 - self.x1) + (self.y2 - self.y1))


class ColorRectangle(Rectangle):  # 자식클래스 생성
    def __init__(
        self, x1, x2, y1, y2, color
    ):  # 자식 클래스가 새 속성을 추가할 경우 부모속성 초기화 필요
        super().__init__(x1, x2, y1, y2)  # 부모 클래스의 메소드 호출
        self.color = color

    def which_color(self, x, y):  # 색표시 결정 클래스
        if (
            self.x1 < x and x < self.x2 and self.y1 < y and y < self.y2
        ):  # 새로 입력받는 값이 x, y의 안에 있을 경우
            return self.color
        else:
            return "무색무취"


r1 = ColorRectangle(0, 5, 0, 5, "red")  # r1이라는 객체 생성하며 속성값
r2 = ColorRectangle(0, 6, 0, 6, "white")  # r1이라는 객체 생성하며 속성값
print("사각형 r1: ", r1.area(), r1.perimeter(), r1.which_color(3, 3))
print("사각형 r2: ", r2.area(), r2.perimeter(), r1.which_color(7, 0))

```

### 7.4.3. 메서도 오버라이딩

```
class Rectangle:  # 클래스 생성
    def __init__(self, x1, x2, y1, y2):  # 생성자로 속성 초기화
        self.x1 = x1
        self.x2 = x2
        self.y1 = y1
        self.y2 = y2

    def area(self):  # 면적구하기 메소드
        return (self.x2 - self.x1) * (self.y2 - self.y1)

    def perimeter(self):  # 둘레 구하기 메소드
        return 2 * ((self.x2 - self.x1) + (self.y2 - self.y1))


class ColorRectangle(Rectangle):  # 자식클래스 생성
    def __init__(self, x1, x2, y1, y2, color):  # 부모속성+새속성
        super().__init__(x1, x2, y1, y2)
        self.color = color

    def area(self):  # 부모메서드 재정의
        return 2 * (self.x2 - self.x1) * (self.y2 - self.y1)

    def color_render(self, x, y):  # 색표시 메서드
        if self.x1 < x and x < self.x2 and self.y1 < y and y < self.y2:
            return self.color
        else:
            "무채색"


r1 = ColorRectangle(0, 7, 0, 7, "red")  # 객체 생성
print(r1.area(), r1.color_render(3, 3))  # 객체의 면적과 색 표시
```

### 7.5. 모듈

> Module: 코드를 구성하는 논리적인 단위

#### 7.5.1. 파이썬의 외부 모듈

|         분야          |     대표적인 외부 모듈     |
| :-------------------: | :------------------------: |
|  데이터분석 및 과학   |    NumPy, Pandas, SciPy    |
|        웹 개발        |       Flask, Django        |
| 머신러닝 및 인공지능  |    TensorFlow, PyTorch     |
| 웹 스크래핑 및 자동화 |  BeautifulSoup, Selenium   |
|        DB연동         | MySQL, PostgreSQL, MongoDB |
|  그래픽 및 게임 개발  |           Pygame           |

#### 7.5.2. 외부 모듈 사용

```
import pytorch  # pytorch 모듈 사용
import pytorch as py  # py로 축약
from random import randint  # random 모듈에서 randint 함수만 사용
random_number = randint(1, 100)
```

#### 7.5.3. pip를 이용한 외부 모듈 설치

```
> pip install requests  # request 모듈 설치
> pip install requests==2.28.1  # 특정 버전 설치
> pip install requests>=2.28.1  # 특정 버전이상 설치
> pip install requests<=2.28.1  # 특정 버전이하 설치
> pip install --upgrade requests  # 특정 모듈 업그레이드
> pip uninstall requests  # 특정 모듈 삭제
```

## 8. 파일 입출력하기

### 8.1. 파일

|  형식  | 장점                      | 단점                                                |
| :----: | :------------------------ | :-------------------------------------------------- |
|  txt   | 편의성 및 범용성          | 구조화 데이터 저장 비효율, 자료가 커지면 속도 격감  |
|  csv   | 테이블 형태 지원          | 복잡구조 및 대용량 부적합, 자료 내 쉼표 구분자 오류 |
|  json  | 계층적 구조지원, 웹 범용  | 텍스트 기반으로 대용량 부적합                       |
|  xml   | 유연한 구조, 다수플랫폼   | 큰 파일크기, 복잡한 파싱과정, 낮은 파싱속도         |
|  yaml  | 고가독성, 설정파일로 사용 | 탭과 공백 민감, 큰 파일은 핸들링이 어려움           |
|  xlsx  | 복잡 구조 및 수식 가능    | 전용라이브러리 필요 및 편집용 상용앱 필요           |
|  hdf5  | 대용량, 과학계산 적합     | 복잡한 API, 특정 사용 사례에만 적합                 |
| SQLite | 경량DB, 서버불요, SQL문법 | 대규모 멀티유저 시스템 부적합                       |

### 8.2. 파일의 경로

```
####### 절대경로 #######
"C:\Users\deokh\Desktop\임시음악"  # Windows
"/home/username/documents/file.txt" # Unix, Linux, macOS

####### 상대경로 #######
./file.txt  # 핸재 디랙터리
../other-folder/file.txt  # 부모 디랙터리

####### 파일경로 사용 #######
path="C:\\Users\\deokh\\Documents\\Daum\\PotEncoder\\thumbnail.jpg"  # 이중 백슬래시 사용
path=r"C:\Users\deokh\Documents\Daum\PotEncoder\thumbnail.jpg"  # raw 문자열 사용
path="/home/username/documents/fi;le.txt"  # 슬래시 사용
path="C:/Users/deokh/Documents/Daum/PotEncoder/thumbnail.jpg"  # 슬래시 사용 가능

####### 모듈을 이용한 경로 사용 #######
import os  # os.path 모듈 사용

path = os.path.join(
    "Users", "Username", "Documents", "file.txt"
)  # Users/Username/Documents/file.txt

from pathlib import Path  # pathlib 모듈 사용

path = Path("Users") / "Username" / "Documents" / "file.txt"
print(path)
```

### 8.3. 파이썬으로 파일 다루기

#### 8.3.1. CSV파일 다루기

| 파일열기모드 |  W  |  R  | 파일없음 | 기존파일 | 커서 |         용도         |
| :----------: | :-: | :-: | :------: | :------: | :--: | :------------------: |
|      r       |  Y  |  N  |   오류   |   유지   | 맨앞 |       읽기전용       |
|      w       |  N  |  Y  |   생성   |   삭제   | 맨앞 |       쓰기전용       |
|      a       |  N  |  Y  |   생성   |   유지   | 맨끝 |       추가쓰기       |
|      x       |  N  |  Y  |   생성   |   오류   | 맨앞 |       새로생성       |
|      r+      |  Y  |  Y  |   오류   |   유지   | 맨앞 |       읽고수정       |
|      w+      |  Y  |  Y  |   생성   |   삭제   | 맨앞 |     새로쓰고읽기     |
|      a+      |  Y  |  Y  |   생성   |   유지   | 맨끝 |     추가쓰고읽기     |
|      rb      |  Y  |  N  |   오류   |   유지   | 맨앞 |     바이너리읽기     |
|      wb      |  N  |  Y  |   생성   |   삭제   | 맨앞 |     바이너리쓰기     |
|      ab      |  N  |  Y  |   생성   |   유지   | 맨끝 |   바이너리추가쓰기   |
|     r+b      |  Y  |  Y  |   오류   |   유지   | 맨앞 |   바이너리읽고쓰기   |
|     w+b      |  Y  |  Y  |   생성   |   삭제   | 맨앞 | 바이너리새로쓰고읽기 |
|     a+b      |  Y  |  Y  |   생성   |   유지   | 맨끝 | 바이너리추가쓰고읽기 |
|      rt      |  Y  |  N  |   오류   |   유지   | 맨앞 |   택스트읽기(기본)   |
|      wt      |  N  |  Y  |   생성   |   삭제   | 맨앞 |      택스트쓰기      |
|      at      |  N  |  Y  |   생성   |   유지   | 맨끝 |    택스트추가쓰기    |

|  newline=값   | 의미                                         |
| :-----------: | :------------------------------------------- |
| None(Default) | 운영체제에 따라 자동줄바꿈 변환(\n <-> \r\n) |
|      ""       | 원본 유지                                    |
|      \n       | 줄바꿈을 \n으로 고정                         |
|     \r\n      | 줄바꿈을 윈도우 스타일로 고정                |
|      \r       | 맥스타일                                     |

[파이썬 내장함수]("https://docs.python.org/ko/3/library/functions.html#open")

```
import csv

data = (
    ["25-Nov-07", "29.76", "29.97", "29.52", "29.96", "92433800", "29.79"],
    ["25-Nov-08", "29.76", "29.97", "29.52", "29.96", "92433800", "29.79"],
)

with open("D:/dev/python/knou/test.csv", "r+", newline="") as file:  # 파일 맨 앞에 위치
    csv_reader = csv.reader(file)  # csv파일을 행 단위로 읽는 이터레이터 생성(파일을 읽어 각 행을 리스트로 반환)
    for row in csv_reader:
        print(row)
    file.seek(0, 2)  # 파일 끝으로 이동
    csv_writer = csv.writer(file)  # csv파일에 행을 추가하는 writer 객체 생성
    for row in data:
        csv_writer.writerow(row)
    file.seek(0)  # 파일 처음으로 이동
    for row in csv_reader:
        print(row)
```

##### 8.3.2. JSON 파일 다루기

```
import json

data = {"name": "John Mac", "email": "john_mac@aaa.com", "phone": "010-1111-0000"}

path = "D:/dev/python/knou/output.json"  # 저장 경로

with open(path, "w+") as file:  # 새로 쓰고 읽기 모드로 열기
    json.dump(data, file, indent=4)  # 딕셔너리를 JSON형식으로 파일에 쓰기
    file.seek(0)  # 커서를 파일 처음으로 이동
    print(json.load(file))  # 파일에서 JSON을 읽어 파이썬 객체로 출력
```

### 8.4. Pandas로 파일 다루기

```
import pandas as pd

# sep로 필드 구분자 설정, 헤더가 없는 경우 header=None
df2 = pd.read_csv("D:/dev/python/knou/test2.csv", sep=";", header=None)

# sep로 필드 구분자 설정, 헤더가 두번째 라인에 있는 경우
df3 = pd.read_csv("D:/dev/python/knou/test3.csv", sep=";", header=1)

data = [["25-Nov-12", "29.76", "29.97", "29.52", "29.96", "92433800", "29.79"],
        ["25-Nov-13", "29.76", "29.97", "29.52", "29.96", "92433800", "29.79"],
        ["25-Nov-14", "29.76", "29.97", "29.52", "29.96", "92433800", "29.79"],]
df = pd.DataFrame(data)  # 데이터 프레임으로 변환
df.to_csv("D:/dev/python/knou/test4.csv", index=False)  # 데이터 프레임 객체를 파일로 저장
print(df)
```

## 9. 데이터 저장 및 조작

### 9.1. Pandas의 특성

- Series라는 1차원 배열과 행과 열로 이루어진 DataFrame라는 테이블 구조를 사용
- 다양한 형태의 데이터(txt, xlsx, sql)를 쉽게 읽고 쓰기 가능
- 복잡한 데이터 조작을 위한 필터링, 그룹화, 변환 등 제공
- 누락된 데이터를 유연하게 처리
- 데이터셋의 병합, 연결, 재구성 등의 작업 용이
- 시계열 데이터를 다루는 기능이 포함

### 9.2. DataFrame

import pandas as pd

# CSV 파일 불러오기

#### 9.2.1. 데이터 프레임 생성

```
imnport pandas as pd

df = pd.read_csv("D:\dev\python\knou\california_housing_test.csv")
print(df.head())
```

#### 9.2.2. 데이터 접근하기

```
import pandas as pd

# "median_income" 필드에 접근
median_income = df["median_income"]
print(median_income.head())

# 레이블이 0, 1, 2 데이터에 접근
record_1to3 = df.loc[[0, 1, 2]]
print(record_1to3)

# 인덱스 0~4 접근
record_slice = df.loc[0:4]
print(record_slice)

# .loc를 이용한 필드 선택
populations = df.loc[:, "population"]
print(populations.head())

# 0번행의 인구
first_populations = df.loc[0, "population"]
print(first_populations)

# median이 4이상인 행의 median_house_value
high_income_house = df.loc[df["median_income"] >= 4, "median_house_value"]
print("median이 4이상인 행의 median_house_value", high_income_house.head())

# 여러조건 median_income이 4 이상이고, median_house_value가 250 이상인 행
filtered_data = df.loc[(df["median_income"] >= 4) & (df["median_house_value"] >= 250)]
print(filtered_data.head())

# 0번째 레코드에 접근
first_record = df.iloc[0]
print(first_record)

# 1, 2, 3번째 레코드에 접근
record_1to3 = df.iloc[[0, 1, 2]]
print(record_1to3)

# 인덱스 0~3 접근(4는 포함 되지 않음.)
record_slice = df.iloc[0:4]
print(record_slice)

# 앞 인자는 행, 뒤 인자는 열
several_slice_data = df.iloc[0:3, 1:3]
print(several_slice_data)
```

#### 9.2.3. 데이터 추가하기

```
import pandas as pd

# csv파엘로 데이터프레임 객체 생성
df = pd.read_csv("D:\dev\python\knou\california_housing_test.csv")

# 새로운 필드"new_column"를 생성하고 초기값은 0으로 설정
df["new_column"] = 0
print(df)

# 필드"new_column"을 기준으로 열기준 삭제, 값반환 없음.
df.drop("new_column", axis=1, inplace=True)
print(df)

# median_house_value 열을 1000으로 나눈 값을 house_value_thousands 열로 추가
df["house_value_thousands"] = df["median_house_value"] / 1000
print(df.loc[:, "house_value_thousands"])

# 새로운 레코드 추가
# 동일한 레이블을 갖는 새로운 데이터 프레임을 생성해서 둘을 Concatenate(결합)시킴.
new_data = pd.DataFrame(
    {
        "longitude": [-124.35],
        "latitude": [40.54],
        "housing_median_age": [52],
        "total_rooms": [1820],
        "total_bedrooms": [300],
        "population": [500],
        "households": [300],
        "median_income": [3],
        "median_house_value": [200000],
    }
)
# 기존 인덱스 무시하고 0부터 다시 연속된 인덱스 생성
df = pd.concat([df, new_data], ignore_index=True)
print(df)
```

#### 9.2.4. 데이터 병합하기

```
import pandas as pd

####### concat은 한축을 따라 여러 데이터프레임을 연결
####### 주료 같은 형태의 데이터를 합칠 때 사용
df_concat1 = pd.DataFrame({"A": ["가나", "다라"], "B": ["마바", "사아"]})
df_concat2 = pd.DataFrame({"A": ["자차", "타카"], "B": ["파하", "으이"]})
print(pd.concat([df_concat1, df_concat2], ignore_index=True))

####### merge는 주어진 key값을 기준으로 둘 이상의 데이터프레임 병합
####### SQL의 JOIN연산과 유사
df_merge1 = pd.DataFrame(
    {"key": ["가0", "가1", "가2", "가3"], "수도권": ["서울", "경기", "인천", "강원"]}
)
df_merge2 = pd.DataFrame(
    {"key": ["가0", "가1", "가2", "가3"], "충청권": ["세종", "대전", "충남", "충북"]}
)
print(pd.merge(df_merge1, df_merge2, on="key"))
```

#### 9.2.5. 데이터 요약하기

```
import pandas as pd

df = pd.read_csv("D:\dev\python\knou\california_housing_test.csv")

####### .describe은 각 열에 대한 descriptive 통계 제공
####### 평균, 표준편차, 최소값, 최대값, 사분위수

print("describe")
print(df.describe())
print(df.describe(include="all"))


####### .info는 데이터프레임 자체에 대한 정보 제공
####### 데이터를 구성하는 열들의 형식, 자료의 수, 메모리 사용량

print("info")
print(df.info())


####### .isnull은 특정열의 값이 null이면 True반환, .sum과 결합가능
####### 데이터를 구성하는 열들의 형식, 자료의 수, 메모리 사용량

print("isnull")
print(df.isnull().sum())
print(
    df.loc[df["new_column"].isnull()],
)  # isnull이 true인 값만 출력


####### value_counts 특정 컳럼의 범주의 수와 각각의 빈도수
print("value_counts()")
print(df["housing_median_age"].value_counts())
```

## 10. 통계 라이브러리

### 10.1. 파이썬 통계 라이브러리

#### 10.1.1. NumPy

- 기본적 수치계산 라이브러리로, 고성능 다차원 배열 객체와 도구 제공
- 벡터, 연산, 브로드캐스팅 및 고속연산 지원
- 선형대수, 난수 생성 등 기본적 수학 함수 및 통계 연산 제공

#### 10.1.2. SciPy

- NumPy 기반
- 최적화, 통계, 신호처리 등 과학 기술 계산 포함
- 통게 모듈은 다양한 확률분포와 통계적 검정 기능 제공

#### 10.1.3. Pandas

- 데이터 처리와 분석을 위한 대중적 라이브러리
- Series와 DataFrame을 제공하여 데이터 조작, 준비, 분석에 용이
- 시계열 데이터 분석, 결측치 처리, 데이터 요약과 변환 등 지원

#### 10.1.4. Statsmodels

- 통계모델, 통계 테스트, 데이터 탐색 및 시계열분석
- 회귀분석, 일반화 선영모델, 시계열분석모델 제공
- 모델 진단, 추정 및 예측, 통계적 검정을 위한 포괄적 도구 제공

#### 10.1.5. Matplotlib

- 대중적 시각화 라이브러리
- 플롯의 각 요소를 세밀하게 제어가능한 커스터마이징 기능

#### 10.1.6. Seaborn

- Matplotlib 기반, 더 심미적이고 복잡한 시각화 가능 제공
- 다변량 데이터 분석에 적합한 시각화 및 팔레트 기능이 특징

### 10.2. SciPy와 Statsmodels

#### 10.2.1. SciPy

```
import pandas as pd
import numpy as np
from scipy import stats
from scipy.optimize import curve_fit
from scipy.signal import convolve
import matplotlib.pyplot as plt

df = pd.read_csv("D:/dev/python/knou/california_housing_train.csv")

####### .descibe은 Pandas 메서드로 기본적 기술통계 정보인 레코드수(count), 평균(mean), 표준편차(std), 최소값(min), 사분위수(25%, 50%, 75%), 최대값(max) 제공

# print(df.describe())

####### stats.descibe()은 데이터수(nobs), 최소/최대값(minmax), 평균(mean), 분산(variance), 분포특성(왜도(skewness), 첨도(kurtosis)) 제공
dese = stats.describe(df)
print(dese.mean)

# t분포(Student’s t-distribution)는 모집단의 표준편차를 알 수 없고 표본 크기가 작은 경우 평균의 차이를 검정하거나 신뢰구간을 추정할 때 사용하는 확률분포

####### 가격중앙값(median_house_value)을 구성하는 1,700개중 500개를 추출하고, 이들이 정규분포를 따르는지 확인하기 위한 Shapiro-Wilk 검정 수행
shapiro_test = stats.shapiro(df["median_house_value"].sample(500))
print(
    f"Shapiro-Wilk Test Statistic: {shapiro_test.statistic}, p-value: {shapiro_test.pvalue}"
)

####### 주택가격 중앙값들의 평균이 특정값과 다른지 검정하는 단일표본 t-검정 수행
####### H0(귀무가설): 평균 중간 주택 가격은 200,000이다.
####### H1(대립가설): 평균 중간 주택 가격은 200,000이 아니다.
t_test_result = stats.ttest_1samp(df["median_house_value"].sample(500), 200000)
print(f"t-Statistic: {t_test_result.statistic}, p-value: {t_test_result.pvalue}")


####### 주택 데이터의 특정특성과 주택가격 중앙값 간의 관계를 모델링하고 이를 최적화하는 문제 고려
####### 선형관계를 모델링하는 함수정의
def liner_model(x, a, b):
    return a * x + b


x_data = df["median_income"]
y_data = df["median_house_value"]
####### curve_fit 함수를 사용해 모델 파라미터 최적화
params, covariance = curve_fit(liner_model, x_data, y_data)
print(f"Optimized parameters: {params}")


####### 필터설계 및 스펙트럼 분석 등
df_median_house_value = df["median_house_value"]
####### 이동 평균을 계산하기 위한 윈도 생성
window_size = 5
window = np.ones(window_size) / window_size
####### 이동 평균 필터 적용
smoothed_signal = convolve(df_median_house_value, window, mode="valid")
####### 원본 신호와 스무딩 신호 비교
plt.figure(figsize=(10, 6))
plt.plot(df_median_house_value.index, df_median_house_value, label="Original")
plt.plot(
    np.arange(window_size - 1, len(df_median_house_value)),
    smoothed_signal,
    label="Smoothed",
    color="red",
)
plt.legend()
plt.show()
```

#### 10.2.2. Statsmodels

```
import pandas as pd
import statsmodels.api as sm

####### 데이터 로드
housing_data = pd.read_csv("D:\dev\python\knou\california_housing_test.csv")
####### 독립변수와 종속변수 선택
X = housing_data["median_income"] # 독립변수
y = housing_data["median_house_value"] # 종속변수
####### 상수형 추가
X = sm.add_constant(X)
####### 선형 회귀모형 피팅
model = sm.OLS(y, X).fit()
####### 결과 요약 출력
print(model.summary())

####### 선형회귀모델을 활용한 예측 과정
new_data = pd.DataFrame({"const": 1, "median_income": [2.5, 4.5, 6.5]})
####### 예측 수행
predictions = model.predict(new_data)
print(predictions)
```

## 참고자료

- 한종대・민경하・유찬우, 파이썬 컴퓨팅, KNOU Press (2024.07.25)
- [Cheat Sheet](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)
- [SciPy API](https://docs.scipy.org/doc/scipy/reference/index.html#scipy-api)
