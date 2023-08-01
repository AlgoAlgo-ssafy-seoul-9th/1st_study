# 1st_study
[1주차] 코딩테스트 준비 1주차
<br/>

[프로그래머스 python 문제 바로가기](https://school.programmers.co.kr/learn/courses/30/lessons/77485)

[백준 문제집 바로가기](https://www.acmicpc.net/workbook/view/16147)

<br/><br/>

# [백준] 백준 문제1

<details>
<summary>접기/펼치기</summary>
<div markdown="1">

## [성구](./백준%20문제1/성구.py)
```py
```
## [민웅](./백준%20문제1/민웅.py)
```py
# 예시
import sys
input = sys.stdin.readline
# 접하면 안된다 -> 같은 직선상에 있는 같은 기울기 선분도 안된다

N = int(input())

nli = list(map(int, input().split()))

check = [0]*50

for i in range(N):
    right, left = float('-inf'), float('inf')
    for j in range(i+1, N):
        temp = (nli[j] - nli[i]) / (j - i)
        if nli[j] >= nli[i]:
            if temp > right:
                check[i] += 1
                check[j] += 1
                right = temp
        # if j == i+1:
        #     if nli[j] == nli[i]:
        #         check[i] += 1
        #         check[j] += 1

    for k in range(i-1, -1, -1):
        temp = (nli[k] - nli[i]) / (k - i)
        if nli[k] > nli[i]:
            if temp < left:
                check[i] += 1
                check[k] += 1
                left = temp

print(max(check))
```
## [병국](./백준%20문제1/병국.py)
```py
```
## [상미](./백준%20문제1/상미.py)
```py
```

</div>
</details>

<br/><br/><br/>


# [백준] 문제2

<details>
<summary>접기/펼치기</summary>
<div markdown="1">

## [성구](./문제2/성구.py)
```py
```
## [민웅](./문제2/민웅.py)
```py
```
## [병국](./문제2/병국.py)
```py
```
## [상미](./문제2/상미.py)
```py
```

</div>
</details>

<br/><br/><br/>


# [백준] 문제3

<details>
<summary>접기/펼치기</summary>
<div markdown="1">

## [성구](./문제3/성구.py)
```py
```
## [민웅](./문제3/민웅.py)
```py
```
## [병국](./문제3/병국.py)
```py
```
## [상미](./문제3/상미.py)
```py
```


</div>
</details>
