# Assignment5.2
package mypack;

public interface Stack {
	void push(int i);
     int pop();
}
package mypack;

public class FixedStack  implements Stack{
	      int i;
          final static int DEFAULT_SIZE = 5; 
    
	public FixedStack(int i) {
			super();
			this.i = i;
		}

	@Override
	public void push(int i) {
		// TODO Auto-generated method stub
		if (i > DEFAULT_SIZE){
			System.out.println("Stack overflow occured for fixedStack");			
		}	
		else{
			System.out.println("Stack push created for fixedStack");
		}
				
	}

	@Override
	public int pop() {
		// TODO Auto-generated method stub
		System.out.println("fixed stack pop operation");
		return 0;
	}

}
package mypack;

public class VariableStack implements Stack{
	int i;
	final static int DEFAULT_SIZE = 5; 

	public VariableStack(int i) {
		super();
		this.i = i;
	}

	@Override
	public void push(int i) {
		// TODO Auto-generated method stub
		System.out.println("new element added for variable stack");	
		
	}

	@Override
	public int pop() {
		// TODO Auto-generated method stub
		System.out.println("Variable stack pop operaion");	
		return 0;
	}
	

}
package mypack;

import java.util.Scanner;

public class MainStack {
      
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Stack st;
		System.out.println("Number statcks needs to be created");
		Scanner sc = new Scanner(System.in);
		int i = sc.nextInt();				       
       st = new FixedStack(i);
       st.push(i);
       st.pop();
       st = new VariableStack(i);
       st.push(i);
       st.pop();    
       
       
	}

}
