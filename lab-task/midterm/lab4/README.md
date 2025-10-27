# MIDTERM LAB TASK 4
### Dictionary Collections

## Problem 1.
Create the following UI for menu items: then allow the user to input orders
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>--------- MENU ---------
pizza     : $3.00
nachos    : $4.50
popcorn   : $6.00
fries     : $2.50
chips     : $1.00
pretzel   : $3.50
soda      : $3.00
lemonade  : $4.25
------------------------
Select and item (q to quit): <span style="color:#0969da;">pizza</span>
Select and item (q to quit): <span style="color:#0969da;">soda</span>
Select and item (q to quit): <span style="color:#0969da;">q</span>
------ YOUR ORDER ------
pizza soda
Total is: $6.00
</code></pre>
  </div>  

The user will continue to input orders until q is typed to quit. Then display the summary of
orders with the total bill.  
1. Use a dictionary (for the menu) and List (for the orders in the cart).  
2. Users may input the same item in the cart.  
3. Follw the exact format and whitespace for the menu.  
4. User input should be case insensitive.  
5. If the user inputted an item not in the Menu – it will not include it in the cart and
display “Not Available” and input another item.  
6. Create a MENU with 10 items and assign prices in Peso (php) - You may choose what
items you would like to put in your cart.

### 💻 Source Code
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>menu = {  
    "burgehr":3.00,  
    "pissah":4.50,  
    "phopchorn":6.00,  
    "frys":2.50,  
    "coffey":1.00,  
    "sandwhich?":3.50,  
    "sowdah":3.00,  
    "shawamah":4.25,  
    "sahlahd":5.00,  
    "ike kleam":2.75  
}  

print("-------- MENNYUU --------")
for item, price in menu.items():
    print(f"{item:<9} : ${price:.2f}")
print("-------------------------")

orders = []
total = 0.0

while True:
    order = input("Select an item (q to quit): ").strip().lower()
    if order == 'q':
        break
    elif order in menu:
        orders.append(order)
        total += menu[order]
    else:
        print("Not Available")

print("\n------ YOUR ORDER ------")
for item in orders:
    print(item, end=" ")
print(f"\nTotal is: ${total:.2f}")
</code></pre>
  </div>  

### 🧾 Sample Output
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>-------- MENNYUU --------
burgehr   : $3.00
pissah    : $4.50
phopchorn : $6.00
frys      : $2.50
coffey    : $1.00
sandwhich? : $3.50
sowdah    : $3.00
shawamah  : $4.25
sahlahd   : $5.00
ike kleam : $2.75
-------------------------
Select an item (q to quit): <span style="color:#0969da;">pissah</span>
Select an item (q to quit): <span style="color:#0969da;">coffey</span>
Select an item (q to quit): <span style="color:#0969da;">sowdah</span>
Select an item (q to quit): <span style="color:#0969da;">q</span>

------ YOUR ORDER ------
pissah coffey sowdah 
Total is: $8.50
</code></pre>
</div>
