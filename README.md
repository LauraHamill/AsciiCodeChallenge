# AsciiCodeChallenge
Create a method which will return user input as ascii code
Create another method to then decode ascii code to find out the name

/**
 * 
 */
package challenge;
import java.util.Arrays;
import java.util.Scanner;

/**
 * @author laura
 *
 */
public class CodeChallenge {

	/**
	 * @param args
	 */
	public static void main(String[] args) {
		
		System.out.println("Please enter your name");
		
		//open scanner
		Scanner scanner = new Scanner(System.in);
		// set input
		String name = scanner.nextLine();
		System.out.println("String to be coded - " + name);
		int[] coded = code(name);
		System.out.println(Arrays.toString(coded));
		scanner.close();
		
		System.out.println("Now to return your code name as a string");
		char[] uncoded = decode(coded);
		System.out.println(Arrays.toString(uncoded));
	}
  
  /**
  * method to change name into code
  */
	public static char[] decode(int[] coded) {
		char[] uncoded = new char[coded.length];
		for (int loop = 0; loop < coded.length; loop++) {
			uncoded[loop] = (char) coded[loop];
		}
		return uncoded;
	}
    /**
  * method to change code into name
  */
	private static int[] code(String name) {
		int [] coded = new int [name.length()];
		for (int loop = 0; loop < name.length(); loop++) {
			coded [loop] = (int) name.charAt(loop);
	}
		return coded;

	}
	
			
			
} // end of class
		
		
		
	



