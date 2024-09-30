# Ayuub

# Feature includes history of calculations

history = []
# Append results to history after each operation
history.append(f"{num1} + {num2} = {add(num1, num2)}")
# Print history upon request
for calculation in history:
    print(calculation)


# Modified code

history = []  # Step 1: Initialize an empty list to store history

while True:
    choice = input("Enter choice(1/2/3/4): ")

    if choice in ('1', '2', '3', '4'):
        try:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
        except ValueError:
            print("Invalid input. Please enter a number.")
            continue

        if choice == '1':
            result = num1 + num2
            print(num1, "+", num2, "=", result)
            history.append(f"{num1} + {num2} = {result}")  # Step 2: Append to history

        elif choice == '2':
            result = num1 - num2
            print(num1, "-", num2, "=", result)
            history.append(f"{num1} - {num2} = {result}")  # Step 2: Append to history

        elif choice == '3':
            result = num1 * num2
            print(num1, "*", num2, "=", result)
            history.append(f"{num1} * {num2} = {result}")  # Step 2: Append to history

        elif choice == '4':
            if num2 != 0:
                result = num1 / num2
                print(num1, "/", num2, "=", result)
                history.append(f"{num1} / {num2} = {result}")  # Step 2: Append to history
            else:
                print("Error! Division by zero.")
                continue

        # Step 3: Ask if the user wants to do another calculation
        next_calculation = input("Let's do next calculation? (yes/no): ")
        if next_calculation == "no":
            break

    else:
        print("Invalid Input")

# Step 4: Print the history when the user is done
if history:
    print("\nHistory of calculations:")
    for record in history:
        print(record) 
else:
    print("No calculations were performed.")





    


    

