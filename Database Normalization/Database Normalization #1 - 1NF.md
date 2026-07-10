## 🚀 29. Database Normalization #1 - 1NF

### 📌 Problem

The following unnormalized table named **PRODUCT** is transformed to **First Normal Form (1NF)** by splitting it into two tables which have **X** and **Y** rows (**X < Y**) respectively. Both the tables have **Z** columns.

| Product-ID | Colors | Price |
|------------|--------|------:|
| 1 | Red, Green | 15.0 |
| 2 | Blue | 18.0 |
| 3 | Yellow, Pink | 2.5 |

Find the values of **X**, **Y**, and **Z**.

---

### 💡 Explanation

The table violates **First Normal Form (1NF)** because the **Colors** column contains **multiple values** in a single cell.

To convert it to **1NF**, split the table into:

**Table 1: PRODUCT**

| Product-ID | Price |
|------------|------:|
| 1 | 15.0 |
| 2 | 18.0 |
| 3 | 2.5 |

- Rows = **3**
- Columns = **2**

**Table 2: PRODUCT_COLORS**

| Product-ID | Color |
|------------|-------|
| 1 | Red |
| 1 | Green |
| 2 | Blue |
| 3 | Yellow |
| 3 | Pink |

- Rows = **5**
- Columns = **2**

Since **X < Y**:

- **X = 3**
- **Y = 5**
- **Z = 2**

---

### 💻 Solution

```text
3
5
2
```
