## Throws

* In java, <span style="color:blue">throws</span> keyword is used for declaring exceptions. If any method is accountable for throwing exceptions, the <span style="color:blue">throws</span> keyword lets the caller of that method aware of those unhandled exceptions and compels the caller to use try-catch block.


	```Java
	public class ExceptionHandling {
    		void toBeInvoked() throws Exception{
        		System.out.println("I may contain exception");
    		}
    		void caller(){
        		toBeInvoked();
    		}
	}
	```

	* The above code won't compile because there is an unhandled exception. Method toBeInvoked() uses the <span style="color:blue">throws</span> keyword in its signature to warn the caller that it might throw an exception. So, the caller must use a try-catch block to handle that exception.

     
	* To resolve this try-catch block is used-

	```Java
	public class ExceptionHandling {
    		void toBeInvoked() throws Exception{
        		System.out.println("I may contain exception");
    		}
    		void caller(){
        		try{
            			toBeInvoked();
        		}catch(Exception e){
            			System.out.println("Handling exception: "+e);
			}
    		}
	}
	```
