# 1. 프로젝트 개요
### 1.1 프로젝트 이름
- 자동차 **경주**
  
### 1.2 프로젝트 설명
- 각 자동차가 경주해 우승한 자동차를 출력하는 프로젝트

---

# 2. 구현할 기능
### 2.1 입력 문구 출력 기능
- 사용자에게 경주할 자동차 이름을 입력하라는 안내 문구를 출력합니다.
  - 예시 : "경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)"
- 사용자에게 시도할 횟수를 입력하라는 안내 문구를 출력합니다.
  - 예시 : "시도할 횟수는 몇 회인가요?"

### 2.2 사용자 입력 기능
- camp.nextstep.edu.missionutils.Console 클래스를 사용하여 사용자로부터 입력을 받습니다.
- 입력한 문자열을 **반환**

### 2.3 검증 기능
- 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시킨 후 프로그램 종료
  #### 2.3.1 자동차 이름 길이 검증
  - 자동차 이름이 5자 초과일 경우 예외 발생
    - 예시 : "bowook,bo,wook"
  - 자동차 이름이 null 또는 공백일 경우 예외 발생
    - 예시 : " ,,wook"
  #### 2.3.2 자동차 이름 중복 검증
  - 자동차 이름이 중복될 경우 예외 발생
    - 예시 : "bo,wook,bo,wook"
  #### 2.3.3 시도 횟수가 숫자 검증
  - 시도 횟수가 숫자가 아닐 경우 예외 발생
    - 예시 : "a", "%" 등
  #### 2.3.4 시도 횟수의 유효성 검증
  - 시도 횟수가 0번 이하일 경우 예외 발생
    - 예시 : "0"

### 2.4 전진 기능
- camp.nextstep.edu.missionutils.Randoms의 pickNumberInRange()를 활용해 나온 값에 따라 전진하는 기능
- 나온 값이 4 이상일 경우 전진

### 2.5 정지 기능
- camp.nextstep.edu.missionutils.Randoms의 pickNumberInRange()를 활용해 나온 값에 따라 정지하는 기능
- 나온 값이 4 미만일 경우 정지

### 2.6 자동차 출력 기능
- 주어진 횟수가 한 번씩 진행될 때마다 자동차의 현재 상황을 출력하는 기능

### 2.7 최종 우승자 출력 기능
- 사용자에게 최종 우승자 안내 문구를 출력합니다.
- 예시 : "최종 우승자 : "

### 2.8 최종 우승자 판단하는 기능
- 각 자동차의 현재 위치를 확인한 후, 1등 자동차의 전진 횟수를 기준으로 하여 현재 위치가 1등 자동차의 전진 횟수와 같은 자동차의 이름을 반환
---

