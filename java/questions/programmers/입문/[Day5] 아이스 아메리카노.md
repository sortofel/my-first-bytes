## [:link:](https://school.programmers.co.kr/learn/courses/30/lessons/120819)


### 문제 설명
머쓱이는 추운 날에도 아이스 아메리카노만 마십니다. 아이스 아메리카노는 한잔에 5,500원입니다. 머쓱이가 가지고 있는 돈 `money`가 매개변수로 주어질 때, 머쓱이가 최대로 마실 수 있는 아메리카노의 잔 수와 남는 돈을 순서대로 담은 배열을 return 하도록 solution 함수를 완성해보세요.
#### 제한사항
- 0 < `money` ≤ 1,000,000
&nbsp;
```java
class Solution {
    public int[] solution(int money) {
        
        int i = money / 5500;
        int j = money - (5500 * i);
        
        int[] arr = {i, j};
        
        return arr;
    }
}
```
### 테스트 결과

|정확성  테스트|
|--|
테스트 1 〉	통과 (0.01ms, 81.8MB)
테스트 2 〉	통과 (0.02ms, 80.3MB)
테스트 3 〉	통과 (0.01ms, 82.2MB)
테스트 4 〉	통과 (0.02ms, 88.9MB)
테스트 5 〉	통과 (0.01ms, 73.3MB)

정확성: 100.0   
합계: 100.0 / 100.0

---

#### 입출력 예
money|result
:--|:--
5,500|[1, 0]
15,000|[2, 4000]

#### 입출력 예 설명
##### 입출력 예 #1
- 5,500원은 아이스 아메리카노 한 잔을 살 수 있고 잔돈은 0원입니다.
##### 입출력 예 #2
- 15,000원은 아이스 아메리카노 두 잔을 살 수 있고 잔돈은 4,000원입니다.
