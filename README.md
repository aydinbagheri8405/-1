# -1import gettext

def main():
    print(gettext.gettext("Simple Calculator"))
    while True:
        num1 = float(input(gettext.gettext("Enter the first number: ")))
        num2 = float(input(gettext.gettext("Enter the second number: ")))
        operation = input(gettext.gettext("Enter the operation (+, -, *, /): "))

        if operation == "+":
            result = num1 + num2
        elif operation == "-":
            result = num1 - num2
        elif operation == "*":
            result = num1 * num2
        elif operation == "/":
            if num2 != 0:
                result = num1 / num2
            else:
                result = gettext.gettext("Error! Division by zero")
        else:
            result = gettext.gettext("Invalid operation")

        print(gettext.gettext("natyge: "), result)

        again = input(gettext.gettext("aya adame mydy? (yes/no): "))
        if again.lower() != "yes":
            break

if __name__ == "__main__":
    main()
