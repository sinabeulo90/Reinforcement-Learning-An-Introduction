## Exercise 6.11

### Question:

Q 학습이 **비활성** 정책 제어 방법으로 고려되는 이유는 무엇인가?

### Answer:

Q 학습은 현재 어떤 정책을 가지느냐에 관계없이, 다음 상태의 탐욕적 행동에 대한 가치 추정값을 통해 갱신이 되기 때문이다.

현재 상태-행동 쌍의 가치를 갱신하기 위해 필요한 이득은 '현재 상태에서 취한 행동의 보상'과 '탐욕적 정책을 따르는 다음 상태-행동 쌍의 가치 추정값'을 더한 값으로 계산하므로, 현재 정책과는 관련이 없다. 현재 정책은 단지 어떤 상태-행동 쌍을 마주치고 갱신할 것인가를 결정한다.
