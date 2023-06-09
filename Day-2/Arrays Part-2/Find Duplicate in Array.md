# Find duplicate in an array

Problem Link:- [Code Studio](https://www.codingninjas.com/codestudio/problems/find-duplicate-in-array_8230816?challengeSlug=striver-sde-challenge)
~~~

int findDuplicate(vector<int> &arr, int n){
	// Write your code here.
	 int slow=arr[0];

    int fast=arr[0];

    do

    {

        slow=arr[slow];

        fast=arr[arr[fast]];

    }

    while(slow!=fast);

    fast=arr[0];

    while(fast!=slow)

    {

        fast=arr[fast];

        slow=arr[slow];

    }

    return fast;
}
~~~
