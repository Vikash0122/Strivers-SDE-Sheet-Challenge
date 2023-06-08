# Merge two sorted arrays

Problem Link:- [Code Studio](https://www.codingninjas.com/codestudio/problems/merge-two-sorted-arrays_8230835?challengeSlug=striver-sde-challenge)
~~~
vector<int> ninjaAndSortedArrays(vector<int>& arr1, vector<int>& arr2, int m, int n) {
	// O((m+n)*Log(m+n)) + O(m) + O(n)
	vector<int> res;
	for(int i=0; i<m; i++){
		res.push_back(arr1[i]);
	}
	for(int i=0; i<n; i++){
		res.push_back(arr2[i]);
	}
	sort(res.begin(), res.end());
	return res;
}
~~~
