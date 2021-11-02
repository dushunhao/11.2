#define _CRT_SECURE_NO_WARNINGS 1

#include<stdio.h>

#include<math.h>

int main()

{

	int i = 0;
  
	for (i = 100; i < 1000; i++)
  
	{
  
		if (i == pow((i / 100), 3) + pow(((i / 10) % 10), 3) + pow((i % 10), 3))
    
		{
    
			printf("%d ", i);
      
		}
    

	}
  
	return 0;
  
}


int is_prime(int n)

{

	//2->n-1之间的数
  
	int j = 0;
  
	for (j = 2; j < n; j++)
  
	{
  
		if (0 == n % j)
    
			return 0;
      
	}
  
	return 1;
  
}


int main()

{

	//100-200之间的素数
  
	int i = 0;
  
	for (i = 100; i <= 200; i++)
  
	{
  
		//判断i是否为素数
    
		if (is_prime(i) == 1)
    
		{
    
			printf("%d ", i);
      
		}
    
	}
  
	return 0;
  
}


int is_prime(int n)

{

	//2->n-1之间的数
  
	int j = 0;
  
	for (j = 2; j <=sqrt(n); j++)
  
	{
  
		if (0 == n % j)
    
			return 0;
      
	}
  
	return 1;
  
}


int main()

{

	//100-200之间的素数
  
	int i = 0;
  
	for (i = 100; i <= 200; i++)
  
	{
  
		//判断i是否为素数
    
		if (is_prime(i) == 1)
    
		{
    
			printf("%d ", i);
      
		}
    
	}
  
	return 0;
  
}


int is_leap_year(int n)

{

	if (0 == n % 4 && n % 100 != 0 || (n % 400 == 0))
  
	{
  
		return 1;
    
	}
  
	else
  
	{
  
		return 0;
    
	}
  
}


int main()

{

	int y = 0;
  
	for (y = 1000; y <= 2000; y++)
  
	{
  
		if (1 == is_leap_year(y))
    
		{
    
			printf("%d ", y);
      
		}
    
	}
  
	return 0;
  
}


int is_leap_year(int n)

{

	return ((0 == n % 4 && n % 100 != 0 || (n % 400 == 0)));
  
}


int main()

{

	int y = 0;
  
	int count = 0;
  
	for (y = 1000; y <= 2000; y++)
  
	{
  
		if (1 == is_leap_year(y))
    
		{
    
			count++;
      
			printf("%d ", y);
      
		}
    
	}
  
	printf("\ncount=%d\n", count);
  
  return 0;
  
}



#include<string.h>

int binary_search(int a[], int k, int s)

{

	int left = 0;
  
	int right = s - 1;
  

	while (left <= right)
  
	{
  
		int mid = (left + right) / 2;
    
		if (a[mid] > k)
    
		{
    
			right = mid - 1;
      
		}
    
		else if (a[mid] < k)
    
		{
    
			left = mid + 1;
      
		}
    
		else
    
		{
    
			return mid;
      
		}
    
	}
  
	return -1;//找不到了
  
}


int main()

{

	int arr[] = { 1,2,3,4,5,6,7,8,9,10 };
  
	int key = 7;
  
	int sz = sizeof(arr) / sizeof(arr[0]);
  
	//找到就返回位置的下标
  
	//找不到就返回-1
  
	int ret = binary_search(arr, key, sz);
	
  
	if (-1 == ret)
  
	{
  
		printf("找不到\n");
    
	}
  
	else
  
	{
  
		printf("找到了，为:%d\n", ret + 1);
    
	}
  
	return 0;
  
}
