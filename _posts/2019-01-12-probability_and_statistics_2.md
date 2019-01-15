---
title: "Independent events and probability"
date: 2019-01-01T18:01:12+09:00
categories:
- "Probability and Statistics"
keywords:
thumbnailImagePosition: #left,top
thumbnailImage: 
coverImage: 
---

### combinatorial analysis

### permutation 순열

> line arrangement of n different objects

순서를 고려하여 나열하는 방법

n개의 카드 중 하나씩을 선택할 때

$$n(n-1)(n-2)(n-3)... = n!$$

아무것도 나열하지 않는 방법 = 한가지

$$0!=1$$

> r out of n object n >= r

n개중 r개를 선택할 때

$$n(n-1)...(n-r+1)=nPr$$

$$\frac { n ! } { ( n - r ) ! }$$

**Group Permutation**

> 서로다른 n개를 n1,n2,...,nk개의 그룹으로 순서있게 배열하는 경우의 수

$$n = n_1+n_2+...+n_k$$

분모에 중복이 있는 것들을 나누어 주면 된다.

$$\frac { n ! } { n _ { 1 } ! n _ { 2 } ! \cdots n _ { k } ! }$$

**Circular Permutation**

![](http://mathworld.wolfram.com/images/eps-gif/CircularPermutations_950.gif)

회전해도 상관없기 때문에 순서대로 쉬프트 하며 놓이는 n만큼 나누어준다.

$$\frac { n ! } { n }$$

### combination 조합

> select r objects out of n

순서에 상관하지 않는다.

$$nCr=\frac { n ! r } { r ! }=\binom{n}{r}=\frac { n ! } { (n-r) ! r! }$$

$$\binom{n+m}{r}=\sum _ { k = 0 } ^ { r }\binom{n}{k}\binom{m}{r-k}$$

n명의 소년과 m명의 소녀중 r명을 고를 때

<table style="width:100%">
  <tr>
    <th>Boys</th>
    <th>Girls</th> 
    <th></th>
  </tr>
  <tr>
    <td>0</td>
    <td>r</td>
    <td>(nC0)(mCr)</td>
  </tr>
  <tr>
    <td>1</td> 
    <td>r-1</td> 
    <td>(nC1)(mC(r-1))</td>
  </tr>
  <tr>
    <td>...</td> 
    <td>...</td> 
  </tr>
    <tr>
    <td>r</td> 
    <td>0</td> 
  </tr>
</table>

### binomial theorem

> 개념을 잘 모르겠다면 [수악중독](https://www.youtube.com/watch?v=9nBCeRhwBzI) 한번 보고오시는 것을 추천합니다.

$$(a+b)^n=A_0a^n+A_1a^{n-1}b^1+A_2a^{n-2}b^2+...+A_nb^n$$

$$=\sum _ { k = 0 } ^ { n }\binom{n}{k}a^kb^{n-k}$$

$$f(x)=(1+x)^n=\sum _ { k = 0 } ^ { n }\binom{n}{k}x^k$$

x에 1을 대입

$$x = 1 \Rightarrow 2 ^ { n }=\sum _ { k = 0 } ^ { n }\binom{n}{k}$$

x에 -1을 대입

$$x = -1 \Rightarrow 0=\sum _ { k = 0 } ^ { n }\binom{n}{k}(-1)^{k}$$

위 둘을 더하면

$$nC2+nC4+...=2^{n-1}$$

위 둘을 빼면

$$nC1+nC3+...=n^{n-1}$$

이후 미분한다.

**미분법의 기본공식**

$$f ( x ) = x ^ { n }$$

$$f ^ { \prime } ( x ) = n x ^ { n - 1 }$$

$$f ^ { \prime } ( x ) =n ( 1 + x ) ^ { n - 1 }=\sum _ { k = 0 } ^ { n }k\binom{n}{k}x^{k-1}$$

$$x = 1 \Rightarrow n 2 ^ { n - 1 } = \sum _ { k = 0 } ^ { n } k\binom{n}{k}$$

$$=nC1+2nC2+3nC3+...$$

이후 한번더 미분한다. (이계도함수)


$$f ^ { \prime \prime } ( x ) = n ( n - 1 ) ( 1 + x ) ^ { n - 2 } = \sum _ { k = 0 } ^ { n } k ( k - 1 )\binom{n}{k}x^{k-2}$$

그리고 위 식은 이항분포에 활용된다.

$$B ( n , p )= _ { n } C _ { x } p ^ { k } (1-p) ^ { n - k }$$

급수를 할 때, 미분으로 복잡한 합을 쉽게 구할 수 있다.

$$f(x)=1+2x+3x^2+4x^3+...$$

$$|x|<1$$

양변에 x를 곱한다.

$$fx(x)=1x+2x^2+3x^3+...$$

$$f(x)-xf(x)$$

$$=(1-x)f(x)=1+x+x^2+x^3+...=\frac { 1 } { 1 - x }$$

$$g ( x ) = \sum _ { k = 0 } ^ { \infty } x ^ { k }=\frac { 1 } { 1 - x }$$

$$g \prime( x ) = \sum _ { k = 0 } ^ { \infty } kx ^ { k-1 }=f(x)=(\frac { 1 } { 1 - x })\prime$$

평균값 분산을 위해 사용

![](https://s3.namuwikiusercontent.com/s/329d4fe7fb08f523fd84f3c74cf9814b80ac4375111437fdd5474819188c5c8615c6f430f8ecd65cc609a13b67663c901e73d50201a40c24a403c3ef81e2493807ca53baddcb6927e6e7b7e0585aa4a19ea66e15eeeab20dfdcda8b9dc621306)

### Stirling’s formula

n!이 커지면 계산하기 힘들다. 

$$n! \approx \sqrt{2\pi n}\, \left(\frac{n}{e}\right)^{n}$$

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Mplwp_factorial_gamma_stirling.svg/300px-Mplwp_factorial_gamma_stirling.svg.png)

### Reliability

어떤 시스템이 어떤 시간동안 고장나지 않고 올바르게 작동하는가

> duration of useful functioning of system

$$R(t)$$

probability that a system will be functioning at time t

시작하는 시점부터 t라는 시점까지 시스템이 잘 동작할 확률

고장은 언제날지 모르지만 t시간 까지 동작할 확률

'어느 시점에서 정지한다'를 규정하는 것은 아님

**Series Connection**

![](https://drive.google.com/uc?id=18p0Ftg3yDafyXbJyL4_Mz0i2YlWtH8wK)

input => [] => output 모듈들이 직렬연결 되어있는 형태

가정) 각 모듈들은 서로간 영향을 주지 않는다.

assume) that all modules are independent

$$R(t)$$

위 전체 시스템이 시점 t 까지 동작할 확률

**팩토리얼 표기**



$$n!=\prod _ { i = 1 } ^ { n }i \,\,\,(n\geq0)$$

$$R(t)=R_1(t)R_2(t)...R_n(t)=\prod _ { i = 1 } ^ { n } R _ { i } ( t )$$

**Parallel Connection**

병렬연결

![](https://doc-10-1o-docs.googleusercontent.com/docs/securesc/hqvb2dlnmf621rsihr92ojsocu67u194/4ntss3n3pbqjau4ata5ghq61ihppt7v9/1546516800000/04461474962854791414/04461474962854791414/1H3i8uggUulifpGf1RjAyLt0Cv8B9XCtR)

적어도 한개의 모듈이 동작하면 된다.

R(t) => at least 1 module functioning

적어도를 구하기 위해서 전체에서 동작하지 않는 경우를 제외

$$1-(1-R_1)(1-R_2)...(1-Rn)$$

$$=1 - \prod _ { i = 1 } ^ { n } \left( 1 - R _ { i } ( t ) \right)$$

복잡한 구조

![](https://drive.google.com/uc?id=1Smj6QoRiSmHhWSXmP65N9z6pR3-_md9F)

(i) C3->functioning at t

$$R_x=P(R(t)|C_3\,functioning)$$

(ii) C3->mal functioning

$$R_y=P(R(t)|C_3\,malfunctioning)$$

$$R=R_xR_3+R_y(1-R_3)$$

### Reference 

[bhsmath](http://bhsmath.tistory.com/145)

[ktword](http://www.ktword.co.kr/abbr_view.php?m_temp1=4123)

[mathfactory](https://www.mathfactory.net/11101)

[수악중독](https://www.youtube.com/watch?v=9nBCeRhwBzI)