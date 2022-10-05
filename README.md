# 绿荫工作室2022年招新最终审核
### 请在本目录下或者本文件下提交项目代码/截图:

计1907李牧霖: 我在等着我的小学弟/学妹们提交文件~
#include <iostream>
#include <string>
using namespace std;
//二、进行排序 
//冒泡排序
void bubbling_sorting(int arr[], int len)
{
	//冒1 外循环
	for (int i = 0; i < len - 1; i++)
	{
		// 冒2 内循环
		for (int j = 0; j < len - i - 1; j++)
		{
			if (arr[j] > arr[j + 1])
			//冒3 交换
			{
				int temp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = temp;
			}
		}
	}
}
//三、打印数组
void printInto(int arr[], int len)
{

	for (int k = 0; k < len; k++)
	{
		cout << arr[k] << "  ";
	}
	cout << endl;
}
int main()
{
	//一、输入数字
	//建立数组
	const int len = 5;
	int arr[len] ;
	int a = 0;
	int b = 0;
	//插入数字
	cout << "请输入"  << len << "个正整数" << endl;
	while (cin >> a)
	{
		arr[b] = a;
		if (b < len - 1 )
			b++;
		else
			break;
	}
	cout << "排序前为：";
	printInto(arr, len);
	bubbling_sorting(arr, len);
	cout << "排序后为：";
	printInto(arr, len);
}

//思想：相邻 比较 若大 交换 循环  
