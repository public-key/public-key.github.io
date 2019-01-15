---
title: "Conditional Probability and Bayes theorem"
date: 2019-01-01T12:58:31+09:00
categories:
- "Probability and Statistics"
keywords:
thumbnailImagePosition: #left,top
thumbnailImage: 
coverImage: 
---

이상화 교수님의 확률과 통계를 듣고 정리한 글입니다.

### Sample Space

$$S ( s e t )$$

> 통계적 실험에서 발생가능한 모든 결과들의 집합

sample spcae를 벗어난다면 생각하지 않아도 된다.

### Event(A)

$$A \subset S$$

> S(sample space)라는 집합의 부분집합 

### P(A)

$$outcome \in A$$

> A라는 이벤트가 발생할 확률

하나의 결과(outcome)을 선택하면 A에 속할 확률 

### Conditional Probability

$$P ( B | A )$$

> A라는 컨디션이 발생했을 때, B라는 이벤트가 발생할 확률

$$P ( B | A ) = \frac { P ( B \cap A ) } { P ( A ) }$$

특정 이벤트 확률은 sample space를 전제로 생각한다.

$$ \frac { P ( B \cap A ) } { P ( A ) } = \frac { P ( B \cap A|S ) } { P ( A|S ) }$$

W: 날씨 t: 오늘

<script type="math/tex; mode=display">
P(W_t|W_{t-1},W_{t-2},...,W_{t-n})
</script>

어제의 날씨, 이틀전의 날씨,...,n일 전의 날씨가 오늘의 날씨에 얼마나 영향을 주는가

### Total Probability

$$P(A)=P(A_1)+P(A_2)+...+P(A_n)$$

$$P(A_1),P(A_2),...,P(A_n)$$ 은 배반사건이다.

**배반사건**

> 동시에 일어날 수 없는 사건

<script type="math/tex; mode=display">
\{A_1, A_2,...,A_n\} = partition\, of\, S
</script>

2.1 독립사건에서 정정 A->S로 정정

$$P(A_1) = P(A_1 \cap A)$$

$$=P(A|A_1)P(A)$$

$$P ( A ) = \sum _ { n = 1 } ^ { N } P ( A | A _ { i } ) P \left( A _ { i } \right)$$

$$P ( A | A _ { i } )$$

> 선행적으로 알고있는 사건이다. (priori)

$$P( A _ { i })$$ 

> 배반사건을 모두 더한다.

### bayesian theorem

$$P ( B | A ) = \frac { P ( B \cap A ) } { P ( A ) } = \frac { P ( A | B ) P ( B ) } { P ( A ) }$$

$$P \left( A _ { i } | A \right) = \frac { P ( A | A i ) P \left( A _ { i } \right) } { P ( A ) }$$

$$A_i$$

> original input (모름)

$$A$$

> observation data 관측한 데이터 (알고있음)

### EX) binary symmetric channel

input symbols : {0,1}

output symbols : {0,1}

$$Pnm$$

n을 보내서 m을 얻을 확률

![](https://drive.google.com/uc?id=1hVFbp1ziaXIN3KliYVcTrbvos_mAyWJ9)

<script type="math/tex; mode=display">
P_{11}, P_{22}
</script>

가 100%이면 에러가 없다.

<script type="math/tex; mode=display">
P_{12}=P_{21}
</script>

이면 대칭적이라고 하여 binary symmetric channel라고 한다.

$$P_{11}=P(y_1|x_1)$$

$$P_{12}=P(y_2|x_1)$$

$$P_{21}=P(y_1|x_2)$$

$$P_{22}=P(y_2|x_2)$$

**P(err)**

P12와 P21가 일어날 확률. P(12)+P(21)

$$P(y_2|x_1)P(x_1)+P(y_1|x_2)P(x_2)$$

