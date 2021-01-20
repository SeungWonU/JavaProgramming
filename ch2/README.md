# 2.자바 기본(Scanner, 비트 논리)

## 타입 변환

- 작은 타입 → 큰 타입 ( 자동 변환)    ex) long m = 25;
- 큰 타입 → 작은타입(강제 타입 변환) ex) int n = 30;  byte b = (byte)n;  -> 데이터 손실 발생!!
- 강제 타입 변환 : 캐스팅(casting)

## 키 입력(System.in)

- System.in 은 키보드 장치를 제어하고 키 입력을 받는 표준 **입력 스트림 객체**이다.
- 이는 입력받은 키를 단순한 바이트 정보로 전달하므로 변환해야하는 번거로움이 있다.
- 따라서 Scanner를 통해 원하는 타입으로 변환해주는 클래스를 사용한다.

## Scanner

- Scanner scanner =  new Scanner(System.in)  :  객체 생성
- java.util 패키지 안에 있다(import java.util.Scanner)
- Scanner는 공백으로 구분한다!(' ' , '\t' , '\n')
- 정수 입력 받기 :  int age  = scanner.nextInt()
- nextLine()은 한 줄이고 next()는 공백이 나올때 까지
- 마지막 scanner.close()

# 증감 연산

- ++a : a를 1 증가시키고 증가 전의 값 반환
- a++ : a를 1증가시키고 증가 된 값 반환

## 비트 연산

- 비트 논리 연산 : AND, OR, XOR, NOT
- 비트 시프트 연산 : 오른쪽이나 왼쪽으로 이동

### 비트 논리 연산

a&b : 모두 1이면 1

a | b : 모두 0이면 0

a^b : 다르면 1,같으면 0

~a : 1→0 , 0 →1

### 비트 시프트 연산

- a>>b : a의 각 비트를 오른쪽으로 b번 이동, 최상위 비트의 빈자리는 시프트 전의 최상위 비트로 채움
- a >>>b : 위와 같고 최상위 비트의 빈자리는 항상 0으로 채움
- a << b : a의 각 비트를 왼쪽으로 b번 쉬프트, 최하위 빈자리는 항상 0 으로 채움

## Switch 문

- switch문의 '식'을 먼저 계산하고 그 결과 값과 일치하는 case 문으로 분기한다. 만약 break를 만나면 벗어난다. default는 if문의 else와 같다.

```java
switch(식){
	case 값1:
			실행문장 1;
			break;
	case 값2:
			실행문장 2;
			break;
	deafault:
			실행문장 3;
}
```