# ARRAYS
Study related arrays

Array - array is basically storing a list of any data
variable - variable store the single value

&& How to initialize array &&
int arr[] = new int[n] - inside this box bracket it will notify the size of the array

int max = arr[0]

int n = arr.length  - length of the array of not given 

int m = arr[0].length - same length giving for the single array 


*** some conding examples ***

1. 2 largest element 

import java.io.*;
import java.util.*;

class Solution {
    public void SecondLargest(int[] arr, int n) {
        int maximumElement = arr[0];
        int indexOfMaximumElement = 0;
        
        for(int i=1; i<n; i=i+1)
        {
            if(arr[i] > maximumElement)
            {
                maximumElement = arr[i];
                indexOfMaximumElement = i;
            }
        }
        
        maximumElement = Integer.MIN_VALUE; // very big negative value -2*10^9 
        
        for(int i=0;i<n;i=i+1)
        {
            if(i!=indexOfMaximumElement)
            {
                if(arr[i]>maximumElement)
                {
                    maximumElement = arr[i];
                }
            }
        }
        
        System.out.println(maximumElement);
        
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n= sc.nextInt();
      	int[] arr= new int[n];

      	for(int i=0;i<n;i++)
            arr[i]=sc.nextInt();
            
        
        Solution Obj = new Solution();
        Obj.SecondLargest(arr,n);
        sc.close();
        
    }
}


2. A contest

import java.io.*;
import java.util.*;
// kth - par_score
// count no. - score > 0 && score > par_score(kth)
public class Main {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
      int n = sc.nextInt();
      int k = sc.nextInt();
      int a[] = new int[n];
      
      for(int i=0;i<n;i++){
        a[i]=sc.nextInt();
      }
      int count=0;
      int par_score=a[k-1];
      
      for(int i=0;i<n;i++){
        if(a[i]>0 && a[i]>=par_score){
          count++;
        }
      }
      System.out.println(count);
    }
}
