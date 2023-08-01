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
