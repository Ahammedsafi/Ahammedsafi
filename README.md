import math

def display_menu():
    print("----- Magical Calculator -----")
    print("1. Addition")
    print("2. Subtraction")
    print("3. Multiplication")
    print("4. Division")
    print("5. Exponentiation")
    print("6. Square Root")
    print("7. Unit Conversion")
    print("8. Exit")

def get_input(prompt):
    return input(prompt)

def perform_addition():
    num1 = float(get_input("Enter the first number: "))
    num2 = float(get_input("Enter the second number: "))
    result = num1 + num2
    print("Result: ", result)

def perform_subtraction():
    num1 = float(get_input("Enter the first number: "))
    num2 = float(get_input("Enter the second number: "))
    result = num1 - num2
    print("Result: ", result)

def perform_multiplication():
    num1 = float(get_input("Enter the first number: "))
    num2 = float(get_input("Enter the second number: "))
    result = num1 * num2
    print("Result: ", result)

def perform_division():
    num1 = float(get_input("Enter the dividend: "))
    num2 = float(get_input("Enter the divisor: "))
    try:
        result = num1 / num2
        print("Result: ", result)
    except ZeroDivisionError:
        print("Error: Division by zero is not allowed.")

def perform_exponentiation():
    base = float(get_input("Enter the base: "))
    exponent = float(get_input("Enter the exponent: "))
    result = base ** exponent
    print("Result: ", result)

def perform_square_root():
    num = float(get_input("Enter a number: "))
    if num < 0:
        print("Error: Square root cannot be calculated for negative numbers.")
    else:
        result = math.sqrt(num)
        print("Result: ", result)

def perform_unit_conversion():
    print("----- Unit Conversion -----")
    print("1. Length")
    print("2. Weight")
    print("3. Volume")
    print("4. Temperature")
    
    choice = int(get_input("Enter your choice: "))
    
    if choice == 1:
        perform_length_conversion()
    elif choice == 2:
        perform_weight_conversion()
    elif choice == 3:
        perform_volume_conversion()
    elif choice == 4:
        perform_temperature_conversion()
    else:
        print("Invalid choice.")

def perform_length_conversion():
    print("1. Feet to Meters")
    print("2. Meters to Feet")
    choice = int(get_input("Enter your choice: "))
    
    if choice == 1:
        feet = float(get_input("Enter length in feet: "))
        meters = feet * 0.3048
        print("Length in meters: ", meters)
    elif choice == 2:
        meters = float(get_input("Enter length in meters: "))
        feet = meters * 3.28084
        print("Length in feet: ", feet)
    else:
        print("Invalid choice.")

def perform_weight_conversion():
    print("1. Pounds to Kilograms")
    print("2. Kilograms to Pounds")
    choice = int(get_input("Enter your choice: "))
    
    if choice == 1:
        pounds = float(get_input("Enter weight in pounds: "))
        kilograms = pounds * 0.453592
        print("Weight in kilograms: ", kilograms)
    elif choice == 2:
        kilograms = float(get_input("Enter weight in kilograms: "))
        pounds = kilograms * 2.20462
        print("Weight in pounds: ", pounds)
    else:
        print("Invalid choice.")

def perform_volume_conversion():
    print("1. Gallons to Liters")
    print("2. Liters to Gallons")
    choice = int(get_input("Enter your choice: "))
    
    if choice == 1:
        gallons = float(get_input("Enter volume in gallons: "))
        liters = gallons * 3.78541
        print("Volume in liters: ", liters)
    elif choice == 2:
        liters = float(get_input("Enter volume in liters: "))
        gallons = liters * 0.264172
        print("Volume in gallons: ", gallons)
    else:
        print("Invalid choice.")

def perform_temperature_conversion():
    print("1. Celsius to Fahrenheit")
    print("2. Fahrenheit to Celsius")
    choice = int(get_input("Enter your choice: "))
    
    if choice == 1:
        celsius = float(get_input("Enter temperature in Celsius: "))
        fahrenheit = (celsius * 9/5) + 32
        print("Temperature in Fahrenheit: ", fahrenheit)
    elif choice == 2:
        fahrenheit = float(get_input("Enter temperature in Fahrenheit: "))
        celsius = (fahrenheit - 32) * 5/9
        print("Temperature in Celsius: ", celsius)
    else:
        print("Invalid choice.")

def magical_calculator():
    while True:
        display_menu()
        choice = get_input("Enter your choice (1-8): ")
        
        if choice == "1":
            perform_addition()
        elif choice == "2":
            perform_subtraction()
        elif choice == "3":
            perform_multiplication()
        elif choice == "4":
            perform_division()
        elif choice == "5":
            perform_exponentiation()
        elif choice == "6":
            perform_square_root()
        elif choice == "7":
            perform_unit_conversion()
        elif choice == "8":
            print("Thank you for using the Magical Calculator!")
            break
        else:
            print("Invalid choice. Please select a number from the menu.")

if _name_ == "_main_":
    magical_calculator()
    
