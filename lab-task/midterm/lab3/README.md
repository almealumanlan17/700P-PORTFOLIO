# MIDTERM LAB TASK 3
### List Collections

**Problem 1. Using List Collection type.***  
Create a program that will allow the user to perform the following **functions**: (add, update, search, delete, display, and sort) items in a list.  

Note: You are free to decide what data you will be storing in the list and name the list based
on the type of data you wish to store.  

**[ MENU OPTIONS]**  
**1 – Add Items**  
**2 – Search for an Item**  
**3 – Remove an Item**  
**4 – View all items (Sorted either A-Z | Z -A)**  
**0 – Exit program**  

**Pick one [0 to quit]: ___**  

**Requirements:**  
1. The user can add items in the list until the user presses x to stop.  
2. The user should be able to perform **search** if an item exists – Display if found or not
found and count the number of instance in the list.  
3. The user should also be given the option to remove an item in the list – Display the
Message “Item found and deleted” once deletion is performed – else display “item
not found-deletion unsuccessful”.  
4. The user may also opt to view items in the list and display items sorted in
Ascending order.  
5. The user may opt to exit the program by typing 0
  
Note: you are free to design the interface of the program, base on the Menu options
shown.  

### 💻 Source Code
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>def menu():
  print("\n[ MENU OPTIONS ]")
  print("1 - Add Items")
  print("2 - Search for an Item")
  print("3 - Remove an Item")
  print("4 - View all items (Sorted A-Z)")
  print("0 - Exit Program")

def main():
  fruits = []

  while True:
    menu()
    choice = input("Pick one [0 to quit]: ")

    if choice == "1":
      while True:
        item = input("Enter item to add (press x to stop): ")
        if item.lower() == "x":
          break
        fruits.append(item)
      print("Items successfully added!")
    elif choice == "2":
      search_item = input("Enter item to search: ")
      count = fruits.count(search_item)
      if count > 0:
        print(f"'{search_item}' found {count} time(s) in the list.")
      else:
        print(f"'{search_item}' not found in the list.")
    elif choice == "3":
      remove_item = input("Enter item to remove: ")
      if remove_item in fruits:
        fruits.remove(remove_item)
        print("Item found and deleted.")
      else:
        print("Item not found - deletion unsuccessful.")
    elif choice == "4":
      if len(fruits) == 0:
        print("List is empty")
      else:
        print("Items in the list (sorted A-Z):")
        for item in sorted(fruits):
          print("-",item)
    elif choice -- "0":
      print("Exiting program... Goodbye!")\
      break
    else:
      print("Invalid choice. Please try again.")

if __name__ == "__main__":
  main()
</code></pre>
  </div>  

### 🧾 Sample Output
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>[ MENU OPTIONS ]
1 - Add Items
2 - Search for an Item
3 - Remove an Item
4 - View all items (Sorted A-Z)
0 - Exit Program
Pick one [0 to quit]: <span style="color:#0969da;">1</span>
Enter item to add (press x to stop): <span style="color:#0969da;">1</span>
Enter item to add (press x to stop): <span style="color:#0969da;">2</span>
Enter item to add (press x to stop): <span style="color:#0969da;">3</span>
Enter item to add (press x to stop): <span style="color:#0969da;">ice</span>
Enter item to add (press x to stop): <span style="color:#0969da;">yelo</span>
Enter item to add (press x to stop): <span style="color:#0969da;">cold</span>
Enter item to add (press x to stop): <span style="color:#0969da;">x</span>
Items successfully added!

[ MENU OPTIONS ]
1 - Add Items
2 - Search for an Item
3 - Remove an Item
4 - View all items (Sorted A-Z)
0 - Exit Program
Pick one [0 to quit]: <span style="color:#0969da;">2</span>
Enter item to search: <span style="color:#0969da;">ice</span>
'ice' found 1 time(s) in the list.

[ MENU OPTIONS ]
1 - Add Items
2 - Search for an Item
3 - Remove an Item
4 - View all items (Sorted A-Z)
0 - Exit Program
Pick one [0 to quit]: <span style="color:#0969da;">3</span>
Enter item to remove: <span style="color:#0969da;">cold</span>
Item found and deleted.

[ MENU OPTIONS ]
1 - Add Items
2 - Search for an Item
3 - Remove an Item
4 - View all items (Sorted A-Z)
0 - Exit Program
Pick one [0 to quit]: <span style="color:#0969da;">4</span>
Items in the list (sorted A-Z):
- 1
- 2
- 3
- ice
- yelo

[ MENU OPTIONS ]
1 - Add Items
2 - Search for an Item
3 - Remove an Item
4 - View all items (Sorted A-Z)
0 - Exit Program
Pick one [0 to quit]: <span style="color:#0969da;">0</span>
Exiting program... Goodbye!
</code></pre>
</div>
