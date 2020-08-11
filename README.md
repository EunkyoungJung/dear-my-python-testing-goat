# dear-my-testing-goat 🐐🐍

## 단위 테스트는 무엇인고, 기능 테스트와 어떤 차이가 있을까?
* 기능 테스트: 사용자 관점에서 애플리케이션 외부를 테스트
* 단위 테스트(Unit Test): 프로그래머 관점에서 그 내부를 테스트

=> 기능 테스트는 제대로 된 기능성을 갖춘 애플리케이션을 구축하도록 도우며,
그 기능성이 망가지지 않도록 보장해준다.
반면, 단위 테스트는 깔끔하고 버그 없는 코드를 작성하도록 돕는다.


## 테스트 작업 순서:
1. 기능 테스트를 작성해서 사용자 관점의 새로운 기능성을 정의
2. 기능 테스트가 실패하고 나면 어떻게 코드를 작성해야 테스트를 통과할지(또는 적어도 현재 문제를 해결할 수 있는 방법)를 생각해보도록 한다. 
   이 시점에서 하나 또는 그 이상의 단위 테스트를 이용해서 어떻게 코드가 동작해야 하는지 정의한다.
   (기본적으로 모든 코드가 (적어도) 하나 이상의 단위 테스트에 의해 테스트돼야 한다.)
3. 단위 테스트가 실패하고 나면 단위 테스트를 통과할 수 있을 정도의 최소한의 코드만 작성.
   기능 테스트가 완전해질 때까지 과정 2와 과정 3을 반복해야할 수도 있다.
4. 기능 테스트를 재실행해서 통과하는지 또는 제대로 동작하는지 확인한다.
   이 과정에서 새로운 단위 테스트를 작성해야 할 수도 있다.


## 단위 테스트-코드 주기
1. 터미널에서 단위 테스트를 실행해서 어떻게 실패하는지 확인한다.
2. 편집기상에서 현재 실패 테스트를 수정하기 위한 최소한의 코드를 변경한다.
그리고 1,2번을 반복한다.


## 알아두면 유용한 TDD 개념
1. 퇴행(Regression)장
   동작하고 있던 애플리케이션 처리가 새롭게 추가된 코드에 의해 망가지는 것
2. 예상치 못한 실패(Unexpected failure)
   우리가 생각하지 못한 방법으로 테스트가 실패하는 것
   - 테스트를 잘못 작성했거나, 테스트 자체가 코드 퇴행을 발견했다는 것을 의미
   - 애플리케이션 코드 수정이 필요하다는 의미
3. 레드(Red)/그린(Green)/리팩터(Refactor)
   - 테스트 작성해서 실패하는 지 보고(Red)
   - 코드를 수정해서 테스트를 통과하도록(Green)
   - 리팩터를 통해 코드를 개선(Refactor)
4. 삼각법(Triangulation)
   - 기존 코드에서 구체적인 테스트를 추가해서 일반화(편법이 될 수도 있는)한 처리를 정당화하는 것
5. 스트라이크 세 개면 리팩터(Three strikes and refactor)
   - 언제 중복 코드를 제거해야하는지 말해주는 일반적인 규칙
6. 작업 메모
   - 코딩을 하는 동안 우리가 해야 할 작업을 기록해두는 곳
