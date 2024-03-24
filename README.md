# Task-2-Python
def calculate(num1, num2, operator):
  """
  Performs the calculation based on the provided operator.

  Args:
      num1: The first number.
      num2: The second number.
      operator: The operator (+, -, *, /).

  Returns:
      The result of the calculation, or None if an invalid operator is provided.
  """
  if operator == '+':
    return num1 + num2
  elif operator == '-':
    return num1 - num2
  elif operator == '*':
    return num1 * num2
  elif operator == '/':
    if num2 == 0:
      print("Error: Division by zero is not allowed.")
      return None
    else:
      return num1 / num2
  else:
    print("Error: Invalid operator. Please use +, -, *, or /.")
    return None

while True:
  # Get user input
  try:
    num1 = float(input("Enter the first number: "))
    num2 = float(input("Enter the second number: "))
    operator = input("Enter the operator (+, -, *, /): ")
  except ValueError:
    print("Invalid input. Please enter numbers only.")
    continue

  # Perform the calculation
  result = calculate(num1, num2, operator)

  # Display the result
  if result is not None:
    print("The result is:", result)
  else:
    # Handle errors (e.g., division by zero)
    continue

  # Ask user if they want to continue
  choice = input("Do you want to perform another calculation? (y/n): ")
  if choice.lower() != 'y':
    break

print("Thank you for using the calculator!")
