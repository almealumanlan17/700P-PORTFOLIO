# MIDTERM LAB TASK 2
### Using Functions

## Problem 1.
Create an n x n Multiplication table using **Nested FOR Loop**. The user must enter the number of rows and columns that will be displayed in the Table.

### 💻 Source Code
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>rows = int(input("Enter rows: "))  
cols = int(input("Enter columns: "))  
print("====================Multiplication Table====================")  
for rows in range(1, rows+1):  
    for cols in range(1,cols+1):  
        print(f" {rows*cols:5d}", end="")
    print("")
</code></pre>
  </div>

### 🧾 Sample Output 1
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>Enter rows: <span style="color:#0969da;">10</span>
Enter columns: <span style="color:#0969da;">10</span>
====================Multiplication Table====================
     1     2     3     4     5     6     7     8     9    10
     2     4     6     8    10    12    14    16    18    20
     3     6     9    12    15    18    21    24    27    30
     4     8    12    16    20    24    28    32    36    40
     5    10    15    20    25    30    35    40    45    50
     6    12    18    24    30    36    42    48    54    60
     7    14    21    28    35    42    49    56    63    70
     8    16    24    32    40    48    56    64    72    80
     9    18    27    36    45    54    63    72    81    90
    10    20    30    40    50    60    70    80    90   100
  </code></pre>
  </div>

### 🧾 Sample Output 2
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>Enter rows: <span style="color:#0969da;">3</span>
Enter columns: <span style="color:#0969da;">5</span>
====================Multiplication Table====================
     1     2     3     4     5
     2     4     6     8    10
     3     6     9    12    15
 </code></pre>
  </div>

## Problem 2.
Create a bank program that will allow user to perform, use **Functions** as necessary.

### 💻 Source Code
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>def show_balance(balance):
  print(f"Your balance is ${balance:.2f}")

def deposit(balance):
  amount = float(input("Enter an amount to be deposited: "))
  if amount > 0:
    balance += amount
  else:
    print("Invalid Amount")
  return balance

def withdraw(balance):
  amount = float(input("Enter an amount to be withdrawn: "))
  if amount > balance:
    print("Insufficient funds!!!")
  elif amount <= 0:
    print("Invalid Amount! Amount must be greater than 0.")
  else:
    balance -= amount
  return balance

def main():
  balance = 0
  while True:
    print("********************")
    print("     RICH ATM       ")
    print("********************")
    print("1. Show Balance")
    print("2. Deposit")
    print("3. Withdraw")
    print("4. Exit")
    print("********************")
    choice = int(input("Enter yout choice (1-4): "))

    if choice == 1:
      show_balance(balance)
    elif choice == 2:
      balance = deposit(balance)
    elif choice == 3:
      balance = withdraw(balance)
    elif choice == 4:
      print("Exiting Program.")
      break
    else:
      print("*************************************") 
      print("Invalid input! Select a valid option.")
      print("*************************************") 
  print("***************************************")
  print("     Thank you for using ABCDE ATM     ")
  print("***************************************")

main()
 </code></pre>
  </div>

### 🧾 Sample Output
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>********************
     RICH ATM       
********************
1. Show Balance
2. Deposit
3. Withdraw
4. Exit
********************
Enter yout choice (1-4): <span style="color:#0969da;">1</span>
Your balance is $0.00
********************
     RICH ATM       
********************
1. Show Balance
2. Deposit
3. Withdraw
4. Exit
********************
Enter yout choice (1-4): <span style="color:#0969da;">2</span>
Enter an amount to be deposited: <span style="color:#0969da;">1000</span>
********************
     RICH ATM       
********************
1. Show Balance
2. Deposit
3. Withdraw
4. Exit
********************
Enter yout choice (1-4): <span style="color:#0969da;">1</span>
Your balance is $1000.00
********************
     RICH ATM       
********************
1. Show Balance
2. Deposit
3. Withdraw
4. Exit
********************
Enter yout choice (1-4): <span style="color:#0969da;">3</span>
Enter an amount to be withdrawn: <span style="color:#0969da;">250</span>
********************
     RICH ATM       
********************
1. Show Balance
2. Deposit
3. Withdraw
4. Exit
********************
Enter yout choice (1-4): <span style="color:#0969da;">1</span>
Your balance is $750.00
********************
     RICH ATM       
********************
1. Show Balance
2. Deposit
3. Withdraw
4. Exit
********************
Enter yout choice (1-4): <span style="color:#0969da;">4</span>
Exiting Program.
***************************************
     Thank you for using ABCDE ATM     
***************************************
</code></pre>
</div>

