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



# Power and Factorial

* [Power()](#Power())
* [Factorial()](#Factorial())

## Power()

제곱계산하기 위해 사용 
$$
x^N
$$

```c
double power(double _x, int N);
```

**Parameters ** 

> _x:  N번 곱할 때 사용할 숫자
>
> N: _x의 곱을 반복을 할 숫자

**Example code **

```c
#include "../../include/myNP.h"

int main(){
    double x=2.0;
    int n=3;
    
    printf("%.2f",power(2,3));
    return 0;
}
```

**output **

```
8.00
```

**Warning ** 

* x는 double, n은 int의 형식이어야 한다



## Factorial()

1부터 x까지 더하기 위해 사용 
$$
x!
$$

```c
double double factorial(int _x);
```

**Parameters ** 

> _x:  1부터 차례대로 더할때 맨 마지막으로 더할 값

**Example code **

```c
#include "../../include/myNP.h"

int main(){
    double x=3.0;
    
    printf("%.2f",factorial(x));
    return 0;
}
```

**output **

```
6.00
```

**Warning ** 

* x는 int의 형식이어야 한다