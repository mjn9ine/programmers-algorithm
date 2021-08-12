# [Programmers] N개의 최소공배수

프로그래머스(Programmers) :  https://programmers.co.kr/learn/courses/30/lessons/12953

### 문제

두 수의 최소공배수(Least Common Multiple)란 입력된 두 수의 배수 중 공통이 되는 가장 작은 숫자를 의미합니다. 예를 들어 2와 7의 최소공배수는 14가 됩니다. 정의를 확장해서, n개의 수의 최소공배수는 n 개의 수들의 배수 중 공통이 되는 가장 작은 숫자가 됩니다. n개의 숫자를 담은 배열 arr이 입력되었을 때 이 수들의 최소공배수를 반환하는 함수, solution을 완성해 주세요.

### 제한사항

- arr은 길이 1이상, 15이하인 배열입니다.
- arr의 원소는 100 이하인 자연수입니다.

#### 예제 입력 1

```  
[2,6,8,14]
[1,2,3]
```  

#### 예제 출력 1

```  
168
6
```  

### 입출력 예 설명

## 2. 내 소스 코드

```python  
def get_gcd(x, y):
    while y != 0:
        x, y = y, x % y
        
    return x

def solution(arr):
    answer = 0
    while len(arr) >= 2:
        a = arr.pop()
        b = arr.pop()
        answer = a * b // get_gcd(a, b)
        arr.append(answer)
        
    return answer
```  



## 3. 풀이 & 개선점