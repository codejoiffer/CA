# 15.1

4 1 -1

# 15.2

24 288 27648

# 15.3

```
x = 1, y = 2
x = 2, y = 1
x = 1, y = 2
```



# 15.9

bugs:

- main函数前未对Func1和Func2声明
-  `x = Func1(x, y);`这个语句传递参数数量错误
- `Func2`中对于局部变量y没有初始化数值

修改：

```c
#include <stdio.h>

int Func1(int x){
	return x + y;
}

int Func2(int x){
	return x - y;
}

int main(){
	int x = 1;
	int y = 2;
	
	x = Func1(x);
	y = Func2(x);
	
	printf("x = %d, y = %d\n", x, y);
}
```

