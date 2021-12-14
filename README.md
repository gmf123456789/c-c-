#include<iostream>
using namespace std;
struct computer
{
	int op1, op2;
	char ch;
};
void fun（computer* pb，int n）					
{
	int i;
	for (i = 0; i < n; i++)
	switch (pb->ch)
	{
	case '+':cout << pb->op1 + pb->op2 << endl; break;
	case '-':cout << pb->op1 - pb->op2 << endl; break;
	case '*':cout << pb->op1 * pb->op2 << endl; break;
	case '/':if (pb->op2 == 0)
		cout << "不能被0除" << endl;
			else
		cout << pb->op1 / pb->op2 << endl;  break;
	default:cout << "运算符有错" << endl;
	}
}
int main()
{
	computer a[100];
	int n, i;
	cin >> n;
	for (i = 0; i < n; i++)
		cin >> a[1].op1 >> a[i].ch >> a[i].op2;
	fun(a,n);		//参数为结构体指针对象，
	return 0;
}
