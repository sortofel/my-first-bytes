## [:link:](https://school.programmers.co.kr/learn/courses/30/lessons/120817)


### 문제 설명
정수 배열 `numbers`가 매개변수로 주어집니다. `numbers`의 원소의 평균값을 return하도록 solution 함수를 완성해주세요.
#### 제한사항
- 0 ≤ `numbers`의 원소 ≤ 1,000
- 1 ≤ `numbers`의 길이 ≤ 100
- 정답의 소수 부분이 .0 또는 .5인 경우만 입력으로 주어집니다.
&nbsp;
```java
    class Solution {
        public double solution(int[] numbers) {

            double answer = 0;

            for (int i= 0; i < numbers.length; i++) {
                answer += numbers[i];
            }

            return answer / numbers.length;
        }
    }
```
### 테스트 결과

|정확성  테스트|
|--|
테스트 1 〉	통과 (0.03ms, 84.2MB)
테스트 2 〉	통과 (0.03ms, 91.4MB)
테스트 3 〉	통과 (0.03ms, 75.1MB)
테스트 4 〉	통과 (0.02ms, 87.7MB)
테스트 5 〉	통과 (0.03ms, 71.6MB)

정확성: 100.0   
합계: 100.0 / 100.0

---

#### 입출력 예
numbers|result
:--|:--
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]|5.5
[89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99]|94.0

#### 입출력 예 설명
##### 입출력 예 #1
- numbers의 원소들의 평균 값은 5.5입니다.
##### 입출력 예 #2
- numbers의 원소들의 평균 값은 94.0입니다.
