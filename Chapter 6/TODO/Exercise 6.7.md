## Exercise 6.7

### Question:

임의의 목표 정책 ![equation](https://latex.codecogs.com/svg.latex?\pi) 및 보증하는 행동 정책 ![equation](https://latex.codecogs.com/svg.latex?b) 와 함께 사용될 수 있는 TD(0) 갱신의 비활성 정책 버전을 설계하라. 이때 매 시간 단계 ![equation](https://latex.codecogs.com/svg.latex?t) 에서 중요도추출비율 ![equation](https://latex.codecogs.com/svg.latex?\rho_{t:t}) (식 5.3)를 이용하라.

### Answer:

**![equation](https://latex.codecogs.com/svg.latex?\inline&space;V&space;\approx&space;v_\pi) 를 추정하기 위한 비활성 TD(0) 예측(정책 평가)**
> 입력: 임의의 목표 정책 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\pi)
>
> 모든 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;s&space;\in&space;S^+) 에 대해 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;V(s)) 를 임의의 값으로 초기화. 단 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;V)(종단) = 0
> 

> (각 에피소드에 대해) 무한 루프:
>
>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;b\leftarrow) 정책 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\pi) 가 보증된 임의의 정책
>>
>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;S) 를 초기화
>>
>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;G\leftarrow0)
>>
>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;W\leftarrow1)
>> 
>> 에피소드의 각 단계에 대한 루프:
>>
>>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;A\leftarrow&space;S) 에 대해 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;b) 에 따라 도출된 행동
>>>
>>> 행동 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;A) 를 취하고 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;R,S') 을 관측
>>>
>>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;C(S,&space;A)&space;\leftarrow&space;C(S,&space;A)&space;&plus;&space;W)
>>>
>>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;V(S)&space;\leftarrow&space;V(S)&space;&plus;&space;\frac{W}{C(S,&space;A)}[R&space;&plus;&space;\gamma&space;V(S')&space;-&space;V(S)])
>>>
>>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;W&space;\leftarrow&space;W&space;\frac{\pi(A|S)}{b(A|S)})
>>>
>>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;S&space;\leftarrow&space;S')
>>
>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;S) 가 종단이면 종료
