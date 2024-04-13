# 객체지향

## 객체지향의 개념

* 객체와 객체 사이의 상호작용으로 프로그램을 구성하는 프로그래밍 패러다임
* 프로그램을 유연하고 변경하기 쉽게 만들어 대규모 소프트웨어 개발에 적용 

### 객체지향 패러다임의 특징

* **추상화** : 공통의 속성이나 기능을 도출
* **캡슐화** : 데이터 구조와 데이터의 연산을 결합
* **상속** : 상위 개념의 특징이 하위 개념에 전달
* **다형성** : 유사 객체의 사용성을 그대로 유지

## 클래스

```py
class Counter:
    # 초기자 정의
    def __init__(self):
        self.count = 1
    
    # 메소드 정의
    def increase(self):
        self.count += 1
```

### 메소드 (method)

* 객체에 대한 행동(연산)을 정의
* 함수의 정의 및 사용 방법과 동일

### 초기자(initializer)

* 객체의 상태를 초기화하는 특수 메소드
* 항상 `__init` 으로 명명

### self 매개변수

* 모든 메소드의 첫번째 매개변수
* 메소드의 구현에 사용되지만 메소드 호출 시 사용되지않음
* 객체 자신을 참조하여 클래스 정의에 포함된 맴버에 접근시 사용

## 클래스 설계

UML 클래스 다이어그램을 통해 데이터필드, 생성자, 메소드 표현 방법 표준화

```
데이터 필드 이름: 데이터 필드 타입
클래스 이름(매개변수 이름: 매개변수 타입)
메소드 이름(매개변수 이름: 매개변수 타입): 반환값 타입
```

[![](https://mermaid.ink/img/pako:eNpNjzsLwzAMhP-K0ZRAhtJuhk7t2qmroYhYTgx-FFsulJD_XucBqRadPt1wN0EfNYGE3mHOd4tDQq-CCustbjGQmFQQdZIUNvCmxz-9eJqE2pYsruJ8Wl-dGMkOI1dy2Ui7uQfi1ye6phXGReQD5pLMQWfowFPyaHUNtyZQwCN5UiCr1GSwOFawWbFwfH5DD5JToQ7KWyPTXgekQZcrJW05psdeeFnzD0rpU5Y?type=png)](https://mermaid.live/edit#pako:eNpNjzsLwzAMhP-K0ZRAhtJuhk7t2qmroYhYTgx-FFsulJD_XucBqRadPt1wN0EfNYGE3mHOd4tDQq-CCustbjGQmFQQdZIUNvCmxz-9eJqE2pYsruJ8Wl-dGMkOI1dy2Ui7uQfi1ye6phXGReQD5pLMQWfowFPyaHUNtyZQwCN5UiCr1GSwOFawWbFwfH5DD5JToQ7KWyPTXgekQZcrJW05psdeeFnzD0rpU5Y)

```puml
classDiagram

class Cone {
    r: int
    h: int
    Cone(radius = 20: int, height = 30: int)
    get_vol() float
    get_surf() float
}
```

## 객체 지향의 활용

### 데이터타입과 객체 

원시 자료형 또한 객체이고 메서드를 지닌다.

파이썬은 내부적으로 원시 자료형을 객체로 감싸 메서드 호출이 가능하게 만든다.

```py
"I don't know python".replace("don't know", "love").upper()
```

### 데이터 필드 감추기

데이터 은닉(data hiding) : 데이터 필드의 직접 변경을 방지하기 위해 사용자의 직접적 접근을 차단

private 데이터 필드
* 클래스 내부에서만 접근 가능
* 앞 두 밑줄(__) 로 정의. `self.__h`

### 접근자와 변경자

* 접근자(accessor) : getter. 데이터 필드 반환
* 변경자(mutator) : setter. 데이터 필드 설정
