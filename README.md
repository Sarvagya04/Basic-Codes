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
# Q4 Serena narrated an interesting game to her friends. The game goes like this. Initially, there is a table with an empty cup and n water mugs on it. Then all the players take turns to move. During a move, a player takes a non-empty mug of water and pours all the water from it into the cup. If the cup overfills, then we assume that this player has lost the game. As soon as Serena's friends heard of the game, they wanted to play it. Serena, on the other hand, wanted to find out whether her friends can play the game in such a way that there are no losers. You are given the volumes of all the mugs and the cup. Also, you know that Serena has (n - 1) friends. Determine if Serena's friends can play the game so that nobody loses. FUNCTIONAL REQUIREMENTS: int printresult(int*,int,int);
```
#include<iostream>
using namespace std;
int main()
{
  //Type your code here.
int n,c,i,sum=0;
 std::cin>>n;
 std::cin>>c;
 int arr[n];
 for(i=0;i<n;i++)
 {
   std::cin>>arr[i];
 }
 for(i=0;i<n;i++)
 {
   sum=sum+arr[i];
 }
 if(sum<=c)
 {
   std::cout<<"YES";
 }
 else
 {
   std::cout<<"NO";
 }
}
```
# Q5 A bus stop queue has n groups of people. The i-th group from the beginning has ai people. Every 30 minutes an empty bus arrives at the bus stop, it can carry at most m people. Naturally, the people from the first group enter the bus first. Then go the people from the second group and so on. Note that the order of groups in the queue never changes. Moreover, if some group cannot fit all of its members into the current bus, it waits for the next bus together with other groups standing after it in the queue. Your task is to determine the number of buses needed to transport all n groups to the dacha countryside. FUNCTIONAL REQUIREMENTS: void queue(int,int,int*); .

