# trove
//static 静态局部变量，还可以限制作用域（仅在本文件中运用）
void test()
 {
   static int a;
   a=1;
   a++;
   printf("%d\n",a);
 }
int main()
{
    int i=0;
    while(i<6)
    {
     test();
     i++;
    }
    return 0;
}



//相加函数
 int Add(int x,int y)
{    int z;
    z=x+y;
     return z;
 }
 //最大值函数
int Max(int x,int y)
{
    if(x>y)
    return x;
    else
    return y;
}
//指针变量，解引用符号（*）认识
int main()
{
    int a=10;
    int*p=&a;
    printf("%d\n",sizeof(p));
    *p=20;
    printf("%d\n",*p);    
    return 0;
    }  
 int main()
 {
     int arr[10]={55,44};
     printf("%d\n",arr[3]);

     return 0;
 }
//三目运算符？：
     int a,b,max;
     scanf("%d%d",&a,&b);
     max=(a>b?a:b);
     printf("%d",max);
//循环语句
     int line=0;
     while(line<200)
     {printf("好好敲代码！(%d)\n",line);
     line++;
    }
    if(line>=200)
     printf("good job!\n");


//选择语句
 {   int a;
     printf("你是否要好好学习？：（0/1）\n");
    scanf("%d",&a);     
    if(a==1)
     printf("good job!\n");
     else
     printf("bad kid\n");
//定义宏运用#define ?:
int main()
{
    #define Max(x,y) (x>y?x:y)
    int a,b,c;
    scanf("%d%d",&a,&b);
    c=Max(a,b);
    printf("c=%d\n",c);
    return 0;
}
//计算字符串长度strlen (以\0为结束标志，"\0"不作长度） 对+=，-=认识
 {   char arr[]="abc\0gugu";
     printf("%d\n",strlen(arr));
     int a;
     a=10;
    a+=50;
     printf("%d\n",a);

//extern 声明函数（可从其他文件调用函数）
int main()
{
     extern Add();
     int  a,b,sum,p,q,e;
   a=20;
    b=30;
     q=90;
     e=70;
     sum=Add(q,b);
    p=Add(a,e);
     printf("%d\n",sum);
     printf("%d\n",p);
        return 0;
}
//review
{   int input=0 ;
    printf("你是否要好好学习?(0/1):");
    scanf("%d",&input);
    if(input==1)
    printf("good!\n");
    else
   printf("bad\n");

    int line=0;
    printf("干就完了\n");
    while(line<20)
    {
    printf("敲一行代码：%d\n",line);
   line++;
   }
    if (line>=20);
    printf("获得一个好offer！");

    return 0;
}
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
//struct 认识结构体及其运用{}；（别忘引号后分号）
struct people
{ char name[20];
  int number;
  char address[30];
};
int main()
{
    struct people p1={"李华",123,"school"};
    struct people*pb=&p1;   //结构体指针
    printf("%d\n",(*pb).number);   //"."对结构体成员选择
    printf("%d\n",pb->number);  //"->"结构指针指向内容符号
    printf("姓名：%s\n",p1.name);
    printf("号码：%d\n",p1.number);
    printf("地址：%s\n",p1.address);
    p1.number=456;   //修改结构体内容
    printf("修改后号码：%d\n",p1.number);
    strcpy(p1.name,"张三");  //strcpy-库函数-要引用头函数<string.h>
    printf("修改后姓名：%s\n",p1.name);
    return 0;
}
//函数运用
int Max(int x,int y)
{
     if(x>y)
        return x;
    else
        return y;
}
//定义宏运用
#define MAX(X,Y)(X>Y?X:Y)
int main()
{
    int a=11;
    int b=55;
    int max=Max(a,b);
    printf("%d\n",max);
    max=MAX(a,b);
    printf("%d\n",max);

    return 0;
}
// void不用返回值，定义函数
void test()
 {
   static int a=1;   //有static a++值不固定，打印22222
   a++;                无static a++值固定为2，打印23456
   printf("a=%d\n",a);
 }
int main()
{
    int i=0;
    while(i<5)
    {
     test();
     i++;
    }
    return 0;
}

