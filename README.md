import java.util.Scanner;
public class TaxCalculator{
    public static void main (String[] args){
        Scanner scanner = new Scanner(System.in);

        // Prompt user for weekly income
        System.out.print("Enter your weekly income: $");
        double income = scanner.nextDouble();

        // Calculate tax withholding based on income
        double taxWitholding = calculateTaxWitholding(income);

        // Display the weekly average tax withholding
        System.out.println("Weekly avarage tax witholding: $" + taxWitholding);
    }

    public static double calculateTaxWitholding(double income){
        double taxRate;

        // Determine tax rate based on income
        if (income < 500){
            taxRate = 0.10;
        } else if (income < 1500){
            taxRate = 0.15;
        } else if (income < 2500){
            taxRate = 0.20;
        } else {
            taxRate = 0.30;
        }

        //  Calculate tax withholding
        double taxWitholding = income * taxRate;

        return taxWitholding;
    }
}
