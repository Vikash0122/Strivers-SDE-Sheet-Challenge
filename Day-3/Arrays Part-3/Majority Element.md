# Majority element

Problem Link:- [Code Studio](https://www.codingninjas.com/codestudio/problems/day-6-majority-element_8230731?challengeSlug=striver-sde-challenge)

~~~
int findMajorityElement(int arr[], int n) {
	map<int,int>mp;
	for(int i =0;i<n ;i++){
		mp[arr[i]]++;
	}
    int low = n/2;
	for(auto i: mp){
		if(i.second>low){
			return i.first;
		}
	}
	return -1;
}
~~~
