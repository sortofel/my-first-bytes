## [:link:](https://school.programmers.co.kr/learn/courses/30/lessons/120812?language=java) 


### 문제 설명
최빈값은 주어진 값 중에서 가장 자주 나오는 값을 의미합니다. 정수 배열 `array`가 매개변수로 주어질 때, 최빈값을 return 하도록 solution 함수를 완성해보세요. 최빈값이 여러 개면 -1을 return 합니다.
#### 제한사항
- 0 < `array`의 길이 < 100
- 0 ≤ `array`의 원소 < 1000
&nbsp;
```java
import java.util.HashMap;

class Solution {
    public int solution(int[] array) {
        HashMap<Integer, Integer> map = new HashMap<>();
        
        for (int num : array) {
            map.put(num, map.getOrDefault(num, 0) + 1);
        }

        int maxCount = 0;
        int mode = -1;
        boolean isDuplicate = false;

        for (int key : map.keySet()) {
            int count = map.get(key);
            if (count > maxCount) {
                maxCount = count;
                mode = key;
                isDuplicate = false;
            } else if (count == maxCount) {
                isDuplicate = true;
            }
        }

        return isDuplicate ? -1 : mode;
    }
}
```
### 테스트 결과

|정확성  테스트|
|--|
테스트 1 〉	통과 (0.06ms, 72.1MB)
테스트 2 〉	통과 (0.35ms, 71.8MB)
테스트 3 〉	통과 (0.46ms, 82.9MB)
테스트 4 〉	통과 (0.10ms, 87.8MB)
테스트 5 〉	통과 (0.10ms, 70.1MB)
테스트 6 〉	통과 (0.09ms, 73MB)
테스트 7 〉	통과 (0.06ms, 83.9MB)
테스트 8 〉	통과 (0.17ms, 79.2MB)
테스트 9 〉	통과 (0.04ms, 73.7MB)
테스트 10 〉	통과 (0.05ms, 89.6MB)
테스트 11 〉	통과 (0.11ms, 82.4MB)
테스트 12 〉	통과 (0.29ms, 86.8MB)
테스트 13 〉	통과 (0.25ms, 78.7MB)
테스트 14 〉	통과 (0.26ms, 84MB)
테스트 15 〉	통과 (0.23ms, 68.9MB)
테스트 16 〉	통과 (0.16ms, 79.8MB)

정확성: 100.0   
합계: 100.0 / 100.0

---

#### 입출력 예
array|result
:--|:--
[1, 2, 3, 3, 3, 4]|3
[1, 1, 2, 2]|-1
[1]|1

#### 입출력 예 설명
##### 입출력 예 #1
- [1, 2, 3, 3, 3, 4]에서 1은 1개 2는 1개 3은 3개 4는 1개로 최빈값은 3입니다.
##### 입출력 예 #2
- [1, 1, 2, 2]에서 1은 2개 2는 2개로 최빈값이 1, 2입니다. 최빈값이 여러 개이므로 -1을 return 합니다.
##### 입출력 예 #3
[1]에는 1만 있으므로 최빈값은 1입니다.
