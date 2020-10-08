## Exercise 4.5

### Question:

행동 가치에 대해서는 정책 반복이 어떻게 정의되는가? 98쪽에서 ![equation](https://latex.codecogs.com/svg.latex?v_*) 를 계산하는 것과 유사하게 ![equation](https://latex.codecogs.com/svg.latex?q_*) 를 계산하기 위한 완전한 알고리즘을 제시하라. 이 연습문제에 특별한 주의를 기울여야 한다. 이 문제에 포함된 개념을 이 책의 나머지 부분에서 계속 사용할 것이기 때문이다.

### Answer:

**1. 초기화**
> 모든 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;s&space;\in&space;\mathcal{S},&space;a&space;\in&space;\mathcal{A}) 에 대해 임의로 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Q(s,a)&space;\in&space;\mathbb{R}) 와 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\pi&space;\in&space;\mathcal{A}(s)) 를 설정
>
> 모든 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;s\in&space;S) 에 대해 빈 리스트를 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Policy(s)) 에 대입

<br>

**2. 정책 평가**
> 루프:
> > ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\Delta\leftarrow0)
> >
> > 모든 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;s&space;\in&space;\mathcal{S},&space;a&space;\in&space;\mathcal{A}) 에 대한 루프:
> >
> > > ![equation](https://latex.codecogs.com/svg.latex?\inline&space;q&space;\leftarrow&space;Q(s,a))
> > >
> > > ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Q(s,a)&space;\leftarrow&space;\sum_{s',r}&space;p(s',r|s,a)[r&space;&plus;&space;\gamma&space;\sum_{a'}\pi(a'|s')q(s',a')])
> > >
> > > ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\Delta&space;\leftarrow&space;\max(\Delta,&space;|q&space;-&space;Q(s,a)|))
> >
> ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\Delta&space;<&space;\theta) 를 만족할 때까지(추정 정밀도를 결정하는 작은 양수)

<br>

**3. 정책 향상**
> 안정적 정책 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\leftarrow&space;true)
>
> 모든 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;s&space;\in&space;\mathcal{S},&space;a&space;\in&space;\mathcal{A}) 에 대해:
>
> > 이전 행동 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\leftarrow&space;\pi(s)) 
> >
> > ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\pi(s)&space;\leftarrow&space;\text{arg}\max_aQ(s,a))
> >
> > ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\pi(s)) 가 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Policy(s)) 리스트에 존재하지 않을 경우, ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Policy(s)) 리스트에 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\pi(s)) 추가하고 안정적 정책 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\leftarrow&space;false)
> >
> 안정적 정책이 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;true) 이면 멈추고, ![equation](https://latex.codecogs.com/svg.latex?\inline&space;V&space;\approx&space;v_*) 와 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\pi&space;\approx&space;\pi_*) 를 반환하라. 그렇지 않으면, 2번 과정으로 돌아가라.
