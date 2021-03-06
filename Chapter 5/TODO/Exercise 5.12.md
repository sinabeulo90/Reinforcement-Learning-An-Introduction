## Exercise 5.12

### Question: 경주 트랙(프로그래밍)

그림 5.5에 보이는 것과 같은 회전 구간에서 경주용 자동차를 운전하는 것을 생각해 보자. 가능한 한 빨리 가기를 원하지만 트랙을 벗어날 정도로 빠르게 가는 것은 원하지 않는다. 이 단순화된 경주 트랙에서 자동차는 그림에 표시된 칸들에 해당하는 이산적인 격자점 중 하나에 위치해 있다. 속도 역시 이산적이고, 수많은 격자 칸이 매 시간 단계마다 수평과 수직 방향으로 이동한다. 행동은 속도 성분에 대한 증가량이다. 속도 성분이 전체 9개(3 X 3)의 행동에 대해 각 단계에서 +1, -1, 또는 0만큼 변화할 수 있다. 속도 성분은 모두 0이상이고 5보다 작은 것으로 제한되고, 시작 시각을 제외하고는 0이 될 수 없다. 각 에피소드는 무작위로 선택된 시작 상태들 중 하나에서 모든 속도 성분이 0인 채로 시작하여 자동차가 결승선을 지나가면 종료된다. 자동차가 결승선을 지나가기 전까지는 모든 단계에 대해 -1의 보상이 주어진다. 자동차가 트랙의 경계와 부딪히면 무작위로 선택된 출발선상의 임의의 위치로 돌아가게 되며, 모든 속도 성분은 0으로 초기화된 이후에 에피소드가 계속된다. 매 시간 단계마다 자동차의 위치를 갱신하기 전에, 투영된 경로가 트랙의 경계를 지나치는지 확인해야 한다. 자동차가 결승선을 지나치면 에피소드가 종료되지만, 그 밖의 다른 곳을 지나치면 자동차가 트랙의 경계를 지나친 것으로 보고 다시 출발점으로 보내진다. 문제를 좀 더 어렵게 만들기 위해, 매 시간 단계에서 애초 의도된 속도 증가량이 얼마이든 상관없이 0.1의 확률로 모든 속도 성분의 증가량을 0으로 만들겠다. 이 문제에 몬테카를로 방법을 적용하여 각각의 시작 상태로부터 최적 정책을 계산하라. 최적 정책을 따르는 여러 가지 상태-행동 궤적을 나타내어라(단, 이 궤적에 대해서는 잡음을 적용하지 마라).

### Answer:
