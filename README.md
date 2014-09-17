//Assignment-1
//============

//SI 543 - Calculator Assignment 
//Calculator Main:
package calc;

public class CalculatorMain {

	public static void main(String[] args) {

		SimpleCalculator s = new SimpleCalculator(5.5);
		
		s.add(4);
		s.add(8);
		
		System.out.println("Calculation 1 (simple) - Expected Value: 17.5, Calculated Value: " + s.getCurrentNumber() + "\n");
		
		ComplexCalculator c = new ComplexCalculator(10.5);
		
		c.add(2);
		c.subtract(3);
		c.multiply(8);
		c.add(2);
		c.divide(2);
		c.power(2);
		
		System.out.println("Calculation 2 (complex) - Expected Value: 1521.0, Calculated Value: " + c.getCurrentNumber());
		
		c.clear();
		c.add(5);
		c.subtract(3);
		c.power(4);
		c.divide(4);
		System.out.println("Calculation 2 (complex) - Expected Value: 4.0, Calculated Value: " + c.getCurrentNumber() + "\n");
		
		
		
		// ~
		// Uncomment the rest of these lines only if you choose to implement the extra functions //
		
		/* 
		
		c.clear();
		c.add(4);
		
		System.out.println("Challenge 1 - Is " + c.getCurrentNumber() + " even?");
		System.out.println("Expected Answer: true, Calculated Answer: " + c.isEven() + "\n");
		
		c.add(3);
		
		System.out.println("Challenge 2 - Is " + c.getCurrentNumber() + " even?");
		System.out.println("Expected Answer: false, Calculated Answer: " + c.isEven() + "\n");
		
		System.out.println("Challenge 3 - Is " + c.getCurrentNumber() + " a prime number?");
		System.out.println("Expected Answer: true, Calculated Answer: " + c.isPrime() + "\n");
		
		c.add(1);
		
		System.out.println("Challenge 4 - Is " + c.getCurrentNumber() + " a prime number?");
		System.out.println("Expected Answer: false, Calculated Answer: " + c.isPrime());

		*/

	}

}

//ComplexCalculator
package calc;

public class ComplexCalculator {

	private double currentNumber;
	
	// constructor
	public ComplexCalculator(double d) {
		currentNumber = d;
	}
	
	// adds d to current number
	public void add(double d) {
		currentNumber = currentNumber + d;
	}
	
	// subtract()
	public void subtract (double d){
		currentNumber = currentNumber - d;
	}
	
	// multiply()
	public void multiply (double d){
		currentNumber = currentNumber * d;
	}
		
	// divide()
	public void divide (double d){
		currentNumber = currentNumber / d;
	}
	
	// clear()
	public void clear () {
		currentNumber = 0;
	}
	
	// power()
	public void power (double d){
		currentNumber = Math.pow (currentNumber, d);
	}
	
	public double getCurrentNumber() {
		return currentNumber;
	}
	
	//////////////////////////////////////////////////
	// EXTRA FUNCTIONS - not needed for full credit //
	
	// isEven()
	// TODO returns true is current number is even, false otherwise
	
	// isPrime()
	// TODO returns true if current number is a prime number, false otherwise
	
	////////////////////////////////////////////////////
	
}
//Simple Calculator:
package calc;

public class SimpleCalculator {

	private double currentNumber;
	
	public SimpleCalculator(double d) {
		
		this.currentNumber = d;
		
	}
	
	public void add(double d) {
		
		currentNumber = currentNumber + d;
		
	}
	
	public double getCurrentNumber() {
		
		return currentNumber;
		
	}
	
}
