# [Programmers] JadenCase 문자열 만들기

프로그래머스(Programmers) :  https://programmers.co.kr/learn/courses/30/lessons/12951

### 문제

JadenCase란 모든 단어의 첫 문자가 대문자이고, 그 외의 알파벳은 소문자인 문자열입니다. 문자열 s가 주어졌을 때, s를 JadenCase로 바꾼 문자열을 리턴하는 함수, solution을 완성해주세요.

### 제한사항

- s는 길이 1 이상인 문자열입니다.
- s는 알파벳과 공백문자(" ")로 이루어져 있습니다.
- 첫 문자가 영문이 아닐때에는 이어지는 영문은 소문자로 씁니다. ( 첫번째 입출력 예 참고 )

#### 예제 입력 1

```  
"3people unFollowed me"
"for the last week"
```  

#### 예제 출력 1

```  
"3people Unfollowed Me"
"For The Last Week"
```  

### 입출력 예 설명

## 2. 내 소스 코드

```python  
def solution(s):
    s = s.split(' ')
    for i in range(len(s)):
        s[i] = s[i].lower().capitalize()
    answer = ' '.join(s)
    return answer
```  



## 3. 풀이 & 개선점