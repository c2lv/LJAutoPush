# [B030] 검색어 목록 정리

[문제 보기](https://localjudge.com/problems/B030)

> 검색어 기록에서 중복을 없애고 짧은 것부터, 길이가 같으면 사전 순으로 정리한다.

## 분류

200점, 케이스 15, 출제 dongbinna, 쉬움, 정렬, 문자열, 한국어

## 문제

한 중고 서점의 검색창에는 하루 동안 검색어 N개가 들어왔다. 들어온 순서대로 모두 기록해 두었기 때문에, 같은 검색어가 여러 번 들어와 있는 경우도 있다. 각 검색어는 영어 소문자로만 이루어진다.

가게 주인은 이 기록을 보기 좋게 정리하려고 한다. 정리하는 방법은 다음과 같다. 먼저 같은 검색어는 한 번만 남기고 나머지는 지운다. 그다음 길이가 짧은 검색어부터 차례대로 늘어놓는다. 길이가 같은 검색어끼리는 사전 순으로 앞에 오는 것을 먼저 놓는다.

검색어 N개가 주어질 때, 정리한 결과를 한 줄에 하나씩 출력하는 프로그램을 작성하여라.

예를 들어 N=6개의 검색어가 다음의 표와 같이 들어왔다고 해보자.

| 순서 | 1 | 2 | 3 | 4 | 5 | 6 |
| --- | --- | --- | --- | --- | --- | --- |
| 검색어 | but | i | wont | hesitate | no | more |

각 검색어의 길이는 다음과 같다.

| 검색어 | but | i | wont | hesitate | no | more |
| --- | --- | --- | --- | --- | --- | --- |
| 길이 | 3 | 1 | 4 | 8 | 2 | 4 |

길이가 짧은 것부터 늘어놓으면 i, no, but 이 차례대로 앞에 온다. 그다음 길이가 4인 검색어는 wont 와 more 두 개인데, 이 둘은 사전 순으로 앞에 오는 more 를 먼저 놓는다. 마지막은 길이가 8인 hesitate 다. 그래서 정리한 결과는 다음과 같다.

| 순서 | 1 | 2 | 3 | 4 | 5 | 6 |
| --- | --- | --- | --- | --- | --- | --- |
| 검색어 | i | no | but | more | wont | hesitate |

지금 예시에는 같은 검색어가 두 번 들어온 경우가 없다. 만약 같은 검색어가 두 번 이상 들어왔다면, 정리한 결과에는 그 검색어가 한 번만 남는다. 그래서 출력하는 줄의 수는 들어온 검색어의 개수보다 적어질 수 있다.

## 입출력 예시

## 예시 1

입력

```
6
but
i
wont
hesitate
no
more
```

출력

```
i
no
but
more
wont
hesitate
```

## 예시 2

입력

```
2
cba
ab
```

출력

```
ab
cba
```

## 예시 3

입력

```
40
bbcab
baabbbbb
ba
bccab
aabcb
aabacc
cbaa
bcbabcab
caccacaa
bcaa
cbbcb
bccbbbb
b
bb
cbbbaaca
accbaac
cbaacacc
bbcca
caacbbc
bcc
cabca
cabcc
bb
bcbbc
b
bbbaacc
caaacccc
baaa
aabc
bbaaa
bcbcaabc
babcac
bbbaaab
bbbbbbb
ccaca
bcbca
b
accaa
abcaaac
aaabaac
```

출력

```
b
ba
bb
bcc
aabc
baaa
bcaa
cbaa
aabcb
accaa
bbaaa
bbcab
bbcca
bcbbc
bcbca
bccab
cabca
cabcc
cbbcb
ccaca
aabacc
babcac
aaabaac
abcaaac
accbaac
bbbaaab
bbbaacc
bbbbbbb
bccbbbb
caacbbc
baabbbbb
bcbabcab
bcbcaabc
caaacccc
caccacaa
cbaacacc
cbbbaaca
```

## 입력 조건

- 가장 먼저 첫째 줄에 들어온 검색어의 개수 N이 주어진다. N은 1 이상 20,000 이하의 자연수다.
- 이어서 N개의 줄에 걸쳐 각 검색어가 들어온 순서대로 한 줄에 하나씩 주어진다. 각 검색어는 영어 소문자로만 이루어지며, 그 길이는 1 이상 50 이하다. 같은 검색어가 여러 번 주어질 수 있다.

## 출력 조건

- 정리한 검색어를 한 줄에 하나씩 출력한다. 같은 검색어는 한 번만 출력하므로, 출력하는 줄의 수는 N보다 적어질 수 있다. 마지막 검색어를 출력한 다음에 빈 줄을 따로 붙이지 않는다.

## 요구사항

- 입력은 표준 입력으로 받고, 결과는 표준 출력으로 내보냅니다
- 같은 검색어는 한 번만 남깁니다
- 길이가 짧은 검색어부터 출력하고, 길이가 같으면 사전 순으로 출력합니다
- 한 줄에 검색어 하나씩 출력합니다
- 마지막 줄 다음에 빈 줄을 따로 붙이지 않습니다
- 표준 입력으로 읽고 표준 출력으로 내보내는 프로그램을 짜야 합니다
- 쓸 수 있는 말은 파이썬, 자바스크립트입니다
- 메모리 제한은 256MB입니다. 브라우저에서는 재지 않고 적기만 합니다
- 시간 제한은 출제자의 정답 코드를 같은 런타임에서 재서 정합니다
- 이 문제는 프롬프트가 아니라 **코드**를 냅니다. 그 코드는 **이 기기의 브라우저에서** 돌고, 서버로는 나온 출력의 지문과 걸린 시간만 갑니다. 맞았는지는 **서버가** 정합니다. 실행 시간은 각자 기기가 적어 보내는 값이라, 코드와 기기 정보를 순위표에 **같이 내걸어** 둡니다.
- 출력이 **글자 하나까지** 기대값과 같아야 합니다. 줄 안의 빈칸은 다른 글자와 똑같이 봅니다.
- 케이스는 15개이고, 그 가운데 3개는 입력과 기대 출력을 함께 보여 줍니다. 나머지는 제출할 때만 쓰이고 화면에는 보여 주지 않습니다.
- 케이스 15개를 **전부** 통과해야 해결입니다.

> 문제의 요구 사항을 잘 읽고 해결해 주세요. 단, 채점 과정을 건드려 통과한 것처럼 꾸미는 경우 적발 시 제재될 수 있습니다. 제출한 코드는 순위표에 함께 공개됩니다.

## 예시

공개 케이스 3개입니다. 채점에는 숨은 케이스가 함께 쓰입니다. 케이스 15개를 전부 통과해야 해결입니다.

**예시 1**

입력

```
2
cba
ab
```

기대 출력

```
ab
cba
```

**예시 2**

입력

```
40
bbcab
baabbbbb
ba
bccab
aabcb
aabacc
cbaa
bcbabcab
caccacaa
bcaa
cbbcb
bccbbbb
b
bb
cbbbaaca
accbaac
cbaacacc
bbcca
caacbbc
bcc
cabca
cabcc
bb
bcbbc
b
bbbaacc
caaacccc
baaa
aabc
bbaaa
bcbcaabc
babcac
bbbaaab
bbbbbbb
ccaca
bcbca
b
accaa
abcaaac
aaabaac
```

기대 출력

```
b
ba
bb
bcc
aabc
baaa
bcaa
cbaa
aabcb
accaa
bbaaa
bbcab
bbcca
bcbbc
bcbca
bccab
cabca
cabcc
cbbcb
ccaca
aabacc
babcac
aaabaac
abcaaac
accbaac
bbbaaab
bbbaacc
bbbbbbb
bccbbbb
caacbbc
baabbbbb
bcbabcab
bcbcaabc
caaacccc
caccacaa
cbaacacc
cbbbaaca
```

**예시 3**

입력

```
6
but
i
wont
hesitate
no
more
```

기대 출력

```
i
no
but
more
wont
hesitate
```
