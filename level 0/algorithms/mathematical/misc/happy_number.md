## Happy Number

 
Write an algorithm to determine if a number is "happy".

What is an happy number can be shown in the following example:

    19 is a happy number
    1^2 + 9^2 = 82
    8^2 + 2^2 = 68
    6^2 + 8^2 = 100
    1^2 + 0^2 + 0^2 = 1

## Java Solution


    public boolean isHappy(int n) {
        HashSet<Integer> set = new HashSet<Integer>();
     
        while(!set.contains(n)){
            set.add(n);
     
            n = getSum(n);
     
            if(n==1)
                return true;
        }
     
        return false;
    }
     
    public int getSum(int n){
        int sum =0;
        while(n>0){
            sum+=(n%10)*(n%10);
            n=n/10;
        } 
        return sum;    
    }
