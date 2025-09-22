📌 Database: ecommerce

This database is designed to manage an online shopping system, handling customers, products, orders, payments, and related entities.

1. Customers Table

Purpose: Stores information about customers who shop on the platform.

Key Fields:

customer_id: Unique identifier for each customer.

name: Full name of the customer.

email: Unique email address (used for login/communication).

phone: Contact number.

address: Shipping/billing address.

2. Categories Table

Purpose: Organizes products into different categories (e.g., Electronics, Clothing, Furniture).

Key Fields:

category_id: Unique identifier for each category.

category_name: Name of the category.

3. Products Table

Purpose: Stores details of items available for sale.

Key Fields:

product_id: Unique identifier for each product.

name: Product name.

price: Cost of the product.

stock: Available quantity in inventory.

category_id: Links product to a category (Foreign Key → Categories).

4. Orders Table

Purpose: Represents purchase transactions made by customers.

Key Fields:

order_id: Unique identifier for each order.

customer_id: Customer who placed the order (Foreign Key → Customers).

order_date: Date and time of order creation.

total: Total order amount.

5. Order_Items Table

Purpose: Manages the many-to-many relationship between Orders and Products.

Key Fields:

order_id: Links to the order (Foreign Key → Orders).

product_id: Links to the product (Foreign Key → Products).

quantity: Number of units of that product in the order.

6. Payments Table

Purpose: Stores payment details for each order.

Key Fields:

payment_id: Unique identifier for each payment.

order_id: Links payment to the order (Foreign Key → Orders).

amount: Payment amount.

payment_date: Date and time of payment.

method: Payment method (Credit Card, UPI, Cash, NetBanking).

✅ Overall Explanation:

Customers place Orders.

Each order contains multiple Products (via Order_Items).

Each order has one Payment record.

Products are grouped under Categories.
