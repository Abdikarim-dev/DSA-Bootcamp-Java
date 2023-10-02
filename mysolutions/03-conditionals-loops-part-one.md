//Part 1
//        [1. Area Of Circle Java Program]
        {int radius = 10;
        double circle =  Math.PI * Math.pow(radius,2);
        System.out.println(circle);}
//        [2. Area Of Triangle]
        double base = 10;
        double height = 10;
        double triangle = (base*height)/2;
        System.out.println(triangle);
//        [3. Area Of Rectangle Program]
        double width = 10;
        double length = 10;
        double rectangle = width*length;
        System.out.println(rectangle);
//        [4. Area Of Isosceles Triangle]
        double isosceles = (base*height)/2;
        System.out.println(isosceles);
//        [5. Area Of Parallelogram]
        double parallelogram = base * height;
        System.out.println(parallelogram);
//        [6. Area Of Rhombus]

        double pDiagonal = 10;
        double qDiagonal = 10;
        double rhombus = (pDiagonal * qDiagonal) /2;
        System.out.println(rhombus);
//        [7. Area Of Equilateral Triangle]

        double a = 60;
        double equilateral = ((3 * 0.5) * (a*a))/4;
        System.out.println(equilateral);
//        [8. Perimeter Of Circle]
        double perimeterOfCircle = 2 * Math.PI * radius;
        System.out.println(perimeterOfCircle);
//        [9. Perimeter Of Equilateral Triangle]
        double perimeterOfEquilateralTriangle = 3*a;
        System.out.println(perimeterOfEquilateralTriangle);
//        [10. Perimeter Of Parallelogram]
        double perimeterOfParallelogram = 2 * (a+base);
        System.out.println(perimeterOfParallelogram);
//        [11. Perimeter Of Rectangle]
        double perimeterOfRectangle = 2*(a+length);
        System.out.println(perimeterOfRectangle);
//        [12. Perimeter Of Square]
        double perimeterOfSquare = 4*a;
        System.out.println(perimeterOfSquare);
//        [13. Perimeter Of Rhombus]
        double perimeterOfRhombus = 4*a;
        System.out.println(perimeterOfRhombus);
//        [14. Volume Of Cone Java Program]
        double volumeOfCone = (Math.PI *Math.pow(radius,2)*height)/3;
//        [15. Volume Of Prism]
        double baseArea = 30;
        double volumeOfPrism = baseArea*height;
        System.out.println(volumeOfPrism);
//        [16. Volume Of Cylinder]
        double volumeOfCylinder = Math.PI * Math.pow(radius,2) * height;
        System.out.println(volumeOfCylinder);
//        [17. Volume Of Sphere]
        double volumeOfSphere = 4 * Math.PI * (Math.pow(radius,3)) /3;
//        [18. Volume Of Pyramid]
        double volumeOfPyramid = length * width *height /3;
        System.out.println(volumeOfPyramid);
//        [19. Curved Surface Area Of Cylinder]
        double CurvedSurfaceAreaOfCylinder = 2 * Math.PI * Math.pow(radius,2) * height;
        System.out.println(CurvedSurfaceAreaOfCylinder);
//        [20. Total Surface Area Of Cube]
        double TotalSurfaceAreaOfCube = 6  *(a*a);
        System.out.println(TotalSurfaceAreaOfCube);
//        [21. Fibonacci Series In Java Programs]
        int pos1 = 0;
        int pos2 = 1;
        int count = 2;
        int inp = 5;
        String out = pos1+" "+pos2+" ";
        while (count < inp ){
            int temp = pos2;
            pos2 = pos1+pos2;
            pos1=temp;
            out += pos2;
        }
        System.out.println(out);
//        [22. Subtract the Product and Sum of Digits of an Integer]
        System.out.println(subtractProductAndSum(12345));
//        [23. Input a number and print all the factors of that number (use loops).]
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int res = 1;
        for(int i=2;i<=n;i++){
            res *=i;
        }
        System.out.println(res);
//        [24. Take integer inputs till the user enters 0 and print the sum of all numbers (HINT: while loop)]
        int sum = 0;
        System.out.println("Enter a number !! that's not a zero!!!");
        int x = in.nextInt();
        while(x != 0){
            sum +=x;
            System.out.println("Enter a number !! that's not a zero!!!");
            x = in.nextInt();
        }
        System.out.println(sum);
//        [25. Take integer inputs till the user enters 0 and print the largest number from all.]
        int largest = 0;
        System.out.println("Enter a number !! that's not a zero!!!");
        int s = in.nextInt();
        while(x != 0){
            int temp = s;

            System.out.println("Enter a number !! that's not a zero!!!");
            x = in.nextInt();
        }
        System.out.println(sum);
//        [26. Addition Of Two Numbers]
        int n1 = in.nextInt();
        int n2 = in.nextInt();
        System.out.println(n1+n2);
    
    public static int subtractProductAndSum(int n) {
        int sum=0;
        int product = 1;
        int res;
        while(n>0){
            int rem = n%10;
            sum +=rem;
            product *= rem;
            n /=10;
        }
        return product-sum;
    }