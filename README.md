# Tanaka
/*
 * Justin Yang
 * 11/26/22
 * Compares text files
 */

 //imports
 
import java.io.FileNotFoundException;
import java.util.Scanner;
import java.io.File;


public class Text {

	public static void main(String[] args) throws FileNotFoundException{
        Scanner textA, textB, lineA, lineB;
        // Assigns text files to textA and textB
        textA = new Scanner(new File("/Users/justinyang/Downloads/AP CSA/5.13/5.13/TextA.txt"));
        textB = new Scanner(new File("/Users/justinyang/Downloads/AP CSA/5.13/5.13/TextB.txt"));

        // Loops through both text files and assigns it to string text1 and text2 
        while(textA.hasNextLine()&& textB.hasNextLine()){
            String text1 = textA.nextLine();
            String text2 = textB.nextLine();
            lineA = new Scanner(text1);
            lineB = new Scanner(text2);
            while(lineA.hasNextLine()&&lineB.hasNextLine()){
                String line1 = lineA.nextLine();
                String line2 = lineB.nextLine();
                if(!line1.equals(line2)){
                    System.out.println("Line A: " + line1);
                    System.out.println("Line B: " + line2);
                }
            }
        }
    }
    
}
