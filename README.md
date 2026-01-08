# Basic-Calculator
A simple Python program that asks the user to input two numbers and a mathematical operation (addition, subtraction, multiplication, or division). Perform the operation based on the user's input and print the result.

while True:
    # Get user input
    try:
        num1 = float(input("\nEnter first number: "))
        num2 = float(input("Enter second number: "))
    except ValueError:
        print("Invalid input. Please enter numeric values.")
        continue

    operation = input("Enter operation (+, -, *, /): ")

    # Perform the calculation
    if operation == '+':
        print(f"{num1} + {num2} = {num1 + num2}")
    elif operation == '-':
        print(f"{num1} - {num2} = {num1 - num2}")
    elif operation == '*':
        print(f"{num1} * {num2} = {num1 * num2}")
    elif operation == '/':
        if num2 != 0:
            print(f"{num1} / {num2} = {num1 / num2}")
        else:
            print("Error: Division by zero is not allowed.")
    else:
        print("Invalid operation.")

    # Check if the user wants to go again
    again = input("\nDo you want to perform another calculation? (y/n): ").lower()
    if again != 'y':
        print("Goodbye!")
        break
