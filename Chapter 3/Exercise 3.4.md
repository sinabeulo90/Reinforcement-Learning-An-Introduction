## Exercise 3.4

### Question:

전이 확률 ![equation](https://latex.codecogs.com/svg.latex?p(s',r|s,a)) 에 대해 예제 3.3에 나온 표와 유사한 표를 만들어라. 그 표에는 ![equation](https://latex.codecogs.com/svg.latex?s,a,s',r,p(s',r|s,a))) 를 위한 열이 있어야 하고, ![equation](https://latex.codecogs.com/svg.latex?p(s',r|s,a)>0) 을 만족하는 모든 순서쌍 (![equation](https://latex.codecogs.com/svg.latex?(s',r,s,a))) 각각에 대해 하나의 행이 있어야 한다.

### Answer:

| ![equation](https://latex.codecogs.com/svg.latex?s) | ![equation](https://latex.codecogs.com/svg.latex?a) | ![equation](https://latex.codecogs.com/svg.latex?s') | ![equation](https://latex.codecogs.com/svg.latex?r) | | ![equation](https://latex.codecogs.com/svg.latex?p(s',r\|s,a)) |
|:-:|:-:|:-:|:-:|:-:|:-:|
| high | search | high | ![equation](https://latex.codecogs.com/svg.latex?r_{search}) | | ![equation](https://latex.codecogs.com/svg.latex?\alpha) |
| high | search | low | ![equation](https://latex.codecogs.com/svg.latex?r_{search}) | | ![equation](https://latex.codecogs.com/svg.latex?1-\alpha) |
| high | wait | high | ![equation](https://latex.codecogs.com/svg.latex?r_{wait}) | | 1 |
| high | wait | low | - | | 0 |
| low | search | low | ![equation](https://latex.codecogs.com/svg.latex?r_{search}) | | ![equation](https://latex.codecogs.com/svg.latex?\beta) |
| low | search | high | -3 | | ![equation](https://latex.codecogs.com/svg.latex?1-\beta) |
| low | wait | low | ![equation](https://latex.codecogs.com/svg.latex?r_{wait}) | |1 |
| low | wait | high | - | | 0 |
| low | recharge | high | 0 | | 1 |
| low | recharge | low | - | | 0 |