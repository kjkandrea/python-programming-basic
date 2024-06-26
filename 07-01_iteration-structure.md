# 반복 구조

## 반복 구조의 개념

특정 영역의 명령문을 여러 번 실행하는 구조

loop, iterate, repeat

`while`

## 리스트

순서화 된 값을 집합체를 저장할 수 잇는 데이터 타입
* 단일 식별자로 연속된 저장 공간 접근 수단 제공
* 개별 원소의 값을 수정, 추가, 삭제 가능
* 원소(element)의 나열을 저장할 수 있는 시퀀스 타입 중 하나
  * 리스트, 세트, 투플, 딕셔너리 등 

`list([1, 2, 3, "foo", "bar" ...]`

### 인덱스 연산자

시퀀스 타입의 원소에 접근하는 연산자

`foo_list[0]`

`for 계수-제어-변수 in 시퀀스:`

## 반복 구조의 확장

### 리스트 생성 자동화

리스트 내 원소에 규칙성이 있는 경우 생성 자동화를 위해 함수 사용 가능

`range(시작, 끝(작은값 까지), 증가단위)`

### 중첩 반복 구조

반복 구조 내 다른 반복구조를 내포한 형식

```py
for 계수-제어-변수 in 시퀀스:
    for 계수-제어-변수 in 시퀀스:
        명령 블록
```
