// Student-Grade-Calculator
import java.util.Scanner;

public class GradeCalculator {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        final int NUM_SUBJECTS = 5; 
        int[] marks = new int[NUM_SUBJECTS];
        int totalMarks = 0;
        for (int i = 0; i < NUM_SUBJECTS; i++) {
            System.out.print("Enter marks for subject " + (i + 1) + " (out of 100): ");
            marks[i] = scanner.nextInt();
            totalMarks += marks[i];
        }
        double averagePercentage = (double) totalMarks / NUM_SUBJECTS;
        char grade;
        if (averagePercentage >= 90) {
            grade = 'A';
        } else if (averagePercentage >= 80) {
            grade = 'B';
        } else if (averagePercentage >= 70) {
            grade = 'C';
        } else if (averagePercentage >=35) {
            grade = 'D';
        }  else {
            grade = 'F'; // Fail if below 35%
        }
        System.out.println("Total Marks: " + totalMarks);
        System.out.println("Average Percentage: " + averagePercentage + "%");
        System.out.println("Grade: " + grade);er
        scanner.close();
    }
}
