# Maximum Subarray Sum

Problem Link:- [Code Studio](https://takeuforward.org/data-structure/kadanes-algorithm-maximum-subarray-sum-in-an-array/)

~~~
// TLE
long long maxSubarraySum(int arr[], int n)
{
    // O(n*n)
    long long maxm=INT_MIN;

    for(int i=0; i<n; i++){
        long long sum=0;
        for(int j=i; j<n; j++){
            sum+=arr[j];
            maxm=max(sum,maxm);
        }
    }
    if(maxm>0)
return maxm;
else
return 0;// empty subarray
}
~~~

~~~
// TC:- O(n)
long long maxSubarraySum(int arr[], int n)
{
    long long maxi = LONG_MIN; // maximum sum
    long long sum = 0;

    for (int i = 0; i < n; i++) {

        sum += arr[i];
        if (sum > maxi) {
            maxi = sum;
        }

        // If sum < 0: discard the sum calculated
        if (sum < 0) {
            sum = 0;
        }
    }

    // consider the sum of the empty subarray
    if (maxi < 0) maxi = 0;

    return maxi;
}
~~~
