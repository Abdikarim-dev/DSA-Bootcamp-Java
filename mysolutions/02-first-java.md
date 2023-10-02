//        //1. Write a program to print whether a number is even or odd, also take input from the user.
       Scanner in = new Scanner(System.in);
//        System.out.println("Enter the number to check if even or Odd!!");
        int n = in.nextInt();

        if(n%2==0)
            System.out.println("Odd");
        else
            System.out.println("Even");
//
//        //2. Take name as input and print a greeting message for that particular name.
        String name = in.nextLine();
        System.out.println("Hello mr/mrs "+name);
//
//        //3. Write a program to input principal, time, and rate (P, T, R) from the user and find Simple Interest.
        int principal = in.nextInt();
        int time = in.nextInt();
        int rate = in.nextInt();
        System.out.println("The simple interest is "+(principal*time*rate));
//
//        //4. Take in two numbers and an operator (+, -, *, /) and calculate the value. (Use if conditions)
        int n1 = in.nextInt();
        int n2 = in.nextInt();
        char op = in.next().trim().charAt(0);

        if(op=='+'){
            System.out.println(n1+n2);
        }
        else if (op=='-'){
            System.out.println(n1-n2);
        }
        else if (op=='*'){
            System.out.println(n1*n2);
        }
        else if (op=='/'){
            if(n2==0){
                System.out.println("it cannot be divided by zero!");
            }
            else
                System.out.println(n1/n2);
        }
//
//        //5. Take 2 numbers as input and print the largest number.
        int num1 = in.nextInt();
        int num2 = in.nextInt();

        if(num1 > num2)
            System.out.println(num1);
        else
            System.out.println(num2);
//
//        //6. Input currency in rupees and output in USD.
        double inr = in.nextInt();
        System.out.println(inr/83.04);

        //7. To calculate Fibonacci Series up to n numbers.
        int fib1 = 0;
        int fib2 = 1;

        int nthFib = in.nextInt();
        int count = 2;
        String out = "";
        out += fib1 +" "+fib2;
        while (count<nthFib){
            int temp = fib2;
            fib2 = fib1+fib2;
            fib1 = temp;
            out +=" "+fib2;
            count++;
        }
        System.out.println(out);

        //8. To find out whether the given String is Palindrome or not.
        String palindrome = "soosi";
        boolean isPal = false;
        for(int i=0,j = palindrome.length()-1;i<j;i++,j--){
            if(palindrome.charAt(i)==palindrome.charAt(j))
                isPal = true;
            else{
                isPal=false;
                break;
            }
        }
        System.out.println(isPal?"Palindrome":"Not Palindrome.");

        //9. To find Armstrong Number between two given number.
        int s = in.nextInt();
        int sum = 0;
        int original= s;
        while(s>0){
            int rem = n&10;
            s /=10;
            sum = sum + rem*rem*rem;
        }
        if(sum==original)
            System.out.println("Palindrome");
        else
            System.out.println("not a palindrome");