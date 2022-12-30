# java-racingcar-kakao

# 자동차 경주
### 구현할 기능 목록
- 자동차
  - [x] 4 이상일 경우 전진, 미만일 경우 정지하는 기능
- 게임
  - [x] 0~9의 수를 Random generate하는 기능
  - [x] 문자열 리스트를 받고 자동차들의 이름과 대수를 파악하여 생성하는 기능 (Cars 생성)
  - [x] 한 턴을 플레이하는 기능
  - [x] 주어진 수 만큼 턴을 반복하는 기능
  - [x] 게임 종료 후 우승자들을 판별해서 반환하는 기능
- UI
  - [x] 자동차들의 이름을 입력받고 리스트를 반환하는 기능 (5자 이내)
  - [x] 시도할 횟수를 입력하는 기능 (0이상의 정수)
  - [x] 턴 실행 결과를 출력하는 기능
  - [x] 최종 우승자를 출력하는 기능

### 리팩토링 목록
- 구현
  - [x] 패키지 구조 변경 (컨트롤러, 도메인)
  - [x] 변경되지 않는 필드 final로 선언
  - [x] RacingCar의 init 메서드를 생성자로 변경
  - [x] 랜덤 숫자 생성 기능을 따로 클래스로 분리
  - [x] 우승자 판별 메서드 stream을 이용해 리팩토링
  - [x] 클래스 내부에서만 사용하는 메서드는 private으로 선언
  - [x] String s와 같이 의미를 알 수 없는 변수명 수정
  - [x] 입력값이 잘못되면 잘못 입력되었다는 메시지를 출력
    - [x] parseCarNames 메서드를 view 에서 분리
    - [x] 자동차 이름 정보 클래스 생성
  - [x] 이름 글자 제한 유효성 검사 추가
  - [x] view 메서드 static으로 변경
  
- 테스트
  - [ ] 이름 글자 수 초과에 대해 테스트 코드 추가
  - [ ] RacingGameTest의 우승자 판별 테스트 조건 수정
  - [ ] @BeforeEach를 사용하여 공통적으로 사용할 객체 초기화
  - [x] 랜덤값 생성 인터페이스를 구현하고 람다를 이용해 테스트
  - [ ] 여러 값을 테스트할 때 어노테이션으로 클린코드 작성
  

# 문자열 계산기 
### 구현할 기능 목록
- [x] 문자열을 분리 후 더하는 기능
  - [x] 문자열을 숫자 리스트로 변환하는 기능
    - [x] 문자열을 split하는 기능
    - [x] 문자열을 숫자로 변환하는 기능
      - 빈 문자열 또는 null 값일 때 0 반환
      - 숫자 하나 입력시 해당 숫자 반환
      - 음수일 때 혹은 숫자가 아닐 때 RuntimeException
  - [x] 분리된 숫자들을 더해서 출력하는 기능
- [x] 커스텀 구분자를 추가하는 기능
  - [x] 문자열에서 커스텀 구분자를 추출하는 기능
- [x] 문자열 입출력 기능
- [x] 계산기 Controller

