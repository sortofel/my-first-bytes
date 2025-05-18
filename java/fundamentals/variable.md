# Java 변수(Variable)

### :link:
- [변수의 정의](#변수의-정의)
- [데이터의 종류](#데이터의-종류)
- [변수, 상수, 리터럴의 차이](#변수-상수-리터럴의-차이)
- [기본형 데이터 타입](#기본형primitive-type-데이터-타입)
- [인코딩과 디코딩](#인코딩encoding과-디코딩decoding)
- [오버플로우와 언더플로우](#오버플로우overflow와-언더플로우underflow)
- [데이터 타입 캐스팅](#데이터-타입-캐스팅type-casting)
- [예제](#예제)
- [정리](#정리)
 
&nbsp;
## 변수의 정의
- 단 하나의 값만을 저장할 수 있는 메모리 공간
- 프로그램이 실행되는 동안 값이 변경될 수 있음 = 데이터를 저장하고 참조하기 위한 이름이 붙은 메모리 공간

```java
int age = 25;  // 'age'라는 이름의 변수에 25라는 값을 저장
age = 26;      // 변수의 값은 변경 가능
```

## 데이터의 종류
1. **기본형(Primitive Type)**: 실제 값을 저장
2. **참조형(Reference Type)**: 객체의 주소를 저장

### 참조형(Reference Type)이란?
- 기본형을 제외한 모든 타입(클래스, 인터페이스, 배열 등)
- 실제 데이터가 아닌 객체의 메모리 주소(참조값)를 저장
- 객체 type에 따라 종류 구분

```java
String name = "Damon";  // String은 참조형 데이터 타입
```

- String의 연산: any type + String   
             -> any type => String 변환 후 문자열 합치기 수행
```java
String name = "Albarn" + 7; //7-> "7" 자동 변환
name = Albarn7;
```

## 변수, 상수, 리터럴의 차이

### 변수(Variable)
- 하나의 값을 저장하기 위한 메모리 공간
- 프로그램 실행 중에 값이 변경될 수 있음

```java
int count = 10;
count = 20;  // 값 변경 가능
```

### 상수(Constant)
- 값을 한 번만 저장할 수 있는 메모리 공간
- 프로그램 실행 중에 값을 변경할 수 없음
- Java에서는 `final` 키워드를 사용하여 상수 선언

```java
final double PI = 3.14159;
// PI = 3.14;  // 오류 발생: 상수는 값 변경 불가
```

### 리터럴(Literal)
- 소스 코드에서 고정된 값을 표현하는 방식 (기존의 상수)
- 변수나 상수에 저장되는 실제 데이터 값

```java
int a = 10;       // 10은 정수 리터럴
double b = 3.14;  // 3.14는 실수 리터럴
char c = 'A';     // 'A'는 문자 리터럴
String d = "Hello";  // "Hello"는 문자열 리터럴
```

## 기본형(Primitive Type) 데이터 타입

### 기본형 타입별 저장 범위 및 크기

| 데이터 타입 | 크기 | 범위 | 기본값 |
|------------|------|------|--------|
| boolean | 1 byte | true 또는 false | false |
| char | 2 bytes | '\u0000' ~ '\uffff' (0 ~ 65,535) | '\u0000' |
| byte | 1 byte | -128 ~ 127 | 0 |
| short | 2 bytes | -32,768 ~ 32,767 | 0 |
| int | 4 bytes | -2,147,483,648 ~ 2,147,483,647 | 0 |
| long(L) | 8 bytes | -9,223,372,036,854,775,808 ~ 9,223,372,036,854,775,807 | 0L |
| float(F) | 4 bytes | 약 ±3.4E+38 (소수점 6-7자리) | 0.0f |
| double | 8 bytes | 약 ±1.8E+308 (소수점 15-16자리) | 0.0d |

- float과 double은 정밀도의 차이   
  float - 7자리, double - 15자리

## 인코딩(Encoding)과 디코딩(Decoding)

### 인코딩(Encoding)
- 문자나 기호를 컴퓨터가 이해할 수 있는 다른 형태(주로 이진수)로 변환하는 과정
- 예: 문자 'A'를 ASCII 코드 값인 65로 변환

### 디코딩(Decoding)
- 인코딩의 반대 과정
- 컴퓨터가 이해하는 형태(이진수 등)를 사람이 이해할 수 있는 문자나 기호로 변환하는 과정
- 예: ASCII 코드 값 65를 문자 'A'로 변환

### char형과 정수형 사이의 인코딩과 디코딩
Java에서 char 타입은 유니코드 문자를 저장합니다. 각 문자는 고유한 숫자 코드를 가지고 있습니다.

```java
char letter = 'A';
int asciiValue = letter;  // 문자 'A'를 정수로 변환 (인코딩) - 65가 됨

int code = 66;
char character = (char) code;  // 정수 66을 문자로 변환 (디코딩) - 'B'가 됨

System.out.println("'A'의 ASCII 값: " + asciiValue);  // 'A'의 ASCII 값: 65
System.out.println("ASCII 값 66의 문자: " + character);  // ASCII 값 66의 문자: B

// 문자와 숫자 간의 연산
char ch = 'A';
System.out.println(ch + 1);  // 66 (A의 코드값 65 + 1)
System.out.println((char)(ch + 1));  // B (65+1=66을 문자로 변환)
```

## 오버플로우(Overflow)와 언더플로우(Underflow)

### 오버플로우(Overflow)
- 특정 데이터 타입이 표현할 수 있는 최대값보다 큰 값을 저장하려고 할 때 발생
- 이 경우, 변수는 해당 타입의 최소값부터 다시 시작

```java
byte smallNumber = 127;  // byte의 최대값
smallNumber++;  // 오버플로우 발생
System.out.println(smallNumber);  // -128 (최소값으로 돌아감)
```

### 언더플로우(Underflow)
- 데이터 타입이 표현할 수 있는 최소값보다 작은 값을 저장하려고 할 때 발생
- 이 경우, 변수는 해당 타입의 최대값으로 돌아감

```java
byte anotherNumber = -128;  // byte의 최소값
anotherNumber--;  // 언더플로우 발생
System.out.println(anotherNumber);  // 127 (최대값으로 돌아감)
```

## 데이터 타입 캐스팅(Type Casting)

- 하나의 데이터 타입을 다른 데이터 타입으로 변환하는 과정   
  (타입) 피연산자;

### 1. 자동 형변환(Promotion, 묵시적 형변환)
- 작은 데이터 타입에서 큰 데이터 타입으로 변환하는 경우
- 자동으로 형변환이 이루어짐
- 데이터 손실의 위험이 없어 명시적 캐스팅 선언 불필요

데이터 타입 크기 순서: `byte < short < int < long < float < double`

```java
byte byteValue = 10;
int intValue = byteValue;  // 자동 형변환 (byte → int)
long longValue = intValue;  // 자동 형변환 (int → long)
float floatValue = longValue;  // 자동 형변환 (long → float)
double doubleValue = floatValue;  // 자동 형변환 (float → double)

System.out.println("byteValue: " + byteValue);    // 10
System.out.println("intValue: " + intValue);      // 10
System.out.println("longValue: " + longValue);    // 10
System.out.println("floatValue: " + floatValue);  // 10.0
System.out.println("doubleValue: " + doubleValue); // 10.0
```

### 2. 강제 형변환(Casting, 명시적 형변환)
- 큰 데이터 타입에서 작은 데이터 타입으로 변환하는 경우
- 명시적으로 캐스팅을 선언해야 함
- 데이터 손실의 위험이 있음

```java
double doubleNum = 10.5;
int intNum = (int) doubleNum;  // 강제 형변환 (double → int)
System.out.println("doubleNum: " + doubleNum);  // 10.5
System.out.println("intNum: " + intNum);        // 10 (소수점 이하 손실)

long longNumber = 100L;
byte byteNumber = (byte) longNumber;  // 강제 형변환 (long → byte)
System.out.println("byteNumber: " + byteNumber);  // 100

// 범위를 벗어나는 경우
int largeValue = 130;
byte smallByte = (byte) largeValue;  // 강제 형변환 (int → byte)
System.out.println("smallByte: " + smallByte);  // -126 (오버플로우 발생)
```

- 형변환 시 피연산자의 실제 값은 변하지 않음. 변환된 값은 임시적으로만 사용됨
- boolean을 제외한 모든 기본형 타입 간 형변환 가능
- 기본형과 참조형 사이 형변환 불가능
- int -> float 형변환은 2진수와 정밀도 관계로 오류 발생할 수 있음  
int -> double 권장

```java
// 기본형과 참조형 간 형변환 불가능 예시
int number = 10;
// String str = (String) number;  // 컴파일 오류: 기본형과 참조형 간 직접 변환 불가

// 대신 다음과 같이 변환 가능
String str = String.valueOf(number);  // int → String
int num = Integer.parseInt("20");     // String → int
```

## 예제

```java
public class TypeCastingExample {
    public static void main(String[] args) {
        // 기본적인 변수 선언과 초기화
        int intValue = 100;
        long longValue = 200L;
        float floatValue = 3.14f;
        double doubleValue = 5.678;
        char charValue = 'A';
        
        // 자동 형변환 예시
        System.out.println("=== 자동 형변환 ===");
        long convertedLong = intValue;  // int → long
        System.out.println("int " + intValue + " → long: " + convertedLong);
        
        double convertedDouble = floatValue;  // float → double
        System.out.println("float " + floatValue + " → double: " + convertedDouble);
        
        int charToInt = charValue;  // char → int (ASCII 값으로 변환)
        System.out.println("char '" + charValue + "' → int: " + charToInt);
        
        // 명시적 형변환 예시
        System.out.println("\n=== 명시적 형변환 ===");
        int doubleToInt = (int) doubleValue;  // double → int
        System.out.println("double " + doubleValue + " → int: " + doubleToInt + " (소수점 이하 손실)");
        
        byte longToByte = (byte) longValue;  // long → byte
        System.out.println("long " + longValue + " → byte: " + longToByte);
        
        char intToChar = (char) 66;  // int → char
        System.out.println("int 66 → char: '" + intToChar + "'");
        
        // 오버플로우 예시
        System.out.println("\n=== 오버플로우 예시 ===");
        int largeValue = 130;
        byte smallByte = (byte) largeValue;
        System.out.println("int " + largeValue + " → byte: " + smallByte + " (오버플로우 발생)");
        
        // 계산 중 자동 형변환
        System.out.println("\n=== 계산에서의 형변환 ===");
        byte b1 = 10;
        byte b2 = 20;
        // byte sum = b1 + b2;  // 컴파일 오류: byte + byte는 int 결과 반환
        byte sum = (byte)(b1 + b2);  // 명시적 캐스팅 필요
        System.out.println("byte끼리의 연산 결과: " + sum);
        
        // 다양한 타입 연산 시 자동으로 큰 타입으로 변환
        int i = 100;
        long l = 200L;
        float f = 3.14f;
        double d = 4.56;
        
        long result1 = i + l;    // int + long → long
        float result2 = l + f;   // long + float → float
        double result3 = f + d;  // float + double → double
        
        System.out.println("int + long → long: " + result1);
        System.out.println("long + float → float: " + result2);
        System.out.println("float + double → double: " + result3);
    }
}
```

## 정리

1. **변수**: 단 하나의 값을 저장하는 메모리 공간
2. **데이터 타입**: 기본형과 참조형으로 나뉨
3. **기본형(Primitive Type)**: 실제 값을 저장
4. **참조형(Reference Type)**: 객체의 메모리 주소를 저장
5. **상수**: 한 번 초기화하면 값을 변경할 수 없는 변수 (`final` 키워드)
6. **리터럴**: 소스 코드에서 직접 표현되는 값
7. **오버플로우/언더플로우**: 데이터 타입의 최대값/최소값을 넘어설 때 발생
8. **형변환**: 자동 형변환(작은→큰)과 강제 형변환(큰→작은)으로 나뉨
9. `boolean`을 제외한 모든 기본형 타입 간에는 형변환이 가능
10. 기본형과 참조형 사이에는 직접적인 형변환이 불가능
