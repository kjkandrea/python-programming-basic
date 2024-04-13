# 함수

## 함수의 개념

함수 : 특정 작업을 수행하는 명령문의 집합
* 특정 작업을 함수의 이름으로 대체
* 유사한 유형의 문제를 해결할 수 있도록 고려

사용자 정의 함수
* 내장 함수와 달리 사용자의 목적에 따라 정의된 함수

```py
def 식별자(매개변수 리스트):
    명령 블록
```

## 동시할당

복수개의 변수에 값을 동시에 할당할 수 있다.

```
temp, season = 27, "summer"
```

파이썬에서는 다음과 같이 swap 이 가능하다.

```
a = 0
b = 1

b, a = a, b
```

## 변수의 스코프

프로그램에서 변수가 참조될 수 있는 영역
* **전역변수** : 프로그램 전체 영역에서 접근
* **지역변수** : 선언된 함수 내부에서만 접근