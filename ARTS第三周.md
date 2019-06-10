##A算法
9. Palindrome Number
Easy

1440

1305

Favorite

Share
Determine whether an integer is a palindrome. An integer is a palindrome when it reads the same backward as forward.

Example 1:

Input: 121
Output: true
Example 2:

Input: -121
Output: false
Explanation: From left to right, it reads -121. From right to left, it becomes 121-. Therefore it is not a palindrome.
Example 3:

Input: 10
Output: false
Explanation: Reads 01 from right to left. Therefore it is not a palindrome.
Follow up:

Coud you solve it without converting the integer to a string?

自己的答案


	import java.math.BigDecimal;

	class Solution {
    public boolean isPalindrome(int x) {
       if (x >= 0) {
            String str = x + "";
            char[] chars = str.toCharArray();
            StringBuffer sb = new StringBuffer();
            for (int i = chars.length - 1; i >= 0; i--) {
                sb.append(chars[i]);
            }

            if (new BigDecimal(sb.toString()).longValue() < Integer.MAX_VALUE && Integer.valueOf(sb.toString()) == x) {
                return true;
            }

        }


        return false;
    }
}




