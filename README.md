# orderagnosticbinsearch



package com.company;
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] arr = {12, 233, 343, 433, 3333, 233333};
        int target = 343;

        System.out.println(index(arr,target));
    }


    public static int index(int[] arr,int targ){
        int start =0;
        int end = arr.length-1;


        if (arr[start]>arr[end]){
            System.out.println("Descending sort");
        while(start<=end){
            int mid = start + ((end - start)/2);
            //System.out.println(mid);
            if (targ>arr[mid]){
                end = mid - 1;
            }
            else if(targ<arr[mid]){
                start = mid + 1;
            }
            else{
                return mid;
            }
        }
        return -1;
    }

        else{
            System.out.println("Ascending sort");

            while(start<=end){
                int mid = start + ((end - start)/2);
                //System.out.println(mid);
                if (targ>arr[mid]){
                    start = mid + 1;
                }
                else if(targ<arr[mid]){
                    end = mid - 1;
                }
                else{
                    return mid;
                }
            }
            return -1;
        }
        }
}
