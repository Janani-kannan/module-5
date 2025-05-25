# EX-26-AREA-OF-CIRCLE-AND-PERIMETER-OF-CIRCLE-USING-POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start
2.	Declare variables: radius, area, perimeter
3.	Declare pointers for each: ptrRadius, ptrArea, ptrPerimeter
4.	Assign the addresses of the variables to the pointers
5.	Input the radius using the pointer
6.	Calculate area: *ptrArea = 3.14 × (*ptrRadius) × (*ptrRadius)
7.	Calculate perimeter: *ptrPerimeter = 2 × 3.14 × (*ptrRadius)
8.	Print area and perimeter using pointers
9.	Stop
10.	
## PROGRAM
```
#include <stdio.h>
int main()
{
    int *a,x;
    scanf("%d",&x);
    a=&x;
    float b=3.14;
    float c=b*(*a)*(*a);
    float d=2*b*(*a);
    printf("Area of Circle = %.2f",c);
    printf("\nPerimeter of Circle = %.2f",d);
    return 0;
    
}
```

## OUTPUT
		       	
![image](https://github.com/user-attachments/assets/a981b07f-3b44-4c30-bb12-54e952ebff67)


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main()
{
    char *str = (char *)malloc(8 * sizeof(char));
    if (str == NULL) {
        printf("Memory allocation failed!\n");
        return 1;
    }

    strcpy(str, "WELCOME");
    printf("%s\n", str);
    free(str);
    str = NULL; 

    return 0; 
}
```

## OUTPUT

![image](https://github.com/user-attachments/assets/7659b052-f124-47a1-97d7-104014a8bd24)


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 


# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>
struct student
{
    char a[50],b[50];
    int c;
    char d[50];
    
}x;
int main()
{
    
    scanf("%s%s",x.a,x.b);
    scanf("%d",&x.c);
    scanf("%s",x.d);
    printf("Name is: %s",x.a);
    printf("\nGender: %s",x.b);
    printf("\nAge is: %d",x.c);
    printf("\nAddress: %s",x.d);
    
    return 0;
    
}
```

## OUTPUT

![image](https://github.com/user-attachments/assets/21739142-7f07-4747-99c7-ab60d0d0f023)


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

// Define the structure for employee
struct employee {
    char name[50];
    int wages;
    float days;
    float basic_pay;
    float hra;
    float net_pay;
};

int main() {
    int n, i;
    scanf("%d", &n);
    struct employee emp[n];
    for (i = 0; i < n; i++) {
        scanf("%s", emp[i].name);
        scanf("%d %f", &emp[i].wages, &emp[i].days);
        emp[i].basic_pay = emp[i].wages * emp[i].days;
        emp[i].hra = 0.12 * emp[i].basic_pay;
        emp[i].net_pay = emp[i].basic_pay + emp[i].hra;
    }

    for (i = 0; i < n; i++) {
        printf("Name: %s\n", emp[i].name);
        printf("BasicPay: %f\n", emp[i].basic_pay);
        printf("HRA:%f\n", emp[i].hra);
        printf("NetPay:%f\n", emp[i].net_pay);
    }

    return 0;
}
```

 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/37b9a5f1-bec9-47c5-842d-c226350e5eca)


## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>
struct Student {
    int regno;
    int mark1, mark2, mark3;
    float total;
    float average;
};

int main() {
    struct Student students[5];
    int i;
    for (i = 0; i < 5; i++) {
        scanf("%d", &students[i].regno);
        scanf("%d", &students[i].mark1);
        scanf("%d", &students[i].mark2);
        scanf("%d", &students[i].mark3);

        // Calculate total and average
        students[i].total = students[i].mark1 + students[i].mark2 + students[i].mark3;
        students[i].average = students[i].total / 3.0;
    }

    // Print results
    printf("Student Details are\n");
    for (i = 0; i < 5; i++) {
        printf("%d       %d       %d       %d       %.2f       %.2f\n",
               students[i].regno,
               students[i].mark1,
               students[i].mark2,
               students[i].mark3,
               students[i].total,
               students[i].average);
    }

    return 0;
}
```


## OUTPUT

![image](https://github.com/user-attachments/assets/33d23211-9521-458f-9c9e-7025b88ba2c0)

![image](https://github.com/user-attachments/assets/d1701e34-a061-46cf-9708-e17bc90b62c2)

![image](https://github.com/user-attachments/assets/6774cb68-1ac2-4755-a392-aeca438354c2)


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


