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



# Interpolation

* [lagrangeInterpolation1()](#lagrangeInterpolation1())

## lagrangeInterpolation1()

lagrange 기법을 이용하여 interpolation을 실시한다. 이때 1차로 interpolation을 실시한다.
$$
y_q=y_i\frac{x_q-x_{i+1}}{x_i-x_{i+1}}+y_{i+1}\frac{x_q-x_i}{x_{i+1}-x_i}
$$


1. xq의 범위를 구한다.
2. 1차 라그랑제 interpolation 식에서 xq를 대입하여 yq를 구한다.

```c
double lagrangeInterpolation1(double* x, double* y, double xq, int m, int order);
```

**Parameters ** 

> x: x의 값들을 모아 놓은 배열
>
> y: y의 값들을 모아 놓은 배열
>
> xq: interpolation을 이용하여 대입할 값
>
> m: x의 배열안에 들어있는 요소들의 개수를 의미한다. 이때 x와 y의 요소의 개수는 같아야 한다.
>
> order: 차수를 의미, 여기서는 1차 라서 order는 1이다.

**Example code **

```c
#include "../../include/myNP.h"

int main(){
    double x[] = { 0, 10, 20, 30, 40, 50, 60, 70, 80 };
    double y[] = { 0.94, 0.96,1,1.05,1.07,1.09,1.14,1.17,1.21 };
    double xq = 75;
    int m= sizeof(x) / sizeof(x[0]);//data 사이즈 계산
    int order = 1;
    double lagrange = 0.;
    lagrange = lagrangeInterpolation1(x, y, xq, m, order);

    printf("yq is %f", lagrage);
    return 0;
}
```

**output **

```
yq is 1.190000
```

**Warning ** 

* x, y, xq는 double, m, order은 int의 형식이어야 한다.
* m은 x의 배열안에 들어있는 요소들의 개수를 의미한다. 이때 x와 y의 요소의 개수는 같아야 한다.
* order는 1이어야 한다.