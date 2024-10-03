## Round 1

https://drive.google.com/file/d/1ocXKZ8VOUABewi2VfbWMFdoO-Bjcaa-I/view?usp=drivesdk

#include <stdio.h> 
int fetchMajEle(int arr[], int n) { 
 int c= arr[0]; 
 int cnt = 1; 
 for (int i = 1; i < n; i++) { 
 if (arr[i] == c) { 
 cnt++; 
 } else { 
 cnt--; 
 } 
 if (cnt == 0) { 
 c = arr[i]; 
 cnt= 1; 
 } 
 } 
 cnt = 0; 
 for (int i = 0; i < n; i++) { 
 if (arr[i] == c) { 
 cnt++; 
 }
 } 
 if (cnt> n / 2) { 
 return c; 
 } else { 
 return -1; 
 } 
} 
int main() { 
 int arr[100], i, input; 
 printf("Enter number of elements: "); 
 scanf("%d", &input); 
 for(i=0; i < input; ++i) { 
 printf("Enter number%d: ",i+1); 
 scanf("%d", &arr[i]); 
 } 
 int n = input-1 / sizeof(arr[0]); 
 int majEle = fetchMajEle(arr, n); 
 if (majEle != -1) { 
 printf("The majority element is %d\n", majEle);  } else { 
 printf("There is no majority element in the array\n");  } 
 return 0;
}
