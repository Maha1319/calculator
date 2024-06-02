def get_number(prompt):
    while True:
        try:
            number = float(input(prompt))
            return number
        except ValueError:
            print("Invalid input. Please enter a valid number.")

def get_operation():
    operations = ['+', '-', '*', '/']
    while True:
        operation = input("Enter operation (+, -, *, /): ")
        if operation in operations:
            return operation
        else:
            print("Invalid operation. Please enter one of +, -, *, or /.")

def calculate(num1, num2, operation):
    if operation == '+':
        return num1 + num2
    elif operation == '-':
        return num1 - num2
    elif operation == '*':
        return num1 * num2
    elif operation == '/':
        if num2 == 0:
            return "Error! Division by zero."
        else:
            return num1 / num2

def main():
    print("Simple Calculator")
    num1 = get_number("Enter the first number: ")
    num2 = get_number("Enter the second number: ")
    operation = get_operation()
    result = calculate(num1, num2, operation)
    print(f"The result of {num1} {operation} {num2} is: {result}")

if _name_ == "_main_":
    main()
