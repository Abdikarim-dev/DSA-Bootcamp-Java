[1. Build Array from Permutation]

public int[] buildArray(int[] nums) {
    int[] ans = new int[nums.length];
        
    for (int i = 0; i < nums.length;++) {
        ans[i] = nums[nums[i]];
    }
        
    return ans;

}

[2. Concatenation of Array]

static int[] getConcatenation(int[] nums) {
    int[] res = new int[nums.length*2];

    for (int i = 0,j=nums.length; i <nums.length; i++,j++) {
        res[i] = nums[i];
        res[j] = nums[i];
    }
    return res;

}

[3. Running Sum of 1d Array]

public int[] runningSum(int[] nums) {
        for(int i=1;i< nums.length ;i++){

            nums[i] = nums[i]+nums[i-1];
        
        }
        
        return nums;
    }

[4. Richest Customer Wealth]

public int maximumWealth(int[][] accounts) {
        int sum = 0;
        int max = 0;
     
        for(int row =0;row<accounts.length;row++){
            for(int column=0;column<accounts[row].length;column++){
                sum += accounts[row][column];
            }
            if(row==0){
                max=sum;
            }
            else if(sum > max){
                max = sum;
            }
            sum=0;

        }
        return max;
    }

[5. Shuffle the Array]

public int[] shuffle(int[] nums, int n) {
    int res[]  = new int[2*n];
    int k = 0;
    int j = n;
    for(int i=0;i<n;i++){
    
        res[k++] = nums[i];
          // k++;
           // 1
        res[k++] = nums[j];
           //k++;
           // 2
        j++;
    }
    return res;
}

[6. Kids With the Greatest Number of Candies]

static List<Boolean> kidsWithCandies(int[] candies, int extraCandies) {
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

[9. Create Target Array in the Given Order]

static int[] createTargetArray(int[] nums, int[] index) {
        ArrayList<Integer> array = new ArrayList<Integer>();
        
        int[] target = new int[nums.length];

        for(int i = 0;i<nums.length;i++){
            array.add(index[i],nums[i]);
        }
        for(int j = 0;j<nums.length;j++){
            target[j] = array.get(j);
        }
        return target;
    }

[10. Check if the Sentence Is Pangram] 

public boolean checkIfPangram(String sentence) {
    for (int i=97;i<=122;i++){
        if(sentence.indexOf((char)i) < 0){
            return false;
        }
    }
    return true;

}

[11. Count Items Matching a Rule]

public static int countMatches(List<List<String>> items, String ruleKey, String ruleValue) {
        int sum =0;
        for(int row =0; row<items.size();row++){
            
            if(ruleKey.equals("type") && items.get(row).get(0).equals(ruleValue)) sum++;
            
            if(ruleKey.equals("color") && items.get(row).get(1).equals(ruleValue)) sum++;
            
            if(ruleKey.equals("name") && items.get(row).get(2).equals(ruleValue)) sum++;
        }
        return sum;
    }

[12. Highest Alititude]
public int largestAltitude(int[] gain) {
    int current = 0;
    int max =0;
    for(int i : gain){
        current +=i;
        max = Math.max(max,current);
    }
    return max;

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

            swap(image[i],start ,end);

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

[15. Matrix Diagonal Sum]

static int diagonalSum(int[][] mat) {
        int d1 = 0;
        int d2 = 0;
        int col1=0;
        int col2=mat.length-1;

        for(int row1and2=0;row1and2 <mat.length;row1and2++){

            // Find the middle index
            int middleIndex = mat.length / 2;
            if(row1and2 == middleIndex && mat.length%2==1)
                d1 +=  mat[middleIndex][middleIndex];
            else{
                d1 += mat[row1and2][col1];
                d2 += mat[row1and2][col2];
            }

            // Retrieve the middle value
            //int middleValue = mat[middleIndex][middleIndex];

            col1 +=1;
            col2 -=1;
        }
        return d1+d2;

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

[17. Transpose Matrix]

static int[][] transpose(int[][] matrix) {
    int numOfRow = matrix.length;
    int numOfCol = matrix[0].length;

    int[][] res = new int[numOfCol][numOfRow];

    for(int row =0;row<numOfRow;row++){
        for(int col =0;col<numOfCol;col++){
            res[col][row] = matrix[row][col];
        }
    }
    return res;

}

[18. Add to Array-Form of Integer]
   public List<Integer> addToArrayForm(int[] num, int k){

        List<Integer> ans = new ArrayList<Integer>();
        int carry = 0;
        // [2,3,7] == we wanna access last index value = num.length-1
        for (int i = num.length-1; i >= 0 || k > 0 ; i--) {
            int sum = carry;

            if(i>=0)
                sum += num[i];
            if(k>0){
                sum += k%10;// 34 = 4 (4+7) = 11
                k /=10;
            }
            ans.add(sum%10);
            carry = sum /10;
        }
        if(carry >0)
            ans.add(carry);
        Collections.reverse(ans);
        return ans;

}

[21. Two sum]

   public int[] twoSum(int[] nums, int target) {
        int[] res = new int[2];

        for(int i = 0 ; i<nums.length;i++){

            for(int j=1 ;j<nums.length;j++){

                if(nums[i] + nums[j] == target && i!=j ){
                    
                    res[0] = i;
                    res[1] = j;

                    return res ;

                }
            }
        
        }
    return res;
    } 