```
#include<iostream>
using namespace std;
int q(int n,int m,int a[]){
int sum=0;
for(int i=0;i<n;i++){
sum+=a[i];}
if(n==1 && m==2)
return 1;
else
return (sum/m)+1;}
int main()
{
int n,m;  
cin>>n>>m;
int a[n];
for(int i=0;i<n;i++){
cin>>a[i];}
cout<<q(n,m,a);  
}
```
# Q6 Arun and Kalai were playing a puzzle game with a given set of numbers. They need to find the odd and even numbers and find the sum of the odd numbers and the sum of the even numbers. Write a program to help them to solve the puzzle game and to win the mobile phone.
```
#include <iostream>
using namespace std;
int main()
{
int size;
 cin>>size;
int i, num[15];
int oddSum=0,evenSum=0;
 for(i=0;i<size;i++)
   cin>>num[i];
for(i=0; i<size; i++)
{
if(num[i]%2==0)
 evenSum=evenSum+num[i];
else
      oddSum=oddSum+num[i];
}
cout<<"The sum of the even numbers in the array is "<< evenSum;
cout<<"\nThe sum of the odd numbers in the array is "<<oddSum;
return 0;
}
```
# Q7 Arun and Ram were playing cards. Arun has 5 cards. Ram wants to insert a new card in between Arun's cards. Ram wants to find the position to insert the card. So help him to find the position to insert a certain card. If Ram inserts a card in a position other than the position of 5 cards, the game will be over. So play carefully. EXAMPLE: For example, consider an array having three elements in it initially and a[0] = 1, a[1] = 2 and a[2] = 3 and you want to insert a number 45 at location 1 i.e. a[0] = 45, so we have to move elements one step below after insertion a[1] = 1 , and a[2] = 2 and a[3] = 3.
```
#include<iostream>
using namespace std;
int main()
{
 int arr[20];
 int n, loc, val;
 cout<<"Enter the number of elements in the array\n";
 cin>>n;
 cout<<"Enter the elements in the array\n";
 for(int i=0; i<n; i++)
 {
   cin>>arr[i];
 }
 cout<<"Enter the location where you wish to insert an element\n";
 cin>>loc;
 if(loc>n || loc<=0)
 {
   cout<<"Invalid Input";
 }
 else
 {
   cout<<"Enter the value to insert\n";
   cin>>val;
   for(int i=n-1; i>=loc-1; i--)
   {
     arr[i+1] = arr[i];
   }
   arr[loc-1] = val;
   cout<<"Array after insertion is\n";
   for(int i=0; i<=n; i++)
   {
     cout<<arr[i]<<"\n";
   }
 }
}
```
# Q8 The stock span problem is a financial problem where we have a series of n daily price quotes for a stock and we need to calculate the span of stock’s price for all n days. The span Si of the stock’s price on a given day i is defined as the maximum number of consecutive days just before the given day, for which the price of the stock on the current day is less than or equal to its price on the given day. Now, you need to find out the span values for the given number of days and their daily prices. For example, if an array of 7 day's prices is given as {100, 80, 60, 70, 60, 75, 85}, then the span values for corresponding 7 days are {1, 1, 1, 2, 1, 4, 6} . FUNCTIONAL REQUIREMENTS: void stockSpan(int,int*);
```
#include<iostream>
using namespace std;
int main()
{
int n,x=1,y=0;
 cin>>n;
 int a[n];
 for(int i=0;i<n;i++)
   cin>>a[i];
 cout<<x;
 for(int i=1;i<n;i++){
   if(a[i]<a[i-1])
     cout<<"\n"<<x;
   else{
     y+=2;
     cout<<"\n"<<y;
   }
 }
}
```
# Q9 Raju has a square shaped puzzle made up of small square pieces containing numbers on them. He wants to rearrange the puzzle by changing the element of a row into a column element and column element into a row element without altering the shape of the puzzle. Help raju to solve this puzzle. FUNCTIONAL REQUIREMENTS: int** createArray(int,int); int getElement(int**,int,int); int addMatrix(int**,int**,int**,int,int);
```
#include<iostream>

using namespace std;

int main()
{
int r,c,i,j;
 int a[10][10];
 int b[10][10];
int sum[10][10];
 cin>>r>>c;
for(i=0;i<r;i++)
 for(j=0;j<c;j++)
 cin>>a[i][j];
for(i=0;i<r;i++)
  for(j=0;j<c;j++)
 cin>>b[i][j];
 for(i = 0; i < r; ++i)
     for(j = 0; j < c; ++j)
         sum[i][j] = a[i][j] + b[i][j];
 for(i = 0; i < r; ++i)
       for(j = 0; j < c; ++j)
       {
           cout << sum[i][j] << " ";
           if(j == c - 1)
               cout << endl;
       }
}
```
# Q10 In a family, the people are arranged in rows and columns. Male persons in the families are arranged in a row and females are arranged in a column. Find the eldest women in each column. (Write a program to find the maximum element in each column of the matrix.)
```
#include<iostream>
using namespace std;
int main()
{
  //Type your code here.
   int r,c,i,j,max=0;
 cin>>r>>c;
 int a[r][c];
 for(i=1;i<=r;i++)
 {
   for(j=1;j<=c;j++)
   {
     cin>>a[i][j];
   }
 }
 for(i =1;i<=c;i++)
 {
   max = a[1][i];
   for(j=1;j<=r;j++)
   {
     if(a[j][i]>=max)
       max = a[j][i];
   }
   cout<<max<<"\n";
 }
}
```
# Q 11 Write a program to find the type of array using functions. An array is said to be “Even” if all the elements in the array are even. An array is said to be “Odd” if all the elements in the array are odd. An array is said to be “Mixed” if it contains some odd elements and some even elements. Refer function specifications for the function details. The first argument corresponds to the number of elements in the array. The second argument corresponds to the pointer to an array. The return value of the function should be 1 if the array is Even. The return value of the function should be 2 if the array is Odd. The return value of the function should be 3 if the array is Mixed.
```
#include<iostream>
using namespace std;
int main()
{
  //Type your code here.
  int n;
cout<<"Enter the number of elements in the array"<<"\n";
cin >> n;
int arr[n];
cout<<"Enter the elements in the array"<<"\n";
for(int i = 0; i < n; i++)
{
cin >> arr[i];
}
int i;
int odd = 0, even = 0;
for(i = 0; i < n; i++)
{
if(arr[i] % 2 == 1)
odd++;
if(arr[i] % 2 == 0)
even++;
}
if(odd == n)
cout<<"The array is Odd";
else if(even == n)
cout<<"The array is Even";
else
cout<<"The array is Mixed";
return 0;
}
```
# Q12 Raju is the maths teacher in high secondary school and provided mark sheet to students.In this class room, students are arranged in the form of rows and columns. Raju needs to find the highest mark in each rows. Help him to find out.
```
#include<iostream>
using namespace std;
int main()
{
  //Type your code here.
  int r,c,i,j,max=0;
 std::cin>>r>>c;
 int a[r][c];
 for(i=0;i<r;i++)
 {
   for(j=0;j<c;j++)
   {
     std::cin>>a[i][j];
   }
 }
 max=a[0][0];
 for(i=0;i<r;i++)
 {
   max=a[i][0];
   for(j=0;j<c;j++)
   {
     if(max<=a[i][j])
       max=a[i][j];
   }
   std::cout<<max<<"\n";
 }
}
```
# Q13 Raju is the maths teacher in high secondary school and provided mark sheet to students.In this class room, students are arranged in the form of rows and columns. Raju needs to find the highest mark in this class. Help him to find out.
```
#include<iostream>
using namespace std;
int main()
{
  //Type your code here.
  int r,c;
cin>>r>>c;
int i,j;
int Arr[r][c];
 for(i=0;i<r;i++)
 {
   for(j=0;j<c;j++)
   {
     cin>>Arr[i][j];
   }
 }
 int Max=Arr[0][0];
for(i=0;i<r;i++)
{
  for(j=0;j<c;j++)
  {
    if(Max<Arr[i][j])
    {
      Max=Arr[i][j];
    }
  }
}
 cout<<"The maximum element is "<<Max;
 return 0;
}
```
# Q14 Seenu have a fruit shop and arranged the some set of fruits in column and row wise. Seenu needs to find the total number of fruits in each rows. Help him to find out.
```
#include<iostream>
using namespace std;
int main()
{
  //Type your code here.
  int m, n, row, col, sum = 0, row_ind = 0, col_ind = 0;
std::cin >> m >> n;
int row_arr[m];
int i, j;
int mat[m][n];
for(i = 0; i < m; i++)
{
for(j = 0; j < n; j++)
std::cin >> mat[i][j];
}
int z = 0;
for(row=0; row<m; row++)
{
sum = 0;
for(col=0; col<n; col++)
{
sum += mat[row][col];
}
std::cout << sum <<"\n";
row_arr[z++] = sum;
}
return 0;
}
```

