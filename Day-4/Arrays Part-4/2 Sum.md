# 2 sum

~~~
vector<int> twoSum(vector<int>& nums, int target) {
    unordered_map<int,int> map;        
        for(int index = 0; index < nums.size(); index++){
			if(map.find(target-nums[index]) != map.end()){
                return {index, map[target-nums[index]]};
            }			
            map[nums[index]] = index;
        }       
        return {};
    }
~~~
