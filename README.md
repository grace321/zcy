# zcy
public static void yanzheng(int guess) {
			if (guess == number){
				System.out.println("恭喜你答对了！");
				System.exit(0);
			}else if (guess > number)
				System.out.println("大了");
			else
				System.out.println("小了");// 用if语句判断你输入的数字与所给的随机数比较
	}
3、功能测试
既然思路出来了，做起来也就方便了。在上面模型里进行添加：
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23	import java.util.Scanner;
    public class TesGussNumber {
public static int number = (int) (Math.random() * 101);
static Scanner input;
public static int shuru() {
		input = new Scanner(System.in);
		System.out.println("请猜测一百以内的数字：");
		int guess = input.nextInt(); 
		return guess;
	}
         public static void yanzheng(int guess) {
			if (guess == number){
				System.out.println("恭喜你答对了！");
				System.exit(0);
			}else if (guess > number)
				System.out.println("大了");
			else
				System.out.println("小了");
	}
	      package Juxing;
public class Test {
	public static void main(String[] args) {
		GussNumber gn=new GussNumber();
		while(true) {
			int x=gn.shuru();
			gn.yanzheng(x);
		}
	}	
	}



   构造方法：
package Juxing;
import java.util.Scanner;
public class TesGussNumber {
public static int number = (int) (Math.random() * 101);// 调用Math方法中的random，// 来获取一个随机数。math中全部是double型，所以强制转换成int型
	static Scanner input;
   public static int shuru() {
		input = new Scanner(System.in);// 输入一个猜测数值
		System.out.println("请猜测一百以内的数字：");
		int guess = input.nextInt(); // 输入你猜测的数字
		return guess;
	}
  public static void yanzheng(int guess) {
			if (guess == number){
				System.out.println("恭喜你答对了！");
				System.exit(0);
			}else if (guess > number)
				System.out.println("大了");
			else
				System.out.println("小了");// 用if语句判断你输入的数字与所给的随机数比较
	}
	}
 测试：
package Juxing;

public class Test {
	public static void main(String[] args) {
		GussNumber gn=new GussNumber();
		while(true) {
			int x=gn.shuru();
			gn.yanzheng(x);
		}
	}
}
