# Basic-Codes




# Q1 
```
#include <iostream>
struct student
{
    char name[50];
    int roll;
    float marks;
};
int main() 
{
   //Your code goes here
  struct student s1;
 std::cout<<"Student Details"<<"\n";
 std::cin.getline(s1.name,50);
 std::cin>>s1.roll; std::cin>>s1.marks;
 std::cout<<"Name: "<<s1.name<<"\n"<<"Roll: "<<s1.roll<<"\n"<<"Marks: "<<s1.marks;
}
```
# Q2 Complex number calculator
```
#include<iostream>
int main()
{
int a,b,c,d,n;
std::cin>>n>>a>>b>>c>>d;
switch(n)
{
case 1:
std::cout<<(a+c)<<"+"<<(b+d)<<"i";
break;
case 2:
std::cout<<(a-c)<<"+"<<(b-d)<<"i";
break;
case 3:
std::cout<<((a*c)-(b*d))<<((b*c)+(a*d))<<"i";
break;
 default:
   std::cout<<"Invalid choice";
}
}
```
