# ⚾ 1주차 숫자야구 게임

## 1. 게임 로직

### 1.1. 게임 시작

- 게임 시작 문구 출력
- 랜덤 숫자 제작

### 1.2. 게임 진행

- 사용자 입력 받기
- 유효성 검사 (숫자가 올바르게 입력 되었는지, 중복된 숫자는 없는 지 등)
- 올바르게 입력 되었다면 사용자 입력에 따른 스트라이크 or 볼 or 낫싱 계산

### 1.2. 게임 종료와 재시작

- 3 스트라이크가 나오면 모두 맞혔다는 문구 띄움 및 게임이 종료
- 재시작할지 종료할지 입력받음
- 유효성 검사 (1 or 2가 제대로 입력 되었는지)
- 재시작을 원한다면 상태를 다시 초기화

### 1.5. 폴더 구조

```
App.js
	- 메인 App.js
constant.js
	- 게임 상수 설정
util.js
	- 자주 쓰이는 유틸함수
```

## 2. 구현 기능 목록

- 사용자 입력값 유효성 검사
    - 3글자 인지?
    - 모두 숫자로 이루어져 있는지?
    - 1~9 사이의 숫자로 이루어져 있는지?
    - 세 수가 중복이 없는 유니크한 값인지?
    
    ⇒ 잘못된 값 입력 시 throw 문을 사용해 예외를 발생시키고 종료
    
- 판정
    - 숫자가 있으나 위치가 다른 경우 BALL
    - 숫자와 위치가 일치한 경우 STRIKE
    - 아무것도 일치하지 않으면 낫싱 (0볼0스트라이크)
- 판정 결과 출력
    - _볼 _스트라이크 / _볼 / _스트라이크 / 낫싱 형식으로 출력
    - 정답이면 (3스트라이크)
        - 정답을 맞췄다는 메시지 출력
        - 재시작 할지 입력값 받기
    - 정답이 아니면
        - 판정 결과 출력