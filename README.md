# Basic-Codes



# Addition of two arrays
```
#include<iostream>
int main()
{
    // Type your code here
int rows, cols, a1[10][10], a2[10][10], sum[10][10];
std::cin>>rows;
std::cin>>cols;
for (int i = 0;i<rows;i++ ) {
for (int j = 0;j < cols;j++ ) {
std::cin>>a1[i][j];
}
}
for (int i = 0;i<rows;i++ ) {
for (int j = 0;j<cols;j++ ) {
std::cin>>a2[i][j];
}
}
for (int i = 0;i<rows;i++ ) {
for (int j = 0;j<cols;j++ ) {
sum[i][j]=a1[i][j]+a2[i][j];
std::cout<<sum[i][j]<<" ";
}
 std::cout<<"\n";
}
return 0;
}
```
