import java.util.Scanner;
import java.util.*;

public class  Studentcalculator{
  public static void main(String[] args) {
  Scanner sc = new Scanner(System.in);
    System.out.println("Enter the number of subjects : ");
    int numSubjects = sc.nextInt();
    int [] mark = new int[numSubjects];
    int total_marks = 0;
    for (int i = 0; i < numSubjects; i++){
     System.out.println("Enter the marks of Subjects" + (i+1) + "(out of 100):"); 
      mark[i] = sc.nextInt();
      total_marks += mark[i];
    }
    // average calculation 
    double avgPercentage = (double) total_marks / numSubjects;
    char Grade;

    if(avgPercentage >= 90){
      Grade = 'A';
    }
      
    else if(avgPercentage >= 80){
       Grade = 'B';
    }
      
    else if(avgPercentage >= 70){
       Grade = 'C';
    }
     else if(avgPercentage >= 60){
         Grade = 'D';
      }
    else{
      Grade = 'E';
    }
    // Display 
    System.out.println("Total marks: " + total_marks);
    System.out.println("avgrage_Percentage: " + avgPercentage);
    System.out.println("Grade : " + Grade);
  }
}
