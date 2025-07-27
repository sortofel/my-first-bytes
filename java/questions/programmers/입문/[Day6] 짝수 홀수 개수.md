## [:link:](https://school.programmers.co.kr/learn/courses/30/lessons/120824?language=java)


### 문제 설명
정수가 담긴 리스트 `num_list`가 주어질 때, `num_list`의 원소 중 짝수와 홀수의 개수를 담은 배열을 return 하도록 solution 함수를 완성해보세요.
#### 제한사항
- 1 ≤ `num_list`의 길이 ≤ 100
- 0 ≤ `num_list`의 원소 ≤ 1,000
&nbsp;
```java
class Solution {
    public int[] solution(int[] num_list) {
        int i = 0;
        int j = 0;

        for (int num : num_list) {
            if (num % 2 == 0) {
                i++;
            } else {
                j++;
            }
        }

        return new int[] {i, j};
    }
}
```
### 테스트 결과

|정확성  테스트|
|--|
테스트 1 〉	통과 (0.02ms, 77.7MB)
테스트 2 〉	통과 (0.01ms, 82.2MB)
테스트 3 〉	통과 (0.01ms, 77.4MB)
테스트 4 〉	통과 (0.02ms, 85.4MB)
테스트 5 〉	통과 (0.01ms, 78.5MB)

정확성: 100.0   
합계: 100.0 / 100.0

---

#### 입출력 예
num_list|result
:--|:--
[1, 2, 3, 4, 5]|[2, 3]
[1, 3, 5, 7]|[0, 4]

#### 입출력 예 설명
##### 입출력 예 #1
- [1, 2, 3, 4, 5]에는 짝수가 2, 4로 두 개, 홀수가 1, 3, 5로 세 개 있습니다.
##### 입출력 예 #2
- [1, 3, 5, 7]에는 짝수가 없고 홀수가 네 개 있습니다.