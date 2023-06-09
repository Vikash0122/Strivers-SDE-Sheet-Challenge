# Search in A 2D matrix

Problem Link:- [Code Studio](https://www.codingninjas.com/codestudio/problems/search-in-a-2d-matrix_8230773?challengeSlug=striver-sde-challenge)

~~~
bool searchMatrix(vector<vector<int>>& mat, int target) {
    int count=0;
    int m=mat.size();
    int n=mat[0].size();
    int i=m-1, j=0;

    while(i>=0 && j<n)
    {
        int val = mat[i][j];

        if(val == target)
            return true;

        (val > target) ? (i--) : (j++);
    }
    return false;
}
~~~
