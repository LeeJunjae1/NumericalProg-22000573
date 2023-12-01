# myNP.h

```c
#include "../../include/myNP.h"
```

자신의 폴더에 위치에 있는 myNP.h라는 헤더파일 가져오는 방법

```c
#define		PI		3.14159265358979323846264338327950288419716939937510582
#include <stdio.h>
#include <stdlib.h>
#include <math.h>
```

PI 값 정의 실시

기본 library를 include 시키기



# TaylorSeries

* [sinTaylor()](#sinTaylor())
* [sindTaylor()](#sindTaylor())
* [cosTaylor()](#cosTaylor())
* [cosTaylor()](#cosTaylor())

## sinTaylor()

sin함수의 값을 알기 위해 taylor 함수를 이용한다. 프로그램 상에서는 10번째 항까지 구하고 나머지 항들을 버림을 실시한다.
$$
\sum_{k=0}^\infty(-1)^k\frac{x^{2k+1}}{(2k+1)!}
$$


```c
double sinTaylor(double _x);
```

**Parameters ** 

> _x:  각도를 의미 이때 radian이다

**Example code **

```c
#include "../../include/myNP.h"

int main(){
    double S_N = 0;
    double x=PI/3;
	S_N = sinTaylor(x);
    
    printf("%3.12f\n", S_N);
    return 0;
}
```

**output **

```
0.866025403784
```

**Warning ** 

* x는 double의 형식이어야 한다



## sindTaylor()

sin함수의 값을 알기 위해 taylor 함수를 이용한다. 프로그램 상에서는 10번째 항까지 구하고 나머지 항들을 버림을 실시한다.
$$
\sum_{k=0}^\infty(-1)^k\frac{x^{2k+1}}{(2k+1)!}
$$


```c
double sindTaylor(double _x);
```

**Parameters ** 

> _x:  각도를 의미 이때 degree이다

**Example code **

```c
#include "../../include/myNP.h"

int main(){
    double S_N = 0;
    double x=60;
	S_N = sindTaylor(x);
    
    printf("%3.12f\n", S_N);
    return 0;
}
```

**output **

```
0.866025403784
```

**Warning ** 

* x는 double의 형식이어야 한다



## cosTaylor()

cos함수의 값을 알기 위해 taylor 함수를 이용한다. 프로그램 상에서는 10번째 항까지 구하고 나머지 항들을 버림을 실시한다.
$$
\sum_{k=0}^\infty(-1)^k\frac{x^{2k}}{(2k)!}
$$


```c
double cosTaylor(double _x);
```

**Parameters ** 

> _x:  각도를 의미 이때 radian이다

**Example code **

```c
#include "../../include/myNP.h"

int main(){
    double S_N = 0;
    double x=PI/3;
	S_N = cosTaylor(x);
    
    printf("%3.12f\n", S_N);
    return 0;
}
```

**output **

```
0.500000000000
```

**Warning ** 

* x는 double의 형식이어야 한다



## cosdTaylor()

sin함수의 taylor 값을 알기 위해 사용. 프로그램 상에서는 10번째 항까지 구하고 나머지 항들을 버림을 실시한다.
$$
\sum_{k=0}^\infty(-1)^k\frac{x^{2k}}{(2k)!}
$$


```c
double cosdTaylor(double _x);
```

**Parameters ** 

> _x:  각도를 의미 이때 degree이다

**Example code **

```c
#include "../../include/myNP.h"

int main(){
    double S_N = 0;
    double x=60;
	S_N = cosdTaylor(x);
    
    printf("%3.12f\n", S_N);
    return 0;
}
```

**output **

```
0.500000000000
```

**Warning ** 

* x는 double의 형식이어야 한다
