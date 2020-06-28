## Step2
최종 목표는 볼링 점수를 계산하는 프로그램을 구현한다. 1단계 목표는 점수 계산을 제외한 볼링 게임 점수판을 구현하는 것이다.
각 프레임이 스트라이크이면 "X", 스페어이면 "9 | /", 미스이면 "8 | 1", 과 같이 출력하도록 구현한다.
스트라이크(strike) : 프레임의 첫번째 투구에서 모든 핀(10개)을 쓰러트린 상태
스페어(spare) : 프레임의 두번재 투구에서 모든 핀(10개)을 쓰러트린 상태
미스(miss) : 프레임의 두번재 투구에서도 모든 핀이 쓰러지지 않은 상태
거터(gutter) : 핀을 하나도 쓰러트리지 못한 상태. 거터는 "-"로 표시
10 프레임은 스트라이크이거나 스페어이면 한 번을 더 투구할 수 있다.


1. 볼링 점수를 생성한다 - RandomGenerator
- 볼링점수 vo - o
- RandomScoreGenerator -> ScoreGenerator - o

2. 점수를 입력받으면 현재프레임 또는 다음 프레임을 반환한다. 
- abstract class Frame 
- NormalFrame : return this Or nextFrame - Score 누적
- FinalFrame : return totalScore
  
- Frame
    - Score: (총 합)
    - Type: STRIKE, SPARE, NONE     

- 결과) BowlingResults 
-> Map<Round, Frame> 

3. 입출력
- InputView: 사용자의 이름을 입력받는다 (영어 세글자) - GameUser (o)
- OutputView: 볼링 결과판을 출력한다(X, /) 


# 볼링 게임 점수판
## 진행 방법
* 볼링 게임 점수판 요구사항을 파악한다.
* 요구사항에 대한 구현을 완료한 후 자신의 github 아이디에 해당하는 브랜치에 Pull Request(이하 PR)를 통해 코드 리뷰 요청을 한다.
* 코드 리뷰 피드백에 대한 개선 작업을 하고 다시 PUSH한다.
* 모든 피드백을 완료하면 다음 단계를 도전하고 앞의 과정을 반복한다.

## 온라인 코드 리뷰 과정
* [텍스트와 이미지로 살펴보는 온라인 코드 리뷰 과정](https://github.com/next-step/nextstep-docs/tree/master/codereview)