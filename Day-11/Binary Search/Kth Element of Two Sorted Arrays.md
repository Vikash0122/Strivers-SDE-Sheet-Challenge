# Kth Element of Two Sorted arrays

~~~
int ninjaAndLadoos(vector<int> &row1, vector<int> &row2, int m, int n, int k) {
   // Write your code here.
   int i=0,j=0;
   int c=0;
   
   int l=min(row1[0],row2[0]);
   int h=max(row1[n-1], row2[m-1]);
   int req=(k-1);
   while(l<h){
       int mid=(l+h)/2;
       
       int lp=0;
       lp+=(upper_bound(row1.begin(), row1.end(), mid)-row1.begin());
       
        lp+=(upper_bound(row2.begin(), row2.end(), mid)-row2.begin());

   if(lp<=req){
       l=mid+1;
       
   }
   else{
       h=mid;
       
   }
   }
   return l;
}
~~~
