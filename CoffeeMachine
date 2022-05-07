package machine;
import java.util.Scanner;
public class CoffeeMachine {
    public static void prepareCoffee() {
        System.out.println("Starting to make a coffee");
        System.out.println("Grinding coffee beans");
        System.out.println("Boiling water");
        System.out.println("Mixing boiled water with crushed coffee beans");
        System.out.println("Pouring coffee into the cup");
        System.out.println("Pouring some milk into the cup");
        System.out.println("Coffee is ready!");
    }
    public static void neededIngredients(int cupNumber) {
        System.out.println("For "+cupNumber+" cups of coffee you will need:");
        System.out.println(cupNumber*200+" ml of water");
        System.out.println(cupNumber*50+" ml of milk");
        System.out.println(cupNumber*15+" g of coffee beans");
    }
    public static int cupNumberCapableMaking(int water, int milk, int bean) {
        return Math.min(water/200,Math.min(milk/50,bean/15));
    }
    public static void cupsAvailable(int water,int milk,int beans ,int cups) {
        if(cupNumberCapableMaking(water,milk,beans)==cups) {
            System.out.println("Yes, I can make that amount of coffee ");
        }
        else if(cupNumberCapableMaking(water,milk,beans)<cups) {
            System.out.println("No, I can make only "+cupNumberCapableMaking(water,milk,beans)+" cup(s) of coffee");
        }
        else if(cupNumberCapableMaking(water,milk,beans)>cups) {
            System.out.println("Yes, I can make that amount of coffee (and even "+(cupNumberCapableMaking(water,milk,beans)-cups)+" more than that)");
        }
    }
    public static void machineOperations() {
        Scanner scan = new Scanner(System.in);
        Scanner sc = new Scanner(System.in);
        int water = 400;
        int milk = 540;
        int beans = 120;
        int cups = 9;
        int money = 550;
        String operation ="";
        while(!operation.equals("exit")) {
            System.out.println("Write action (buy, fill, take, remaining, exit): ");
            operation = scan.next();
            switch(operation) {
                case "buy" :
                    System.out.println("What do you want to buy? 1 - espresso, 2 - latte, 3 - cappuccino: ");
                    String coffeeType = sc.next();
                    switch(coffeeType) {
                        case "1" :
                            if(water<250) {
                                System.out.println("can't make coffe, don't have enough water");
                                break;
                            }
                            if(beans<16) {
                                System.out.println("can't make coffe, don't have enough beans");
                                break;
                            }
                            if(money<4) {
                                System.out.println("can't make coffe, don't have enough money");
                                break;
                            }
                            if(cups<1) {
                                System.out.println("can't make coffe, don't have enough cups");
                                break;
                            }
                            System.out.println("I have enough resources, making you a coffee!");
                            water -= 250;
                            beans -= 16;
                            money += 4;
                            cups -=1;

                            break;
                        case "2" :
                            if(water<350) {
                                System.out.println("can't make coffe, don't have enough water");
                                break;
                            }
                            if(beans<20) {
                                System.out.println("can't make coffe, don't have enough beans");
                                break;
                            }
                            if(money<7) {
                                System.out.println("can't make coffe, don't have enough money");
                                break;
                            }
                            if(cups<1) {
                                System.out.println("can't make coffe, don't have enough cups");
                                break;
                            }
                            if(milk<100) {
                                System.out.println("can't make coffe, don't have enough cups");
                                break;
                            }
                            System.out.println("I have enough resources, making you a coffee!");
                            water -= 350;
                            milk -= 75;
                            beans -= 20;
                            money += 7;
                            cups -= 1;

                            break;
                        case "3" :
                            if(water<200) {
                                System.out.println("can't make coffe, don't have enough water");
                                break;
                            }
                            if(beans<12) {
                                System.out.println("sorry, not enough beans!");
                                break;
                            }
                            if(money<6) {
                                System.out.println("sorry, not enough money!");
                                break;
                            }
                            if(cups<1) {
                                System.out.println("sorry, not enough cups!");
                                break;
                            }
                            if(milk<100) {
                                System.out.println("sorry, not enough milk!");
                                break;
                            }
                            System.out.println("I have enough resources, making you a coffee!");
                            water -= 200;
                            milk -= 100;
                            beans -= 12;
                            money += 6;
                            cups -= 1;
                            break;
                        case "back" :
                            break;
                    }
                    break;
                case "fill" :
                    System.out.println("Write how many ml of water you want to add: ");
                    water += scan.nextInt();
                    System.out.println("Write how many ml of milk you want to add: ");
                    milk += scan.nextInt();
                    System.out.println("Write how many grams of coffee beans you want to add: ");
                    beans += scan.nextInt();
                    System.out.println("Write how many disposable cups of coffee you want to add: ");
                    cups += scan.nextInt();
                    break;
                case "take" :
                    System.out.println("I gave you $"+money);
                    money = 0;
                    break;
                case "remaining" :
                    System.out.println("The coffee machine has:");
                    System.out.println(water+" ml of water");
                    System.out.println(milk+" ml of milk");
                    System.out.println(beans+" g of coffee beans");
                    System.out.println(cups+" disposable cups");
                    System.out.println("$"+money+" of money");
                    break;

            }
        }
    }
    public static void main(String[] args) {

        machineOperations();
    }
}
