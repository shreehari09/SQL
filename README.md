
# 🛒 Zepto Inventory Analysis SQL Project

This project involves analyzing and cleaning a product inventory dataset using SQL. The dataset mimics real-world product data from an e-commerce platform like Zepto and helps derive meaningful business insights.

## 📁 Project Structure

- **Schema Definition**: Table structure for the `zepto` inventory.
- **Data Exploration**: Basic queries to understand data distribution, null values, duplicates, and product availability.
- **Data Cleaning**: Handling invalid data (e.g., prices as 0 or stored in paise instead of rupees).
- **Data Analysis**: Insightful queries to extract business value.

## 🧱 Table Schema: `zepto`

| Column Name             | Data Type      | Description                                 |
|------------------------|----------------|---------------------------------------------|
| `sku_id`               | SERIAL         | Unique identifier for each product SKU      |
| `category`             | VARCHAR(120)   | Product category                            |
| `name`                 | VARCHAR(150)   | Product name                                |
| `mrp`                  | NUMERIC(8,2)   | Maximum Retail Price                        |
| `discountPercent`      | NUMERIC(5,2)   | Discount applied on MRP                     |
| `availableQuantity`    | INTEGER        | Quantity currently available in inventory   |
| `discountedSellingPrice` | NUMERIC(8,2) | Final price after discount                  |
| `weightInGms`          | INTEGER        | Weight of the product in grams              |
| `outOfStock`           | BOOLEAN        | Product availability status                 |
| `quantity`             | INTEGER        | Quantity of product unit (in packs etc.)    |

## 🔍 Data Exploration

- **Total Rows**  
  `SELECT COUNT(*) FROM zepto;`

- **Sample Data**  
  `SELECT * FROM zepto LIMIT 10;`

- **Null Check**  
  Checks for missing values across important columns.

- **Distinct Categories**  
  `SELECT DISTINCT category FROM zepto;`

- **Stock Status**  
  Products in-stock vs out-of-stock analysis.

- **Duplicate Product Names**  
  Identifies same product name with different SKUs.

## 🧹 Data Cleaning

- **Removing Invalid Price Rows**  
  Deletes rows where MRP or discounted price is zero.

- **Unit Conversion**  
  Converts price from paise to rupees.

## 📊 Data Analysis

1. **Top 10 Best Discounts**  
   Products with the highest discount percentages.

2. **High MRP but Out of Stock**  
   Identifies expensive items currently unavailable.

3. **Estimated Revenue by Category**  
   Total value of inventory based on discounted price × available quantity.

4. **High MRP, Low Discount**  
   Premium products that don’t offer large discounts.

5. **Top 5 Categories with Highest Average Discount**

6. **Price per Gram Analysis**  
   Finds best value-for-money products.

7. **Weight-Based Categorization**  
   Classifies products into Low, Medium, or Bulk based on weight.

8. **Total Inventory Weight by Category**

## 🚀 How to Use

1. Run the table creation SQL in a PostgreSQL database.
2. Insert your product data into the `zepto` table.
3. Execute the SQL queries for insights and cleaning.

## 📈 Use Cases

- Business Intelligence (BI) dashboard backend
- E-commerce inventory optimization
- Pricing strategy evaluation
- Product availability and stock monitoring

## 💡 Future Enhancements

- Visual dashboards using Power BI or Tableau  
- Automated alerts for out-of-stock high-value items  
- Integration with Python for dynamic reporting

## 📬 Contact

For any queries or contributions, feel free to reach out to me via GitHub Issues or Pull Requests.
