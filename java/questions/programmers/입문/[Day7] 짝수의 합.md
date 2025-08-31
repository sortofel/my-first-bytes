## [:link:](https://school.programmers.co.kr/learn/courses/30/lessons/120831)


### 문제 설명
정수 `n`이 주어질 때, `n`이하의 짝수를 모두 더한 값을 return 하도록 solution 함수를 작성해주세요.
#### 제한사항
0 < `n` ≤ 1000
&nbsp;
```java
class Solution {
    public int solution(int n) {
        int sum = 0;
        for (int i = 2; i <= n; i += 2) { 
            sum += i;
        }
        return sum;
    }
}
```
### 테스트 결과

|정확성  테스트|
|--|
테스트 1 〉	통과 (0.02ms, 82.3MB)
테스트 2 〉	통과 (0.01ms, 76MB)
테스트 3 〉	통과 (0.02ms, 80.1MB)
테스트 4 〉	통과 (0.02ms, 84.7MB)
테스트 5 〉	통과 (0.01ms, 77MB)
테스트 6 〉	통과 (0.02ms, 88.7MB)
테스트 7 〉	통과 (0.02ms, 84.1MB)

정확성: 100.0   
합계: 100.0 / 100.0

---

#### 입출력 예
n|result
:--|:--
10|30
4|6

#### 입출력 예 설명
##### 입출력 예 #1
- `n`이 10이므로 2 + 4 + 6 + 8 + 10 = 30을 return 합니다.
##### 입출력 예 #2
- `n`이 4이므로 2 + 4 = 6을 return 합니다.
