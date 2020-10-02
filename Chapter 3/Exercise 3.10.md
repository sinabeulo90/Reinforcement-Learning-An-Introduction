## Exercise 3.10

### Question:

식 3.10의 두 번째 부등식을 증명하라.

### Answer:

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;G_t&space;&\doteq&space;R_{t&plus;1}&space;&plus;&space;\gamma&space;R_{t&plus;2}&space;&plus;&space;\gamma^2&space;R_{t&plus;3}&space;&plus;&space;\cdots&space;&plus;&space;\gamma^{T-t-1}&space;R_T&space;\\&space;\gamma&space;G_t&space;&\doteq&space;\gamma&space;R_{t&plus;1}&space;&plus;&space;\gamma^2&space;R_{t&plus;2}&space;&plus;&space;\gamma^3&space;R_{t&plus;3}&space;&plus;&space;\cdots&space;&plus;&space;\gamma^{T-t}&space;R_T&space;\end{align*}" title="\begin{align*} G_t &\doteq R_{t+1} + \gamma R_{t+2} + \gamma^2 R_{t+3} + \cdots + \gamma^{T-t-1} R_T \\ \gamma G_t &\doteq \gamma R_{t+1} + \gamma^2 R_{t+2} + \gamma^3 R_{t+3} + \cdots + \gamma^{T-t} R_T \end{align*}" />

![equation](https://latex.codecogs.com/svg.latex?G_t) 와 ![equation](https://latex.codecogs.com/svg.latex?\gamma&space;G_t) 를 빼면,

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;G_t&space;-&space;\gamma&space;G_t&space;&=&space;R_{t&plus;1}&space;-&space;\gamma^{T-t}&space;R_T&space;\\&space;(1&space;-&space;\gamma)G_t&space;&=&space;R_{t&plus;1}&space;-&space;\gamma^{T-t}&space;R_T&space;\\&space;G_t&space;&=&space;\frac{R_{t&plus;1}&space;-&space;\gamma^{T-t}&space;R_T}{1&space;-&space;\gamma}&space;\end{align*}" title="\begin{align*} G_t - \gamma G_t &= R_{t+1} - \gamma^{T-t} R_T \\ (1 - \gamma)G_t &= R_{t+1} - \gamma^{T-t} R_T \\ G_t &= \frac{R_{t+1} - \gamma^{T-t} R_T}{1 - \gamma} \end{align*}" />

이 된다.

연속된 시간 단계에서 ![equation](https://latex.codecogs.com/svg.latex?\gamma<1,&space;\&space;T\rightarrow&space;\infty) 이고 식 3.10의 보상이 +1의 고정값이므로, ![equation](https://latex.codecogs.com/svg.latex?G_t&space;=&space;\frac{1}{1&space;-&space;\gamma}) 임을 알 수 있다.