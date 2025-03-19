# CX VEC

this is a header only library intended for vector linear algebra. It should work for both C and C++.

C++ should have their respective operator overloads. (this expects the `__cplusplus` macro to be defined)
(however this will change in the future, as instead, you can define `CX_OP_OVERLOAD` macro instead to freely support)

## how to use

Simply clone this repository, and copy the `cxvec.h` file into your project.

normally the header file acts as a definition only file unless macro the `CXVEC_IMPL_ONCE` has been defined.

examples of this:
```c
#include <stdio.h>

// effectively allow cxvec to act like a implementation file (cxvec.c)
#define CXVEC_IMPL_ONCE 
#include "cxvec.h"

int main(void) {
    Vec3f pt1 = {0f, -2.1f, 30.0f};

    Vec3f pt2 = {20f, 0f, 0f};

    Vec3f result = Vec3f_add(pt1, pt2);

    printf("result: ");
    Vec3f_fprint(result); // output: <20.00, -2.10, 30.00>

    return 0;
}
```

more functions shown in the header file. (may be documented here in the future)

LICENSED UNDER MIT-No-Attribution
