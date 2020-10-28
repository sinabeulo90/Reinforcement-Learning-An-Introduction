## Exercise 5.4

### Question:

몬테카를로 ES에 대한 의사코드는 비효율적이다. 각각의 상태-행동 쌍에 대해 모든 이득의 리스트를 유지하고 반복적으로 그들의 평균을 계산하기 때문이다. 2.4절에서 설명한 것과 유사한 기술을 사용하는 편이 더 효율적일 것이다. 즉, 평균과 (각 상태-행동 쌍의) 개수를 유지하고 이 값들을 점진적으로 갱신하는 것이다. 이렇게 하려면 의사코드를 어떻게 수정해야 하는지 설명하라.

### Answer:

**초기화**
> ...
>
> [-] 모든 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;s\in&space;S,&space;a\in&space;A(s)) 에 대해 빈 리스트를 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Returns(s)) 에 대입
>
> [+] 모든 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;s\in&space;S,&space;a\in&space;A(s)) 에 대해 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Q(s,a)&space;\leftarrow&space;0)
>
> [+] 모든 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;s\in&space;S,&space;a\in&space;A(s)) 에 대해 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;N(s,a)&space;\leftarrow&space;0)

**(각 에피소드에 대해) 무한 루프**
> ...
> > ![equation](https://latex.codecogs.com/svg.latex?\inline&space;G) 에 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\gamma&space;G+R_{t+1}) 을 대입
> >
> > [+] ![equation](https://latex.codecogs.com/svg.latex?\inline&space;N(s,a)&space;\leftarrow&space;N(s,a)+1)
> >
> > [+] ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Q(s,a)&space;\leftarrow&space;Q(s,a)+\frac{1}{N(s,a)}[G-Q(S,a)])
> >
> > > ...
> > >
> > > [-] ![equation](https://latex.codecogs.com/svg.latex?\inline&space;average(Returns(S_t,A_t))) 를 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Q(S_t,A_t)) 에 대입
> > >
> > > ...
> >
>
