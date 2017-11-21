## Notes

* A primitive type value can be automatically converted to an object using a wrapper class, and vice versa, depending on the context.

* Converting a primitive value to a wrapper object is called boxing. The reverse conversion is called unboxing.

* Java allows autoboxing and autounboxing.

* Autoboxing-
	
	```Java
	Integer intObject = 2;
	```
	* What actually is happening-
	
	```Java
	Integer intObject= new Integer(2);
	```

* Autoboxing while declaring and initializing array in one statemenet
	
	```Java
	Integer[] arr = {1, 2, 3};
	```
	* What actually is happening-
	
	```Java
	arr=new Integer(1);
	arr=new Integer(2);
	arr=new Integer(3);
	```
* Autounboxing while printing that array: arr;
	
	```Java
	System.out.println(intArray[0] + intArray[1] + intArray[2]);
	```

	* The objects intArray[0], intArray[1], and intArray[2] are automatically unboxed into int values that are added together.


* Autoboxing using Generics

	```Java
	List<Integer> li = new ArrayList<>();
	for (int i = 1; i < 50; i += 2)
    	li.add(i);
	```
	
	* Although you add the int values as primitive types, rather than Integer objects, to li, the code compiles. Because li is a list of Integer objects, not a list of int values, you may wonder why the Java compiler does not issue a compile-time error. The compiler does not generate an error because it creates an Integer object from i and adds the object to li. Thus, the compiler converts the previous code to the following at runtime:

	```Java
	List<Integer> li = new ArrayList<>();
	for (int i = 1; i < 50; i += 2)
    	li.add(Integer.valueOf(i));
	```