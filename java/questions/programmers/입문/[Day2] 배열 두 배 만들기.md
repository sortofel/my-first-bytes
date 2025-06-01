## [:link:](https://school.programmers.co.kr/learn/courses/30/lessons/120809) 


### 문제 설명
정수 배열 `numbers`가 매개변수로 주어집니다. `numbers`의 각 원소에 두배한 원소를 가진 배열을 return하도록 solution 함수를 완성해주세요.
#### 제한사항
- -10,000 ≤ `numbers`의 원소 ≤ 10,000
- 1 ≤ `numbers`의 길이 ≤ 1,000
&nbsp;
```java
class Solution {
    public int[] solution(int[] numbers) {
        int[] answer = new int[numbers.length];
        
        for(int i=0; i<numbers.length; i++) {
            answer[i] = numbers[i]*2;
        }
        
        return answer;
    }
}
```
### 테스트 결과

|정확성  테스트|
|--|
테스트 1 〉	통과 (0.02ms, 80.4MB)
테스트 2 〉	통과 (0.01ms, 84.2MB)
테스트 3 〉	통과 (0.02ms, 78.2MB)
테스트 4 〉	통과 (0.01ms, 79.7MB)
테스트 5 〉	통과 (0.02ms, 87.8MB)
테스트 6 〉	통과 (0.05ms, 94.6MB)
테스트 7 〉	통과 (0.03ms, 74.2MB)
테스트 8 〉	통과 (0.03ms, 90MB)
테스트 9 〉	통과 (0.02ms, 90MB)
테스트 10 〉	통과 (0.02ms, 88.3MB)

정확성: 100.0   
합계: 100.0 / 100.0

---

#### 입출력 예
|numbers|	result|
|--|--|
|[1, 2, 3, 4, 5]|[2, 4, 6, 8, 10]|
|[1, 2, 100, -99, 1, 2, 3]|	[2, 4, 200, -198, 2, 4, 6]|

#### 입출력 예 설명
##### 입출력 예 #1
- [1, 2, 3, 4, 5]의 각 원소에 두배를 한 배열 [2, 4, 6, 8, 10]을 return합니다.
##### 입출력 예 #2
- [1, 2, 100, -99, 1, 2, 3]의 각 원소에 두배를 한 배열 [2, 4, 200, -198, 2, 4, 6]을 return합니다.

