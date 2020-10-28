## Exercise 5.9

### Question:

2.4절에서 설명한 표본평균에 대해 점증적 구현을 사용할 수 있도록 최초 접촉 MC 정책 평가(5.1절)를 위한 알고리즘을 수정하라.

### Answer:

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;V_{n&plus;1}&space;&=&space;\frac{1}{n}\sum_{i=1}^{n}&space;G_i&space;\\&space;&=&space;\frac{1}{n}&space;(G_n&space;&plus;&space;\sum_{i=1}^{n-1}G_i)&space;\\&space;&=&space;\frac{1}{n}&space;(G_n&space;&plus;&space;(n-1)\frac{1}{n-1}\sum_{i=1}^{n-1}G_i)&space;\\&space;&=&space;\frac{1}{n}&space;(G_n&space;&plus;&space;(n-1)V_n)&space;\\&space;&=&space;\frac{1}{n}&space;(G_n&space;&plus;&space;nV_n&space;-&space;V_n)&space;\\&space;&=&space;V_n&space;&plus;&space;\frac{1}{n}[G_n&space;-&space;V_n]&space;\end{align*}" title="\begin{align*} V_{n+1} &= \frac{1}{n}\sum_{i=1}^{n} G_i \\ &= \frac{1}{n} (G_n + \sum_{i=1}^{n-1}G_i) \\ &= \frac{1}{n} (G_n + (n-1)\frac{1}{n-1}\sum_{i=1}^{n-1}G_i) \\ &= \frac{1}{n} (G_n + (n-1)V_n) \\ &= \frac{1}{n} (G_n + nV_n - V_n) \\ &= V_n + \frac{1}{n}[G_n - V_n] \end{align*}" />
