# StudentTestSystem

namespace StudentTestSystem;

class Program
{

    static void Main(string[] args)
    {
    
        string teacherName, runAgainStr = "";
        bool runAgain = true;
        
        int numberOfStudents, score, totalScore, highestScore, lowestScore;
        float averageScore;
        
        Console.WriteLine("Welcome to the Student Test System!");
        while (runAgain)
        {
            runAgain = false;
            Console.WriteLine("Please enter the teacher's name");
            teacherName = Console.ReadLine();
            Console.WriteLine("Welcome to the System, " + teacherName);

            Console.WriteLine("Please enter the number of students: ");
            numberOfStudents = Convert.ToInt32(Console.ReadLine());


            totalScore = 0;
            highestScore = 0;
            lowestScore = 100;

            for (int i = 0; i < numberOfStudents; i++)
            {
                score = -1;
                while (score < 0 || score > 100)
                {
                    Console.WriteLine("Please enter a score between 0 and 100");
                    score = Convert.ToInt32(Console.ReadLine());
                }

                totalScore += score;

                if (score > highestScore)
                {
                    highestScore = score;
                }

                if (score < lowestScore)
                {
                    lowestScore = score;
                }

                if (score > 90)
                {
                    Console.WriteLine("Grade 9 Assigned.");
                }
                else if (score > 77)
                {
                    Console.WriteLine("Grade 8 Assigned.");
                }
                else if (score > 68)
                {
                    Console.WriteLine("Grade 7 Assigned.");
                }
                else if (score > 59)
                {
                    Console.WriteLine("Grade 6 Assigned.");
                }
                else if (score > 50)
                {
                    Console.WriteLine("Grade 5 Assigned.");
                }
                else
                {
                    Console.WriteLine("Student Failed.");
                }

            }

            averageScore = totalScore / numberOfStudents;
            Console.WriteLine("Average Score: " + averageScore);
            Console.WriteLine();
            while (runAgainStr != "Y" || runAgainStr != "N")
            {
                Console.WriteLine("Run Again? Enter Y for yes or N for no");
                runAgainStr = Console.ReadLine().ToUpper();
            }

            if (runAgainStr == "Y")
            {
                runAgain = true;
            }
            else
            {
                runAgain = false;
            }
        }
    }
}


