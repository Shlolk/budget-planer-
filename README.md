# Budget App

## Overview

The Budget App is a Python application that helps track deposits, withdrawals, transfers, and spending across different budget categories. It also generates a spending chart that visualizes the percentage of total spending for each category.

This project demonstrates object-oriented programming concepts such as classes, methods, instance attributes, and string formatting.

---

## Features

### Category Management

Each budget category is represented by a `Category` object.

Supported operations:

* Deposit money into a category
* Withdraw money from a category
* Transfer money between categories
* Check available funds
* View current balance
* Display a formatted ledger

---

## Category Class

### Create a Category

```python
food = Category("Food")
```

### Deposit Funds

```python
food.deposit(1000, "initial deposit")
```

### Withdraw Funds

```python
food.withdraw(15.89, "restaurant")
```

### Transfer Funds

```python
clothing = Category("Clothing")

food.transfer(50, clothing)
```

### Get Balance

```python
food.get_balance()
```

### Check Funds

```python
food.check_funds(100)
```

Returns:

```python
True
```

or

```python
False
```

---

## Example Ledger Output

```python
food = Category("Food")

food.deposit(1000, "initial deposit")
food.withdraw(10.15, "groceries")
food.withdraw(15.89, "restaurant and more food for dessert")

print(food)
```

Output:

```text
*************Food*************
initial deposit        1000.00
groceries               -10.15
restaurant and more foo -15.89
Total: 973.96
```

---

## Spending Chart

The application can generate a bar chart showing the percentage of total spending by category.

Example:

```python
create_spend_chart([food, clothing, auto])
```

Output:

```text
Percentage spent by category
100|
 90|
 80|
 70|
 60| o
 50| o
 40| o
 30| o
 20| o  o
 10| o  o  o
  0| o  o  o
    ----------
     F  C  A
     o  l  u
     o  o  t
     d  t  o
        h
        i
        n
        g
```

---

## Methods

### Category

| Method                          | Description                    |
| ------------------------------- | ------------------------------ |
| `deposit(amount, description)`  | Add funds to a category        |
| `withdraw(amount, description)` | Remove funds if balance allows |
| `get_balance()`                 | Return current balance         |
| `transfer(amount, category)`    | Move funds between categories  |
| `check_funds(amount)`           | Verify sufficient balance      |
| `__str__()`                     | Return formatted ledger output |

### Functions

| Function                         | Description                          |
| -------------------------------- | ------------------------------------ |
| `create_spend_chart(categories)` | Generate a spending percentage chart |

---

## Concepts Used

* Python Classes
* Object-Oriented Programming (OOP)
* Instance Attributes
* Methods
* String Formatting
* Lists and Dictionaries
* Data Visualization with Text-Based Charts

---

## Requirements

* Python 3.x

---

## License

This project was created for educational purposes as part of the FreeCodeCamp Scientific Computing with Python Certification.
