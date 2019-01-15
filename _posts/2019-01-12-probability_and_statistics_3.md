---
title: "Definition of probability variables"
date: 2019-01-05T18:03:29+09:00
categories:
- "Probability and Statistics"
keywords:
thumbnailImagePosition: #left,top
thumbnailImage: 
coverImage: 
---

### Random Variables

definition of RV(확률변수)

$$X(w)=x$$

RV : real numbers

mapping을 통해 만들어진다.

> mapping each outcome of random experiment to a real value 

tossing a coin 

X : H = 1

X : T = 0

1,0 등의 정의는 마음대로 

P(H)=P(1)=1/2

P(T)=P(0)=1/2

이제 확률(P)을 함수처럼 사용한다.

$$P(A)$$

A를 이벤트->확률변수

tossing two coin

RV : #of heads

o => {TT} => P(0) = P({TT}) = 1/4

1 => {HT,TH} => P(1) = P({HT,TH}) = 1/2

2 => {HH} = P(2) = P({HH}) = 1/4

$$X(w_i)=x_i$$

> by the conventional notation

RV : X,Y,Z (대문자)

a specific(fixed) value of X : x,y,z

### Event defined by notation

> let Ax be an event

w=outcome

$$A_x = \\{ \mathrm { w } | \mathrm { X } ( \mathrm { x } ) = \mathrm { x } \\}$$

두 개의 코인을 던질 때,

$$A_0=\\{TT\\}, A_1=\\{HT,TH\\}$$

$$P(A_x)=P_x(X=x)$$

$$P(A_1)=P(1)$$

$$P(a< x \leq b)=P(A)$$

$$A=\\{w|a < X_{(w)} \leq b\\}$$

<script type="math/tex; mode=display">
P(X \leq 1) = P(\{TT,HT,TH\})= 3/4 
</script>

### Distribution Function

> for an RV X, real value x

cumulative distribution function (cdf)

확률값을 더해나간다. (누적확률)

$$F_X(x) \stackrel { d } { = } P(X \leqq x)$$

![](https://i2.wp.com/alfredessa.com/wp-content/uploads/2017/11/elitecdf.png)

$$1)\, if\,x_1< x_2$$

$$F_X(x1) \leq F_X(x2)$$

다음이 성립하면 위 식의 equal이 성립한다.
$$P(x1 < x \leq x2)=0$$

$$2)\, 0 \leqq F_X(x) \leqq 1$$

무한 대입

확률 변수가 무한대보다 작거나 같을 확률(모든 real-number 포함)=1
$$3)\,F_X(\infty)=\lim _ { x \rightarrow \infty }F_X(x)=1$$

$$4)\,F_X(-\infty)=\lim _ { x \rightarrow -\infty }F_X(x)=0$$

$$5)\,P(a< x \leqq b) = F_X(b)-F_X(a)$$

$$6)\,P(X>a) = 1-F_X(a)$$

<script type="math/tex; mode=display">
a)\,F _ { x } ( x ) = \left\{ \begin{array} { c c } { 0 , } & { x < 0 } \\ { x + \frac { 1 } { 2 } , } & { 0 \leqq x \leq \frac { 1 } { 2 } } \\ { 1 , } & { x > \frac { 1 } { 2 } } \end{array} \right.
</script>

![](https://drive.google.com/uc?id=1idy3jzCQrfdiHOu6GNDL_VuBEmGKosOu)

<script type="math/tex; mode=display">
b)\,P( X > 1/4)
</script>

<script type="math/tex; mode=display">
=1-P(X \leqq 1/4)
</script>

<script type="math/tex; mode=display">
=1-F_X(1/4)=1-3/4=1/4
</script>

$$c\)\,P(X>0)$$

<script type="math/tex; mode=display">
=1-F_X(0)=1-1/2=1/2
</script>

$$d)\,P(x \geqq 0)=1$$

<script type="math/tex; mode=display">
P(X=0)=1/2
</script>

equality의 유무에 따라서 복잡해진다.

<script type="math/tex; mode=display">
P(X \geqq 1/4)
</script>

<script type="math/tex; mode=display">
=1-P(x<1/4)
</script>

$$1-\lim _ { x \rightarrow 4 }$$

<script type="math/tex; mode=display">
F_X(x)=1/4
</script>


REF

http://alfredessa.com/2017/11/cumulative-distribution-function-what-it-is-and-why-its-important-part-i/
