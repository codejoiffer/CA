# 12.6

```
......
A:		.word		xFFFF 0010	;KBDSR的起始地址
......

		LW			R1, A(R0)
START:	LW			R2, 0(R1)	;测试是否有非零值
		BEQZ		R2, START
		LW			R1. A(R0)
		LW			R4, 0(R1)
		J			NEXT_TASK
```

# 12.7

```
......
B:			.word		xFFFF 0010	;IOSR的起始地址
......
			LW			R1, B(R0)
START:		LW			R2, 0(R1)
			ANDI		R3, R2, #2
			BWQZ		R3, START
......
```

```
......
C:			.word		xFFFF 0010	;IOSR的起始地址
......
			LW			R1, C(R0)
START:		LW			R2, 0(R1)
			ANDI		R3, R2, #1
			BWQZ		R3, START
......
```

# 12.8

在显示屏上按顺序打印26个小写英文字母
