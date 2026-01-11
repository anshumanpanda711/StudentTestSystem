# StudentTestSystem

namespace StudentTestSystem;

class Program
{
    static void Main(string[] args)
    {
        string teacherName, runAgain;
        int numberOfStudents, score, totalScore, highestScore, lowestScore;
        float averageScore;
        //Random random = new Random();
        //int[] students = new int[random.Next(25, 33)];
        //for (int i = 0; i < students.Length; i++)
        //{
        //    students[i] = random.Next(100);
        //}
        Console.WriteLine("Welcome to the Student Test System!");
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
        }
            
    }
}
