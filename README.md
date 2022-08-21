#include <stdio.h>
int binarysearch(int n ,  int key, int arr[]){
    int s=0;
    int e=n;
    int mid;
    while(s<=e){
        int mid=(s+e)/2;
        if(arr[mid] == key){
            return mid;
        }
        else if(arr[mid]>key){
            e ==  mid-1;
        }
        else{
            s == mid+1;
        }
    }
return -1;
}

int main(){
int n;
int arr[n];
int key;
printf("enter the size of array you want \n");
scanf("%d",&n);
for( int i=0; i<n; i++){
    printf("enter the elements you want to put in array ");
    scanf("%d",&arr[i]);
}
printf("enter the element you want to search in array ");
scanf("%d",&key);
printf("your element is indexed at %d" ,binarysearch(n,key,arr));
return 0;
}
