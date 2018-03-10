# 题目一  <h1>
这里是内容
## 题目二 <h2>

- 条件一
- 条件二

> 这里引用一个名言

```C++
# include<iostream>
using namespace std;
int main()
{
	int a[100],i,j;
	int N,M,X;
	cin>>N>>M>>X;
	for(i=0;i<M;i++)
	cin>>a[i];
	for(int n=0;n<N;n++)
	{
	  for(i=1;i<=X;i++)
	  {
		int temp;
		temp=a[0];
		for(j=0;j<M-1;j++)
			a[j]=(a[j]+a[(j+1)%M])%100;
			a[M-1]=(a[M-1]+temp)%100; 
	for(i=0;i<M;i++)
	cout<<a[i]%100<<" ";
	cout<<endl;
}
}
	return 0;
}
```
