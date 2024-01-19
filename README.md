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


# 2- Project Java
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

# 3-Project Java
# Currency Convertor

import java.util.Scanner;

     public class Main{
              public static void main(String[] args){
              Scanner sc = new Scanner(System.in);
              System.out.println("Enter the country code \n Indian rupees: 1 \n Us Dollar: 2 \n British Pound: 3 \n Kuwaiti Dinar: 4" );
              int code = sc.nextInt();
              double amount ;

             if(code == 1 ){
                 System.out.println("Enter amount in Indian rupees");
                 amount = sc.nextDouble();
                 System.out.println("US Dollar: " + amount * 0.0120251584 );
                 System.out.println("British Pound: " +  amount * 0.0094919);
                 System.out.println("Kuwaiti Dinar: " + amount * 0.0037033 );
             }
             else if(code == 2 ){
                 System.out.println("Enter amount in US Dollar");
                 amount = sc.nextDouble();
                 System.out.println("Indian Rupees: " + amount * 83.158988 );
                 System.out.println("British Pound: " +  amount * 0.788848 );
                 System.out.println("Kuwaiti Dinar: " + amount * 0.307875 );
             }
             else if(code == 3 ){
                 System.out.println("Enter amount in British Pound");
                 amount = sc.nextDouble();
                 System.out.println("Indian Rupees: " + amount * 105.427);
                 System.out.println("US Dollar: " +  amount * 1.26814);
                 System.out.println("Kuwaiti Dinar: " + amount * 0.390428);
             }
             else if(code == 4 ){
                 System.out.println("Enter amount in Kuwaiti Dinar");
                 amount = sc.nextDouble();
                 System.out.println("Indian Rupees: " + amount * 270.025);
                 System.out.println("US Dollar: " +  amount * 3.24805);
                 System.out.println("British Pound: " + amount *2.56003 );
             }
             else{
                 System.out.println("Invalid Code ");
             }
         }
     }
    }

