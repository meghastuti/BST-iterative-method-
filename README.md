public class BinarySearch {				
    int binarySearch(int arr[], int search)				
    {				
        int left = 0,  right = arr.length - 1;				
        while (left<= right) 				
        {				
            int mid = (right +left) / 2;				
 				
           if (arr[mid] == search)				
				return mid;
				
			if (arr[mid] < search)	
				left = mid + 1;
				
			if (arr[mid] > search)	
				right = mid - 1;
        }				
          return -1;				
   }				
  				
    public static void main(String args[])				
    {				
       	BinarySearch tree = new BinarySearch();			
	int arr[] = { 2, 3, 4, 15, 25, 40, 60, 70 };		
	int search = 25;		
	int result = tree.binarySearch(arr, search);		
	if (result == -1)		
		System.out.println("Element not present");	
	else		
		System.out.println("Element index " + result);	

    }				
}				
			
