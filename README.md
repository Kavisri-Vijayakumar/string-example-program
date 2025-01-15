package stringoperationsenhanced;
import java.util.Scanner;
public class Stringoperationsenhanced {
    public static void main(String[] args) { 
        try (Scanner scanner = new Scanner (System.in)) {
            System.out.println("enter the first string:");
            String str1=scanner.nextLine();
            System.out.println("enter the second string:");
            String str2=scanner.nextLine();
            System.out.println("\n choose a string function");
            System.out.println("1.find length");
            System.out.println("2.convert to upper case");
            System.out.println("3.convert to lower case");
            System.out.println("4.reverse the string");
            System.out.println("5.concatenate the string");
            System.out.println("6.compare the string");
            System.out.println("7.check if substring exists");
            System.out.println("8.replace a character");
            System.out.println("9.find character at index");
            System.out.println("10.split the string");
            System.out.println("11.trim whitespace");
            System.out.println("12.check if string is empty");
            System.out.println("13.convert to character array");
            System.out.println("14.exit"); 
            int choice;
            do{
                System.out.println("\n enter your choice");
                choice=scanner.nextInt();
                scanner.nextLine();
                switch(choice){
                    case 1:
                        System.out.println("lenght of first string"+str1.length());
                        System.out.println("lenght of second string"+str2.length());
                        break;
                    case 2:
                        System.out.println("first string in upper case:"+str1.toUpperCase());
                        System.out.println("second string in upper case:"+str2.toUpperCase());
                        break;
                    case 3:
                        System.out.println("first string in lower case:"+str1.toLowerCase());
                        System.out.println("second string in lower case:"+str2.toLowerCase());
                        break;
                    case 4:
                        System.out.println("Reversed first string: "+new StringBuilder(str1).reverse());
                        System.out.println("reversed second string: "+new StringBuilder(str2).reverse());
                        break;
                    case 5:
                        System.out.println("concatenated string is:"+str1.concat(str2));
                        break;
                    case 6:
                        int comparision = str1.compareTo(str2);
                        if(comparision==0) {
                            System.out.println("the strings are equal");
                        } else if(comparision > 0) {
                            System.out.println("the first string is lexicographically greater");
                        }else {
                            System.out.println("the second string is lexicographically greater");
                        }
                        break;
                    case 7:
                        System.out.println("enter the substring to check in the first string");
                        String substring = scanner.nextLine();
                        System.out.println("the substring exists in the first string"+str1.contains(substring));
                        break;
                    case 8:
                        System.out.println("enter the character to replace: ");
                        char oldchar = scanner.next().charAt(0);
                        System.out.println("enter the new character");
                        char newchar = scanner.next().charAt(0);
                        System.out.println("First string after replacement: "+ str1.replace(oldchar, newchar));
                        System.out.println("Second string after replacement: "+ str2.replace(oldchar, newchar));
                        break;
                    case 9:
                        System.out.print("Enter the index to find the character (0-based):");
                        int index = scanner.nextInt();
                        try {
                            System.out.println("Character at index "+ index + " in first string: "+ str1.charAt(index));
                            System.out.println("Character at index "+ index + "in second string: " + str2.charAt(index)); 
                        } catch (IndexOutOfBoundsException e) {
                            System.out.println("Index out of range!");
                        }
                        break;
                    case 10:
                        System.out.print("Enter the delimiter to split the first string: ");
                        String delimiter = scanner.nextLine();
                        String[] parts = str1.split(delimiter);
                        System.out.println("First string split into parts:");
                        for (String part : parts) {
                            System.out.println(part);
                        }
                        break;
                    case 11:
                        System.out.println("First string after trimming: [" + str1.trim() + "]");
                        System.out.println("Second string after trimming: [" + str2.trim() + "]");
                        break;
                    case 12:
                        System.out.println("Is the first string empty? "+ str1.isEmpty());
                        System.out.println("Is the second string empty? " + str2.isEmpty());
                        break;
                    case 13:
                        System.out.println("Character array of first string:");
                        for (char c : str1.toCharArray()) {
                            System.out.print(c + "");
                        }
                        System.out.println();
                        break;
                    case 14:
                        System.out.println("Exiting...");
                        break;
                    default:
                        System.out.println("Invalid choice. Please try again.");
                }
            } while (choice != 14);
        }
     }
}

Output
enter the first string:
kavi
enter the second string:
sri

 choose a string function
1.find length
2.convert to upper case
3.convert to lower case
4.reverse the string
5.concatenate the string
6.compare the string
7.check if substring exists
8.replace a character
9.find character at index
10.split the string
11.trim whitespace
12.check if string is empty
13.convert to character array
14.exit

 enter your choice
3
first string in lower case:kavi
second string in lower case:sri

 enter your choice
 5
concatenated string is:kavisri
