#include<stdio.h>
#include<conio.h>
void main(){
int i,opt,n,ele,pos,pos1,sum=0,f=0;
float avg=0.0;
int a[50];      clrscr();
printf("Enetr the no.of.elements in array: ");
scanf("%d",&n);
for(i=1;i<=n;i++){
printf("Enter the element %d : ",i);
scanf("%d",&a[i]);
}
do{
printf("\n\n         WELCOME TO SIMPLE ARRAY CALCULATION ");
printf("\n 1.Sum and Average \n 2.Insert \n 3.Update \n 4.Deletion \n 5.Search \n 6.Display \n 7.Close \n\n Enter the option: ");
scanf("%d",&opt);
switch(opt){
case 1:
for(i=1;i<=n;i++){
sum=sum+a[i];
}
avg=sum/n;
printf("Sum : %d \n Average : %2f",sum,avg);
break;
case 2:
printf("Enter the position to insert the element in array: ");
scanf("%d",&pos);
printf("Enter the element:");
scanf("%d",&ele);
for(i=n+1;i>=pos;i--){
a[i]=a[i-1];

}
a[pos]=ele;
n++;
break;
case 3:
printf("Enter the position to update the element in array: ");
scanf("%d",&pos);
printf("Enter the element:");
scanf("%d",&ele);
a[pos]=ele;
break;
case 4:
printf("Enter the position of the element to be delete: ");
scanf("%d",&pos);

for(i=pos;i<=n;i++){
a[pos]=a[pos+1];
}
n--;
break;
case 5:
printf("Enter the element to check present in the array:");
scanf("%d",&ele);
for(i=1;i<=n;i++){
if(a[i]==ele){
f=1;
pos1=i;
}
}
if(f==1){
printf("Yes , %d is present at the position %d in the array",ele,pos1);
}
else{
printf("No , %d is not there in the array",ele);
}

break;

case 6:
for(i=1;i<=n;i++){
printf("%d ",a[i]);
}
break;
case 7:exit(0);break;
default:printf("\nEnter the correct option");
}
}
while(1);
getch();
}