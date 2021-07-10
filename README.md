# Basic-Codes

# Write a program to compute GCD of 2 numbers using recursion.
```
#include<iostream>
int gcd(int n1,int n2)
{
  int small=0,gcd=0;
 if(n1<n2)
 {
   small=n1;
 }
  else
    small=n2;
  while(small>=1)
  {
    if(n1%small==0&&n2%small==0)
    {
    gcd=small;
    break ;
  }
  small--;
}
}
int main()
{
  //Type your code here.
  int a,b;
  std::cin>>a>>b;
  std::cout<<"G.C.D of "<<a<<" and "<<b<<" = "<<gcd(a,b);
  return 0;
}
```
