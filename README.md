# CODALPHA-TASKS
 TASK 1 - STUDENT GRADE TRACKER
import java.util.Scanner;

public class GradeCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input the number of students
        System.out.print("Enter the number of students: ");
        int numStudents = scanner.nextInt();

        // Declare arrays to store student names and grades
        String[] studentNames = new String[numStudents];
        double[] studentGrades = new double[numStudents];

        // Input student names and grades
        for (int i = 0; i < numStudents; i++) {
            System.out.print("Enter name of student " + (i + 1) + ": ");
            studentNames[i] = scanner.next();
            System.out.print("Enter grade of " + studentNames[i] + ": ");
            studentGrades[i] = scanner.nextDouble();
        }

        // Calculate average, highest, and lowest grades
        double total = 0;
        double highest = studentGrades[0];
        double lowest = studentGrades[0];
        String highestStudent = studentNames[0];
        String lowestStudent = studentNames[0];

        for (int i = 0; i < numStudents; i++) {
            total += studentGrades[i];
            if (studentGrades[i] > highest) {
                highest = studentGrades[i];
                highestStudent = studentNames[i];
            }
            if (studentGrades[i] < lowest) {
                lowest = studentGrades[i];
                lowestStudent = studentNames[i];
            }
        }

        double average = total / numStudents;

        // Display results
        System.out.println("\nResults:");
        System.out.println("Average grade: " + average);
        System.out.println("Highest grade: " + highest + " by " + highestStudent);
        System.out.println("Lowest grade: " + lowest + " by " + lowestStudent);

        scanner.close();
    }
}


COMPANY NAME - CODEALPHA 
NAME - MANYA SRIVASTAVA 
INTERN ID - CA/MA1/6231
DOMAIN - JAVA PROGRAMMING 
DURATION - 15 TH MAY TO 15 TH JUNE 

