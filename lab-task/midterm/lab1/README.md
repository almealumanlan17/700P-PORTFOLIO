# MIDTERM LAB TASK 1

## PROBLEM 1.
Use Appropriate Escape Sequence ( \n, \t \b \ ..etc) for the problem below  
  
### 💻 Source Code
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>
print("Database Record") 
print("\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\")
print("Name:\t\tJohn Doe")
print("Email:\t\tjohn.doe@example.com")
print("University:\tABC University\n")
</code></pre>
</div>


### 🧾 Sample Output
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>
Database Record 
\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
Name:     John Doe
Email:    john.doe@example.com
University:     ABC University
</code></pre>
  </div>  

## PROBLEM 2.
Using Placeholders for Email Details: Use appropriate type specifiers %s, %d, %f etc... for this task  
  
### 💻 Source Code
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>
name = "John" 
subject = "Greeting"
sender = "Jane"
version = 1.2
discount = 10.50
status = 'A'
code = "ABCD123"
location = "City XYZ" 
age = 30
company = "ABC Corporation"
website = "www.example.com" 
phone = "+1 123-456-789"
job_title = "Software Engineering"
department = "Engineering"

email_template = """Dear %s, I hope this email find you well.
I wanted to reach out and say hello.
I hope you are doing well and enjoring your day.
It's been a while since we last spoke, and I wanted to cath up with you.
Let's plan to meet up soon and have a great time together!
Subject: %s
Sender: %s
Version: %.1f
Discount: %.2f%
Status: %s
Code: %s
Location: %s
Age: %d
Company: %s
Website: %s
Phone: %s
Job: %s
Department: %s
"""

print(email_template % (name, subject, sender, version, discount, status, 
code, location, age, company, website, phone, job_title, department))

</code></pre>
  </div>  

### 🧾 Sample Output
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>
Dear John, I hope this email find you well.
I wanted to reach out and say hello.
I hope you are doing well and enjoring your day.
It's been a while since we last spoke, and I wanted to cath up with you.
Let's plan to meet up soon and have a great time together!
Subject: Greeting
Sender: Jane
Version: 1.2
Discount: 10.50%
Status: A
Code: ABCD123
Location: City XYZ
Age: 30
Company: ABC Corporation
Website: www.example.com
Phone: +1 123-456-789
Job: Software Engineering
Department: Engineering
</code></pre>
  </div>  
  

    
## PROBLEM 3.
Book Reservation; Accept User Input  
  
### 💻 Source Code
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>
title = input("Enter the book title: ")
author = input("Enter the author: ")
year = int(input("Enter the year of publication: "))
genre = input("Enter the genre: ")
library = input("Enter the library: ")
member_id = input("Enter your member ID: ")
return_date = input("Enter the return date: ")

print(f'You have successfully reserved the book "{title}" by {author}')
print(f"Year of Publication: {year}")
print(f"Genre: {genre}")
print(f"Library: {library}")
print(f"Member ID: {member_id}")
print(f"Return Date: {return_date}")
</code></pre>
  </div>  
  
### 🧾 Sample Output
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>
Enter the book title: <span style="color:#0969da;">1984</span>
Enter the author: <span style="color:#0969da;">Orwell</span>
Enter the year of publication: <span style="color:#0969da;">1949</span>
Enter the genre: <span style="color:#0969da;">Dystopian</span>
Enter the library: <span style="color:#0969da;">Central</span>
Enter your member ID: <span style="color:#0969da;">12345</span>
Enter the return date: <span style="color:#0969da;">2023-07-10</span>
You have successfully reserved the book "1984" by Orwell
Year of Publication: 1949
Genre: Dystopian
Library: Central
Member ID: 12345
Return Date: 2023-07-10
</code></pre>
  </div>  

## PROBLEM 4.
Day Identifier  
  
### 💻 Source Code
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>
day = int(input("Enter Day: "))
  
if day == 1:
    print("Monday")
elif day == 2:
    print("Tuesday")
elif day == 3:
    print("Wednesday")
elif day == 4:
    print("Thursday")
elif day == 5:
    print("Friday")
elif day == 6:
    print("Saturday")
elif day == 7:
    print("Sunday")
else:
    print("Invalid Input")
</code></pre>
  </div>  
  
### 🧾 Sample Output
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>
Enter Day: <span style="color:#0969da;">7</span>
Sunday
</code></pre>
</div>
