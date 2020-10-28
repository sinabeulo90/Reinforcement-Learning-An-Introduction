## Exercise 6.12

### Question:

행동 선택이 탐욕적이라고 가정하자. 그렇다면 Q 학습은 살사와 정확히 같은 알고리즘이 되는가? Q 학습과 살사가 정확히 동일하게 행동 선택과 가중치 갱신을 수행할까?

### Answer:

**![equation](https://latex.codecogs.com/svg.latex?\inline&space;Q&space;\approx&space;q_*) 를 추정하기 위한 살사(활성 정책 TD 제어)**

>> ...
>>
>> 에피소드의 각 단계에 대한 루프:
>>
>>> 행동 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;A) 를 취하고, ![equation](https://latex.codecogs.com/svg.latex?\inline&space;R,S') 을 관측
>>> 
>>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Q)로부터 유도된 정책을 사용하여 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;S') 으로부터 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;A') 을 선택
>>>
>>> ![equation](https://latex.codecogs.com/svg.latex?Q(S,&space;A)&space;\leftarrow&space;Q(S,&space;A)&space;&plus;&space;\alpha&space;[R&space;&plus;&space;\gamma&space;Q(S',&space;A')&space;-&space;Q(S,&space;A)])
>>>
>>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;S&space;\leftarrow&space;S';&space;A&space;\leftarrow&space;A';)
>>
>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;S) 가 종단이면 종료

살사는 현재 상태-행동 쌍의 가치를 갱신할 떄, 다음 상태와 다음 상태의 행동을 미리 결정한다. 갱신을 마치면, 다음 상태와 다음 상태의 행동을 기준으로 갱신을 준비한다.

만약 현재 상태와 다음 상태가 동일할 경우 행동 선택이 탐욕적이라면, 갱신을 수행할 때 현재 상태에서 선택하는 행동과 다음 상태에서 선택하는 행동이 동일 할 것이다.

**![equation](https://latex.codecogs.com/svg.latex?\inline&space;\pi&space;\approx&space;\pi_*) 를 추정하기 위한 Q 학습(비활성 정책 TD 제어)**

>> ...
>>
>> 에피소드의 각 단계에 대한 루프:
>>
>>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Q)로부터 유도된 정책을 사용하여 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;S') 으로부터 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;A') 을 선택
>>> 
>>> 행동 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;A) 를 취하고, ![equation](https://latex.codecogs.com/svg.latex?\inline&space;R,S') 을 관측
>>>
>>> ![equation](https://latex.codecogs.com/svg.latex?Q(S,&space;A)&space;\leftarrow&space;Q(S,&space;A)&space;&plus;&space;\alpha&space;[R&space;&plus;&space;\gamma&space;Q(S',&space;A')&space;-&space;Q(S,&space;A)])
>>>
>>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;S&space;\leftarrow&space;S')
>>
>> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;S) 가 종단이면 종료

Q 학습은 현재 상태-행동 쌍의 가치를 갱신할 떄, 다음 상태만 필요하다. 갱신을 마치면, 다음 상태를 기준으로 정책에 따라 행동을 새로 선택하고 갱신을 준비한다.

만약 현재 상태와 다음 상태가 동일할 경우 행동 선택이 탐욕적이라면, 갱신을 수행할 때 선택되는 행동들은 현재 마주치는 상태에 따라 매번 바뀔 수 있다.