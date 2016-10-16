---
layout: post
title: C++ Class
---

start this blog with c++ codes.

```C++
#include <iostream>

using namespace std;

class USERDATA
{
public:
	//멤버 변수 선언
	int nAge;
	char szName[32];

	//멤버 함수 선언 및 정의
	void Print(void)
	{
		//nAge와 szName은 Prite()함수의 지역 변수가 아니다!
		printf("%d, %s\n", nAge, szName);
	}
};

int main(void)
{
	USERDATA user = { 10, "Thankyou" };
	user.Print();

	return 0;
}
```
