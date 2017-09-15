using System;
using System.Linq;

namespace DeliverableOne
{
    class MainClass
    {
        public static void Main(string[] args)
        {
            CompareDigits();
            
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
                Console.WriteLine("False. Maybe next time!");
                return false;

                }

                }
        }
}
