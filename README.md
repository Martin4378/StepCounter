# StepCounter

import java.util.Scanner;

public class P48_StepCounter {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        int steps = 0;
        int goal = 10000;

        while (true) {
            String type = scanner.nextLine();

            if (type.equalsIgnoreCase("Going home")) {
                int number = Integer.parseInt(scanner.nextLine());
                steps += number;
                break;
            }

            int num = Integer.parseInt(type);
            steps += num;
            if (steps >= goal){
                break;
            }


        }
        if (steps >= goal){
            System.out.println("Goal reached! Good job!");
        }
        else {
            System.out.printf("%d more steps to reach goal.",(goal - steps));
        }
    }

}
