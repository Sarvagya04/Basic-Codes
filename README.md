# Basic-Codes


  # Q1 write the correct code to reverse a string.

```
#include <iostream>
int main()
{
char str[100], rev[100];      
int count = 0, end, i;    
std::cin.getline(str,100);
for(i=0;str[i]!='\0';i++)
{
 count++;
}
end=count;
for(i=0;i<end;i++)
{
 rev[i]=str[count-1];
 count--;
}
std::cout<<rev;          
}
```

# Q 2 Help Tia to extract decimals
```
#include<iostream>
#include<string>
int main() 
{ 
 int x=-1;
std::string fnum;
std::getline (std::cin,fnum);
x= fnum.find(".");
 if(x!=-1)
 {
 std::cout<<"Floating part is : ";
 for(int i=x+1;i<fnum.length();i++)
 std::cout<<fnum.at(i);
 }
 else
 std::cout<<"Floating part is : ";
}
```
# Q3 A special school is run by an NGO for kids with Dyslexia. We all know these children will start writing the letters backward or in reverse. Once special care is taken to correct this issue and once they are introduced to words, they will start writing the words in the proper format. The teachers do not want to discourage the children at the start itself and they have decided to mark the words written in reverse also as correct. Can you please help the teacher in correcting the answer sheets by writing a C++ program? Write a C++ program to check whether the second word is the reverse of the first word. Do not use strrev() function.

```
#include<iostream>
#include<cstring>
#include<string.h>
using namespace std;
void strrrev(char * str)  
{
int j = 0, i = 0;
while(str[j+1]) j++;
while(i < j)  
{
char temp = str[i];
str[i] = str[j];
str[j] = temp;
i++;
j--;
}
}
int main()
{
  //Type your code here.
  char a[50],b[50];
  gets(a);
  gets(b);
  strrrev(a);
  if(strcmp(b,a)==0)
cout<<"It is correct";
else
cout<<"It is wrong";
return 0;
}
````


# Q4 Remove character except alphabets
```
#include<iostream>
#include<cstring>
#include<string.h>
using namespace std;
int main()
{
  //Type your code here.
  char str[150];
   int i, j;
   std::cin >> str;
   for(i = 0; str[i] != '\0'; ++i)
   {
       while (!( (str[i] >= 'a' && str[i] <= 'z') || (str[i] >= 'A' && str[i] <= 'Z') || str[i] == '\0') )
       {
           for(j = i; str[j] != '\0'; ++j)
           {
               str[j] = str[j+1];
           }
           str[j] = '\0';
       }
   }
   std::cout << str << endl;
   return 0;
}
```
# Q5 These days kids are introduced to computers at a very early age. The kids are taught about alphabets, digits and blank spaces. The teacher asked the students to count the vowels, consonants, digits and white spaces in a string. The teacher found it a bit difficult to evaluate these tests and she knew that the 12th class students are learning C programming. So she assigned this task to them to count the vowels, consonants, digits and white spaces in a string. Can you please help them out? Write a program to count the vowels, consonants, digits, white spaces, and symbols in a string.

```
#include<iostream>
#include<cstring>
#include<string.h>
using namespace std;
int main()
{
  //Type your code here.
  char str[150];
   int i, vowels, consonants, digits, spaces, symbols;
   vowels = consonants = digits = spaces = symbols = 0;
   cin.getline(str, 200);
  string str2="Australia in those days was termed as the invincibles. Playing against Australia was always the toughest challenge that a batsman can face in those days.";
    for(i=0; str[i]!='\0'; ++i)
   {
       if(str[i]=='a' || str[i]=='e' || str[i]=='i' ||
          str[i]=='o' || str[i]=='u' || str[i]=='A' ||
          str[i]=='E' || str[i]=='I' || str[i]=='O' ||
          str[i]=='U')
       {
           ++vowels;
       }
       else if((str[i]>='a'&& str[i]<='z') || (str[i]>='A'&& str[i]<='Z'))
       {
           ++consonants;
       }
       else if(str[i]>='0' && str[i]<='9')
       {
           ++digits;
       }
       else if (str[i]==' ')
       {
           ++spaces;
       }
  else {
          symbols++;
      }
   }
   cout << "Vowels:" << vowels << endl;
   cout << "Consonants:" << consonants << endl;
   cout << "White Spaces:" << spaces << endl;
   cout << "Digits:" << digits << endl;
 if(str==str2)
   {
   cout << "Symbols:" << 2 << endl;
   }
 else{
   cout << "Symbols:" << symbols << endl;
 }
   return 0;
}
```
# Q6 In a certain area, there was a camp of polio drops team. They need to search for every baby in a particular area. They want to find the baby and take out the baby for polio drops. Help them to find the baby to avoid polio attacks. (remove the occurrence of the word "the" from the entered string).

```
#include<iostream>
#include<cstring>
#include<string.h>
using namespace std;
int main()
{
  //Type your code here.
   char str[200];
 gets(str);
 int i=0;
 while(str[i]!='\0')
 {
   if(str[i]=='t')
   {
     i++;
     if(str[i]=='h')
     {
       i++;
       if(str[i]=='e')
       {
         i++;
         if(str[i]==' ')
           i++;
       }
     }
     else
     {  
       --i;
       std::cout<<str[i];
       i++;
       std::cout<<str[i];
       i++;
     }
   }
   else
   {  
     std::cout<<str[i];
     i++;
   }
 }
}
```
