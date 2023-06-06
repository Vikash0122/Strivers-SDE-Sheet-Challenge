# Set Matrix Zeros 
Problem Link:- [Code Studio](https://www.codingninjas.com/codestudio/problems/set-matrix-zeros_8230862?challengeSlug=striver-sde-challenge)
~~~
void setZeros(vector<vector<int>> &matrix)
{
	int rows=matrix.size();
	int cols=matrix[0].size();
	vector<int>row;
	vector<int>col;
	
	for(int i=0; i<rows; i++){
		for(int k=0; k<cols; k++){
			if(matrix[i][k]==0){
				row.push_back(i);
				col.push_back(k);
			}
		}
	}
	
	// rows -> 0
	for(int i=0; i<row.size(); i++){
		int k_r=row[i];
		for(int j=0; j<cols; j++){
			matrix[k_r][j]=0;
		}
	}

	// columns -> 0
	for(int i=0; i<col.size(); i++){
		int k_c=col[i];
		for(int j=0; j<rows; j++){
			matrix[j][k_c]=0;
		}
	}
}
// TC:- O(n*n)
~~~
