![11e470e9022f4fc5b367429bcbb285bc](https://github.com/comsci-uwc-isak/unit2_2023/assets/53995212/1d14b1d3-ae39-4ef3-8ec9-3329630eacae)

# Unit 3: A Clothing Factory GUI

## Criteria A: Planning

## Problem definition

The client is the manager of a clothes making factory that produces luxury shirts in three different colors (red, blue, yellow). He suffers from frequent short term memory loss which causes him to forget how much money he has as well as how many shirts he has in inventory. This therefore results in losses for the factory as they take on orders they do not have the supply to meet, costing them their reputation and clients. He tried keeping track on paper, but it became tedious and inefficient, especaily because he needs a way to account for barganing, since the clothes are so luxurious they are not sold at a specific price. His short term memory loss also results in him losing his password often, which is a problem he has faced with other services in the past. Another problem he has faced with these services is passwords that are too easy to guess, which associates of his use and result in the company losing a lot of money to dataleaks and unethical hackers. Finally, since many of his associates produce goods and make sales without coordinating decisions, productions and sales get lost overtime.

## Proposed Solution

**Design statement**

``` Fill out here```

## Success Criteria
1. A page that keeps track of how much money the client has (Issue Tackled: "forget how much money he has")
2. A page that shows the current inventory of the factory (Issue Tackled: "[forget] how many shirts his has in inventory")
3. One page that allows the client to create his product (Issue Tackled: "his associates produce goods and makes sales without coordinating decisions")
4. A registration system with a password policy and a hint option (Issue Tackled: losing his password, passwords are too easy to guess")
5. A transaction table that shows all earning and losses faced by the factory (Issue Tackled: "productiond and sales get lost overtime")
6. A shipment page that return an error if the inventory does not have enough items to meet the order and allows the user to enter the earning amount (Issue Tackled: "take on order they do not have the supply to meet, needs a way to account for barganing")


# Criteria B: Design

## Wireframe Diagram
![image](https://github.com/Amine-Itani/Unit-3/assets/123438294/3f41eb43-509e-4f1e-96bc-3391c2fe191d)

<sub>**Fig.1** Figure shows the wireframe diagram of the application</sub>

## UML Diagram 


<sub>**Fig.2** </sub>

## Flow Diagrams

### New Shipment Upload (Simple)
The purpose of the new shipment upload is to update the balance, inventory, and shipment databases, and to check if the requested shipment of products is possible.

![image](https://github.com/Amine-Itani/Unit-3/assets/123438294/236f3c29-6938-48d7-9751-8d93d25ba513)

The function does this through taking the requested amount of a certain item, calling the amount of that item from the database, and comparing to see if that request is possible. If the amount requested is greater than the existing amount, it will return an error telling the user that the shipment is not possible. If the amount requested is not greater than the existing amount, then it will increase the balance by the earning entered, it will decrease the inventory by the amount of the product requested, and add the details of the order to the shipments database.

<sub>**Fig.3** Figure shows simple flow diagram</sub>

### Login Procedure (Medium)
The purpose of the login procedure is not just to confirm that the user exists, but also to offer a hint in the case that the user forgets their password. It also checks hashes instead of the actual password for increased security.

![image](https://github.com/Amine-Itani/Unit-3/assets/123438294/6237cc1a-4243-4683-9132-0b9c5ae26900)

The function will first ensure that the user exists through checking if the username is in the users database. It will return an error if it does not find a matching user. If the user exists, it will procceed to the password check where it will hash the given password and compare it to the hashed password associated with the username given in the database. If these match, it will then move to the menu page. If these do not match, it will offer the user use a forgot password button. If they decide to do so, the hint associated with the username in the database will be shown on screen.

<sub>**Fig.4** Figure shows medium flow diagram</sub>

### Registration Precodure (Complex)
The purpose of the registration procedure is to signup users to the database but also to check if they meet the required security measures put in place by the client.

![image](https://github.com/Amine-Itani/Unit-3/assets/123438294/d819ae11-b300-420e-a04a-bc51c6c0db40)

The function takes the given username, password, password retype (check), and hint from the user through kivy textfields. It then iterates through the password and increase a numeric counter by one for every number in the password and increases an alphabetical (alpha) counter by one for every letter in the password. Once the loop is done, if either counters are 0, the function will return an error. If these counters meet the requirements, it will then check that the password is greater than 7 characters, and that the given username does not already exists. If either of these requirements are not met, the function will return an error. If all is well, then the function will hash the password and upload everything to the database.

<sub>**Fig.5** Figure shows complex flow diagram</sub>

## Record of Tasks
| Task No | Planned Action                                                | Planned Outcome                                                                                                 | Time estimate | Target completion date | Criterion |
|---------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|---------------|------------------------|-----------|
| 1       | Write the Problem context                        | 10min         | Nov 22                 | A         |

## Test Plan

# Criteria C: Development

## List of techniques used

## Development


# Criteria D: Functionality

A 7 min video demonstrating the proposed solution with narration
