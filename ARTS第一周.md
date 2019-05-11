##1 A-algorithms

###题干
	Given an array of integers, return indices of the two numbers such that they add up to a specific target.
	You may assume that each input would have exactly one solution, and you may not use the same element twice.
	Example:

	Given nums = [2, 7, 11, 15], target = 9,

	Because nums[0] + nums[1] = 2 + 7 = 9,
	return [0, 1].

###解答
	class Solution {
    public int[] twoSum(int[] nums, int target) {
        int[] result = new int[2]  ;
        for (int i=0;i<nums.length ; i++) {
            for(int j=i+1;j<nums.length;j++){
                    int twoSum = nums[i] + nums[j];
                    if(twoSum==target){
                        result[0] = i;
                        result[1] = j;
                    }                
            }
        }
        return result;
    }
}

##2 R-review
https://blog.acolyer.org/2019/05/07/distributed-consensus-revised-part-i/

	分布式共识修订，没太看懂，需要恶补很多分布式的知识

##3 T-titls
分享一个小技巧，一个Linux命令，查询最近1分钟被修改过的.log后缀文件，对于不知道日志位置的时候，能够很好的定位问题
	
	find / -name '*.log' -mmin -1　
	
	
##4 S-Share
这次推荐的是王垠的如何掌握所有的编程语言，给我很大的启发，尤其是对于语言就是组装机的概念，也说明了纠结哪门语言好与坏是非常幼稚的行为。

	http://www.yinwang.org/blog-cn/2017/07/06/master-pl
	


