# StackInC

**All Opration Of Stack Including PUSH,POP,PEEP,CHANGE,DISPLAY implemented using C programm**

```js
#include <stdlib.h>
#include <stdio.h>
#include <conio.h>
#define size 5 // Stack limit

int t = -1, stack[size];
void push()
{
    int element;
    if (t == max - 1)
    {
        printf("\nStack Overflow");
    }
    else
    {
        printf("\nEnter your Element:");
        scanf("%d", &element);
        t = t + 1;
        stack[t] = element;
    }
}
void pop()
{
    if (t == -1)
    {
        printf("\nStack underflow");
    }
    else
    {
        printf("Deleted element is %d", stack[t]);
        t = t - 1;
    }
}
void peep()
{
    int element;
    printf("Which element do you want to Fetch:");
    scanf("%d", &element);
    if (t - element + 1 <= -1)
    {
        printf("Stack Underflow");
    }
    else
    {
        printf("Your %d element is :%d", element, stack[t - element + 1]);
    }
}
void change()
{
    int element;
    int new_element;
    printf("Which element do you want to Change:");
    scanf("%d", &element);
    printf("Enter new value of Element number %d:", element);
    scanf("%d", &new_element);
    if (t - element + 1 <= -1)
    {
        printf("Stack Underflow on Change");
    }
    else
    {
        stack[t - element + 1] = new_element;
        printf("Your Element number %d is Changed SuccesFully..", element);
    }
}
void display()
{
    if (t == -1)
    {
        printf("\nOopps....Stack is Empty");
    }
    else
    {
        printf("\n*****************************\n");
        printf("\tStack Elements");
        printf("\n*****************************\n");
        for (int i = t; i >= 0; --i)
        {
            printf("* %d *\n", stack[i]);
            printf("*****\n");
        }
    }
}
void main()
{
    int choice;
    while (1)
    {
        printf("\n******Menu******");
        printf("\n1.Push\n2.Pop\n3.Peep\n4.Change\n5.Display\n6.Exit");
        printf("\nEnter Your Choise(1-5):");
        scanf("%d", &choice);
        switch (choice)
        {
        case 1:
            push();
            break;
        case 2:
            pop();
            break;
        case 3:
            peep();
            break;
        case 4:
            change();
            break;
        case 5:
            display();
            break;
        case 6:
            exit(0);
        default:
            printf("\nEnter valid Choise...!\n");
            break;
        }
    }
}

```

_For More Details or problems contact Jigarvakil9200@gmail.com_
