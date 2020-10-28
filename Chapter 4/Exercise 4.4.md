## Exercise 4.4

### Question:

98쪽에 있는 정책 반복 알고리즘에는 미묘한 오류가 있다. 바로 두 개 이상의 최적 정책 사이에 계속해서 정책 반복이 수행된다면 정책 반복이 끝없이 진행된다는 것이다. 교육적 목적에서는 이 오류가 문제가 되지 않지만, 실제 활용에서는 문제가 된다. 수렴성이 보장되도록 의사코드를 수정하라.

### Answer:

**1. 초기화**
> ...
>
> [+] 모든 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;s\in&space;S) 에 대해 빈 리스트를 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Policy(s)) 에 대입

**3. 정책 향상**
> ...
> > ...
> >
> > [-] 이전 행동 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\neq&space;\pi(s)) 이면, 안정적 정책 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\leftarrow&space;false)
> >
> > [+] ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\pi(s)) 가 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Policy(s)) 리스트에 존재하지 않을 경우, ![equation](https://latex.codecogs.com/svg.latex?\inline&space;Policy(s)) 리스트에 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\pi(s)) 추가하고 안정적 정책 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\leftarrow&space;false)
>
> ...
