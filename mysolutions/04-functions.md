[1.Define two methods to print the maximum and the minimum number respectively among three numbers entered by the user.]

[2.Define a program to find out whether a given number is even or odd.]

static String checkEvenOrOdd(int n){
        String s="";
        if(n%2==0)
            s="Even";
        else
            s="Odd";
        return s;
    }

[3.A person is eligible to vote if his/her age is greater than or equal to 18. Define a method to find out if he/she is eligible to vote.]

static String eligibleToVote(int age){
        String s = "";
        if(age>=18)
            s="You re eligible to vote!!!";
        else
            s="Youre not eligible to vote";
        return s;
    }

[4. Write a program to print the sum of two numbers entered by user by defining your own method.]
static double sumOftwoValues(int n1,int n2){
        return n1+n2;
    }

[5.Define a method that returns the product of two numbers entered by user.]
static double productOftwoValues(int n1,int n2){
        return n1*n2;
    }

[6.Write a program to print the circumference and area of a circle of radius entered by user by defining your own method.]

static double circumferenceAndAreaOfCircle(double r){
        return Math.PI * r * 2;
    }

[7.Define a method to find out if a number is prime or not.]

static boolean isPrime(int n){
        if(n<=1)
            return false;
        int c = 2;
        while (c*c<=n){
            if(n%c == 0)
                return false;
            c++;
        }
        return c * c > n;
    }

[8.Write a program that will ask the user to enter his/her marks (out of 100). Define a method that will display grades according to the marks entered as below:]

static String displayGrade(int n){
        String s = "";
        if(n>=91 && n<= 100)
            s="AA";
        else if(n>=81 && n<=90)
            s="AB";
        else if(n>=71 && n<=80)
            s="BB";
        else if(n>=61 && n<=70)
            s="BC";
        else if(n>=51 && n<=60)
            s="CD";
        else if(n>=41 && n<=50)
            s="DD";
        else if (n>=0 && n<=40)
            s="Fail";
        else
            s="Invvalid Mark";

        return s;
    }

[9.Write a program to print the factorial of a number by defining a method named 'Factorial'. Factorial of any number n is represented by n! and is equal to 1 * 2 * 3 * .... * (n-1) *n. E.g.-]
[
    4! = 1 * 2 * 3 * 4 = 24 
    3! = 3 * 2 * 1 = 6 
    2! = 2 * 1 = 2 
    Also, 
    1! = 1 
    0! = 1
]

static int nFactorial(int n){
        int fac=1;
        for (int i=2;i<=n;i++){
            fac *= i;
        }
        if(n == 0 || n == 1)
            return 1;
        return fac;
    }

[10.Write a function to find if a number is a palindrome or not. Take number as parameter.]

static boolean checkPalindrome(int n){
        boolean isPal = false;
        int temp = n;
        int out=0;
        while (n>0) {
            int rem = n % 10;
            out = out * 10 + rem;
            n /= 10;
        }
        if(temp==out)
            isPal=true;

        return isPal;
    }

[11.Convert the programs in flow of program, first java, conditionals & loops assignments into functions.]

[12.Write a function to check if a given triplet is a Pythagorean triplet or not. (A Pythagorean triplet is when the sum of the square of two numbers is equal to the square of the third number).]

[13.Write a function that returns all prime numbers between two given numbers.]

[14.Write a function that returns the sum of first n natural numbers.]
