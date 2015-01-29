# CollectionExample
My Collection Example  Demo

package com.delhiguru.collection;

import java.util.ArrayList;
import java.util.LinkedHashSet;
import java.util.List;
import java.util.Scanner;

public class StringExample {
	public static void main(String[] ars){ 
	StringBuilder str = new StringBuilder("india");
	StringBuffer str1=new StringBuffer("Binit Kumar jha");
	System.out.println("string = " + str);
    System.out.println("String reverse.........."+str1);
	// reverse characters of the StringBuilder and prints it
	System.out.println("reverse = " + str.reverse());
	System.out.println("reverse = " + str1.reverse());
	
	
	//without using fuction
	   String a="Siva";
	   for(int i=0;i<=a.length()-1;i++)
	    {
	     System.out.print(a.charAt(i));
	    }

	    for(int i = a.length() - 1; i >= 0; --i)
	    {
	     System.out.println(a.charAt(i)); 
	    }
	    
	  /*  //reverse string using user input
	      String reverse = "";
	      Scanner in = new Scanner(System.in);
	 
	      System.out.println("Enter a string to reverse");
	      String original = in.nextLine();
	 
	      int length = original.length();
	 
	      for ( int i = length - 1 ; i >= 0 ; i-- )
	         reverse = reverse + original.charAt(i);
	 
	      System.out.println("Reverse of entered string is: "+reverse);*/
	      
	      
	      //copy data from one arraylist to another arraylist 
	      List<String> list=new ArrayList<String>();
	      list.add("Binit");
	      list.add("mohan");
	      list.add("sohan");
	      list.add("Binit");
	      System.out.println("List ="+list);
	     // List<String> list1=new ArrayList<String>();
	     
	      
	      
	     // List<String> list1 = new ArrayList<String>(list);
	      List<String> list1 = new ArrayList<String>();
	      list1.add("Binit");
	      list1.add("sohan");
	      list1.add("rani");
	      list.addAll(list1);
	      System.out.println("list all data...."+list);
	      LinkedHashSet<String> listToSet = new LinkedHashSet<String>(list);
	      System.out.println("ArrayList after removing duplicates in same order: " + listToSet);

	      
	      //java program to return the sum of all integers found in the parameter String
	      String str2 = "5 hi when 5 and 9";
	      str2=str2.replaceAll("[\\D]+"," ");
	      String[] numbers=str2.split(" ");
	      int sum = 0;
	      for(int i=0;i<numbers.length;i++){
	          try{
	              sum+=Integer.parseInt(numbers[i]);
	          }
	          catch( Exception e ) {
	            //Just in case, the element in the array is not parse-able into Integer, Ignore it
	          }
	      }
	      System.out.println("The sum is:"+sum);
	
	}
}


//number exist
public class NumberExistExample {
	public static void main(String args[]) throws IOException
	{
		String str;
		int vowels = 0, digits = 0, blanks = 0;
		char ch;

		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

		System.out.print("Enter a String : ");
		str = br.readLine();

		for(int i = 0; i < str.length(); i ++)
		{
			ch = str.charAt(i);

			if(ch == 'a' || ch == 'A' || ch == 'e' || ch == 'E' || ch == 'i' || 
			ch == 'I' || ch == 'o' || ch == 'O' || ch == 'u' || ch == 'U')
				vowels ++;
			else if(Character.isDigit(ch))
				digits ++;
			else if(Character.isWhitespace(ch))
				blanks ++;
		}

		System.out.println("Vowels : " + vowels);
		System.out.println("Digits : " + digits);
		System.out.println("Blanks : " + blanks);
	}

}


//list itertor
public class MyListIterator {
	public static void main(String[] args){
		List<String> list=new ArrayList<String>();
		list.add("Binit");
		list.add("Mohan");
		list.add("Eric");
		list.add("sohan");
		System.out.println("Before listIterte:::"+list);
		ListIterator<String> itr=list.listIterator();
		while(itr.hasNext()){
			System.out.println("After listiterator:::"+itr.next());
		}
		while(itr.hasPrevious()){
			System.out.println("After priovous::::"+itr.previous());
		}
	
	}

}

