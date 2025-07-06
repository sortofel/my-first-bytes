## [:link:](https://school.programmers.co.kr/learn/courses/30/lessons/120823)

### 문제 설명
`*`의 높이와 너비를 1이라고 했을 때, `*`을 이용해 직각 이등변 삼각형을 그리려고합니다. 정수 `n` 이 주어지면 높이와 너비가 `n` 인 직각 이등변 삼각형을 출력하도록 코드를 작성해보세요.
#### 제한사항
- 1 ≤ `n` ≤ 10
&nbsp;
```java
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        for(int i = 1; i <= n; i++) {         
            for(int j = 1; j <= i; j++) {     
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```
### 테스트 결과

|정확성  테스트|
|--|
테스트 1 〉	통과 (176.97ms, 72.4MB)
테스트 2 〉	통과 (189.73ms, 70.4MB)
테스트 3 〉	통과 (178.79ms, 76.4MB)
테스트 4 〉	통과 (204.92ms, 71.2MB)
테스트 5 〉	통과 (158.32ms, 70.9MB)
테스트 6 〉	통과 (208.31ms, 79.4MB)
테스트 7 〉	통과 (148.34ms, 66.8MB)
테스트 8 〉	통과 (183.80ms, 73.9MB)
테스트 9 〉	통과 (171.76ms, 69.9MB)
테스트 10 〉	통과 (200.13ms, 65.5MB)

정확성: 100.0   
합계: 100.0 / 100.0

---

#### 입출력 예
입력 #1
```
3
```
출력 #1
```
*
**
***
```
#### 입출력 예 설명
##### 입출력 예 #1
- `n`이 3이므로 첫째 줄에 * 1개, 둘째 줄에 * 2개, 셋째 줄에 * 3개를 출력합니다.