# Dart-language
flutter 다트 문법 정리

## 기본 문법

### 주석
```
주석을 코드에 달아두는 방법은 총 3가지 
// : 한 줄 주석
/*  ... */ : 여러 줄 주석
/// : 문서 주석
```

### 문장
```
void main() {
  print("Hello"); // 문장의 끝은 세미콜론(;)으로 표시
}
```

### 변수
```
기본 타입을 제공
int : 정수
double : 실수(소수점)
String : 문자열
bool : 참/거짓

String name; // 변수 선언
name = "홍길동"; // 값 할당

bool 타입은 값으로 true와 false를 갖습니다.

bool b = true;
bool b2 = i < 10; 
bool b3 = s.isEmpty; 

int와 double은 num타입에 포함

num a = 10;
num b = 20.0; 

큰 자료형에 작은 타입을 대입하는 자동 형변환은 지원하지 않습니다.

변수 값 재할당은 언제든지 값을 다른 값으로 변환할 수 있습니다.

String s = 'hello';
s = 'world'; // world로 재할당
```

### 타입 추론
```
다트는 타입을 직접 명시하지 않고 var로 대체할 수 있는 타입 추론을 지원

var i = 10; // int 타입
var d = 10.0 // double 타입
var s = 'hello'; // 문자열 타입
var b = true; // 불리언 타입
```

### 상수 final, const
```
선언할 때 final 키워드를 제일 앞에 붙이면 값이 수정되지 않는 상수

final String name = "홍길동";
name = '임꺽정'; // 에러

final name = "홍길동"; 타입을 생략하고 짧게 작성할 수도 있습니다.
```

### 산술 연산자
```
+ : 더하기
- : 빼기
* : 곱하기
/ : 나누기 (double 타입 반환)
~/ : 몫 (int 타입 반환)
% : 나머지 (int 타입 반환)

assert() 함수는 계산 결과가 참인지 검사

더하기 연산자는 문자열 두 개를 결합할 때에도 사용
```

### 증감 연산자
```
후위 연산 : a++, a--
전위 연산 : ++a, --a
```

### 비교 연산자
```
== : 같다
!= : 다르다
> :  더 크다
< : 더 작다
>= : 크거나 같다
<= : 작거나 같다
```

### 논리 연산자
```
&& : 그리고 
|| : 또는
== : 같다
! : 부정
!= : 다르다
```

### 타입 검사(is, is! 키워드)
```
타입을 검사하는 키워드 
is : 같은 타입이면 true
is! : 다른 타입이면 true

int a = 10;
if(a is int) {
  print('정수');
} // 결과는 true
```

## 형변환(as 키워드)
```
int 와 double은 num을 구현하는 타입이지만 서로는 관계가 없기에 형변환 불가능
var c = 30.5; // double
int d = c as int; // int로 변환 x

num으로는 형변환 가능
dynamic d = 30.5;
num n = d; // as num; 생략 가능
```

