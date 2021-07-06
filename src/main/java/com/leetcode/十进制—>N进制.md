```java
package com.zth;
import java.util.Scanner;
public class JinZhi {
  // 十进制转换为 n 进制
  public String fun(int n,int num) {
    // n 表示目标进制, num 要转换的值
    String str= "";
    int yushu ;      // 保存余数
    int shang = num;      // 保存商
    while (shang>0) {
      yushu = shang %n;
      shang = shang/n;
      
      // 10-15 -> a-f
      if(yushu>9) {
        str =(char)('a'+(yushu-10)) + str;
      }else {
        str = yushu+str;
      }
    }
    
    return str;
  }
 
  public static void main(String[] args) {
    // TODO Auto-generated method stub
    JinZhi s1 = new JinZhi();
    
    Scanner scanner = new Scanner(System.in);
    System.out.print("请输入目标进制：");
    int jinzhi = scanner.nextInt();
    System.out.print("请输入要转换的数字：");
    int num = scanner.nextInt();
    scanner.close();
    
    System.out.println(s1.fun(jinzhi, num));
  }
 
}
```