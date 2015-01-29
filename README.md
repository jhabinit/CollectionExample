# CollectionExample
My Collection Example  Demo
//Search and delete in list
public class MyCollectionIterator {
	public static void main(String[] args){
		String removeList="Mohan";
		List<String> list=new ArrayList<String>();
		list.add("Binit");
		list.add("Rohan");
		list.add("Mohan");
		list.add("Ravi");
		list.add("Anand");
		list.add("Rohan");
		System.out.println("List of Item::::::"+list);
		/*Iterator<String> itr=list.iterator();
		while(itr.hasNext()){
			if(removeList.equals(itr.next())){
				itr.remove();
			}
			//System.out.println("after Iterator:::::"+itr.next());
		}
		System.out.println("After Remove List::::"+list);*/
		for(String r:list){
			list.remove(r);
		}
	}

}

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

//iterator example
public class IteratorExample {
	public static void main(String args[]){
		List<Integer> list=new ArrayList<Integer>();
		list.add(1);
		list.add(5);
		list.add(3);
		//list.add("binit");
		System.out.println("List of item"+list);
		System.out.println("to get idex......."+list.get(0));
		System.out.println("Does list contains 5? "+list.contains("5"));
		list.add(2,11);
		System.out.println("after List of item"+list);
		System.out.println("size of list of item"+list.size());
		System.out.println("Index of list of item"+list.indexOf(5));
		Collections.sort(list);
        System.out.println("After sort"+list);
        
       /* List<String> list1=new ArrayList<String>();
		list1.add("1");
		list1.add("binit");
		list1.add("ram");
		list1.add("aman");
		list1.add("10");
		list1.add("5");
		//list.add("binit");
		System.out.println("List of item"+list1);
        Collections.sort(list1);
        System.out.println("After sort"+list1);
        Iterator<String> itr=list1.iterator();
        	while(itr.hasNext())
        	{
        		System.out.println("list-------"+itr.next());
        	}
        
        	
        	Map<Integer,String> map=new HashMap<Integer,String>();
        		map.put(1,"binit");
        		map.put(2, "mohan");
        		map.put(3, "rahul");
        		map.put(4, "binod");
        		map.put(5,"varsha");
        		System.out.println("List of-----"+map);
        		
        		*/
        
        List<Integer> li = new ArrayList<Integer>();
        ListIterator<Integer> litr = null;
        li.add(23);
        li.add(98);
        li.add(29);
        li.add(71);
        li.add(5);
        litr=li.listIterator();
        System.out.println("Elements in forward directiton");
        while(litr.hasNext()){
            System.out.println(litr.next());
        }
        System.out.println("Elements in backward directiton");
        while(litr.hasPrevious()){
            System.out.println(litr.previous());
        }
        
        String removeElem = "Perl";
		List<String> myList = new ArrayList<String>();
		myList.add("Java");
		myList.add("Unix");
		myList.add("Oracle");
		myList.add("C++");
		myList.add("Perl");
		System.out.println("Before remove:");
		System.out.println(myList);
		Iterator<String> itr = myList.iterator();
		while(itr.hasNext()){
			if(removeElem.equals(itr.next())){
				itr.remove();
			}
		}
		System.out.println("After remove:");
		System.out.println(myList);
		
		
		 Vector<String> lang = new Vector<String>();
	        Enumeration<String> en = null;
	        lang.add("JAVA");
	        lang.add("JSP");
	        lang.add("SERVLET");
	        lang.add("EJB");
	        lang.add("PHP");
	        lang.add("PERL");
	        en = lang.elements();
	        while(en.hasMoreElements()){
	            System.out.println(en.nextElement());
	        }
        	
	        
	        Hashtable<String, String> hm = new Hashtable<String, String>();
			//add key-value pair to Hashtable
			hm.put("first", "FIRST INSERTED");
			hm.put("second", "SECOND INSERTED");
			hm.put("third","THIRD INSERTED");
			System.out.println(hm);
			Set<String> keys = hm.keySet();
			for(String key: keys){
				System.out.println("Value of "+key+" is: "+hm.get(key));
			}
			
			
			
			HashMap<String, String> hm1 = new HashMap<String, String>();
			//add key-value pair to hashmap
			hm1.put("first", "FIRST INSERTED");
			hm1.put("second", "SECOND INSERTED");
			hm1.put("third","THIRD INSERTED");
			System.out.println(hm1);
			
			Set<String> keys1 = hm.keySet();
			for(String key: keys1)
			{ 
				System.out.println("Value of "+key+" is: "+hm.get(key));
			} 
			//getting value for the given key from hashmap
			System.out.println("Value of second: "+hm1.get("second"));
			System.out.println("Is HashMap empty? "+hm1.isEmpty());
			hm1.remove("third");
			System.out.println(hm1);
			System.out.println("Size of the HashMap: "+hm1.size());
			
			
			if(hm1.containsValue("SECOND INSERTED")){
				System.out.println("The hashmap contains value SECOND INSERTED");
			} else {
				System.out.println("The hashmap does not contains value SECOND INSERTED");
			}
			
			//How to get all keys from HashMap?
			//Set<String> keys = hm.keySet();
			for(String key: keys){
				System.out.println(key);
			}
			
			
			//How to get entry set from HashMap?
			Set<Entry<String, String>> entires = hm.entrySet();
			for(Entry<String,String> ent:entires){
				System.out.println(ent.getKey()+" ==> "+ent.getValue());
			}
        
	}
