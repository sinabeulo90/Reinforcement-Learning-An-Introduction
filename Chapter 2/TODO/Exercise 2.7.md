## Exercise 2.7

### Question: 편차 없는 고정 시간 간격 기법

이 장의 대부분에서 행동 가치를 추정하기 위해 표본평균을 이용했다. 그 이유는 표본평균을 사용하면 고정 시간 간격의 경우 발생하는 초기 편차를 없앨 수 있기 때문이다(식 2.6의 분석을 참고하라). 하지만 표본평균은 완전히 만족스러운 해결책은 아니다. 비정상적 문제에서는 형편없는 성능을 보일 수 있기 때문이다. 비정상적 문제에 대해 고정 시간 간격의 장점을 유지하면서도 편차를 없애는 것이 가능할까? 한 가지 방법은 특별한 행동에 대해 ![equation](https://latex.codecogs.com/svg.latex?n) 번째 보상을 처리하기 위해 다음과 같은 시간 간격을 이용하는 것이다.

![equation](https://latex.codecogs.com/svg.latex?\beta_n&space;\doteq&space;\alpha/\overline{o}_n)

여기서 ![equation](https://latex.codecogs.com/svg.latex?\alpha>0) 는 계속 사용하던 고정 시간 간격이고, ![equation](https://latex.codecogs.com/svg.latex?\overline{o}_n) 은 0에서 시작하는 값의 일반항이다.

![equation](https://latex.codecogs.com/svg.latex?\overline{o}_n&space;\doteq&space;\overline{o}_{n-1}&space;&plus;&space;\alpha(1-\overline{o}_{n-1}),\quad&space;\overline{o}_n&space;\doteq&space;0,&space;n&space;\geq&space;0) 인 경우

식 2.6과 같은 분석을 수행하여 
![equation](https://latex.codecogs.com/svg.latex?Q_n) 이 **초기 편차가 없는** 기하급수적 최신 가중 평균임을 보여라.

### Answer:

