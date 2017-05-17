Java核心卷  第三章

1. 访问修饰符用于控制程序的其他部分对该段代码的访问级别;

   1. int 4个字节

   2. short 2个字节

   3. double 8个字节

   4. long 8个字节

   5. float 4个字节

      1. float类型的数值有一个后缀F或f。没有后缀F的浮点数值默认为double类型。也可以在浮点数值后面添加后缀D或d;

   6. byte 1个字节

2. 下面使用于表示溢出和出错情况的三个特殊的浮点数值：

   1. 正无穷大

   2. 负无穷大

   3. NaN

   4. 例如：一个正整数除以0的结果为正无穷大;计算0/0或者负数的平分根结果为NaN

3. 二进制系统中无法精确地表示分数1/10,这就好像十进制无法精确表示分数1/3一样。如果在数值计算中不允许有任何舍入误差，就应该使用BigDecimal类;

4. char类型原本用于表示单个字符。不过，现在情况已经有所变化;

5. char类型的字面量值要用单引号括起来; ‘A’是编码值为65所对应的字符常量，它与"A"表示不同，"A"是包含一个字符A的字符串;

6. Unicode转义序列会在解析代码之前得到处理;\(注意注释空格\u\)

7. 专业术语解析java语言中解决Unicode中字符超过65635个字符的问题：

   1. 码点：是指一个编码表中的某个字符对应的代码值;

8. 声明一个变量之后，必须用赋值语句对变量进行显式初始化，千万不要使用未初始化的变量;

9. 在java中，利用关键字final指示常量。关键字final表示这个变量只能被赋值一次。一旦被赋值成功，就不能够再更改了;

10. 整数被0除将会产生一个异常，而浮点数被0除将会得到无穷大或NaN结果;

11. 强制类型转换通过折断小数点部分将浮点型转换为浮点型;

12. 不要在boolean类型与任何数值类型之间进行强制类型转换;少数情况的时候，可以使用条件表达式 b？1：0

13. 移位运算符的使用：

    1. &lt;&lt;表示左移，左移一位表示原来的值乘2;

    2. ![](/assets/import.png)

    3. 同理，&gt;&gt;表示右移，右移一位表示除2;

    4. 位移运算符还包括： 与\(&\)、非\(～\)、或\(\|\)、异或\(^\)

14. 为了避免变量中可能保存一个错误的值，可以自定义枚举类型;枚举类型包括有限个命名的值

15. 使用equals\(\)方法检测两个字符串是否相等;比较的可以使字符串变量，也可以是字符串字面量;一定不要使用==运算符检测两个字符串是否相等，实际上，只有字符串常量是共享的;

    1. ```java
       public class TestCharpt {
       	public static void main(String[] args) {
       		String string = "Hello";
       		String string2 = "Hello";
       		StringBuffer stringBuffer = new StringBuffer();
       		stringBuffer.append(string);
       		if (string == "Hello") {
       			System.out.println("true");
       			//表示两个字符串放在同一个地方
       		}
       		if (string == string2) {
       			System.out.println("true2");
       		}
       		if (string.equals(string2)) {
       			System.out.println("true2");
       			System.out.println(string.hashCode());
       			System.out.println(string2.hashCode());
       		}
		
       	}
       }
       ```

16. 空串" "是长度为0的字符串，空串是一个Java对象，有自己串长度（长度为0）和内容（内容为空）;String变量还可以存放一个特殊的值，名为null，这表示目前没有任何对象与该变量关联;

17. Java字符串由char值序列组成; char数据类型是一个采用UTF-16编码表示Unicode码点的代码单元 
18. 


