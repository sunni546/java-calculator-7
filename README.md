# java-calculator-precourse

## 문자열 덧셈 계산기

입력한 문자열에서 선택한 구분자 사용하여, 숫자를 추출하고 더하는 계산기

## 구현 기능 목록

- [x] 입력 요구 메세지를 출력한다.
- [x] 문자열을 입력 받는다.
- [x] 구분자를 결정한다.
    - 기본 구분자(쉼표, 콜론)
        - 문자열이 숫자로 시작
    - 커스텀 구분자("//"와 "\n" 사이에 위치하는 문자)
        - 문자열이 "//"로 시작
- [x] 구분자를 통해 숫자를 추출한다.
- [x] 추출된 숫자를 더한다.
- [x] 덧셈 결과 메세지 출력한다.

### Exception

- 사용자가 잘못된 값을 입력할 경우, `IllegalArgumentException` 발생
    - [x] 시작 문자가 숫자나 "//"가 아닌 경우
    - 기본 구분자(쉼표, 콜론) 사용 - 숫자로 시작
        - [ ] <1> 숫자가 아닌 문자 중에서 기본 구분자 이외의 문자인 경우
        - [ ] <2> 마지막 문자가 숫자가 아닌 경우
    - 커스텀 구분자("//"와 "\n" 사이에 위치하는 문자) 사용 - "//"로 시작
        - [ ] "//" 이후에 "\n"가 없는 경우
        - [ ] 사이에 문자가 없는 경우
        - [ ] 사이에 문자가 숫자인 경우
        - [ ] 사이에 문자가 2개 이상인 경우
        - [ ] "\n" 이후의 문자열에서, 숫자가 아닌 문자 중에서 커스텀 구분자 이외의 문자인 경우

### 입출력 예시

### 입력

- 기본 구분자(쉼표, 콜론)와 양수로 구성된 문자열
    ```
    1,2:3
    ```

- 지정할 커스텀 구분자와 양수로 구성된 문자열
    ```
    //;\n1;2;3
    ```

### 출력

- 입력 요구 메세지
    ```
    덧셈할 문자열을 입력해 주세요.
    ```

- 덧셈 결과 메세지
    ```
    결과 : 6
    ```

### 실행 결과

- 기본 구분자(쉼표, 콜론) 사용
    ```
    덧셈할 문자열을 입력해 주세요.
    1,2:3
    결과 : 6
    ```

- 커스텀 구분자 사용
    ```
    덧셈할 문자열을 입력해 주세요.
    //,\n1,2,3
    결과 : 6
    ```
