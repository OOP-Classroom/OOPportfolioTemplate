# ﻿3 Selection and Iteration
***Ensure you commit the exercises to GitHub.***

## Programming Projects:
***1) Computing A Pay Increase***


File Salary.java contains most of a program that takes as input an employee's salary and a rating of the employee's performance and computes the raise for the employee. The performance rating here is being entered as a String—the three possible ratings are "Excellent", "Good", and "Poor". An employee who is rated excellent will receive a 6% raise, one rated good will receive a 4% raise, and one rated poor will receive a 1.5% raise. 


Add the if... else... statements to program Salary to make it run as described above. Note that you will have to use the equals method of the String class (not the relational operator ==) to compare two strings.

```
// ***************************************************************
//   Salary.java
//
//   Computes the amount of a raise and the new
//   salary for an employee.  The current salary
//   and a performance rating (a String: "Excellent",
//   "Good" or "Poor") are input.
// ***************************************************************


import java.util.Scanner;
import java.text.NumberFormat;


public class Salary
{
   public static void main (String[] args)
   {
       double currentSalary;  // employee's current  salary
       double raise;          // amount of the raise
       double newSalary;      // new salary for the employee
       String rating;         // performance rating


       Scanner scan = new Scanner(System.in);


       System.out.print ("Enter the current salary: ");
       currentSalary = scan.nextDouble();
       System.out.print ("Enter the performance rating (Excellent, Good, or Poor): ");
       rating = scan.next();


       // Compute the raise using if ...


       newSalary = currentSalary + raise;


       // Print the results
       NumberFormat money = NumberFormat.getCurrencyInstance();
       System.out.println();
       System.out.println("Current Salary:       " + money.format(currentSalary));
       System.out.println("Amount of your raise: " + money.format(raise));
       System.out.println("Your new salary:      " + money.format(newSalary));
       System.out.println();
    }
}
```


```
Sample Output:


Enter the current salary: 53187.54
Enter the performance rating (Excellent, Good, or Poor): Excellent


Current Salary:       $53,187.54
Amount of your raise: $3,191.25
Your new salary:      $56,378.79
```

	

***2) Rock, Paper, Scissors***


Program Rock.java contains a skeleton for the game Rock, Paper, Scissors. Add statements to the program as indicated by the comments so that the program asks the user to enter a play, generates a random play for the computer, compares them and announces the winner (and why). 


Note that the user should be able to enter either upper or lower case r, p, and s. The user's play is stored as a string to make it easy to convert whatever is entered to upper case. Use a switch statement to convert the randomly generated integer for the computer's play to a string.

```
// ****************************************************************
//   Rock.java
//
//   Play Rock, Paper, Scissors with the user
//          
// ****************************************************************
import java.util.Scanner;
import java.util.Random;


public class Rock
{
   public static void main(String[] args)
   {
      String personPlay;    //User's play -- "R", "P", or "S"
        String computerPlay;  //Computer's play -- "R", "P", or "S"
        int computerInt;      //Randomly generated number used to determine
                              //computer's play


        Scanner scan = new Scanner(System.in);
        Random generator = new Random();


        //Get player's play -- note that this is stored as a string
        //Make player's play uppercase for ease of comparison
        //Generate computer's play (0,1,2)
        //Translate computer's randomly generated play to string
        switch (computerInt)
        {


        }


        //Print computer's play
        //See who won.  Use nested ifs instead of &&.
        if (personPlay.equals(computerPlay))  
            System.out.println("It's a tie!");
        else if (personPlay.equals("R"))
            if (computerPlay.equals("S"))
                System.out.println("Rock crushes scissors.  You win!!");
            else


                //...  Fill in rest of code
   }
}
```

***3) String Reverser***

Write a small program that prompts the user for a sentence and then outputs the same sentence with the characters in each word reversed. For example, if the user enters “This is a sample sentence.” then the output would be “sihT si a elpmas .ecnetnes.” Note the use of multiple Scanner objects may be helpful with this program.


***4) Punctuation Marks***


Design and implement a program that counts the number of punctuation marks in the following string “Mary had a little lamb, her fleece was as white as snow, and everywhere Mary went, the lamb was sure to go.
-that was a nice poem-
the end.
”. 
Produce a table that shows how many times each symbol occurred.


