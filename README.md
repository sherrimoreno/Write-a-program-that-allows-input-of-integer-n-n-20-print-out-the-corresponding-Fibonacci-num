# Write-a-program-that-allows-input-of-integer-n-n-20-print-out-the-corresponding-Fibonacci-num
Write a program that allows input of integer n( n &lt;= 20 ), print out the corresponding Fibonacci number.
import java.util.Scanner;

public class Fibonacci
{
    public int CalculateFi(int n)
    {
       if (n == 0 || n == 1){
          return 1;
       }
       return CalculateFi(n-1) + CalculateFi(n-2);
    }
}

public class HelloWorld
{
    public static void main(String[] args)
    {
       int n;
       int Fi;
       System.out.println("Integer:");
       Scanner sc = new Scanner(System.in);

       n = sc.nextInt();

       Fibonacci fibonacci = new Fibonacci();
       Fi = fibonacci.CalculateFi(n);

       System.out.println("Fi(" + n + ") = " + Fi);
    }
}
