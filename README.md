insert value in array c language

#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
#define size 10
void insert(int a[], int data, int position, int last);
int main(void) {
   int array[size] = { 10,20,30,40,50,60,80,90,100 };
   int data, position, last;
   insert(array, 70, 7,9);
   system("pause");
   return 0;
}
void insert(int a[], int data, int position, int last) {
   if (last >= size) {
      printf("array overflow");
      exit(1);

   }
   for (int i = last; i >= position-1; i--) {
      a[i + 1] = a[i];
   
   }
   a[position-1] = data;
   last++;
   for (int i = 0; i < size; i++) {
      printf("arr[%d]= %d\n",i, a[i]);
   }
}
