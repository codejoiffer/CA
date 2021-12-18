# 6.9

1. 01000100
2. 0100
3. 0100
4. 11011101
5. 1101
6. 1101
7. 1011
8. 1000
9. 0101
10. 1101
11. 1000

# 6.16

输出整数i的二进制表示中1的个数

# 6.20

```c
#include <stdio.h>

int main(){
    int n;
    scanf("%d", &n);
    for(int i = 31; i >= 0; i --)
        printf("%d", (n>>i) & 1);
}
```

# 7.1

1. ![无标题的笔记本-2](https://i.loli.net/2020/11/13/dfBJ9aNYsmFOITL.jpg)Ⅰ. 0

   Ⅱ. 0

   Ⅲ. 1

2. ![无标题的笔记本-3](https://i.loli.net/2020/11/13/C9ZLDKijdQNrFvu.jpg)

   Ⅰ. 0

   Ⅱ. 1

   Ⅲ. 1

# 7.2

1. 

| A    | B    | C    | D    |
| ---- | ---- | ---- | ---- |
| 0    | 0    | 0    | 1    |
| 0    | 0    | 1    | 1    |
| 0    | 1    | 0    | 1    |
| 0    | 1    | 1    | 0    |
| 1    | 0    | 0    | 1    |
| 1    | 0    | 1    | 0    |
| 1    | 1    | 0    | 1    |
| 1    | 1    | 1    | 0    |

2.

![无标题的笔记本-4](https://i.loli.net/2020/11/13/D451gbZ73jMecNB.jpg)

# 7.3

当A, B输入不同时，上下的晶体管会连通

# 7.4

![无标题的笔记本-5](https://i.loli.net/2020/11/13/fBwQcXSpEG9Ny7C.jpg)

# 7.5

![无标题的笔记本-6](https://i.loli.net/2020/11/13/S8TGLIO5MzRmVgH.jpg)

# 7.6

![无标题的笔记本-7](https://i.loli.net/2020/11/13/kTugHixdtGyEPnq.jpg)

# 7.7

![无标题的笔记本-8](https://i.loli.net/2020/11/13/FwDck3SNRdE2ZLe.jpg)

# 7.8

![计基作业-9](https://i.loli.net/2020/11/13/AjrQ9b2WiBl6SIJ.jpg)



# 7.9

| A    | B    | C    | D    |
| ---- | ---- | ---- | ---- |
| 0    | 0    | 0    | 0    |
| 0    | 0    | 1    | 0    |
| 0    | 1    | 0    | 1    |
| 0    | 1    | 1    | 0    |
| 1    | 0    | 0    | 1    |
| 1    | 0    | 1    | 1    |
| 1    | 1    | 0    | 1    |
| 1    | 1    | 1    | 1    |

# 7.10

1. x = 0时,  S<sub>i</sub> = A<sub>i</sub> + B<sub>i</sub> + carry

   x = 1时, S<sub>i</sub> = A<sub>i</sub> + C<sub>i</sub> + carry

2. 

![计基作业-10](https://i.loli.net/2020/11/13/O6WLvGTcf2mQN9R.jpg)

# 7.11

1. 3

2. 3

3. 12

4. 96


# 7.12

1. 

| A    | B    | G    | E    | L    |
| ---- | ---- | ---- | ---- | ---- |
| 1    | 1    | 0    | 1    | 0    |
| 1    | 0    | 1    | 0    | 0    |
| 0    | 1    | 0    | 0    | 1    |
| 0    | 0    | 0    | 1    | 0    |

# 7.13

1. 不确定
2. 0
3. 是

# 7.14

2<sup>66</sup> B

2<sup>69</sup> b

 # 7.15

2<sup>15</sup>

# 7.16

1. A[1:0] 11
   WE 1
2. 4条
   不变

# 7.17

```c
#include <stdio.h>
#define FALSE 0
#define TRUE 1

int main(){
    char nextChar;
    int gotI = FALSE;
    int gotIN = FALSE;
    int count = 0;

    printf("Enter your string:");
    do{
        scanf("%c", &nextChar);
        switch(nextChar){
            case'i':
                gotI = TRUE;
                gotIN = FALSE;
                break;    
            case'n':
                if(gotIN)
                    gotIN = FALSE;
                if(gotI)
                    gotIN = TRUE;
                gotI = FALSE;
                break;
            case't':
                if(gotIN)
                    count++;
                gotI = FALSE;
                gotIN = FALSE;
                break;
            defalut:
            gotI = FALSE;
            gotIN = FALSE;
        }
    } while (nextChar != '\n');
    printf("count = %d\n", count);
}
```

