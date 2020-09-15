## Exercise 2.9

### Question:

행동이 두 개일 경우, 통계학과 인공지능 신경망에서 자주 사용되는 로지스틱 또는 시그모이드 함수로 주어지는 분포가 소프트맥스 분포와 같음을 보여라.

### Answer:

#### 소프트맥스 분포

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;Pr&space;\left&space;\{&space;A_t&space;=&space;a&space;\right&space;\}&space;&=&space;\frac{e^{H_t(a)}}{\sum_{b=1}^{k}e^{H_t(b)}}&space;\\&space;&=&space;\frac{e^{H_t(a)}}{e^{H_t(a)}&space;&plus;&space;e^{H_t(b)}}&space;\\&space;&=&space;\frac{1}{1&space;&plus;&space;e^{H_t(b)-H_t(a)}}&space;\end{align*}" title="\begin{align*} Pr \left \{ A_t = a \right \} &= \frac{e^{H_t(a)}}{\sum_{b=1}^{k}e^{H_t(b)}} \\ &= \frac{e^{H_t(a)}}{e^{H_t(a)} + e^{H_t(b)}} \\ &= \frac{1}{1 + e^{H_t(b)-H_t(a)}} \end{align*}" />

#### 시그모이드 함수(로지스틱 함수)

<img src="https://latex.codecogs.com/svg.latex?Pr&space;\left&space;\{&space;A_t&space;=&space;a&space;\right&space;\}&space;=&space;\frac{1}{1&space;&plus;&space;e^{-H_t(a)}}" title="Pr \left \{ A_t = a \right \} = \frac{1}{1 + e^{-H_t(a)}}" />

각 행동 행동 선호도 ![equation](https://latex.codecogs.com/svg.latex?H_t(a),&space;H_t(b)) 는 한 행동이 다른 행동에 대해 갖는 상대적 선호도만 중요하므로, ![equation](https://latex.codecogs.com/svg.latex?H_t(a)&space;>&space;H_t(b)) 이라고 가정하면 (또는 ![equation](https://latex.codecogs.com/svg.latex?H_t(a)&space;<&space;H_t(b)) ), 소프트맥스 분포와 시그모이드 함수에서 같은 방식으로 행동이 선택된다.
