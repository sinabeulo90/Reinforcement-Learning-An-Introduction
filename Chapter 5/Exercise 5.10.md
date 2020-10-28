## Exercise 5.10

### Question:

식 5.7로부터 가중 평균 갱신 규칙(식 5.8)을 유도하라. 가중치가 없는 규칙(식 2.3)을 유도하는 방식을 따르라.

### Answer:

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;V_{n&plus;1}&space;&\doteq&space;\frac{\sum_{k=1}^{n}&space;W_kG_k}{\sum_{k=1}^{n}&space;W_k}&space;\\&space;&=&space;\frac{W_nG_n&space;&plus;&space;\sum_{k=1}^{n-1}&space;W_kG_k}{\sum_{k=1}^{n-1}&space;W_k}&space;\frac{\sum_{k=1}^{n-1}&space;W_k}{\sum_{k=1}^{n}&space;W_k}&space;\\&space;&=&space;[\frac{W_nG_n}{\sum_{k=1}^{n-1}&space;W_k}&space;&plus;&space;V_n]&space;\frac{\sum_{k=1}^{n-1}&space;W_k}{\sum_{k=1}^{n}&space;W_k}&space;\\&space;&=&space;\frac{1}{\sum_{k=1}^{n}&space;W_k}&space;[W_nG_n&space;&plus;&space;V_n&space;\sum_{k=1}^{n-1}&space;W_k]&space;\\&space;&=&space;\frac{1}{\sum_{k=1}^{n}&space;W_k}&space;[W_nG_n&space;&plus;&space;V_n&space;\sum_{k=1}^{n-1}&space;W_k&space;&plus;&space;V_nW_k&space;-&space;V_nW_k]&space;\\&space;&=&space;V_n&space;&plus;&space;\frac{W_k}{\sum_{k=1}^{n}}[G_n&space;-&space;V_n]&space;\\&space;&=&space;V_n&space;&plus;&space;\frac{W_k}{C_n}[G_n&space;-&space;V_n]&space;\end{align*}" title="\begin{align*} V_{n+1} &\doteq \frac{\sum_{k=1}^{n} W_kG_k}{\sum_{k=1}^{n} W_k} \\ &= \frac{W_nG_n + \sum_{k=1}^{n-1} W_kG_k}{\sum_{k=1}^{n-1} W_k} \frac{\sum_{k=1}^{n-1} W_k}{\sum_{k=1}^{n} W_k} \\ &= [\frac{W_nG_n}{\sum_{k=1}^{n-1} W_k} + V_n] \frac{\sum_{k=1}^{n-1} W_k}{\sum_{k=1}^{n} W_k} \\ &= \frac{1}{\sum_{k=1}^{n} W_k} [W_nG_n + V_n \sum_{k=1}^{n-1} W_k] \\ &= \frac{1}{\sum_{k=1}^{n} W_k} [W_nG_n + V_n \sum_{k=1}^{n-1} W_k + V_nW_k - V_nW_k] \\ &= V_n + \frac{W_k}{\sum_{k=1}^{n}}[G_n - V_n] \\ &= V_n + \frac{W_k}{C_n}[G_n - V_n] \end{align*}" />
