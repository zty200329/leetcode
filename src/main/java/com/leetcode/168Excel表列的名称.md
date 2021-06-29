理解成一个26进制 1-26要转换成0-25
```java
class Solution {
    public static String convertToTitle(int n) {
	StringBuilder stringBuilder = new StringBuilder();
	while (n != 0) {
		n--; // 依次获取 26 进制逻辑上的个位、十位、百位…（虽然在 26 进制中不这么叫）
		stringBuilder.append((char) ('A' + n % 26));
		n /= 26;
	}
	return stringBuilder.reverse().toString();
    }
}
```