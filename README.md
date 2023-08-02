# 1st_study
[1주차] 코딩테스트 준비 1주차
<br/>

[프로그래머스 python 문제 바로가기](https://school.programmers.co.kr/learn/challenges?order=recent)

[백준 문제집 바로가기](https://www.acmicpc.net/workbook/view/16346)

<br/><br/>

# [백준] 어두운 굴다리

<details>
<summary>접기/펼치기</summary>
<div markdown="1">

## [성구](./어두운%20굴다리/성구.py)
```py
```
## [민웅](./어두운%20굴다리/민웅.py)
```py
# 17266_어두운 굴다리
import sys
import math
input = sys.stdin.readline

N = int(input())
M = int(input())

location = list(map(int, input().split()))

case1 = location[0]
case2 = N-location[-1]
case3 = 0

for i in range(M-1):
    temp = math.ceil((location[i+1]-location[i])/2)
    # print(temp)
    if temp > case3:
        case3 = temp

ans = max(case1,case2,case3)

print(ans)
```
## [병국](./어두운%20굴다리/병국.py)
```py
```
## [상미](./어두운%20굴다리/상미.py)
```py
```

</div>
</details>

<br/><br/><br/>


# [백준] 겹치는 건 싫어

<details>
<summary>접기/펼치기</summary>
<div markdown="1">

## [성구](./겹치는%20건%20싫어/성구.py)
```py
```
## [민웅](./겹치는%20건%20싫어/민웅.py)
```py
# 20922_겹치는 건 싫어_Hate-Overlap
import sys
input = sys.stdin.readline

N, K = map(int, input().split())
sequence = list(map(int, input().split()))

i, j = 0, 0

num = {}
length = 0
ans = 0
while i<=j and j < N:
    if sequence[j] not in num.keys():
        num[sequence[j]] = 1
        j += 1
        length += 1
    else:
        if num[sequence[j]] >= K:
            num[sequence[i]] -= 1
            i += 1
            length -= 1
        else:
            num[sequence[j]] += 1
            j += 1
            length += 1
    if length > ans:
        ans = length

print(ans)
```
## [병국](./겹치는%20건%20싫어/병국.py)
```py
```
## [상미](./겹치는%20건%20싫어/상미.py)
```py
```

</div>
</details>

<br/><br/><br/>


# [백준] 비슷한 단어

<details>
<summary>접기/펼치기</summary>
<div markdown="1">

## [성구](./비슷한%20단어/성구.py)
```py
```
## [민웅](./비슷한%20단어/민웅.py)
```py
```
## [병국](./비슷한%20단어/병국.py)
```py
```
## [상미](./비슷한%20단어/상미.py)
```py
```


</div>
</details>
