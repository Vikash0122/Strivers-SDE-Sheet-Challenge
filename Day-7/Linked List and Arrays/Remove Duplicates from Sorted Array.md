# Remove Duplicates from Sorted Array

~~~
#include <bits/stdc++.h>
int removeDuplicates(vector<int> &arr, int n) {
	int ptr1 = 0, ptr2 = 1;
    while(ptr2 < n){
        if(arr[ptr1] == arr[ptr2])
            ptr2++;
        else{
            arr[ptr1+1] = arr[ptr2];
            ptr1++; ptr2++;
        }
    }
    return ptr1+1;
}
~~~
