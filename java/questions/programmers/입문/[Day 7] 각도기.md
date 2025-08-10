## [:link:](https://school.programmers.co.kr/learn/courses/30/lessons/120829) 


### 문제 설명
각에서 0도 초과 90도 미만은 예각, 90도는 직각, 90도 초과 180도 미만은 둔각 180도는 평각으로 분류합니다. 각 `angle`이 매개변수로 주어질 때 예각일 때 1, 직각일 때 2, 둔각일 때 3, 평각일 때 4를 return하도록 solution 함수를 완성해주세요.
- 예각 : 0 < `angle` < 90
- 직각 : `angle` = 90
- 둔각 : 90 < `angle` < 180
- 평각 : `angle` = 180
#### 제한사항
- 0 < `angle` ≤ 180
- `angle`은 정수입니다.
&nbsp;
```java
class Solution {
    public int solution(int angle) {
        
        if (angle < 90){
            return 1;
        } else if (angle == 90){
            return 2;
        } else if (angle == 180){
            return 4;
        } else {
            return 3;
        }
    }
}
```
### 테스트 결과

|정확성  테스트|
|--|
테스트 1 〉	통과 (0.01ms, 76.1MB)
테스트 2 〉	통과 (0.01ms, 74.9MB)
테스트 3 〉	통과 (0.03ms, 71.7MB)
테스트 4 〉	통과 (0.02ms, 87.5MB)
테스트 5 〉	통과 (0.01ms, 78.5MB)
테스트 6 〉	통과 (0.01ms, 92MB)
테스트 7 〉	통과 (0.02ms, 88MB)
테스트 8 〉	통과 (0.01ms, 86.1MB)

정확성: 100.0   
합계: 100.0 / 100.0

---

#### 입출력 예
|numbers|	result|
|--|--|
|[1, 2, 3, 4, 5]|[2, 4, 6, 8, 10]|
|[1, 2, 100, -99, 1, 2, 3]|	[2, 4, 200, -198, 2, 4, 6]|

angle|result
--|--
70|1
91|3
180|4

#### 입출력 예 설명
##### 입출력 예 #1
- `angle`이 70이므로 예각입니다. 따라서 1을 return합니다.
##### 입출력 예 #2
- `angle`이 91이므로 둔각입니다. 따라서 3을 return합니다.
##### 입출력 예 #2
- `angle`이 180이므로 평각입니다. 따라서 4를 return합니다
