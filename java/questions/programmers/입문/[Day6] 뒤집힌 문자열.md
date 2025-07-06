## [:link:](https://school.programmers.co.kr/learn/courses/30/lessons/120822)


### 문제 설명
문자열 `my_string`이 매개변수로 주어집니다. `my_string`을 거꾸로 뒤집은 문자열을 return하도록 solution 함수를 완성해주세요.
#### 제한사항
- 1 ≤ `my_string`의 길이 ≤ 1,000
&nbsp;
```java
class Solution {
    public String solution(String my_string) {
        return new StringBuilder(my_string).reverse().toString();
    }
}
```
### 테스트 결과

|정확성  테스트|
|--|
테스트 1 〉	통과 (0.03ms, 85.5MB)
테스트 2 〉	통과 (0.03ms, 86MB)
테스트 3 〉	통과 (0.03ms, 69.7MB)
테스트 4 〉	통과 (0.04ms, 93.4MB)
테스트 5 〉	통과 (0.03ms, 88.4MB)

정확성: 100.0   
합계: 100.0 / 100.0

---

#### 입출력 예
my_string|return
:--|:--
"jaron"|"noraj"
"bread"|"daerb"

#### 입출력 예 설명
##### 입출력 예 #1
- `my_string`이 "jaron"이므로 거꾸로 뒤집은 "noraj"를 return합니다.
##### 입출력 예 #2
- `my_string`이 "bread"이므로 거꾸로 뒤집은 "daerb"를 return합니다.