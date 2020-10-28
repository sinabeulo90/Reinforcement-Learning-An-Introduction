## Exercise 6.6

### Question:

예제 6.2에서 무작위 행보 예제의 실제 가치가 상태 A부터 E까지 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\frac{1}{6},\frac{2}{6},\frac{3}{6},\frac{4}{6},\frac{5}{6}) 라고 했었다. 이 값들을 계산하기 위한 최소 두 가지의 서로 다른 방법을 설명하라. 어떤 방법을 이 책에서 실제로 사용했을 것 같은가? 왜 그렇게 생각하는가?

### Answer:

상태 A에서 왼쪽 종단 상태로 갈 확률을 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;P_A(L)), 오른쪽 종단 상태로 갈 확률을 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;P_A(R)) 이라고 하면, 아래와 같이 계산할 수 있다.

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\begin{align*}&space;P_A(L)&space;&=&space;1&space;-&space;P_A(R)&space;\\&space;&=&space;1&space;-&space;P_A(B)&space;\cdot&space;P_B(R)&space;\\&space;&=&space;1&space;-&space;P_A(B)&space;\cdot&space;[P_B(A)&space;\cdot&space;P_A(R)&space;&plus;&space;P_B(C)&space;\cdot&space;P_C(R)]&space;\\&space;&=&space;1&space;-&space;0.5&space;\cdot&space;[0.5&space;\cdot&space;P_A(R)&space;&plus;&space;0.5&space;\cdot&space;0.5]&space;\\&space;1&space;-&space;P_A(L)&space;&=&space;0.5&space;\cdot&space;[0.5&space;\cdot&space;P_A(R)&space;&plus;&space;0.5&space;\cdot&space;0.5]&space;\\&space;P_A(R)&space;&=&space;0.5&space;\cdot&space;[0.5&space;\cdot&space;P_A(R)&space;&plus;&space;0.5&space;\cdot&space;0.5]&space;\\&space;P_A(R)&&space;=&space;\frac{1}{6}&space;\end{align*}" title="\begin{align*} P_A(L) &= 1 - P_A(R) \\ &= 1 - P_A(B) \cdot P_B(R) \\ &= 1 - P_A(B) \cdot [P_B(A) \cdot P_A(R) + P_B(C) \cdot P_C(R)] \\ &= 1 - 0.5 \cdot [0.5 \cdot P_A(R) + 0.5 \cdot 0.5] \\ 1 - P_A(L) &= 0.5 \cdot [0.5 \cdot P_A(R) + 0.5 \cdot 0.5] \\ P_A(R) &= 0.5 \cdot [0.5 \cdot P_A(R) + 0.5 \cdot 0.5] \\ P_A(R)& = \frac{1}{6} \end{align*}" />

상태 B부터 E에 대해 위와 같은 방식을 따르면, 무작위 행보 예제의 실제 가치를 구할 수 있다.