#include<stdio.h>
int menu();
void bike();
void rikshaw();
void car();
void showData();
void Delete ();
int No_b=0,No_a=0,No_c=0,amount=0,total_count=0;

int menu()
{
    printf("**** WELCOME TO VEHICLE ENTRY SYSTEM ****");
    int ch;
    printf("\n1) Enter bike ");
    printf("\n2) Enter auto ");
    printf("\n3) Enter car ");
    printf("\n4) Show status ");
    printf("\n5) Delete Data ");
    printf("\n\n Enter your choice ");
    scanf("%d",&ch);
    printf("****************************************\n");
    return ch;
}
void showData()
{
    printf("\nNumber of bikes = %d",No_b);
    printf("\nNumber of autos = %d",No_a);
    printf("\nNumber of cars = %d",No_c);
    printf("\nTotal number of vehicles = %d",total_count);
    printf("\nTotal amoount recived = %d",amount);
}
void Delete()
{
    No_b=0;
    No_a=0;
    No_c=0;
    amount=0;
    total_count=0;
}
void bike()
{
    printf("Entry of bike is successfully done\n ") ;
    printf("_______________________________________\n");
    No_b ++;
    amount = amount + 20;
    total_count ++;
}
void rikshaw()
{
    printf(" Entry of rikshaw is successfully done\n ") ;
    printf("_______________________________________\n");
    No_a ++;
    amount = amount + 50;
    total_count ++;
}
void car()
{
    printf(" Entry of car is successfully done \n") ;
    printf("_______________________________________\n");
    No_c ++;
    amount = amount + 100;
    total_count ++;
}
int main()
{
    while(1) 
    {
        switch(menu())
        {
            case 1:
            bike();
            break;

            case 2:
            rikshaw();
            break;

            case 3:
            car();
            break;

            case 4:
            showData();
            break;

            case 5:
            Delete();
            break;
 
            default :
            printf("Invalid choice !\n");
        }
    }
}
