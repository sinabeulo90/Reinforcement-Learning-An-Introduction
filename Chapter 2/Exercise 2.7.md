## Exercise 2.7

### Question: 편차 없는 고정 시간 간격 기법

이 장의 대부분에서 행동 가치를 추정하기 위해 표본평균을 이용했다. 그 이유는 표본평균을 사용하면 고정 시간 간격의 경우 발생하는 초기 편차를 없앨 수 있기 때문이다(식 2.6의 분석을 참고하라). 하지만 표본평균은 완전히 만족스러운 해결책은 아니다. 비정상적 문제에서는 형편없는 성능을 보일 수 있기 때문이다. 비정상적 문제에 대해 고정 시간 간격의 장점을 유지하면서도 편차를 없애는 것이 가능할까? 한 가지 방법은 특별한 행동에 대해 ![equation](https://latex.codecogs.com/svg.latex?n) 번째 보상을 처리하기 위해 다음과 같은 시간 간격을 이용하는 것이다.

![equation](https://latex.codecogs.com/svg.latex?\beta_n&space;\doteq&space;\alpha/\overline{o}_n)

여기서 ![equation](https://latex.codecogs.com/svg.latex?\alpha>0) 는 계속 사용하던 고정 시간 간격이고, ![equation](https://latex.codecogs.com/svg.latex?\overline{o}_n) 은 0에서 시작하는 값의 일반항이다.

![equation](https://latex.codecogs.com/svg.latex?\overline{o}_n&space;\doteq&space;\overline{o}_{n-1}&space;&plus;&space;\alpha(1-\overline{o}_{n-1}),\quad&space;\overline{o}_n&space;\doteq&space;0,&space;n&space;\geq&space;0) 인 경우

식 2.6과 같은 분석을 수행하여 
![equation](https://latex.codecogs.com/svg.latex?Q_n) 이 **초기 편차가 없는** 기하급수적 최신 가중 평균임을 보여라.

### Answer:

시간 간격의 크기가 ![equation](https://latex.codecogs.com/svg.latex?\beta_n) 인 기하급수적 최신 가중 평균은 아래와 같다.

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;Q_{n&plus;1}&space;&=&space;Q_n&space;&plus;&space;\beta_n[R_n-Q_n]&space;\\&space;&=&space;\beta_nR_n&space;&plus;&space;(1-\beta_n)Q_n&space;\\&space;&=&space;\beta_nR_n&space;&plus;&space;(1-\beta_n)[\beta_{n-1}R_{n-1}&space;&plus;&space;(1-\beta_{n-1})Q_{n-1}]&space;\\&space;&=&space;\beta_nR_n&space;&plus;&space;(1-\beta_n)\beta_{n-1}R_{n-1}&space;&plus;&space;(1-\beta_n)(1-\beta_{n-1})Q_{n-1}&space;\\&space;&=&space;\beta_nR_n&space;&plus;&space;(1-\beta_n)\beta_{n-1}R_{n-1}&space;&plus;&space;\cdots&space;&plus;&space;\prod_{i=2}^{n}(1-\beta_i)\beta_1R_1&space;&plus;&space;\prod_{i=1}^{n}(1-\beta_i)Q_1&space;\\&space;&=&space;\beta_nR_n&space;&plus;&space;\sum_{i=1}^{n-1}\prod_{j=i&plus;1}^{n}(1-\beta_j)\beta_iR_i&space;&plus;&space;\prod_{i=1}^{n}(1-\beta_i)Q_1&space;\end{align*}" title="\begin{align*} Q_{n+1} &= Q_n + \beta_n[R_n-Q_n] \\ &= \beta_nR_n + (1-\beta_n)Q_n \\ &= \beta_nR_n + (1-\beta_n)[\beta_{n-1}R_{n-1} + (1-\beta_{n-1})Q_{n-1}] \\ &= \beta_nR_n + (1-\beta_n)\beta_{n-1}R_{n-1} + (1-\beta_n)(1-\beta_{n-1})Q_{n-1} \\ &= \beta_nR_n + (1-\beta_n)\beta_{n-1}R_{n-1} + \cdots + \prod_{i=2}^{n}(1-\beta_i)\beta_1R_1 + \prod_{i=1}^{n}(1-\beta_i)Q_1 \\ &= \beta_nR_n + \sum_{i=1}^{n-1}\prod_{j=i+1}^{n}(1-\beta_j)\beta_iR_i + \prod_{i=1}^{n}(1-\beta_i)Q_1 \end{align*}" />

![equation](https://latex.codecogs.com/svg.latex?Q_n) 이 **초기 편차가 없다** 는 것을 증명하기 위해선 초기 편차를 가지는 항 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\prod_{i=1}^{n}(1-\beta_i)Q_1) 이 0이 되는 지를 확인해야 한다.

![equation](https://latex.codecogs.com/svg.latex?\overline{o}_n) 은 보상값이 1이고 고정 시간 간격 ![equation](https://latex.codecogs.com/svg.latex?\alpha) 를 가지는 기하급수적 최신 가중치 평균이므로, (식 2.6) 방법으로 정리하면 아래와 같다.

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\begin{align*}&space;\overline{O}_n&space;&=&space;\overline{O}_{n-1}&space;&plus;&space;\alpha[1-\overline{O}_{n-1}]&space;\\&space;&=&space;\cdots&space;\\&space;&=&space;(1-\alpha)^nQ_0&space;&plus;&space;\sum_{i=0}^{n-1}\alpha(1-\alpha)^n&space;\\&space;&=&space;\sum_{i=0}^{n-1}\alpha(1-\alpha)^n&space;\end{align*}" title="\begin{align*} \overline{O}_n &= \overline{O}_{n-1} + \alpha[1-\overline{O}_{n-1}] \\ &= \cdots \\ &= (1-\alpha)^nQ_0 + \sum_{i=0}^{n-1}\alpha(1-\alpha)^n \\ &= \sum_{i=0}^{n-1}\alpha(1-\alpha)^n \end{align*}" />

![equation](https://latex.codecogs.com/svg.latex?\overline{o}_1=\alpha) 일 때 ![equation](https://latex.codecogs.com/svg.latex?\beta_1=1) 이 되므로, ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\prod_{i=1}^{n}(1-\beta_i)) 의 나열되는 항들 중 ![equation](https://latex.codecogs.com/svg.latex?n=1) 인 항이 0이 된다. 따라서 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\prod_{i=1}^{n}(1-\beta_i)Q_1=0) 이 되므로 ![equation](https://latex.codecogs.com/svg.latex?Q_n) 이 초기 편차가 없는 기하급수적 최신 가중 평균임을 알 수 있다.
