# C语言基本数据类型

## 基础框架

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
int main()
{
    printf();
    return 0;
}
```



## 整型int

1.4b = 32bit

2.范围：-2147483648~2147483647

3.unsigned int：4byte=32bit

   范围：0~4294967295；

## 字符型char

声明

```c
char response;
char a,b;
```

初始化

```c
char grade='A';
printf("%c",grade)；
```

'A'表示字符常量

“A”表示字符串

### _Bool类型

1.用于表示布尔值 即逻辑值true（1）和false（0）

2.整数类型 实际仅占用1位存储空间

### 可移值类型：stdint.h和inttypes.h

```c
#include<stdio.h>
#include<inttypes.h>//支持可移值类型
int main(void)
[
	int32_t me32;//me32是一个32位有符号整型变量
	me32 = 45933945;
	printf("First,assume int32_t is int:");
	printf("me32 = %d\n", me32);
	printf("Instead,use a  \"macro\" from inttypes.h:");
	printf("me32 = % " PRId32 "\n", me32);
	return 0;
]
```

### float、double和long double

float:占32位

double：占64位 提高精度 减少舍入误差

ps.在浮点数后加f/F可覆盖默认设置 看作float；用l/L看作double；0x或0X为十六进制前缀

### 

### EOF文件结束标志

eof=end of file ->  -1

eof == ctrl+z

### static

可以修饰局部变量、全局变量、函数
修饰的变量可以被改变

### sqrt

为开平方的数学库函数 要引用include<math.h>

### goto语句

最常见用法：终止程序在某些深度嵌套的结构的处理过程 例如跳出两层或多层循环

```c
for()
    for()
        for()
        {
            if(disaster)
                goto error;
        }
error:
if()
return 0;
```

###### 关机程序

```c
#include<string.h>
#include<stdio.h>
int main()
{
    char input[20]={0};
    //shutdown -s -t 60
    //system() -执行系统命令的
    system("shutdown -s -t 60");
again:
    printf("你的电脑将在1min内关机 如果输入:我是猪,则取消关机");
    scanf("%s",input);
    if(strcmp(input,"我是猪")==0)
    {
        system("shutdown -a");
    }
    else
    {
        goto again;
    }
    return 0;
}
```

