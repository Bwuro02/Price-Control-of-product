import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;
 

class Product {
    private final String name;
    private final double price;

    public Product(String name, double price) {
        this.name = name;
        this.price = price;
    }

    public String getName() {
        return name;
    }

    public double getPrice() {
    return price;
    }
}

public class PriceComparisonProgram {
    public static void main(String[] args){
        try (Scanner scanner = new Scanner(System.in)) {
            List<Product> products = new ArrayList<>();
            
            // Input at least 20 different prices
            for (int i = 1; i <= 20; i++) {
                System.out.print("Enter the name of product " + i + ": ");
                String name = scanner.nextLine();
                
                System.out.print("Enter the price of product " + i + ": ");
                double price = scanner.nextDouble();
                scanner.nextLine(); // consume the newline character
                
                products.add(new Product(name, price));
            }
            
            // Compare prices and display the result
            System.out.println("\nComparison Result:");
            for (int i = 0; i < products.size(); i++) {
                for (int j = i + 1; j < products.size(); j++) {
                    Product product1 = products.get(i);
                    Product product2 = products.get(j);
                    
                    int result = Double.compare(product1.getPrice(), product2.getPrice());
                    
                    if (result == 0) {
                        System.out.println(product1.getName() + " and " + product2.getName() + " have the same price.");
                    } else if (result < 0) {
                        System.out.println(product1.getName() + " is cheaper than " + product2.getName() + ".");
                    } else {
                        System.out.println(product1.getName() + " is more expensive than " + product2.getName() + ".");
                    }
                }
            }
        }
    }
}

