## [:link:](https://school.programmers.co.kr/learn/courses/30/lessons/120826?language=java)

### 문제 설명

문자열 `my_string`과 문자 `letter`이 매개변수로 주어집니다.
`my_string`에서 `letter`를 제거한 문자열을 return 하도록 `solution` 함수를 완성해주세요.

### 제한사항

* 1 ≤ `my_string`의 길이 ≤ 100
* `letter`은 길이가 1인 영문자입니다.
* `my_string`과 `letter`은 알파벳 대소문자로 이루어져 있습니다.
* 대문자와 소문자를 구분합니다.

```java
class Solution {
    public String solution(String my_string, String letter) {
        return my_string.replace(letter, "");
    }
}
```

### 테스트 결과

|정확성  테스트|
|--|
테스트 1 〉	통과 (0.02ms, 88.6MB)
테스트 2 〉	통과 (0.03ms, 75.6MB)
테스트 3 〉	통과 (0.03ms, 87.8MB)
테스트 4 〉	통과 (0.03ms, 78.7MB)
테스트 5 〉	통과 (0.03ms, 71.8MB)
테스트 6 〉	통과 (0.02ms, 70.9MB)
테스트 7 〉	통과 (0.02ms, 66.8MB)
테스트 8 〉	통과 (0.02ms, 84MB)
테스트 9 〉	통과 (0.04ms, 81.1MB)
테스트 10 〉	통과 (0.04ms, 85MB)
테스트 11 〉	통과 (0.02ms, 89.7MB)
테스트 12 〉	통과 (0.04ms, 77.1MB)
테스트 13 〉	통과 (0.04ms, 83.3MB)
테스트 14 〉	통과 (0.02ms, 74.9MB)
테스트 15 〉	통과 (0.03ms, 76.9MB)
테스트 16 〉	통과 (0.03ms, 73.2MB)
테스트 17 〉	통과 (0.04ms, 72.4MB)
테스트 18 〉	통과 (0.03ms, 82.2MB)
테스트 19 〉	통과 (0.04ms, 86.8MB)
테스트 20 〉	통과 (0.03ms, 72.2MB)

정확성: 100.0
합계: 100.0 / 100.0

---

#### 입출력 예

| my\_string | letter | result  |
| :--------- | :----- | :------ |
| "abcdef"   | "f"    | "abcde" |
| "BCBdbe"   | "B"    | "Cdbe"  |

#### 입출력 예 설명

##### 입출력 예 #1

* `"abcdef"`에서 `"f"`를 제거하면 `"abcde"`가 됩니다.

##### 입출력 예 #2

* `"BCBdbe"`에서 `"B"`를 모두 제거하면 `"Cdbe"`가 됩니다.