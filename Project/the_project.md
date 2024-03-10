![luxuryclothes](https://github.com/Amine-Itani/Unit-3/assets/123438294/c42364ea-9db9-444d-bfac-ac329e160a58)

<sub> Image shows picture taken from https://en.freejpg.com.ar/stockphotos/premium/831656828/luxury-clothing-store-for-men </sub>
# Unit 3: A Clothing Factory GUI

## Criteria A: Planning

## Problem definition

The client is the manager of a clothes making factory that produces luxury shirts in three different colors (red, blue, yellow). He suffers from frequent short term memory loss which causes him to forget how much money he has as well as how many shirts he has in inventory. This therefore results in losses for the factory as they take on orders they do not have the supply to meet, costing them their reputation and clients. He tried keeping track on paper, but it became tedious and inefficient, especaily because he needs a way to account for barganing, since the clothes are so luxurious they are not sold at a specific price. His short term memory loss also results in him losing his password often, which is a problem he has faced with other services in the past. Another problem he has faced with these services is passwords that are too easy to guess, which associates of his use and result in the company losing a lot of money to dataleaks and unethical hackers. Finally, since many of his associates produce goods and make sales without coordinating decisions, productions and sales get lost overtime. He also suffers from not being able to upgrade the software he currently uses to meet the ever-changing demands of the factory.

## Design statement

I plan to develop a system for a luxury clothing factory using Python, Kivymd, and SQLite. It will provide a login and registration system to tackle privacy concerns of the client. It will also have multiple tables to keep track of the factory's inventory, it's transacations, as well as it's shipments to address the client's short term memory loss difficulties. Additional functions such as the ability to directly make an item in the GUI (Graphical User Interface) as well as error raises if the user takes on impossible shipments will help with additional issues faced by the client. This will all be made as user-friendly as possible so that the client and all their associates can use the GUI with ease. It will also be made open to upgrading in the future so that the factory can keep on improving as it expands to best suit their needs.

## Proposed Solution

Keeping in mind the problems faced by my client, it would be best advised to develop an easy-to-use GUI that keeps tracks of factory details to make things feasable to manage. It will display output as a GUI and not in terminal to make it more accessible to the client and their associates. This program will be developed using Python for back-end, Kivy for front-end, and SQLite for the database management. The reasons behind the choice of these languages and models are as follows.

It makes most sense to use Python instead of a language like C because of Python's access to object oriented programming (OOP). This is especially useful in the clients case considering they are a factory manager, each one of their objects has an ability that is useful to them such as being sold, or being made, etc. Therefore, many repetitive functions are executed on similar objects, which is exactly what OOP is made for, and reduces the load on the operating system by a lot. When comparing Python to another language such as Java, it makes sense to use Python in the case of my client as due to it's popularity, it will be easy for him to hire another developer once I have finished my work to improve on what I have built. In that sense, Python's redability is also useful to the client.

KivyMD is therefore a logical step from Python due to it's easy compatibility with Python. When comparing it with other equally compatibile languages such as PyQT, KivyMD clearly stands out for it's use of Google's Material Design guidelines, which cause it to be visually appealing and easy-to-use. In my client's case, his short term memory loss may cause him to forget how to use the application, so it not needing a learning curve everytime he goes to use it will also be useful for him. His associates will also have an easier time coming to grasp with the application. KivyMD's cross platform abilites could be useful in the case of my clients further development of the GUI, which he said he was interested in. If he decides to expand to mobile phone usage, the switch will be much less time consuming due to the use of KivyMD. When it comes to commercial use, KivyMD is free while PyQT has a cost, which may prove cumbersome to my client.

When considering what database program to use, SQLite comes up in consideration of the client's need for safety from unethical hackers and databreaches. When comparing it to other databases such as comma seperated values (CSV) files, it is much safer as only those with access can directly access it. SQLite is also scalable, therefore meaning that if the factory were to expand and increase their inventory, their systems would not suffer from the extra load, since SQLite would easily adapt. Since it is highly sensitive data, SQLite consistent saving properties will also help in the case of a databreach.

## Success Criteria
1. A page that keeps track of how much money the client has (Issue Tackled: "forget how much money he has")
2. A page that shows the current inventory of the factory (Issue Tackled: "[forget] how many shirts his has in inventory")
3. One page that allows the client to create his product (Issue Tackled: "his associates produce goods and makes sales without coordinating decisions")
4. A registration system with a password policy and a hint option (Issue Tackled: losing his password, passwords are too easy to guess")
5. A transaction table that shows all earning and losses faced by the factory (Issue Tackled: "productiond and sales get lost overtime")
6. A shipment page that return an error if the inventory does not have enough items to meet the order and allows the user to enter the earning amount (Issue Tackled: "take on order they do not have the supply to meet, needs a way to account for barganing")


# Criteria B: Design

## System Diagram
![image](https://github.com/Amine-Itani/Unit-3/assets/123438294/5eefe328-d4fd-4c5a-a193-903d7743ff51)

The system diagram displays the hardware that is needed to run the application, using Python version 3.10.11 and Kivy version 2.3.0. It discusses necessary parts such as RAM, CPU, Operating System, etc.

<sub>**Fig. 1** Figure shows the system diagram of the application</sub>

## Wireframe Diagram
![image](https://github.com/Amine-Itani/Unit-3/assets/123438294/3f41eb43-509e-4f1e-96bc-3391c2fe191d)

This diagram is the wireframe diagram of the application. It shows how different screens connect to each other through different buttons, and a more general flow of the applicatoin itself from the login page to the registration and then the menu or directly to the menu.

<sub>**Fig. 2** Figure shows the wireframe diagram of the application</sub>

## ER Diagram
![image](https://github.com/Amine-Itani/Unit-3/assets/123438294/8c754753-bd9f-4dcf-8402-544293744750)

This diagram shows the relationship between the different entities (databases) that are used by the program. Since all the users have access and the same relation to the databases, this creates many to many relationships. The only exception is the money database, since all the users only deal with one balance, which is that of the factory's capital.

<sub>**Fig. 3** Figure shows the entity relationship diagram of the application</sub>

## UML Diagram 
![image](https://github.com/Amine-Itani/Unit-3/assets/123438294/b10bbd21-a341-4d5b-8971-c1e388e7b12a)

The diagram is the UML diagram for the OOP classes and methods used in this program. Most of the classes inherit from the imported class MDScreen, and the general program to run the application from MDApp. DatabaseBridge is the connection between the program and the sqlite databases.

<sub>**Fig. 4** Figure shows the UML Diagram of the program</sub>

## Flow Diagrams

### New Shipment Upload (Simple)
The purpose of the new shipment upload is to update the balance, inventory, and shipment databases, and to check if the requested shipment of products is possible.

![image](https://github.com/Amine-Itani/Unit-3/assets/123438294/236f3c29-6938-48d7-9751-8d93d25ba513)

The function does this through taking the requested amount of a certain item, calling the amount of that item from the database, and comparing to see if that request is possible. If the amount requested is greater than the existing amount, it will return an error telling the user that the shipment is not possible. If the amount requested is not greater than the existing amount, then it will increase the balance by the earning entered, it will decrease the inventory by the amount of the product requested, and add the details of the order to the shipments database.

<sub>**Fig. 5** Figure shows simple flow diagram</sub>

### Login Procedure (Medium)
The purpose of the login procedure is not just to confirm that the user exists, but also to offer a hint in the case that the user forgets their password. It also checks hashes instead of the actual password for increased security.

![image](https://github.com/Amine-Itani/Unit-3/assets/123438294/6237cc1a-4243-4683-9132-0b9c5ae26900)

The function will first ensure that the user exists through checking if the username is in the users database. It will return an error if it does not find a matching user. If the user exists, it will procceed to the password check where it will hash the given password and compare it to the hashed password associated with the username given in the database. If these match, it will then move to the menu page. If these do not match, it will offer the user use a forgot password button. If they decide to do so, the hint associated with the username in the database will be shown on screen.

<sub>**Fig. 6** Figure shows medium flow diagram</sub>

### Registration Precodure (Complex)
The purpose of the registration procedure is to signup users to the database but also to check if they meet the required security measures put in place by the client.

![image](https://github.com/Amine-Itani/Unit-3/assets/123438294/873cb2fa-4240-4eab-8d9a-d9fddd7c9312)

The function takes the given username, password, password retype (check), and hint from the user through kivy textfields. It then iterates through the password and increase a numeric counter by one for every number in the password and increases an alphabetical (alpha) counter by one for every letter in the password. Once the loop is done, if either counters are 0, the function will return an error. If these counters meet the requirements, it will then check that the password is greater than 7 characters, and that the given username does not already exists. If either of these requirements are not met, the function will return an error. If all is well, then the function will hash the password and upload everything to the database.

<sub>**Fig. 7** Figure shows complex flow diagram</sub>

## Record of Tasks
| Task No |                Planned Action                |                                                                                                         Planned Outcome                                                                                                        | Time Estimate | Target Completion Date | Criterion |
|:-------:|:--------------------------------------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:-------------:|------------------------|-----------|
|    1    |               Meet with client               |                                                                      Gain a better idea of the problems the client is faciing and how these can be solved.                                                                     |     20 min    | February 25            | A         |
|    2    |            Write problem definiton           |                                                                                          Lay the groudwork for the aim of the project.                                                                                         |     10 min    | February 25            | A         |
|    3    |    Finalize problem defintion with client    |                                                                      Go over the problem definition with the client to solidify the target of the project.                                                                     |     10 min    | February 25            | A         |
|    4    |            Write success criteria            |      Basing the success criteria off the solidified problem definition, these will guide the creation of functions from this point forward. They are based directly off the success criteria and meat each one separately.     |     20 min    | February 25            | A         |
|    5    |            Write design statement            |                                                                             Short, concise explaation of what to expect in the working application.                                                                            |     5 min     | February 25            | A         |
|    6    | Proposed Solution and Justification of Tools |                                                                        Justification of why each step is taken in consideration of the clients problems.                                                                       |     30 min    | February 26            | A         |
|    7    |             Create system diagram            |                           This is done to understand the operating system that the software needs to run on. Should be legibile, efficient, and incorporate the whole mechanism from input to output.                          |     30 min    | March 1                | B         |
|    8    |           Create wireframe diagram           |                                                   Gives an idea of what the interface should look like and how the buttons and different connections to screens should work.                                                   |     1 hour    | March 1                | B         |
|    9    |             Create flow diagrams             |                                              Gives a comprehensive overview of how important algorithms from simple to complex should work. Uses human terms and visualizes data.                                              |    2 hours    | March 8                | B         |
|    10   |               MVP Presentation               |             Garner feedback from other developers in order to see where program can evolve from the minimum viable product and what can be altered for future use. A type of functional and non-functional testing.            |     20 min    | March 10               | B         |
|    11   |               Create test plan               |                                   Investigate different discrepancies surrounding the code and it's functionality as well as the UI and the integration of entities (tables) upon each other.                                  |    2 hours    | March 10               | B         |
|    12   |               Create ER Diagram              |                                                                        Clear layout of how databases interact with each other and what columns they own.                                                                       |     1 hour    | March 10               | B         |
|    13   |              Create UML Diagram              |                                                                Displays inheritance of different classes from MDScreen or MDApp and their functions accordingly.                                                               |     1 hour    | March 11               | B         |
|    14   |               Code login system              |                                                                         This system consults the database for users and encrypted password using hash.                                                                         |     30 min    | March 11               | C         |
|    15   |           Code registration system           | Allows users to signup to the application and contains many filters, including unique username, 8 character letter and number password, and hint requirement. Will raise corresponding error depending on requirement not met. |    2 hours    | March 11               | C         |
|    16   |                   Code menu                  |                                                      Allows the switching between different screens and functionalities. Also contains button that closes the application.                                                     |     30 min    | March 11               | C         |
|    17   |             Code shipments screen            |                                          This screen contains a table that updates with name of shipment receiver, amount, item, and earning. This also affects balance and inventory.                                         |    2 hours    | March 11               | C         |
|    18   |              Code balance screen             |                                                           Create update balance function and a transaction history that records earning, spending, date, and amount.                                                           |    2 hours    | March 11               | C         |
|    19   |             Code inventory scree             |                    Create a inventory that shows the amount of yellow, blue, and red shirts in stock. It should also show the cost to produce each shirt and a button that allows you to create this shirts.                   |    2 hours    | March 11               | C         |
|    20   |                 Polish design                |                                                                   Spend some time matching colors, font size, and overall making the app more user friendly.                                                                   |     2 hour    | March 11               | C         |
|    21   |               Finalize program               |                                        Consult client for final brush-ups then consolidate on future improvements if the program were to be developed further. Halt the editing process                                        |     30 min    | March 11               | C         |
|    22   |         Compile GitHub Documentation         |               Spend long hours arranging documentation to ensure that all criterion are met from A to D and all the details within it. All diagrams are present, and additional proposed problems and solutions.               |     30 min    | March 11               | C         |
|    23   |         Record a video demonstrating         |                                                7 minute video explaining the application from A-Z to clarify all possible improvements and functionalities surrounding the code.                                               |     10 min    | March 11               | D         |
## Test Plan

|             Description             |           Test Type          |                                                                                  Input                                                                                  |                                                                                                                                   Expected Output                                                                                                                                  |
|:-----------------------------------:|:----------------------------:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
|    Registration System: Username    |     Functional: Unit Test    |                                                        1. Run program 2. Press register button 3. Enter username                                                        | After the tester enters a username that already exists when attempting to register, the algorithm runs a users database search based on the username entered by the tester. If the username already exists, return error. If username does not exist, proceed and save to database |
|    Registration System: Password    |    Functional: Unit Test 2   |                                      1. Run program 2. Press register button 3. Enter username, password, password check, and hint                                      |               After the tester enters their password, if the password and password check do not match, raise error in check text field. If password does not meet policy, raise corresponding error. If all conditions are met, proceed and upload to users database               |
|   Add Shipment Effect On Own Table  |     Functional: Unit Test    |                       1. Run program 2. Enter login info 3. Press login 4. Go to menu 5. Press on shipment 6. Fill out textfields 7. Press update                       |    After the tester does required steps, algorithm will check the number of items available for shipping from the type selected by the user. If there are not enough items for shipments, raise error in amount textfield. If number is avaialable, upload transaction to table.   |
| Add Shipment Effect On Other Tables | Functional: Integration Test | 1. Run program 2. Enter login info 3. Press login 4. Go to menu 5. Press on shipment 6. Fill out textfields 7. Press update 8. Check balance and inventory pages tables |                After the tester does required steps, and algorithm uploads to table, other tables must be affected. Balance amount must have increased by earning entered in shipments, and amount of item selected by user must have decreased by amount requested.               |
|               UI Test               |      Non-Functional Test     |                 1. Run Program 2. Attempt login 3. Attempt registration 4. Attempt menu navigation 5. Create product 6. Create shipment 7. Check balance                |                                                    Tester investigates possible inconveniences or illogical connections in the system. This leads to the discovery of the need for a "back to menu" button and a "close" button.                                                   |
|             Code Review             |      Non-Functional Test     |   Read over code to check legibility and good coding practices. Should be easy to follow and build-upon in the case of improvements on the application in the future.   |                                           Couple changes in naming protocol and insertion of comments in more complex parts of the program. Parameter definition of commonly used functions, especially those taken from other libraries.                                          |

# Criteria C: Development

## List of techniques used

- OOP paradigm
- KivyMD
- SQLite/Relational Databases
- Hashing
- For loops
- If statements
- Boolean logic

## Development
### Try Login
```.py
    def try_login(self):
        meet_req = False
        username = self.ids.uname.text
        password = self.ids.pword.text
        query = f"""SELECT username, password from users where username = '{username}'"""
        table_username = db.search(query, multiple=False)
        meet_req = check_password(table_username[1], password)
        if meet_req == True:
            self.parent.current = "Menu"
        else:
            print("Error. No login info")
```
This function is a login function that will only switch parent.current to menu (move forward to menu) if the username given already exists in the database and the password it is associated with matches the one in the database. It does this by running a query that looks for the username and password in the users database where the username is equal to that given by the user. It then checks the password associated to that given. It uses boolean logic in the sense that if either of these conditions are not met, a meet requirement variable is set to false and an if statements blocks procedure unless that requirement is set to true by the algorithm in both matching cases.

### Get Hint
```.py
    def give_hint(self):
        username = self.ids.uname.text
        hint = db.search(f"""SELECT hint from users where username = '{username}'""", multiple=False)
        self.ids.hinto.opacity = 100
        self.ids.hinto.text = f"Hint: {hint[0]}"
```
Although a simple function, it is critical to solve client problems. Due to their short term memory loss, they often forget their password. This function returns a hint entered upon registration by taking it from the database. It does this through a database search where it gets the associated hint with the username given then sets the text of a small MDLabel in the top of the screen to that hint. It then increase the opacity from 0 to 100 so that the user may only see it upon request.

### New shipment update
```.py
    def update(self):
        self.ids.amount.error = False
        db = DatabaseBridge('dylanclothes2.db')
        name = self.ids.customer_name.text
        amount = self.ids.amount.text
        item = self.ids.request.text
        earning = self.ids.earning.text
        shirts = db.search(query= f"SELECT amount from products where item = '{item}'", multiple=False)
        new_shirts = shirts[0] - int(amount)
        if new_shirts < 0:
            self.ids.amount.error = True
        else:
            db.insert(insert_query=f"""INSERT into shipments (name, amount, items, earning)
                                           values ('{name}','{amount}','{item}','{earning}')""")
           # reset text fields
            self.show()
            db.run_query(query=f"Update products set amount = {new_shirts} where item = '{item}'")
            money1 = db.search(query= "SELECT amount from money", multiple=False)
            new_earning = int(earning)
            new_money = money1[0] + new_earning
            db.run_query(query= f"Update money set amount = {new_money} where id = 1")
            db.insert(insert_query=f"""insert into transactions (amount, type, date)
                                    values ({new_earning}, 'earn', date())""")
        db.close()
```
<sub>comments replace unecessary code</sub>

This function takes in a new shipment, which requires recording in three different databases: balance, transactions, and shipments. It also checks if the shipment is possible in the first place or if the inventory is lacking. The function does this by breaking down the incoming information from KivyMD into variables, then taking the amount of the existing inventory of the requested item by using a database search where item is user given item. It then compares the existing item amount with the requested amounts, and if the latter is bigger it will raise an error. If that is not the case, then the procedur will continue. The money database will update by searching for the current money and updating that variable with the current money in addition to the one saved in the variable before. The same happens with the amount of shirts, and the full variable chain is inserted through another query into the shipments log database.

# Criteria D: Functionality
https://drive.google.com/drive/folders/1AqxZBVOQDglBhOh8aPGSFg3OY21M7LC6?usp=drive_link 

A 7 min video demonstrating the proposed solution + additional notes with narration
