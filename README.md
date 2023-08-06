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
n = int(input())
m = int(input())
arr = list(map(int,input().split()))

answer1 = 0

# n = 1 일때,, 시작점 잡아주는 느낌,,
if len(arr) == 1:
    answer1 = max(arr[0] - 0, n - arr[0])
# n > 1 일때
else:
    for i in range(len(arr)):
        # 시작점
        if i == 0:
            answer = arr[i]-0
        # 끝점
        elif i == len(arr)-1:
            answer = n-arr[i]
        # 중간지점(중요)
        else:
            check = (arr[i]-arr[i-1])
            if check%2:
                answer = check // 2 +1
            else:
                answer = check // 2
        answer1 = max(answer,answer1)
print(answer1)


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

# 하나씩 넣을때마다 갯수 체크할까,,
# n이 총 개수 , k가 허용가능한 개수
# 이게아니었고,, 시작점이 중요한거,, 그 시작점부터 가장 큰 부분수열,,구하는거

# cnt = 0
# max_cnt = 0
# answer_dict = {}
# for i in range(n):
#     if arr[i] in answer_dict:
#         if answer_dict[arr[i]]+1 > k:
#             break
#         else:
#             answer_dict[arr[i]] += 1
#             cnt += 1
#     else:
#         answer_dict[arr[i]] = 1
#         cnt += 1
# max_cnt = (max_cnt,cnt)

n, k = map(int,input().split())
arr = list(map(int,input().split()))

# 투포인터로 풀어볼게요,,
left,right = 0,0 # 처음엔 0부터 시작합시다..
counter = [0]*(max(arr)+1) # 항목 개수세어줄 리스트
answer = 0 # 답

while right < n: # 배열 끝까지 갈때까지할건데,,
    if counter[arr[right]]<k: # k보다 작다면
        counter[arr[right]] += 1
        right += 1
    else: # k보다커져버렸다면,, 이제 left를 한칸땡겨요
        counter[arr[left]] -= 1 # 이건빼줘야겠져
        left += 1
    answer = max(answer, right-left) #이게 답
print(answer)

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
# 2179_비슷한단어_similar-word
# 26% 까지 맞음
import sys
input = sys.stdin.readline


N = int(input())

words = []

for i in range(N):
    words.append([input().strip(), i])

words.sort(key=lambda x:x[0])
temp = [words[0], words[1]]
ans = 0

for i in range(1, N):
    l1, l2 = len(words[i-1][0]), len(words[i][0])
    r = min(l1, l2)
    idx = 0
    while idx < r:
        if words[i-1][0][idx] == words[i][0][idx]:
            idx += 1
        else:
            break
    if idx > ans:
        temp = [words[i-1], words[i]]
        ans = idx
    elif idx == ans:  # idx와 ans가 같은 경우를 추가
        sub = [words[i - 1], words[i], temp[0], temp[1]]
        sub.sort(key=lambda x: x[1])
        temp = [sub[0], sub[1]]

print(temp[0][0])
print(temp[1][0])
```
## [병국](./비슷한%20단어/병국.py)
```py
```
## [상미](./비슷한%20단어/상미.py)
```py
```


</div>
</details>
