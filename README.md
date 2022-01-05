# Helllo_World

import java.util.Scanner;

public class QickSort {
int pivot=0;int pa=0;
public void sort(int aray[],int low,int high) {
   
if(low<high) {
pa=partistion(aray,low,high);
sort(aray,low,pa-1);
sort(aray,pa+1,high);

}

}
int partistion(int aray[],int low,int high) {
pivot=aray[high];
int i=0;
for(int j=0;j<high-1;j++) {
if(aray[i]<=aray[j]) {
int temp=0;
temp=aray[i];
aray[i]=aray[j];
aray[j]=temp;
}
}
int temp=0;
temp=aray[i+1];
aray[i+1]=aray[high];
aray[high]=temp;
return i+1;
}
void display(int aray[],int size) {
for(int t=0;t<size;t++) {
System.out.println(aray[t]);
}
}


public static void main(String[] args) {
// TODO Auto-generated method stub
QickSort obj=new QickSort();
Scanner sc=new Scanner(System.in);
System.out.println("Enter the size of array:");
   int size=sc.nextInt();
   int array[]=new int[size];
System.out.println("Enter the elements in array:");
for(int i=0;i<size;i++) {
array[i]=sc.nextInt();
}
System.out.println("Enter the Choise: Where 1)Sorting the array 2)display the sorted array");
int chs;
do {
System.out.println("Enter the Choise1:");
chs=sc.nextInt();
switch(chs){

case 1:
obj.sort(array,0, size-1);
 
   break;
case 2:
obj.display(array,size);
System.out.println("The quick sorted Array is:");
break;

}
}while(chs<=2);
}

}
