Scanner in = new Scanner(System.in);

//        [1. Factorial Program In Java]
        int factorial = 5;
        int res=1;
        for(int i = 2;i<=factorial;i++){
            res *=i;
        }
        System.out.println(res);
//        [2. Calculate Electricity Bill]
        int watts = 1000;
        double rate = 0.4;
        double finalResult = watts*rate;
        System.out.println(finalResult);
//        [3. Calculate Average Of N Numbers]
        int n = in.nextInt();
        int sum = 0;
        for (int i=1;i<=n;i++){
            System.out.print("Enter number ."+i+" ");
            int num = in.nextInt();
            sum += num;
        }
        double avg = sum / n;
        System.out.println("The average is "+avg);
//       [4. Calculate Discount Of Product]
        double listPrice = 600;
        double sellingPrice = 80;
        double discount = (listPrice - sellingPrice *100)/listPrice;
        System.out.println(discount);
//       [5. Calculate Distance Between Two Points]
        int x1=10,x2=15,y1=3,y2=8;
        double distance = sqrt((y2 - y1) * (y2 - y1) + (x2 - x1) * (x2 - x1));
        System.out.println(distance);
//        [6. Calculate Commission Percentage]

//        [ 7. Power In Java]
        int base = 3, exponent = 4;
        long result = 1;
        while (exponent != 0){
            result *=base;
            --exponent;
        }
        System.out.println("Answer = " + result);
//        [8. Calculate Depreciation of Value]
//        [9. Calculate Batting Average]
//        [10. Calculate CGPA Java Program]
//        [11. Compound Interest Java Program]
//        [12. Calculate Average Marks]
        int marks = 578;
        int subjects = 6;
        System.out.println("Avg : "+marks/subjects);
//        [13. Sum Of N Numbers]
        int d = in.nextInt();
        int iskudar = 0;
        for (int i=1;i<=n;i++){
            System.out.print("Enter number ."+i+" ");
            int num = in.nextInt();
            iskudar += num;
        }
        System.out.println(iskudar);
//        [14. Armstrong Number In Java]
//        [15. Find Ncr & Npr]
//        [16. Reverse A String In Java]

//        [17. Find if a number is palindrome or not]
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
        System.out.println(checkPalindrome(1001));
//        Future Investment Value
//        [19. HCF Of Two Numbers Program]
        System.out.print("Enter a number 1 : ");
        int number1 = in.nextInt();
        System.out.print("Enter a number 2 : ");
        int number2 = in.nextInt();

        int no1 = number1;
        int no2 = number2;
        int maxNo =  Math.min(number1,number2);
        int i = 2;
        int hcf=1;
        while (i<=maxNo){
            if(number1 % i == 0 && number2 % i ==0){
                hcf *= i;
                number1 /=i;
                number2 /=i;
            }
            else
                i++;
        }
        System.out.println("The Highest Common Divisor : "+hcf);
//       [20. LCM Of Two Numbers]
        int lcm = 1;
        int j= 2;
        while (j<=maxNo){
            if(no1 % j == 0 && no2 % j ==0){
                lcm *= j;
                no1 /=j;
                no2 /=j;
            }
            else if(no1 % j == 0){
                lcm *=j;
                no1 /=j;
            }
            else if(no2 % j == 0){
                lcm *=j;
                no2 /=j;
            }
            else{
                j++;
            }
        }
        System.out.println("The Least Common Divisor : "+lcm);

//        [21. Java Program Vowel Or Consonant]
        char inp = 'f';
        if(inp > 'a' && inp <= 'z' ){
            if(inp =='a' || inp =='e' || inp =='i' || inp =='o' || inp =='u')
                System.out.println("Vowel");
            else
                System.out.println("Consonant");
        }
//        [22. Perfect Number In Java]

//       [23. Check Leap Year Or Not]
        int year = in.nextInt();
        if(year % 4 == 0)
            System.out.println("Leap year");
        else
            System.out.println("Not...");
//        [24. Sum Of A Digits Of Number]
        int sumOfDigits = 0;
        int s = in.nextInt();
        while(s>0){
            int rem = s%10;
            sumOfDigits += rem;
            s/=10;
        }
        System.out.println(sumOfDigits);
//       [25. Kunal is allowed to go out with his friends only on the even days of a given month. Write a program to count the number of days he can go out in the month of August.]
        int daysAllowed=0;
        for(int k = 2; k <=30;k+=2){
            daysAllowed++;
        }
        System.out.println(daysAllowed);
//        [26. Write a program to print the sum of negative numbers, sum of positive even numbers and the sum of positive odd numbers from a list of numbers (N) entered by the user. The list terminates when the user enters a zero.]

    