## [:link:](https://school.programmers.co.kr/learn/courses/30/lessons/120821)


### 문제 설명
정수가 들어 있는 배열 `num_list`가 매개변수로 주어집니다. `num_list`의 원소의 순서를 거꾸로 뒤집은 배열을 return하도록 solution 함수를 완성해주세요.
#### 제한사항
- 1 ≤ `num_list`의 길이 ≤ 1,000
- 0 ≤ `num_list`의 원소 ≤ 1,000
&nbsp;
```java
class Solution {
    public int[] solution(int[] num_list) {
        int len = num_list.length;
        int[] reversed = new int[len];

        for (int i = 0; i < len; i++) {
            reversed[i] = num_list[len - 1 - i];
        }

        return reversed;
    }
}
```
### 테스트 결과

|정확성  테스트|
|--|
테스트 1 〉	통과 (0.01ms, 77.5MB)
테스트 2 〉	통과 (0.02ms, 87.3MB)
테스트 3 〉	통과 (0.01ms, 84.1MB)
테스트 4 〉	통과 (0.01ms, 85.9MB)

정확성: 100.0   
합계: 100.0 / 100.0

---

#### 입출력 예
num_list|result
:--|:--
[1, 2, 3, 4, 5] | [5, 4, 3, 2, 1]
[1, 1, 1, 1, 1, 2] | [2, 1, 1, 1, 1, 1]
[1, 0, 1, 1, 1, 3, 5] | [5, 3, 1, 1, 1, 0, 1]

#### 입출력 예 설명
##### 입출력 예 #1
- `num_list`가 [1, 2, 3, 4, 5]이므로 순서를 거꾸로 뒤집은 배열 [5, 4, 3, 2, 1]을 return합니다.
##### 입출력 예 #2
- `num_list`가 [1, 1, 1, 1, 1, 2]이므로 순서를 거꾸로 뒤집은 배열 [2, 1, 1, 1, 1, 1]을 return합니다.
##### 입출력 예 #3
- `num_list`가 [1, 0, 1, 1, 1, 3, 5]이므로 순서를 거꾸로 뒤집은 배열 [5, 3, 1, 1, 1, 0, 1]을 return합니다.