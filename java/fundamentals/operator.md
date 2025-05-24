# Java 연산자(Operator)
### :link:
- [연산자 종류](#1-연산자-종류)
- [연산자 우선순위](#2-연산자-우선순위)
- [복합 대입 연산자](#3-복합-대입-연산자-compound-assignment-operators)
- [활용 예시](#4-활용-예시)
 
&nbsp;
## 1. 연산자 종류

### 단항 연산자 (Unary Operators)
| 연산자 | 설명 | 결합 규칙 | 우선순위 | 예시 |
|--------|------|-----------|----------|------|
| `++` | 전위/후위 증가 | ← | 1 | `++i`, `i++` |
| `--` | 전위/후위 감소 | ← | 1 | `--i`, `i--` |
| `+` | 양수 (단항 플러스) | ← | 1 | `+5` |
| `-` | 음수 (단항 마이너스) | ← | 1 | `-10` |
| `!` | 논리 NOT | ← | 1 | `!true` |
| `~` | 비트 NOT | ← | 1 | `~5` |

```java
int i = 5;
System.out.println(++i);  // 6 (전위: 먼저 증가 후 사용)
System.out.println(i++);  // 6 (후위: 먼저 사용 후 증가)
System.out.println(i);    // 7

boolean flag = true;
System.out.println(!flag); // false
```

### 산술 연산자 (Arithmetic Operators)
| 연산자 | 설명 | 결합 규칙 | 우선순위 | 예시 |
|--------|------|-----------|----------|------|
| `*` | 곱셈 | → | 2 | `5 * 3` |
| `/` | 나눗셈 | → | 2 | `10 / 2` |
| `%` | 나머지 | → | 2 | `7 % 3` |
| `+` | 덧셈 | → | 3 | `5 + 3` |
| `-` | 뺄셈 | → | 3 | `10 - 4` |

```java
int a = 10, b = 3;
System.out.println(a * b);  // 30
System.out.println(a / b);  // 3
System.out.println(a % b);  // 1
System.out.println(a + b);  // 13
System.out.println(a - b);  // 7
```

### 시프트 연산자 (Shift Operators)
| 연산자 | 설명 | 결합 규칙 | 우선순위 | 예시 |
|--------|------|-----------|----------|------|
| `<<` | 왼쪽 시프트 | → | 4 | `8 << 2` |
| `>>` | 오른쪽 시프트 (부호 유지) | → | 4 | `16 >> 2` |
| `>>>` | 오른쪽 시프트 (부호 무시) | → | 4 | `-8 >>> 2` |

```java
int x = 8;
System.out.println(x << 2);  // 32 (8 * 2^2)
System.out.println(x >> 2);  // 2  (8 / 2^2)
```

### 비교 연산자 (Relational Operators)
| 연산자 | 설명 | 결합 규칙 | 우선순위 | 예시 |
|--------|------|-----------|----------|------|
| `<` | 미만 | → | 5 | `5 < 10` |
| `<=` | 이하 | → | 5 | `5 <= 5` |
| `>` | 초과 | → | 5 | `10 > 5` |
| `>=` | 이상 | → | 5 | `10 >= 10` |
| `instanceof` | 인스턴스 확인 | → | 5 | `obj instanceof String` |

```java
int x = 10, y = 20;
System.out.println(x < y);   // true
System.out.println(x >= 10); // true

String str = "Hello";
System.out.println(str instanceof String); // true
```

### 등가 연산자 (Equality Operators)
| 연산자 | 설명 | 결합 규칙 | 우선순위 | 예시 |
|--------|------|-----------|----------|------|
| `==` | 동등 비교 | → | 6 | `5 == 5` |
| `!=` | 부등 비교 | → | 6 | `5 != 3` |

```java
int a = 5, b = 5;
System.out.println(a == b);  // true
System.out.println(a != 3);  // true

String s1 = new String("Hello");
String s2 = new String("Hello");
System.out.println(s1 == s2);        // false (참조 비교)
System.out.println(s1.equals(s2));   // true (내용 비교)
```

### 비트 연산자 (Bitwise Operators)
| 연산자 | 설명 | 결합 규칙 | 우선순위 | 예시 |
|--------|------|-----------|----------|------|
| `&` | 비트 AND | → | 7 | `5 & 3` |
| `^` | 비트 XOR | → | 8 | `5 ^ 3` |
| `\|` | 비트 OR | → | 9 | `5 \| 3` |

```java
int a = 5;  // 101 (2진수)
int b = 3;  // 011 (2진수)
System.out.println(a & b);  // 1 (001)
System.out.println(a ^ b);  // 6 (110)
System.out.println(a | b);  // 7 (111)
```

### 논리 연산자 (Logical Operators)
| 연산자 | 설명 | 결합 규칙 | 우선순위 | 예시 |
|--------|------|-----------|----------|------|
| `&&` | 논리 AND (단축 평가) | → | 10 | `true && false` |
| `\|\|` | 논리 OR (단축 평가) | → | 11 | `true \|\| false` |

```java
boolean x = true, y = false;
System.out.println(x && y);  // false
System.out.println(x || y);  // true

// 단축 평가
int i = 0;
if (i != 0 && 10/i > 2) {
    System.out.println("실행되지 않음");
}
```

### 삼항 연산자 (Ternary Operator)
| 연산자 | 설명 | 결합 규칙 | 우선순위 | 예시 |
|--------|------|-----------|----------|------|
| `? :` | 조건 연산자 | ← | 12 | `조건 ? 값1 : 값2` |

```java
int a = 10, b = 20;
int max = (a > b) ? a : b;  // 20
System.out.println("최댓값: " + max);

String result = (a % 2 == 0) ? "짝수" : "홀수";
System.out.println(a + "는 " + result);  // 10는 짝수
```

### 대입 연산자 (Assignment Operators)
| 연산자 | 설명 | 결합 규칙 | 우선순위 | 예시 |
|--------|------|-----------|----------|------|
| `=` | 단순 대입 | ← | 13 | `x = 5` |

```java
int x = 10;
int y = x = 5;  // x = 5, y = 5
System.out.println("x: " + x + ", y: " + y);
```
 
&nbsp;
## 2. 연산자 우선순위

### 기본 우선순위 원칙
1. **산술 > 비교 > 논리 > 대입** (대입은 항상 마지막)
2. **단항(1개) > 이항(2개) > 삼항(3개)** 순서
3. 대입 연산자를 제외하고 **왼쪽에서 오른쪽**으로 진행

### 우선순위 예시
```java
int result = 5 + 3 * 2 > 8 && true;
// 3 * 2 = 6      
// 5 + 6 = 11     
// 11 > 8 = true  
// true && true = true 
// result = true 

int a = 2, b = 3, c = 4;
int x = a + b * c++;
// c++ → c; 4 사용 후 5로 증가
// b * 4 = 12
// a + 12 = 14
// x = 14
```
 
&nbsp;
## 3. 복합 대입 연산자 (Compound Assignment Operators)

### 산술 복합 대입 연산자
| op= | 동등한 표현 | 예시 |
|-----|-------------|------|
| `+=` | `i = i + 3` | `i += 3` |
| `-=` | `i = i - 3` | `i -= 3` |
| `*=` | `i = i * 3` | `i *= 3` |
| `/=` | `i = i / 3` | `i /= 3` |
| `%=` | `i = i % 3` | `i %= 3` |

```java
int num = 10;
num += 5;   // num = num + 5;  → 15
num -= 3;   // num = num - 3;  → 12
num *= 2;   // num = num * 2;  → 24
num /= 4;   // num = num / 4;  → 6
num %= 5;   // num = num % 5;  → 1
```

### 비트 복합 대입 연산자
| op= | 동등한 표현 | 예시 |
|-----|-------------|------|
| `&=` | `i = i & 3` | `i &= 3` |
| `\|=` | `i = i \| 3` | `i \|= 3` |
| `^=` | `i = i ^ 3` | `i ^= 3` |

```java
int bits = 12;  // 1100 (2진수)
bits &= 10;     // bits = bits & 10;  → 8 (1000)
bits |= 5;      // bits = bits | 5;   → 13 (1101)
bits ^= 7;      // bits = bits ^ 7;   → 10 (1010)
```

### 시프트 복합 대입 연산자
| op= | 동등한 표현 | 예시 |
|-----|-------------|------|
| `<<=` | `i = i << 2` | `i <<= 2` |
| `>>=` | `i = i >> 2` | `i >>= 2` |
| `>>>=` | `i = i >>> 2` | `i >>>= 2` |

```java
int value = 16;
value <<= 2;    // value = value << 2;  → 64
value >>= 3;    // value = value >> 3;  → 8
value >>>= 1;   // value = value >>> 1; → 4
```
 
&nbsp;
## 4. 활용 예시
```java
int a = 5, b = 10, c = 15;
boolean result = ++a * 2 > b + c / 3 && a != 6;

// 1. ++a → a = 6
// 2. 6 * 2 = 12
// 3. c / 3 = 15 / 3 = 5
// 4. b + 5 = 10 + 5 = 15
// 5. 12 > 15 = false
// 6. a != 6 → 6 != 6 = false
// 7. false && false = false
```
```java
int count = 0;
count += 1;  // count++

// 누적 합계
int sum = 0;
int[] numbers = {1, 2, 3, 4, 5};
for (int num : numbers) {
    sum += num;  // sum = sum + num
}

int flags = 0;
flags |= 0b0001;
flags |= 0b0100;
flags &= ~0b0001;
```
