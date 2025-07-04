## [:link:](https://school.programmers.co.kr/learn/courses/30/lessons/120815) 


### 문제 설명
머쓱이네 피자가게는 피자를 여섯 조각으로 잘라 줍니다. 피자를 나눠먹을 사람의 수 n이 매개변수로 주어질 때, `n`명이 주문한 피자를 남기지 않고 모두 같은 수의 피자 조각을 먹어야 한다면 최소 몇 판을 시켜야 하는지를 return 하도록 solution 함수를 완성해보세요.
#### 제한사항
- 1 ≤ `n` ≤ 100
&nbsp;
```java
    class Solution {
        public int solution(int n) {
            int i;
            for (i = 1; (i * 6) % n != 0; i++);
            return i;
        }
    }
```
### 테스트 결과

|정확성  테스트|
|--|
테스트 1 〉	통과 (0.02ms, 72.4MB)
테스트 2 〉	통과 (0.01ms, 88MB)
테스트 3 〉	통과 (0.01ms, 71.1MB)
테스트 4 〉	통과 (0.02ms, 80.3MB)
테스트 5 〉	통과 (0.02ms, 75MB)
테스트 6 〉	통과 (0.01ms, 82.2MB)
테스트 7 〉	통과 (0.02ms, 75.1MB)
테스트 8 〉	통과 (0.01ms, 73.8MB)
테스트 9 〉	통과 (0.02ms, 80.1MB)
테스트 10 〉	통과 (0.01ms, 82.9MB)
테스트 11 〉	통과 (0.01ms, 73.2MB)
테스트 12 〉	통과 (0.01ms, 89.6MB)
테스트 13 〉	통과 (0.02ms, 68.9MB)

정확성: 100.0   
합계: 100.0 / 100.0

---

#### 입출력 예
|n|	result|
|--|--|
|6|1|
|10|5|
|4|2|

#### 입출력 예 설명
##### 입출력 예 #1
- 6명이 모두 같은 양을 먹기 위해 한 판을 시켜야 피자가 6조각으로 모두 한 조각씩 먹을 수 있습니다.
##### 입출력 예 #2
- 10명이 모두 같은 양을 먹기 위해 최소 5판을 시켜야 피자가 30조각으로 모두 세 조각씩 먹을 수 있습니다.
##### 입출력 예 #3
- 4명이 모두 같은 양을 먹기 위해 최소 2판을 시키면 피자가 12조각으로 모두 세 조각씩 먹을 수 있습니다.
