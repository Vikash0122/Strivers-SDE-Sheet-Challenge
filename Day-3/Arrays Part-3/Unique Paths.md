# Unique paths

Problem Link:- [Code Studio](https://www.codingninjas.com/codestudio/problems/unique-paths_8230802?challengeSlug=striver-sde-challenge)

~~~
int uniquePaths(int m, int n) {
 // Using P & C
    int Nn=m+n-2;
    int R =m-1;
    double res=1;

    for(int i=1;i<=R;i++)
    {
        res=res* (Nn-R+i)/i;
    }

    return (int)res;
}
~~~
