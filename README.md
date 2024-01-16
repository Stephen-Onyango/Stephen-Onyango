import java.util.ArrayList;
import java.util.List;

class Order {
    private int orderId;
    private String customerName;
    private List<String> items;

    public Order(int orderId, String customerName, List<String> items) {
        this.orderId = orderId;
        this.customerName = customerName;
        this.items = items;
    }

    // Getters and setters

    public int getOrderId() {
        return orderId;
    }

    public String getCustomerName() {
        return customerName;
    }

    public List<String> getItems() {
        return items;
    }

    // Other methods, if needed
}

public class OrderManagementSystem {
    private static List<Order> ordersDatabase = new ArrayList<>();
    private static int orderIdCounter = 1;

    public static void main(String[] args) {
        // Create a new order
        List<String> orderItems = new ArrayList<>();
        orderItems.add("Product A");
        orderItems.add("Product B");

        Order newOrder = createOrder("John Doe", orderItems);

        // Display the order details
        displayOrderDetails(newOrder);

        // Retrieve all orders
        List<Order> allOrders = getAllOrders();
        System.out.println("\nAll Orders:");
        for (Order order : allOrders) {
            displayOrderDetails(order);
        }
    }

    private static Order createOrder(String customerName, List<String> items) {
        Order newOrder = new Order(orderIdCounter++, customerName, items);
        ordersDatabase.add(newOrder);
        return newOrder;
    }

    private static List<Order> getAllOrders() {
        return ordersDatabase;
    }

    private static void displayOrderDetails(Order order) {
        System.out.println("\nOrder ID: " + order.getOrderId());
        System.out.println("Customer Name: " + order.getCustomerName());
        System.out.println("Items: " + order.getItems());
    }
}
- 👋 Hi, I’m @Stephen-Onyango
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Stephen-Onyango/Stephen-Onyango is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
