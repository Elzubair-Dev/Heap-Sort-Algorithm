# Heap-Sort-Algorithm
Heap Sort is one of the advanced sorting algorithms
      
#### - It is based on the heap concept which is based on the concept of complete binary tree
        
## Code:
```
using namespace std;
#include<iostream>
#include<algorithm>
void heapify(int arr[], int n, int i)
{
	int l = 2 * i + 1;
	int r = 2 * i + 2;
	int max = i;
	if (l<n && arr[l] > arr[max])
		max = l;
	if (r<n && arr[r] > arr[max])
		max = r;
	if (max != i)
	{
		swap(arr[i], arr[max]);
		heapify(arr, n, max);
	}
		
}
void build_heapify(int arr[], int n)
{
	for (int i = n / 2 - 1; i >= 0; i--)
	{
		heapify(arr, n, i);
	}
}
void HSort(int arr[], int n)
{
	build_heapify(arr, n);
	for (int i = n - 1; i >= 0; i--)
	{
		swap(arr[0], arr[i]);
		heapify(arr, i, 0);
	}
}
void Display(int arr[],int n)
{
	cout << "[ ";
	for (int i = 0; i < n; i++)
	{
		cout << arr[i] << " ";
	}
	cout << "]\n";
}
int main()
{
	int z[] = { 40,20,30,10 };
	int n = sizeof(z) / sizeof(z[0]);
	Display(z, n);
	HSort(z, n);
	cout << "\n--------------After Heap Sorting----------------\n\n";
	Display(z, n);
}
```
        
## Buy me a Coffee:  
      
if you want to support me 
(https://www.buymeacoffee.com/zu698air)
        
#### Don't forgit to give me a Star
      
## Done
