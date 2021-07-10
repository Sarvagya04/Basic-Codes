# Basic-Codes


# Compute a^n
```
#include<iostream>
using namespace std;
int pow(int a, int n)
{
 if(n!=0)
   return (a*pow(a,n-1));
   else
   {
     return 1;
   }
}
int main()
{
  //Type your code here.
  int a,n;
  std::cout<<"Enter the value of a"<<"\n";
  std::cin>>a;
  std::cout<<"Enter the value of n"<<"\n";
  std::cin>>n;
  std::cout<<"The value of "<<a<<" power "<<n<<" is "<<pow(a,n);
}
```
