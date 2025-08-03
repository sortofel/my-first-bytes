## [:link:](https://school.programmers.co.kr/learn/courses/30/lessons/120825?language=java)

### 문제 설명
문자열 `my_string`과 정수 `n`이 매개변수로 주어질 때, `my_string`에 들어있는 각 문자를 `n`만큼 반복한 문자열을 return 하도록 solution 함수를 완성해보세요.

#### 제한사항
- 2 ≤ `my_string` 길이 ≤ 5
- 2 ≤ `n` ≤ 10
- "my_string"은 영어 대소문자로 이루어져 있습니다. 
&nbsp;

```java
class Solution {
    public String solution(String my_string, int n) {
        StringBuilder sb = new StringBuilder();

        for (int i = 0; i < my_string.length(); i++) {
            char ch = my_string.charAt(i); 
            for (int j = 0; j < n; j++) {
                sb.append(ch); 
            }
        }

        return sb.toString();
    }
}
```

### 테스트 결과

|정확성 테스트|  
|--|  
테스트 2 〉	통과 (0.03ms, 79.9MB)
테스트 3 〉	통과 (0.03ms, 74.2MB)
테스트 4 〉	통과 (0.03ms, 86MB) 

정확성: 100.0  
합계: 100.0 / 100.0

---

#### 입출력 예

|num_list|result|
|--|--|
|my_strin|n|result|
|:--|:--|:--|
|"hello"|3|"hhheeellllllooo"|

#### 입출력 예 설명

##### 입출력 예 #1
- "hello"의 각 문자를 세 번씩 반복한 "hhheeellllllooo"를 return 합니다.
