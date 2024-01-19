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
