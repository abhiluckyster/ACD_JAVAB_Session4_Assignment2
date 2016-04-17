# ACD_JAVAB_Session4_Assignment2
import java.util.Scanner;
public class SortArray {
	Scanner input = new Scanner(System.in);
	int i, temp,num;
	public void insert(int a[] )
	{
		System.out.println("Enter total number you want to enter");
		num = input.nextInt();
		for(i =1; i<=num; i++)
		{
			System.out.println("Enter "+i+" number");
			a[i-1]=input.nextInt();
		}
		System.out.println("Array is ");
		for(i =1; i<=num; i++)
		{
			System.out.println(i+" number is "+a[i-1]+"; ");
		}
	}
		
	public void sortArray(int a[])
	{
		for(i=0; i<=num;i++)
			for(int j=i; j>0; j--)
			{
				if(a[j]<a[j-1])
				{
					temp = a[j-1];
					a[j-1]=a[j];
					a[j]=temp;
				}
			}
		System.out.println("Sorted Array is ");
		for(i =1; i<=num; i++)
		{
			System.out.println(i+" number is "+a[i]+"; ");
		}
		input.close();
	}
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int a[]=new int[100];
		SortArray sa = new SortArray();
		sa.insert(a);
		sa.sortArray(a);
	}

}
