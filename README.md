using System.Linq;

namespace MathChallenge
{
    class MainClass
    {
        public static void Main(string[] args)
        {
            CompareDigits();
            /*Input: Your program should read two integer numbers from the user with the same number of digits(example: number1 = 234, number2 = 564).
             
            Task: Check if each corresponding place in the two numbers(ones, tens, hundreds, …) sums to the same total.
            
            Output: Your program should print out: True or False based on the result.
            
            Examples:
            Number1 = 153 , Number2 = 345  => 1 + 3 ≠ 5 + 4 ≠ 3 + 5 Program prints False.Number1 = 543 , 
            Number2 = 456  => 5 + 4 = 4 + 5 = 3 + 6 Program prints True.
            
            Things to look for: 
            -Do proper validation on the user’s input.
            - Write the task in a separate method.
            - Provide adequate comments.- Provide adequate user prompts.*/
        }
      private static bool CompareDigits()
            {

                int userEnteredNum1;
                int userEnteredNum2;


            Console.WriteLine("Welcome! Are you ready for a math excercize? Your goal is to enter two sets of three integers. The corresponding place in the first set (ones, tens, hundreds), should equal the same total from the second set. Enter your first three digits: ");
                userEnteredNum1 = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("Enter three additional digits: ");
                userEnteredNum2 = Convert.ToInt32(Console.ReadLine());


                string lengthOfNum1 = userEnteredNum1.ToString();
                string lengthOfNum2 = userEnteredNum2.ToString();
            /*System.Index out of range exception. Index outside bounds of array for else (may need to change to else if) statement. Equation is needed in array for variables of numbers entered outside of 3 digits.*/
                int firstTotalPlace = Convert.ToInt32(lengthOfNum1[0] + Convert.ToInt32(lengthOfNum2[0]));
                int secondTotalPlace = Convert.ToInt32(lengthOfNum1[1] + Convert.ToInt32(lengthOfNum2[1]));
                int thirdTotalPlace = Convert.ToInt32(lengthOfNum1[2] + Convert.ToInt32(lengthOfNum2[2]));


                if ((firstTotalPlace == secondTotalPlace) && (secondTotalPlace == thirdTotalPlace) && (firstTotalPlace == thirdTotalPlace))

                {
                Console.WriteLine("True. See you in class!");    
                return true;

                }

                else if ((firstTotalPlace != secondTotalPlace) && (secondTotalPlace != thirdTotalPlace) && (firstTotalPlace != thirdTotalPlace))
                {
                Console.WriteLine("False. Maybe next time!");
                return false;

                }


                else
                {
                Console.WriteLine("That is an incorrect amount of integers. Please run again.");
                return false;

                }

                }
        }
}
