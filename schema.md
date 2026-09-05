# Database Schema

## E-Commerce Database

The project uses five related tables:

```text
customers
    │
    │ customer_id
    ▼
orders
    │
    ├───────────────┐
    │ order_id      │
    ▼               ▼
order_items      payments
    │
    │ product_id
    ▼
products
```

## Tables

### 1. customers

Stores customer information.

| Column        | Description          |
| ------------- | -------------------- |
| `customer_id` | Unique customer ID   |
| `first_name`  | Customer first name  |
| `last_name`   | Customer last name   |
| `city`        | Customer city        |
| `state`       | Customer state       |
| `signup_date` | Customer signup date |
| `email`       | Customer email       |

### 2. products

Stores product information.

| Column         | Description       |
| -------------- | ----------------- |
| `product_id`   | Unique product ID |
| `product_name` | Product name      |
| `category`     | Product category  |
| `brand`        | Product brand     |
| `price`        | Product price     |

### 3. orders

Stores order information.

| Column        | Description                   |
| ------------- | ----------------------------- |
| `order_id`    | Unique order ID               |
| `customer_id` | Customer who placed the order |
| `order_date`  | Date of the order             |
| `status`      | Order status                  |

### 4. order_items

Stores the individual products included in each order.

| Column          | Description          |
| --------------- | -------------------- |
| `order_item_id` | Unique order-item ID |
| `order_id`      | Related order        |
| `product_id`    | Purchased product    |
| `quantity`      | Quantity purchased   |
| `unit_price`    | Price paid per unit  |

### 5. payments

Stores payment information.

| Column           | Description             |
| ---------------- | ----------------------- |
| `payment_id`     | Unique payment ID       |
| `order_id`       | Related order           |
| `payment_method` | Method used for payment |
| `amount`         | Payment amount          |

## Relationships

```text
customers.customer_id
        ↓
orders.customer_id

orders.order_id
        ↓
order_items.order_id

products.product_id
        ↓
order_items.product_id

orders.order_id
        ↓
payments.order_id
```

## Dataset Size

| Table       | Records |
| ----------- | ------: |
| Customers   |   3,000 |
| Products    |     300 |
| Orders      |  15,000 |
| Order Items |  26,251 |
| Payments    |  15,000 |

The dataset is synthetic and contains no real customer information.
****
