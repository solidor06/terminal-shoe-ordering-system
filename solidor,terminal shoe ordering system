print("=" * 50)
print("Welcome to FootPrintz Shoe Store".center(50))
print("=" * 50)


shoes = {
    1: {"name": "Nike Air Max", "price": 4500},
    2: {"name": "Adidas Ultraboost", "price": 5200},
    3: {"name": "Puma RS-X", "price": 3800},
    4: {"name": "Vans Old Skool", "price": 3000},
    5: {"name": "Converse Chuck Taylor", "price": 3200}
}

cart = []
total = 0


while True:
    print("\n" + "-" * 50)
    print("Available Shoes".center(50))
    print("-" * 50)

    for num, shoe in shoes.items():
        print(f"{num}. {shoe['name']:<25} ₱{shoe['price']:,}")

    print("\n" + "=" * 50)
    print("OPTIONS".center(50))
    print("=" * 50)
    print("1 - Order a Shoe")
    print("2 - View Cart")
    print("3 - Checkout and Exit")

    choice = input("\nEnter your choice (1-3): ")

    
    if choice == "1":
        try:
            item = int(input("Enter shoe number: "))

            if item in shoes:
                qty = int(input("Enter quantity: "))

                if qty <= 0:
                    print("Invalid quantity! Please enter a positive number.")
                    continue

                subtotal = shoes[item]["price"] * qty
                cart.append((shoes[item]["name"], qty, subtotal))
                total += subtotal

                print(f"\nAdded {qty}x {shoes[item]['name']} — ₱{subtotal:,}")
            else:
                print("Invalid shoe number. Please try again.")

        except ValueError:
            print("Please enter numbers only.")

    
    elif choice == "2":
        print("\n" + "-" * 50)
        print("YOUR CART".center(50))
        print("-" * 50)

        if not cart:
            print("Your cart is empty.")
        else:
            for item in cart:
                print(f"{item[1]}x {item[0]:<25} = ₱{item[2]:,}")
            print("-" * 50)
            print(f"TOTAL: ₱{total:,}".rjust(30))

    
    elif choice == "3":
        print("\n" + "=" * 50)
        print("CHECKOUT".center(50))
        print("=" * 50)

        if total == 0:
            print("Your cart is empty. Please order something first.")
            continue

        for item in cart:
            print(f"{item[1]}x {item[0]:<25} = ₱{item[2]:,}")

        print("-" * 50)
        print(f"Total Amount: ₱{total:,}".rjust(45))
        print("=" * 50)
        print("Thank you for ordering at FootPrintz Store!")
        print("=" * 50)
        break

    
    else:
        print("Invalid option. Please enter 1, 2, or 3.")
