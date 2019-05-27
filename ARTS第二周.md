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