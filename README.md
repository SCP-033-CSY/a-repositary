# a-repositary
Just another repositary
#include <iostream>
#include <cctype>
using namespace std;
char exchange1 (char s);
void exchange3 (int x);
void output(int x);
int main()
{
	char s1[10], s2[10], s3[10], s4[10];
	int r,sum,i;
	scanf("%s %s %s %s", &s1, &s2, &s3, &s4);
	if (strcmp(s1, "整数") == 0 && strcmp(s3, "等于") == 0)
		r = 1;
	else
		r = 0;
	if (r == 0)
		printf("Input Error\n");
	else if (r == 1)
	{
		char s5[10], s6[10], s7[20];
		while (1)
		{
			i = exchange1(s7);
			if (strcmp(s6, "增加") == 0)
				sum = sum + i;
			else if (strcmp(s6, "减少") == 0)
				sum = sum - i;
			else if (strcmp(s5, "看看") == 0)
			{
				output(sum);
				break;
			}
		}
	}
}
char exchange1(char s)
{
	if (strcmp(s, "零") == 0)
		return 0;
	else if (strcmp(s, "一") == 0)
		return 1;
	else if (strcmp(s, "二") == 0)
		return 2;
	else if (strcmp(s, "三") == 0)
		return 3;
	else if (strcmp(s, "四") == 0)
		return 4;
	else if (strcmp(s, "五") == 0)
		return 5;
	else if (strcmp(s, "六") == 0)
		return 6;
	else if (strcmp(s, "七") == 0)
		return 7;
	else if (strcmp(s, "八") == 0)
		return 8;
	else if (strcmp(s, "九") == 0)
		return 9;
}
void exchange3(int x)
{
	if (x == 0)
		printf("零");
	else if (x == 1)
		printf("一");
	else if (x == 2)
		printf("二");
	else if (x == 3)
		printf("三");
	else if (x == 4)
		printf("四");
	else if (x == 5)
		printf("五");
	else if (x == 6)
		printf("六");
	else if (x == 7)
		printf("七");
	else if (x == 8)
		printf("八");
	else if (x == 9)
		printf("九");
}
void output(int x)
{
	int a, b;
	a = x / 10;
	b = x % 10;
	if (a == 0)
		printf("%s", exchange3(b));
	else if (a == 1)
		printf("十%s", exchange3(b));
	else if (a != 0 && a != 1)
		printf("%s十%s", exchange3(a), exchange3(b));
	else if (x < 0)
		printf("财政赤字");
}
