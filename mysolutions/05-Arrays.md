[3. Running Sum of 1d Array]

public int[] runningSum(int[] nums) {
        for(int i=1;i< nums.length ;i++){
            nums[i] = nums[i]+nums[i-1];
        }
        return nums;
    }

[6. Kids With the Greatest Number of Candies]

public List<Boolean> kidsWithCandies(int[] candies, int extraCandies) {
        List<Boolean> list = new ArrayList<>();
        int max = 0;
        for(int i=0;i<candies.length;i++){
            if(candies[i]>max)
                max=candies[i];
        }
        for (int kid = 0; kid <candies.length ; kid++) {
            if(candies[kid]+extraCandies >= max)
                list.add(true);
            else
                list.add(false);
        }
        return list;
}

[7. Number of Good Pairs]

public int numIdenticalPairs(int[] nums) {
        int out = 0;
        for(int i=0;i<nums.length;i++){
            for(int j=nums.length-1;i<j;j--)
                if(nums[i]==nums[j] && i<j)
                    out++;
        }
        return out;
}

[8. How Many Numbers Are Smaller Than the Current Number]

public int[] smallerNumbersThanCurrent(int[] nums) {
        int[] res = new int[nums.length];
    for(int i=0;i<nums.length;i++){
        for(int j=0;j < nums.length;j++){
            if(nums[i] > nums[j] && i!=j){
                res[i] += 1;
            }
        }
    }
    return res;
}

[13. Flipping an Image]

public int[][] flipAndInvertImage(int[][] image) {
    for(int i = 0 ; i < image.length;i++){
        for(int j=0;j < image[i].length;j++){
             if(image[i][j] == 0)
                 image[i][j] = 1;
             else
                 image[i][j] = 0;
        }
        int start = 0;
        int end = image[i].length-1;
        for(int j=0;j <= image.length;j++){
            while(start < end){
//                swap(image[i],start ,end);
                int temp = image[i][end];
                image[i][end] = image[i][start];
                image[i][start]= temp ;
                start++;
                end--;
            }
        }
    }
    return image;
}
[16. Find Numbers with Even Number of Digits]

public int findNumbers(int[] nums) {
    int[] temp = nums;
    int sum = 0;
    int even =0;
    for(int i =0;i<nums.length;i++){
        while(temp[i] >0){
            int rem = temp[i] % 10;
            temp[i] /=10;
            sum++;
        }
        if(sum % 2 == 0){
            even++;
            sum =0;
        }
        else
            sum=0;
    }
    return even;
}
