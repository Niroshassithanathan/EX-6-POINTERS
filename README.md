# EX-6-A-POINTERS
## AIM :
write a C program to find area of a circle & perimeter of a circle for the radius 35 using
pointer
## AIGORITHAM :
1.Start

2.Declare a pointer variable for the radius and initialize it to 35.

3.Create functions to calculate the area and perimeter of the circle:

a. Calculate the area using the formula area = π * r * r, where π is approximately 3.14159.

b. Calculate the perimeter (circumference) using the formula perimeter = 2 * π * r.

4.Use pointers to calculate and store the area and perimeter.

5.Print the calculated area and perimeter.

6.End.
## PROGARM :
```
# include <stdio.h>
int main()
{
float r,*a=&r;
scanf("%f",&r);
float area = (3.14*(*a)*(*a));
float peri = (2*3.14*(*a));
printf("Area of Circle = %.2f\n",area);
printf("Perimeter of Circle = %.2f",peri);
}
```
## OUTPUT :
![image](https://github.com/Niroshassithanathan/EX-6-POINTERS/assets/121418437/499582db-4fd8-4f7c-8c76-d6ee462f3326)

## RESULT :
Thus , The C program has been executed successfully.
# EX-6-B-DYNAMIC MEMORY ALLOCATION
## AIM :
Write a C program to count total number of odd elements in the following array 33,55,302,231,250 using malloc()
## AIGORITHAM :
1.Start

2.Declare a pointer to an integer to represent the array.

3.Declare a variable to store the number of elements (e.g., n).

4.Prompt the user to enter the number of elements (n).

5.Allocate memory for the array using malloc based on the number of elements (n).

6.Read the elements of the array from the user and store them in the allocated memory.

7.Initialize a variable oddCount to 0 to keep track of the count of odd elements.

8.Loop through the elements of the array:
a. Check if the current element is odd (element % 2 is not equal to 0).
b. If it's odd, increment the oddCount by 1.

9.Print the total count of odd elements (oddCount).

10.Release the allocated memory using free.

11.End.
## PROGARM :
```
#include <stdio.h>
#include<stdlib.h>
int main()
{
int i,odd=0,
*ptr;
ptr=(int*)malloc(5*sizeof(int));
ptr[0]=33;
ptr[1]=55;
ptr[2]=302;
ptr[3]=231;
ptr[4]=250;
for(i=0; i<5; i++)
{
if(ptr[i]%2!= 0)
{
odd++;
}
}
printf("Total odd elements:%d"
, odd);
return 0;
}
```
## OUTPUT :
![image](https://github.com/Niroshassithanathan/EX-6-POINTERS/assets/121418437/75998120-df79-4648-8edb-7e48d9f674ab)

## RESULT :
Thus , The C program has been executed successfully.
# EX-6-C-STRUCTURE
## AIM :
```
Create a C Program to store the student information and display it
using structure
struct student
{ char
name[50];int
roll;
float marks;
} ;
```
## AIGORITHAM :
1.Start

2.Define a structure named student with members for storing student information, such as name (a character array), roll number (an integer), and marks (a floating-point number).

3.Declare a variable of type student to represent a student's record.

4.Prompt the user to enter student information (name, roll number, and marks) and store it in the student variable.

5.Display the student information by accessing the members of the structure.

6.End.
## PROGARM :
```
#include <stdio.h>
struct student {
char name[50];
int roll;
float marks;
} s;
int main()
{
scanf("%s %d %f"
,s.name,&s.roll,&s.marks);
printf("Displaying Information:\n");
printf("Name: ");
printf("%s\n"
, s.name);
printf("Roll number: %d\n"
,
s.roll);printf("Marks: %.1f\n"
,
s.marks);
return 0;
}
```
## OUTPUT :
![image](https://github.com/Niroshassithanathan/EX-6-POINTERS/assets/121418437/1354cf8c-7b6e-40bb-a783-e6780dafbe99)

## RESULT :
Thus , The C program has been executed successfully.
# EX-6-D-USER DEFINED DATA TYPES
## AIM :
Create a structure for student and read the regno,name,no.of.present in the month of
jun, july, aug and sep and check the eligibility for writing the examination and display
the details using function(use structure variable as global)?
(Total working days=84(no.of.working days jun=21, july=21, aug=21, sep=21) above
>=75 percentage eligibility is "yes" otherwise "no". No.of.working days in a month
should be  less than equal to 21)
## AIGORITHAM :
1.Start

2.Define a structure Student with the following members

3.Declare a structure variable student of type Student.

4.Create a function readStudentDetails to read the student's details

5.Create a function checkEligibility to check eligibility for the examination

6.Create a function displayStudentDetails to display the student's details and eligibility status.

7.End.
## PROGARM :
```
#include<stdio.h>
struct attend
{
int regno;
char name[60];
int jun,july,aug,sept;
}a;
void attendence(struct attend a);
int main(){
scanf("%d %s %d %d %d %d",&a.regno,a.name,&a.jun,&a.july,&a.aug,&a.sept);
attendence(a);
}
void attendence(struct attend a){
float total=(a.jun+a.july+a.aug+a.sept);
if(a.regno<1001) {
float e=(total*100/84);
printf("Reg.no:%d\nName:%s\nTotal.No.of.present
days:%.f\nAttendence:%.2f\n",a.regno,a.name,total,e);
if(e<100 &&
e>50){ printf("eligibility:
yes");
}
else
{
printf("eligibility:no");
}
}
else {
printf("Invalid data:No.of.present days is greater than working day");
}
}
```
## OUTPUT :
![image](https://github.com/Niroshassithanathan/EX-6-POINTERS/assets/121418437/4af7f6b9-cfd0-4856-a504-eba2209d3f5d)

## RESULT :
Thus , The C program has been executed successfully.
