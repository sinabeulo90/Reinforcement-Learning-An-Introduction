## TODO

Exercise 2.3, Exercise 2.5, Exercise 2.7, Exercise 2.11

# 목차  

[Exercise 2.1](#Exercise-21)  
[Exercise 2.2](#Exercise-22)  
[Exercise 2.4](#Exercise-24)  
[Exercise 2.6](#Exercise-26)  
[Exercise 2.8](#Exercise-28)  
[Exercise 2.9](#Exercise-29)  
[Exercise 2.10](#Exercise-210)  

## Exercise 2.1

### Question:

입실론 탐욕적 행동 선택에서 두 개의 행동이 있고, ![equation](https://latex.codecogs.com/svg.latex?\epsilon=0.5) 라면 탐욕적 행동을 선택할 확률은 얼마인가?

### Answer:
0.5 + 0.5 * 0.5 = 0.75

처음 탐욕적 행동이 선택될 확률이 50%(0.5), 처음 탐욕적 행동이 선택되고 두번째에도 탐욕적 행동이 선택될 확률은 25%(0.5 * 0.5)이므로 0.75이다.

<br>

## Exercise 2.2

### Question: 다중 선택 예제

네 개의 행동 중 하나를 선택하는 다중 선택 문제를 생각해 보자. 각 행동은 번호 1, 2, 3, 4로 구분한다. 이 문제에 입실론 탐욕적 행동 선택을 위한 다중 선택 알고리즘을 적용한다고 생각해 보자. 이때 이 알고리즘은 표본평균 행동 가치 추정값을 이용하고 초기 추정값 ![equation](https://latex.codecogs.com/svg.latex?Q_1(a)=0) 을 적용한다. 시간 관계에 따른 행동 및 가치의 몇몇 초기값들이 ![equation](https://latex.codecogs.com/svg.latex?A_1=1), ![equation](https://latex.codecogs.com/svg.latex?R_1=-1), ![equation](https://latex.codecogs.com/svg.latex?A_2=2), ![equation](https://latex.codecogs.com/svg.latex?R_2=1), ![equation](https://latex.codecogs.com/svg.latex?A_3=2), ![equation](https://latex.codecogs.com/svg.latex?R_3=-2), ![equation](https://latex.codecogs.com/svg.latex?A_4=2), ![equation](https://latex.codecogs.com/svg.latex?R_4=2), ![equation](https://latex.codecogs.com/svg.latex?A_5=3), ![equation](https://latex.codecogs.com/svg.latex?R_5=0) 이라고 가정해 보자. 이 시간 단계 중 일부에서 행동이 무작위로 선택되는 입실론 상황이 발생했을 수 있다. 어떤 시간 단계에서 이 상황이 확실하게 발생했을까? 어떤 시간 단계에서 이 상황이 발생하는 것이 가능했을까?

### Answer:

| ![equation](https://latex.codecogs.com/svg.latex?t) | | ![equation](https://latex.codecogs.com/svg.latex?Q_t(1)) | ![equation](https://latex.codecogs.com/svg.latex?Q_t(2)) | ![equation](https://latex.codecogs.com/svg.latex?Q_t(3)) | ![equation](https://latex.codecogs.com/svg.latex?Q_t(4)) | | ![equation](https://latex.codecogs.com/svg.latex?A_t) | ![equation](https://latex.codecogs.com/svg.latex?R_t) | | 설명 |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| 1 | | 0 | 0 | 0 | 0 | | 1 | -1 | | 탐욕적 행동 선택 or 무작위 행동 선택 |
| 2 | | -1 | 0 | 0 | 0 | | 2 | 1 | | 탐욕적 행동 선택 or 무작위 행동 선택 |
| 3 | | -1 | 1 | 0 | 0 | | 2 | -2 | | 탐욕적 행동 선택 |
| 4 | | -1 | -0.5 | 0 | 0 | | 2 | 2 | | 무작위 행동 선택 <br> (탐욕적 행동 선택일 경우 3 또는 4 선택) |
| 5 | | -1 | 0.3 | 0 | 0 | | 3 | 0 | | 무작위 행동 선택 <br> (탐욕적 행동 선택일 경우 2 선택) |

<br>

## Exercise 2.4

### Question:

시간 간격의 크기 ![equation](https://latex.codecogs.com/svg.latex?\alpha_n) 이 고정된 값이 아니라면 추정값 ![equation](https://latex.codecogs.com/svg.latex?Q_n) 은 이전까지 받은 보상들의 가중 평균이고, 이때 가중치는 식 2.6에서 주어지는 것과는 다르다. 식 2.6과 유사한 일반적인 경우에 있어서 바로 이전 보상에 적용할 가중치는 얼마인가? 시간 간격의 크기와 관련하여 답변해 보라.

### Answer:

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;Q_{n&plus;1}&space;&=&space;Q_n&space;&plus;&space;\alpha_n[R_n-Q_n]&space;\\&space;&=&space;\alpha_nR_n&space;&plus;&space;(1-\alpha_n)Q_n&space;\\&space;&=&space;\alpha_nR_n&space;&plus;&space;(1-\alpha_n)[\alpha_{n-1}R_{n-1}&space;&plus;&space;(1-\alpha_{n-1})Q_{n-1}]&space;\\&space;&=&space;\alpha_nR_n&space;&plus;&space;(1-\alpha_n)\alpha_{n-1}R_{n-1}&space;&plus;&space;(1-\alpha_n)(1-\alpha_{n-1})Q_{n-1}&space;\\&space;&=&space;\alpha_nR_n&space;&plus;&space;(1-\alpha_n)\alpha_{n-1}R_{n-1}&space;&plus;&space;\cdots&space;&plus;&space;\prod_{i=2}^{n}(1-\alpha_i)\alpha_1R_1&space;&plus;&space;\prod_{i=1}^{n}(1-\alpha_i)Q_1&space;\\&space;&=&space;\alpha_nR_n&space;&plus;&space;\sum_{i=1}^{n-1}\prod_{j=i&plus;1}^{n}(1-\alpha_j)\alpha_iR_i&space;&plus;&space;\prod_{i=1}^{n}(1-\alpha_i)Q_1&space;\end{align*}" title="\begin{align*} Q_{n+1} &= Q_n + \alpha_n[R_n-Q_n] \\ &= \alpha_nR_n + (1-\alpha_n)Q_n \\ &= \alpha_nR_n + (1-\alpha_n)[\alpha_{n-1}R_{n-1} + (1-\alpha_{n-1})Q_{n-1}] \\ &= \alpha_nR_n + (1-\alpha_n)\alpha_{n-1}R_{n-1} + (1-\alpha_n)(1-\alpha_{n-1})Q_{n-1} \\ &= \alpha_nR_n + (1-\alpha_n)\alpha_{n-1}R_{n-1} + \cdots + \prod_{i=2}^{n}(1-\alpha_i)\alpha_1R_1 + \prod_{i=1}^{n}(1-\alpha_i)Q_1 \\ &= \alpha_nR_n + \sum_{i=1}^{n-1}\prod_{j=i+1}^{n}(1-\alpha_j)\alpha_iR_i + \prod_{i=1}^{n}(1-\alpha_i)Q_1 \end{align*}" />

<br>

## Exercise 2.6

### Question: 신비한 스파이크

그림 2.3에 보이는 결과는 무작위로 선택한 2000번의 10중 선택 결과에 대한 평균이기 때문에 매우 믿을 만하다. 그렇다면 왜 긍정적 방법의 경우 곡선의 처음 부분에서 요동과 스파이크가 나타나는가? 다시 말하면 무엇이 이 방법의 성능을 평균적으로, 특히 처음 부분에서 특별히 더 좋거나 나쁘게 만드는가?

### Answer:

긍정적 초기값을 사용하면, 어떤 행동이 초기에 선택될 때 보상은 초기 추정값보다 작으므로 다른 행동을 시도해 볼 것이다. 모든 행동을 한번씩 탐색한 뒤 가장 높은 추정값을 선택하게 된다. 초기에 최적행동을 선택할 가능성이 높을 지라도(스파이크), 초기에 선택한 추정값이 업데이트 되면서 나머지 추정값보다 낮아지게 될 때 행동 선택이 요동치게 된다.

초기값을 일괄적으로 설정한 뒤에 운좋게 초기에 탐욕적 행동 선택으로 최적 행동을 선택하더라도 가치 추정값이 업데이트되면서 요동을 피하기는 어려우므로, 처음 부분에 특별히 더 좋거나 나쁘게 만든다고 말하기가 어렵다. 하지만 정상적 문제에서 탐욕적 행동을 할지라도 좀 더 다양한 탐색을 유도할 수 있기 때문에 최적 행동의 성능이 향상 될 수 있다.

<br>

## Exercise 2.8

### Question: UCB 스파이크

그림 2.4에서 UCB 알고리즘은 11번째 단계의 성능에서 뚜렷한 스파이크를 보여준다. 왜 이런 현상이 생길까? 완전히 만족스러운 답변을 하려면 11번째 단계에서 왜 보상이 증가하는지, 그리고 왜 이어지는 단계에서는 감소하는지를 설명해야 한다. 힌트: ![equation](https://latex.codecogs.com/svg.latex?c=1) 이면 스파이크가 덜 두드러진다.

### Answer:

처음 행동을 선택할 때, ![equation](https://latex.codecogs.com/svg.latex?N_t(a)=0) 이므로 무작위로 한번씩 모든 행동을 선택하게 되고, 가치 추정값이 갱신된다. 11번째 단계에서는 가장 높은 가치 추정값을 가지는 행동을 선택하여, 평균 보상이 급격히 높아진다. 하지만 아직 추정값이 기대값에 근접하게 수렴하지 않으므로, 요동치는 가치 추정값에 따라 보상이 낮아지게 된다.

<br>

## Exercise 2.9

### Question:

행동이 두 개일 경우, 통계학과 인공지능 신경망에서 자주 사용되는 로지스틱 또는 시그모이드 함수로 주어지는 분포가 소프트맥스 분포와 같음을 보여라.

### Answer:

#### 소프트맥스 분포

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;Pr&space;\left&space;\{&space;A_t&space;=&space;a&space;\right&space;\}&space;&=&space;\frac{e^{H_t(a)}}{\sum_{b=1}^{k}e^{H_t(b)}}&space;\\&space;&=&space;\frac{e^{H_t(a)}}{e^{H_t(a)}&space;&plus;&space;e^{H_t(b)}}&space;\\&space;&=&space;\frac{1}{1&space;&plus;&space;e^{H_t(b)-H_t(a)}}&space;\end{align*}" title="\begin{align*} Pr \left \{ A_t = a \right \} &= \frac{e^{H_t(a)}}{\sum_{b=1}^{k}e^{H_t(b)}} \\ &= \frac{e^{H_t(a)}}{e^{H_t(a)} + e^{H_t(b)}} \\ &= \frac{1}{1 + e^{H_t(b)-H_t(a)}} \end{align*}" />

#### 시그모이드 함수(로지스틱 함수)

<img src="https://latex.codecogs.com/svg.latex?Pr&space;\left&space;\{&space;A_t&space;=&space;a&space;\right&space;\}&space;=&space;\frac{1}{1&space;&plus;&space;e^{-H_t(a)}}" title="Pr \left \{ A_t = a \right \} = \frac{1}{1 + e^{-H_t(a)}}" />

각 행동 행동 선호도 ![equation](https://latex.codecogs.com/svg.latex?H_t(a),&space;H_t(b)) 는 한 행동이 다른 행동에 대해 갖는 상대적 선호도만 중요하므로, ![equation](https://latex.codecogs.com/svg.latex?H_t(a)&space;>&space;H_t(b)) 이라고 가정하면 (또는 ![equation](https://latex.codecogs.com/svg.latex?H_t(a)&space;<&space;H_t(b)) ), 소프트맥스 분포와 시그모이드 함수에서 같은 방식으로 행동이 선택된다.

<br>

## Exercise 2.10

### Question:

행동 가치의 참값이 단계마다 무작위로 변하는 이중 선택 문제가 있다고 해 보자. 매 단계에서 행동 1과 2에 대한 가치의 참값이 0.5의 확률로 각각 0.1과 0.2인 경우(경우 A)와 0.5의 확률로 각각 0.9와 0.8인 경우(경우 B)를 가정해 보자. 어떤 단계가 어떤 경우에 해당하는지를 모른다고 할 때, 얻을 수 있는 최고의 기댓값은 얼마이며 그 기댓값을 얻기 위해서는 어떻게 행동해야하는가? 이제 매 단계가 어떤 경우인지를 안다고 하면(행동 가치의 참값은 여전히 모르지만), 이것은 연관 탐색 문제가 된다. 이 문제에서 얻을 수 있는 최고의 기댓값은 얼마이며, 그것을 얻기 위해 어떻게 행동해야 하는가?

### Answer:

1. 무작위로 이중 선택 문제 : 매 단계마다 무작위로 참값이 변하므로, 어떤 방법을 사용하던 기댓값은 0.5이다.  
   - 행동 1을 선택할 확률 * (경우 A가 나타날 확률 * 경우 A의 행동 1의 가치 참값 + 경우 B가 나타날 확률 * 경우 B의 행동 1의 가치 참값)
   - 행동 2를 선택할 확률 * (경우 A가 나타날 확률 * 경우 A의 행동 2의 가치 참값 + 경우 B가 나타날 확률 * 경우 B의 행동 2의 가치 참값)
2. 연관 탐색 문제 : 매 단계마다 어떤 경우인지 알수 있으므로 각 경우에 맞는 행동을 선택하면 되며, 이때 얻을 수 있는 최고의 기댓값은 0.55이다.  
   - 경우 A가 나타날 확률 * 경우 A의 최대 가치 참값 + 경우 B가 나타날 확률 * 경우 B의 최대 가치 참값
