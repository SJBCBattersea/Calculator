import math

def scientific_calculator():
    print("\nScientific Calculator")
    print("Select operation:")
    print("1. Square Root (√)")
    print("2. Power (x^y)")
    print("3. Sine (sin)")
    print("4. Cosine (cos)")
    print("5. Tangent (tan)")
    print("6. Logarithm (log)")

    while True:
        choice = input("Enter choice (1/2/3/4/5/6) or 'q' to quit: ")
        if choice == 'q':
            break
        
        if choice in ('1', '2', '3', '4', '5', '6'):
            try:
                if choice == '1':
                    num = float(input("Enter number: "))
                    print(f"√{num} = {math.sqrt(num)}")
                elif choice == '2':
                    base = float(input("Enter base: "))
                    exponent = float(input("Enter exponent: "))
                    print(f"{base} ^ {exponent} = {math.pow(base, exponent)}")
                elif choice == '3':
                    angle = float(input("Enter angle in degrees: "))
                    print(f"sin({angle}) = {math.sin(math.radians(angle))}")
                elif choice == '4':
                    angle = float(input("Enter angle in degrees: "))
                    print(f"cos({angle}) = {math.cos(math.radians(angle))}")
                elif choice == '5':
                    angle = float(input("Enter angle in degrees: "))
                    print(f"tan({angle}) = {math.tan(math.radians(angle))}")
                elif choice == '6':
                    num = float(input("Enter number: "))
                    print(f"log({num}) = {math.log(num)}")
            except ValueError:
                print("Invalid input. Please enter numbers only.")
            except Exception as e:
                print(f"Error: {e}")
        else:
            print("Invalid choice. Please select a valid operation.")

# Uncomment the line below to run the scientific calculator
# scientific_calculator()



    


    

