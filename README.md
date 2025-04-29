# Student-record-management-system-
This C program is a Student Information Management System that allows a user to manage student records via a console-based interface. It provides basic CRUD (Create, Read, Update, Delete) functionalities for storing and handling up to 65 student records.
#include<stdio.h>
#include<stdlib.h>
#include<string.h>

#define MAXSTUDENTS 65
#define LENGTHOFNAME 50
#define LENGTHOFID 15
#define LENGTHOFAADHAR 15
#define LENGTHOFDOB 15

typedef struct{
    char name[LENGTHOFNAME];
    char Id[LENGTHOFID];
    char aadhar[LENGTHOFAADHAR];
    char DOB[LENGTHOFDOB];
}student;
int i,j,studentcount=0;
 student students[MAXSTUDENTS];
 
 
 void choices();
 void adddetails();
  void viewdetails();
  void searchdetails();
  void deletedetails();
 
void main(){
    int choice;
    while(1){
        choices();
        printf("Enter ur choice:");
        scanf("%d",&choice);
        switch(choice){
            case 1:
            adddetails();
            break;
            case 2:
            viewdetails();                                                 
            break;
            case 3:
            searchdetails();
            break;
            case 4:
            deletedetails();
            break;
            case 5:
            printf("The Program is terminated\n");
            exit(0);
            default:
            printf("Invalid choice...\n");
        }
    }
    return ;
}
void choices(){
    printf("\nStudent Information Portal \n");
    printf("1. Add details of student\n");
    printf("2. View details of student\n");
    printf("3. Search details of student\n");
    printf("4. Delete details of student\n");
    printf("5. Exit\n");
}
void adddetails(){
    
    
    student newdetails;
    printf("Enter Student name:\n");
    scanf("%s",newdetails.name);
    printf("Enter Student Id:\n");
    scanf("%s",newdetails.Id);
    printf("Enter Student Aadhar:\n");
    scanf("%s",newdetails.aadhar);
    printf("Enter Student DOB:\n");
    scanf("%s",newdetails.DOB);
    students[studentcount++]=newdetails;
    printf("Details added successfully\n.");
}
    void viewdetails(){
        if(studentcount==0){
            printf("No students to display\n");
            return;
        }
        printf("Students List:\n");
     
       
        for(i=0;i<studentcount;i++){
            printf("Name:%s\n Id:%s\n Aadhar:%s\n DOB:%s\n",students[i].name,students[i].Id,students[i].aadhar,students[i].DOB);
           
        }
    }
    void searchdetails(){
        if(studentcount==0){
            printf("No students to display\n");
            return;
        }
        char name[LENGTHOFNAME];
        printf("Enter the name to search:");
        scanf("%s",name);
        for(i=0;i<studentcount;i++){
            if(strcmp(students[i].name,name)==0){
                printf("Student found: Name:%s\n  Id:%s\n Aadhar:%s\n DOB:%s\n",students[i].name,students[i].Id,students[i].aadhar,students[i].DOB);
            return;
              
            }
        }
        printf("Student with name %s not found.\n", name);
    }
    void deletedetails(){
      if(studentcount==0){
            printf("No students to display\n");
            return;
    }
    char name[LENGTHOFNAME];
        printf("Enter the name to delete:\n");
        scanf("%s",name);
        for(i=0;i<studentcount;i++){
            if(strcmp(students[i].name,name)==0){
              for(j=i;j<studentcount;j++){
                students[j]=students[j+1];
              }
                studentcount--;
                printf("Student details deleted successfully...\n");
                return;
              
            }
        }
        printf("Student with name %s not found.\n", name);
    }#include<stdio.h>
#include<stdlib.h>
#include<string.h>

#define MAXSTUDENTS 65
#define LENGTHOFNAME 50
#define LENGTHOFID 15
#define LENGTHOFAADHAR 15
#define LENGTHOFDOB 15

typedef struct{
    char name[LENGTHOFNAME];
    char Id[LENGTHOFID];
    char aadhar[LENGTHOFAADHAR];
    char DOB[LENGTHOFDOB];
}student;
int i,j,studentcount=0;
 student students[MAXSTUDENTS];
 
 
 void choices();
 void adddetails();
  void viewdetails();
  void searchdetails();
  void deletedetails();
 
void main(){
    int choice;
    while(1){
        choices();
        printf("Enter ur choice:");
        scanf("%d",&choice);
        switch(choice){
            case 1:
            adddetails();
            break;
            case 2:
            viewdetails();                                                 
            break;
            case 3:
            searchdetails();
            break;
            case 4:
            deletedetails();
            break;
            case 5:
            printf("The Program is terminated\n");
            exit(0);
            default:
            printf("Invalid choice...\n");
        }
    }
    return ;
}
void choices(){
    printf("\nStudent Information Portal \n");
    printf("1. Add details of student\n");
    printf("2. View details of student\n");
    printf("3. Search details of student\n");
    printf("4. Delete details of student\n");
    printf("5. Exit\n");
}
void adddetails(){
    
    
    student newdetails;
    printf("Enter Student name:\n");
    scanf("%s",newdetails.name);
    printf("Enter Student Id:\n");
    scanf("%s",newdetails.Id);
    printf("Enter Student Aadhar:\n");
    scanf("%s",newdetails.aadhar);
    printf("Enter Student DOB:\n");
    scanf("%s",newdetails.DOB);
    students[studentcount++]=newdetails;
    printf("Details added successfully\n.");
}
    void viewdetails(){
        if(studentcount==0){
            printf("No students to display\n");
            return;
        }
        printf("Students List:\n");
     
       
        for(i=0;i<studentcount;i++){
            printf("Name:%s\n Id:%s\n Aadhar:%s\n DOB:%s\n",students[i].name,students[i].Id,students[i].aadhar,students[i].DOB);
           
        }
    }
    void searchdetails(){
        if(studentcount==0){
            printf("No students to display\n");
            return;
        }
        char name[LENGTHOFNAME];
        printf("Enter the name to search:");
        scanf("%s",name);
        for(i=0;i<studentcount;i++){
            if(strcmp(students[i].name,name)==0){
                printf("Student found: Name:%s\n  Id:%s\n Aadhar:%s\n DOB:%s\n",students[i].name,students[i].Id,students[i].aadhar,students[i].DOB);
            return;
              
            }
        }
        printf("Student with name %s not found.\n", name);
    }
    void deletedetails(){
      if(studentcount==0){
            printf("No students to display\n");
            return;
    }
    char name[LENGTHOFNAME];
        printf("Enter the name to delete:\n");
        scanf("%s",name);
        for(i=0;i<studentcount;i++){
            if(strcmp(students[i].name,name)==0){
              for(j=i;j<studentcount;j++){
                students[j]=students[j+1];
              }
                studentcount--;
                printf("Student details deleted successfully...\n");
                return;
              
            }
        }
        printf("Student with name %s not found.\n", name);
    }
