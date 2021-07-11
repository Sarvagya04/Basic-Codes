# Basic-Codes
# Q1 The teacher who handles science for 3rd-standard class distributes the mark sheets to her students, she needs to find the highest mark among the "n" students. Help the teacher to find the maximum mark.
```
#include<iostream>
int main()
{
  // Type your code here
  int n,i,value,j;
std::cin>>n;
 int a[n];
 for( i=0; i<=n; i++)
 {
   std::cin>>a[i];
 }
     value=a[0]; 
 for(i=1;i<n;i++)
 {
   if(a[i]>value)
value=a[i];
}
std::cout<<value;
 return 0;
}
```


# Q2 Meera wrote SBI PO exam and was waiting for her result. After a week, SBI released the results on its website. On the website, she needs to click the results after that she will get a pdf. In that pdf, test passed candidate register numbers are displayed. Then, Meera has to check whether her register number is there or not. If her register number is found, then she has passed her exam. Otherwise, she failed.

```
#include<iostream>
int main()
{
  // Type your code here
   int n,arr[15],i,a,flag=0;
  std::cin>>n;
  for(i=0;i<n;i++)
  {
     std::cin>>arr[i];
  }
  std::cin>>a;
   for(i=0;i<n;i++){
     if(arr[i]==a){
        flag=1;
        break;
     }
    }
  if(flag==1)
     std::cout<<"She passed her exam";
  else
     std::cout<<"She failed";
 return 0;
}
```
# Q3 Raju has a square-shaped puzzle made up of small square pieces containing numbers on them. He wants to rearrange the puzzle by changing the elements of a row into a column element and column element into a row element. Help Raju to solve this puzzle.
```
#include<iostream>
int main()
{
    // Type your code here
  int rows, cols, a1[10][10], a2[10][10];
std::cin>>rows;
std::cin>>cols;
for (int i = 0;i<rows;i++ ) {
for (int j = 0;j < cols;j++ ) {
std::cin>>a1[i][j];
}
}
 for(int i=0;i<cols;i++)
 {
  for(int j=0;j<rows;j++)
   {
     std::cout<<a1[j][i]<<" ";
   }
   std::cout<<"\n";
 }
  return 0;
}
```
