# Codsoft_java
# 1- Project Java;
# Guess number game

import java.util.*;
/**
 * Random_num
 */
 
public class Main{

    public static void main(String[] args) {
        
        int Ran_num = 1 + (int)(100
                               * Math.random());
        
        try (Scanner sc = new Scanner(System.in)) {
            
            int user;
            int times = 5;

            int count = 0;

            for(int i=0 ; i<times ; i++){
                
                System.out.println("Guess your number ");
                user = sc.nextInt();

                if(user < Ran_num ){

                    System.out.println(user + " Your number is less than exact value");
                    System.out.println(5-(i+1) + " Left chance");
                    count ++;
                }
                else if(user > Ran_num){
                    System.out.println(user + " Your number is greater then exact value");
                    System.out.println(5-(i+1) + " Left chance");
                    count++;
                }
                else{
                    System.out.println(user + " Your number is equal exact value");
                    System.out.println( "you take " + count++ + " times to choosing correct number");
                    System.out.println("You are win !!");
                }

            }
            
                 System.out.println( Ran_num + " It's Random Value");
        }
    }
}


#2- Project Java
# Student Check Grades

import java.util.Scanner;

/**
 * student_grades
 */
public class Main {
    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter student numbers ");
        System.out.println("Math ");
        int math = sc.nextInt();
        System.out.println("Physics ");
        int phy = sc.nextInt();
        System.out.println("Chemistry");
        int chem = sc.nextInt();
        System.out.println("English " );
        int Eng = sc.nextInt();
        System.out.println("Hindi");
        int hin = sc.nextInt();

        float total = math + phy + chem+ Eng + hin;

        System.out.println("Student total number: " + total);

        float per = total / 5;
        
        System.out.println("Student percentage: " + per + "%");

        if(per <= 45){
            System.out.println("Third division");
        }
        else if(per < 60  && per > 45 ){
            System.out.println("Second Division");
        }
        else {
            System.out.println("Fisrt division");
        }
    }

}
