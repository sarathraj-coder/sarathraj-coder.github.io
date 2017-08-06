### 1) Using default in the interface  

 	Java 8 enables us to add non-abstract method implementations to interfaces by utilizing the default keyword.

 		public class Java801 {
    	void addData(){
        	Calculator c= new Calculator(){
            	@Override
            	public int add() {
               	return 100+getValue();
            }
       		 };
      	 System.out.print("Sum with default value:"+ c.add());  
   		}
    
    	public static void main(String[] args){
        new Java801().addData();
    	}
		}

		interface Calculator{
       		 default int getValue(){
            return 555;
        	}
        	int add();
		}