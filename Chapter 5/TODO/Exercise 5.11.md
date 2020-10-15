## Exercise 5.11

### Question:

비활성 MC 제어를 위한 글상자 안의 알고리즘에서, ![equation](https://latex.codecogs.com/svg.latex?W) 갱신이 중요도추출비율 ![equation](https://latex.codecogs.com/svg.latex?\inline\frac{\pi(A_t|S_t)}{b(A_t|S_t)}) 를 포함하기를 기대했을 수도 있다. 하지만 그 대신 ![equation](https://latex.codecogs.com/svg.latex?W) 갱신은 ![equation](https://latex.codecogs.com/svg.latex?\inline\frac{1}{b(A_t|S_t)}) 을 포함한다. 그럼에도 불구하고 이것이 합당한 이유는 무엇인가?

### Answer:

어떤 상태에 놓여 있던 목표 정책이 항상 결정론적으로 행동하므로, ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\pi(A_t|S_t)=1) 으로 설정할 수 있다.
