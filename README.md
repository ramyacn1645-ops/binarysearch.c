# binarysearch.c
<bh>
//finding a book in a digital bookshelf
#include<stdio.h>
int main(){
int i,n,key,low,mid,high,found=0;
printf("enter number of books:\n");
scanf("%d",&n);
int book[n];
printf("enter %d book ID's in ascendng order :\n",n);
for(i=0;i<n;i++){
scanf("%d",&book[i]);
}
printf("enter book ID to be searched:\n");
scanf("%d",&key);
low=0;high=n-1;
while(low<=high){
mid=(low+high)/2;
if(book[mid]==key){
found=1;
break;
}

else if(book[mid]<key){
low=mid+1;
}
else{
high=mid-1;
}
}
if(found){
printf("Book is available");
}
else{
printf("Book is not available");
}
return 0;
}
