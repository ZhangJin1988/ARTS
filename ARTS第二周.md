##1 算法

Reverse Integer
Easy

2155

3271

Favorite

Share
Given a 32-bit signed integer, reverse digits of an integer.

Example 1:

Input: 123
Output: 321
Example 2:

Input: -123
Output: -321
Example 3:

Input: 120
Output: 21
Note:
Assume we are dealing with an environment which could only store integers within the 32-bit signed integer range: [−231,  231 − 1]. For the purpose of this problem, assume that your function returns 0 when the reversed integer overflows.

	
		
	import java.math.BigDecimal;
	
	class Solution {
	    public int reverse(int x) {
	       String s = String.valueOf(x);
	        char[] charsSource = s.toCharArray();
	        char[] charsTarget = new char[charsSource.length];
	        int j = 0;
	        if ("-".equals(String.valueOf(charsSource[0]))) {
	            charsTarget[0] = '-';
	            j = 1;
	        }
	
	        for (int i = charsSource.length - 1; i >= 0; i--, j++) {
	
	            if (String.valueOf(charsSource[i]).equals("-")) {
	                break;
	            }
	            if (i == 0 && String.valueOf(charsSource[i]).equals("0") && charsSource.length > 1 ) {
	                break;
	            }
	            charsTarget[j] = charsSource[i];
	
	        }
	        BigDecimal bigDecimal =new BigDecimal(String.valueOf(charsTarget));
	        if(bigDecimal.longValue() > Integer.MAX_VALUE || bigDecimal.longValue() < Integer.MIN_VALUE){
	            return 0;
	        }
	
	        return Integer.valueOf(String.valueOf(charsTarget));
	    }
	}
	




##2	论文以及英文文章
###来自quora的问答 azkaban airflow rundeck jenkins 谁是更好的调度工具
https://www.quora.com/What-is-the-best-scheduler-Azkaban-Airflow-Rundeck-or-Jenkins


##3 小技巧
Linux如何排查空间不足的问题
https://www.cnblogs.com/QuestionsZhang/p/10874575.html

##4 分享的文章
公众号caoz的梦呓
听说你想炒币
https://mp.weixin.qq.com/s?__biz=MzI0MjA1Mjg2Ng==&mid=2649868479&idx=1&sn=d19e41ba2426dfec5890dbae4d8c82e8&chksm=f10752d2c670dbc4da4877da63ad90a1d6e97950224206d53ee0b9f99632d835f27f9cf50dbd&mpshare=1&scene=1&srcid=&key=b9ef0817915a95665ffafce3f3866ef79985c7ba1c8d1104682c375030fc4a03d5af1e20a6fe50a25c471fda4b5c592a3a1c10a051154952557d9a4995a4648bf9f1f3b27cd1be13718a7d5bc57e4440&ascene=0&uin=MjQ2NjEwMjA0Mw%3D%3D&devicetype=iMac+MacBookPro11%2C5+OSX+OSX+10.14.3+build(18D109)&version=11020012&lang=zh_CN&pass_ticket=ksTDmxPKgPt%2BPP6iEp3XNWoU2yMe60otdiTxYxY5tGJXNCbc9VgkClqHnfmvOWpK






