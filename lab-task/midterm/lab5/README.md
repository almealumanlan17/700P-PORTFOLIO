# MIDTERM LAB TASK 5
### Creating Class and Instantiating Objects in Pythons

## Problem 1. Users in Social Media

a. Create User Class with the ff: attributes (Use Constructor for this)  
    ∙ first_name  
    ∙ last_name  
    ∙ followers_count  
    ∙ friends_name [LIST]  
Note: You can make a List an attribute of a class  

b. Create the ff: methods  
    - introduce_self – which should output “ Hi I am {first_name} {last_name}  
    - view_full_profile – which outputs all the information of the user as shown below  

c. Create a separate TestUser class to test if the program is working as expected, allowing for
user input to be passed as parameters of the object. Create atleast 2 object instance to test
the class template.  

**Rubric:**
1. Completeness of the code requirements – 10  
2. Correctness of the expected input and output - 10  
3. Use of proper naming conventions – 5

### 💻 Source Code
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>class User:
    def __init__(self, first_name, last_name, followers_count, friends_name):
        self.first_name = first_name
        self.last_name = last_name
        self.followers_count = followers_count
        self.friends_name = friends_name

    def introduce_self(self):
        print(f"HI I am {self.first_name} {self.last_name}")

    def view_full_profile(self):
        print(
            f"Profile Name is: {self.first_name} {self.last_name} with {self.followers_count} followers"
        )
        print("Your friends are:", " ".join(self.friends_name))
        print()


class TestUser:
    def __init__(self):
        self.users = []

    def add_user(self):
        while True:
            ans = input("Insert a Record?[y[n]: ").lower()
            if ans == "y":
                first_name = input("First Name: ")
                last_name = input("Last Name: ")
                followers = int(input("Followers: "))
                print("Friends:")
                friends = []
                while True:
                    friend = input()
                    if friend == "":
                        break
                    friends.append(friend)

                user = User(first_name, last_name, followers, friends)
                self.users.append(user)

            elif ans == "n":
                break
            else:
                print("Please enter 'y' or 'n' only.")

    def display_all_users(self):
        print("\nHere are the Records...")
        for user in self.users:
            user.introduce_self()
            user.view_full_profile()
        print(f"There are currently {len(self.users)} Members in the Social Media page")


if __name__ == "__main__":
    test = TestUser()
    test.add_user()
    test.display_all_users()
</code></pre>
  </div>  
  
### 🧾 Sample Output
<div style="background-color:#f6f8fa; color:#24292e; padding:15px; border-radius:8px; border:1px solid #d0d7de; overflow-x:auto;">
<pre style="margin:0;"><code>Insert a Record?[y[n]: <span style="color:#0969da;">y</span>
First Name: <span style="color:#0969da;">Almea</span>
Last Name: <span style="color:#0969da;">Lumanlan</span>
Followers: <span style="color:#0969da;">123456789</span>
Friends:
<span style="color:#0969da;">Enzo</span>
<span style="color:#0969da;">Justine</span>
<span style="color:#0969da;">Noel</span>
<span style="color:#0969da;">Yshian</span>
<span style="color:#0969da;">Blaine</span>

Insert a Record?[y[n]: <span style="color:#0969da;">y</span>
First Name: <span style="color:#0969da;">Almea</span>
Last Name: <span style="color:#0969da;">Lumanlan</span>
Followers: <span style="color:#0969da;">123456789</span>
Friends:
<span style="color:#0969da;">Fiona</span>
<span style="color:#0969da;">Traces</span>
<span style="color:#0969da;">Jennilyn</span>
<span style="color:#0969da;">Tyrese</span>
<span style="color:#0969da;">Charles</span>

Insert a Record?[y[n]: <span style="color:#0969da;">n</span>

Here are the Records...
HI I am Almea Lumanlan
Profile Name is: Almea Lumanlan with 123456789 followers
Your friends are: Enzo Justine Noel Yshian Blaine

HI I am Almea Lumanlan
Profile Name is: Almea Lumanlan with 123456789 followers
Your friends are: Fiona Traces Jennilyn Tyrese Charles

There are currently 2 Members in the Social Media page
</code></pre>
</div>
