# Leetcode_problem_80
Remove Duplicates from Sorted ArrayII
class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        int length = nums.size();
        vector<int> nums2;
        int i = 0,j,k = 0;
        if(length <2){
            return length;
        }
        
        while(i < length){
            int count = 0;
           for(j = i+1; j < length; j++){ 
               if(nums[i] == nums[j]){
                   count++;
               }
               else{
                   break;
               }
           }
           if(count == 0){
               
               nums2.push_back(nums[i]);
           }
           else{
               nums2.push_back(nums[i]);
               nums2.push_back(nums[i]);
           }
           i = i + count + 1;

        }
        int len = nums2.size();
        cout<<"Length "<<len<<endl;
        for(int y = 0; y<len; y++){
            cout<<nums2[y]<<" ";
            nums[y] = nums2[y];
        }
        return length-(length - len);
    }

};
