# 📘 TIL - 2025-04-04

## 📍 공부한 내용
- [ 누구나 쉽게 즐기는 C언어 콘서트 ]
- [ chapter1 프로그래밍 소개, chapter2 기초사항 ]

## ✨ 핵심 정리
- 핵심 개념 1  
/* 이걸 사용해서 주석 넣기 여러줄 가능 */  
//한 줄 주석은 이렇게  
- 핵심 개념 2   
printf("형식지정자", 변수)  : "" 안의 내용을 콘솔화면에 출력하는 함수  
ex) printf("1+1=%d", sum)   
줄바꿈 하고싶을 땐 \n  
- 핵심 개념 3  
scanf_s("형식 지정자", &변수) : 키보드로부터 입력 된 데이터를 변환해 변수에 저장하는 함수  
ex) scanf_s(%d, &x)  
%d : 정수형, %f : 실수형  
- 핵심 개념 4   
변수란 프로그램이 사용하는 데이터를 일시적을 저장하는 목적으로 사용하는 메모리 공간  
정수형 : short, int, long long  
부동소수점형 : float, double, long double  
문자형 : char  
- 핵심 개념 5   
산술 연산자 - 덧셈 : +, 뺄셈 : -, 곱셈 : *, 나눗셈 : /, 나머지 : %  
- 핵심 개념 6  
형식 지정자 - %d : 정수형태 , %f/%lf : 실수형태, %c : 문자형태, %s :문자열 형태  

## 🔍 예제 코드 / 실습

```c
#include <stdio.h>

int main() {

	//총 여행비용을 계산해주는 프로그램을 작성해보자
	int day, airp, hotel, money, sum, total;
	printf("여행은 몇박인가요?: ");
	scanf_s("%d", &day);
	printf("항공권 가격: ");
	scanf_s("%d", &airp);
	printf("호텔 1박 가격: ");
	scanf_s("%d", &hotel);
	printf("하루에 필요한 용돈: ");
	scanf_s("%d", &money);
	total = airp + (hotel * day) + (money * (day + 1));
	printf("===============================\n");
	printf("총 여행 비용: %d\n", total);
	printf("===============================\n");
	printf(" 계속하려면 아무 키나 누르십시오 . . .\n");
}
