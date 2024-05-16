Check Two Strings are Anagram or Not
Anagrams words have the same word length, but the characters are rearranged, here we have coded a java program to find out whether two words are anagram or not
Lets take an example
Consider two strings elbow and below
Both the strings have the same length
Both the strings have same letters
But the letters are re-arranged in a way to form two different words
some more examples of anagram words are arc and car, state and taste, night and thing and  many more
 

Checking if two strings are anagram or not in C
Algorithm
Take string input from user and store it in the variable called “str” .
Call isAnagram() method by passing two string as parameter .
Write if condition if(s1.length()!=s2.length()) set statue = false;
else  convert both array to character arrya using toCharArray()
After that sort both the array using Arrays class sort() after that return status
Code in Java (Check Two Strings are Anagram or Not)
import java.util.Arrays;
import java.util.Scanner;
public class CheckIfTwoStringsAreAnagramAreNot {
    static boolean isAnagram(String str1 , String str2) {
    String s1 = str1.replaceAll("[\\s]", "");
    String s2 = str2.replaceAll("[\\s]", "");
    boolean status=true;

     if(s1.length()!=s2.length())
         status = false;
     else {
         char[] a1 = s1.toLowerCase().toCharArray();
         char[] a2 = s2.toLowerCase().toCharArray();
         Arrays.sort(a1);
         Arrays.sort(a2);
         status = Arrays.equals(a1, a2);
       }
       return status;
} 
   public static void main(String[] args) {
     Scanner sc = new Scanner(System.in);
     System.out.print("Enter two String :");
     String s1 = sc.next();
     String s2 = sc.next();
     boolean status = isAnagram(s1,s2);
       if(status)
          System.out.println(s1+" and "+s2+" are Anagram");
       else 
          System.out.println(s1+" and "+s2+" are not Anagram");
       }
}
Output
Enter two String : prep
repp
prep and repp are Anagram
