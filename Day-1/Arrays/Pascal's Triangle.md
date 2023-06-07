# Pascal's Triangle

Problem Link :- [Code Studio](https://takeuforward.org/data-structure/program-to-generate-pascals-triangle/)

~~~
vector<vector<long long int>> printPascal(int n) 
{
  vector<vector<long long int>>arr;
  for(int i=0; i<n; i++){
    vector<long long int> res;
    for(int j=0; j<=i; j++){
      if(i==j||j==0){
        res.push_back(1);
      }
      else
       res.push_back(arr[i-1][j-1] + arr[i-1][j]);
    }
    arr.push_back(res);
  }
  return arr;
}
~~~
