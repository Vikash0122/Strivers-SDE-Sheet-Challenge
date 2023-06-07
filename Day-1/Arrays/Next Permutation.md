# Next Permutaion

Problem Link:- [Code Studio](https://takeuforward.org/data-structure/next_permutation-find-next-lexicographically-greater-permutation/)

~~~
// C++ In-Built Function
vector<int> nextPermutation(vector<int> &permutation, int n)
{
    next_permutation(permutation.begin(), permutation.end());   
    return permutation;
}
  
~~~  

~~~
// Optimal Implementation
vector<int> nextPermutation(vector<int> &permutation, int n)
{

    int idx=-1;
    // finding the breaking point
    for(int i=n-2; i>=0; i--){
        if(permutation[i]<permutation[i+1]){
            idx=i;
            break;
        }
    }
    // last permutation -> reverse will be the answer i.e. first permutation
    if(idx==-1){
        reverse(permutation.begin(), permutation.end());
        return permutation;
    }

    // finding just greater element than the idx element and SWAP
    for(int i=n-1; i>idx; i--){
        if(permutation[i]>permutation[idx]){
            swap(permutation[i], permutation[idx]);
            break;
        }
    }

    // for making it next greater permutation, we will reverse the elements from idx till end
    reverse(permutation.begin() + idx +1 , permutation.end());
    return permutation;
}
// TC:- O(n)
~~~
