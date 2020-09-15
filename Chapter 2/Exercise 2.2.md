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