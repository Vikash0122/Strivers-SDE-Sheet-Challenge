# Best Time to Buy and Sell Stock

Problem Link:- [Code Studio](https://takeuforward.org/data-structure/stock-buy-and-sell/)

~~~
//Optimal Solution
// TC:- O(n)
int maximumProfit(vector<int> &arr){
    int maxPro = 0;
    int n = arr.size();
    int minPrice = INT_MAX;

    for (int i = 0; i < arr.size(); i++) {
        minPrice = min(minPrice, arr[i]);
        maxPro = max(maxPro, arr[i] - minPrice);
    }
    
    return maxPro;
}

~~~
