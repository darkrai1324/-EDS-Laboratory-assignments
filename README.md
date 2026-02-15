# -EDS-Laboratory-assignments
QUE.1. To accept an object mass in kilograms and velocity in meters per second and display its momentum.
Momentum is calculated as e=mc2 where m is the mass of the object and c is its velocity.

SOLUTION: 

mass = float(input("Enter the object's mass in kilograms: "))
velocity = float(input("Enter the object's velocity in meters per second: "))

momentum = mass * velocity

print(f"The momentum is {momentum:.2f} kg·m/s")
-------------------------------------------------------------------------------------------------
QUE.2. Write a Python program for following conditions.
 If n is single digit print square of it.
 If n is two digit print square root of it.
 If n is three digit print cube root of it.

SOLUTION:

import math


n = int(input("Enter a number n: "))

digits = len(str(n))

if digits == 1:
    result = n ** 2
    print(f"Square of {n} is {result}")
elif digits == 2:
    result = math.sqrt(n)
    print(f"Square root of {n} is {result:.2f}")
elif digits == 3:
    result = n ** (1/3)
    print(f"Cube root of {n} is {result:.2f}")
else:
    print("Please enter a 1, 2, or 3 digit number.")
-------------------------------------------------------------------------------------------------
QUE.3. Read the birth date and salary in rupees of employees. Perform data transformation for birthdate
to age and also salary which is in rupees to salary in dollars using functions

SOLUTION:

from datetime import date

def calculate_age(birth_date):
    today = date.today()
    age = today.year - birth_date.year - ((today.month, today.day) < (birth_date.month, birth_date.day))
    return age

def rupees_to_dollars(rupees):
    exchange_rate = 86.5
    return rupees / exchange_rate

birth_str = input("Enter birth date (YYYY-MM-DD): ")
salary_rupees = float(input("Enter salary in rupees: "))

year, month, day = map(int, birth_str.split('-'))
birth_date = date(year, month, day)

age = calculate_age(birth_date)
salary_dollars = rupees_to_dollars(salary_rupees)

print(f"Age: {age} years")
print(f"Salary in USD: ${salary_dollars:.2f}")
-------------------------------------------------------------------------------------------------
QUE.4. Print the reverse number of a given number

SOLUTION:

n = int(input("Enter a number: "))
rev = 0

while n > 0:
    digit = n % 10
    rev = rev * 10 + digit
    n = n // 10

print("Reverse:", rev)
-------------------------------------------------------------------------------------------------
