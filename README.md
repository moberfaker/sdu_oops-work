# sdu_oops-work
网安21-刘晨曦

输入4时，不会Javascript，用C++编写了一段类似的试了一下：得出结果
1 3 6 10 ？ ？ 
2 5 9 ？ ？
4 8 ？ ？
7 ？ ？
//以下为翻译的代码，不知道对不对

int main()
{
	int inp;
  
	cin >> inp;
	const int line = inp;
	unsigned short res[99][99];
	res[0][0] = 1;

	for(int i = 1;i < line;i++)
	{
		res[0][i] = res[0][i - 1] + i + 1;
    res[i][0] = res[i - 1][0] + i;
	}    

	 for(int lineCount = 1;lineCount < line;lineCount++)
   {        
   for(let j = 1; j < line - lineCount;j++){
         res[lineCount][j] = res[lineCount][j-1] + lineCount + j + 1
   }
  
	for (int i = 0; i <= line-1; i++) 
	{
		（int j = 0; j <line -i-1; j = ] ）
		{
			cout << res[i][j] << " ";
		}
		cout << endl;
	}

	return 0;
}


//以下为我自己编写的代码：

unsigned short number[101][101]{0};
int main()
{
	unsigned short aim_line;
	cin >> aim_line;												//输入行数

	for (int i = 1; i <= aim_line; i++) 
	{
		for (int j = 1; j <= aim_line - i + 1; j++) 
		{
			if (i == 1) { number[i][j] = number[i][j - 1] + j; }	//公式计算
			else { number[i][j] = number[i - 1][j] + i + j - 2; }	//公式计算

			cout << number[i][j] << " ";
		}
		cout << endl;
	}

	system("pause");
	return 0;
}





