import java.util.Arrays;

class Remove{  
public static int remove(int arr[], int n){  
        int[] temp = new int[n];  
        int j = 0;  
        for (int i=0; i<n-1; i++){  
            if (arr[i] != arr[i+1]){  
                temp[j++] = arr[i];  
            }  
         }  
        temp[j++] = arr[n-1];     
        for (int i=0; i<j; i++){  
            arr[i] = temp[i];  
        }  
        return j;  
    }  
}

public class Jala {
public static void main(String[] args) 
	{
	int arr[] = {10,70,30,90,20,20,30,40,70,50};
    Arrays.sort(arr);
    int length = arr.length;  
    Remove obj = new Remove();
    length = obj.remove(arr, length);
    for (int i=0; i<length; i++)
    { 
       System.out.print(arr[i]);

	}
	
    }
}
