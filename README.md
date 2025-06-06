# 19CS301-Module5

Exp.No:5(a)	Constructors
### AIM
To write a Python code to create a Class for a Person with the parameterised constructor which will take the name and userid of the person as parameters print the userid  of the person,
### ALGORITHM

Step 1:	 Begin the program.

Step 2:	 Define the person class.

Step 3:	 The class person has an __init__ method, which is the constructor. It accepts two parameters: name and userid. 

Step 4:	Inside the __init__ method: Assign the name to self.name. Assign the userid to self.userid.

Step 5:	 Print the self.userid.

Step 6:	 Prompt the user to enter the name (string) and id.

Step 7:	 Create an instance s1 of the person class by passing the entered name and userid to the constructor.

Step 8:	 Terminate the program.
### PROGRAM
```
class person:
    def __init__(self,name,userid):
        self.name=name
        self.userid=userid
        print(self.userid)
name=input()
userid=input()
s1=person(name,userid)
```
### OUTPUT
 ![image](https://github.com/gokulkrishnan2005/19CS301-Module5/blob/main/15.png)

### RESULT
Thus the python program for parameterised constructor which will take the name and userid of the person as parameters print the userid  of the person, was implemented and executed successfully.

Exp.No:5(b)	Destructor

### AIM
To create  a  Python Class Student with a destructor.
### ALGORITHM
Step 1:	 Begin the program.

Step 2:	 Define the student class:

Step 3:	 Inside the class student, define the __init__ method (constructor) and the __del__ method (destructor).

Step 4:	 Create an object s2 of the student class. When the object s2 is created, the __init__ method is called, and its print statements are executed.

Step 5:	 Use the del statement to delete the object s2. This triggers the __del__ method (destructor), and the respective print statements are executed.

Step 6:	  Terminate the program.

### PROGRAM
```
class student:
    def __init__(self):
        print("Inside Constructor")
        print("Object initialized")
        print("Hello, my name is Emma")
    def __del__(self):
        print("Inside destructor")
        print("Object destroyed")
s2=student()
del s2
```
### OUTPUT
 ![image](https://github.com/gokulkrishnan2005/19CS301-Module5/blob/main/16.png)

### RESULT
Thus the python program for Class Student with a destructor, was implemented and executed successfully.

Exp.No:5(c)	Multiple Inheritance

### AIM
To Write a python Program to Calculated Division, sub & Multiplication using Multiple Inheritance.
### ALGORITHM
Begin the program.

Class numbers:

Defines two class variables a and b, both initialized to 0.

Class calculators inherits from numbers:

*div() – prints a / b

*sub() – prints a - b

*mul() – prints a * b

An object c of class calculators is created.

User inputs two integers, assigned to c.a and c.b.

Calls methods to perform and print the results of:

*Division

*Subtraction

*Multiplicationprint the result.
### PROGRAM
```
class numbers:
    a=0
    b=0
class calculators(numbers):
    def div(self):
        print(self.a/self.b)
    def sub(self):
        print(self.a-self.b)
    def mul(self):
        print(self.a*self.b)
c=calculators()
c.a=int(input())
c.b=int(input())
c.div()
c.sub()
c.mul()
```
### OUTPUT
![image](https://github.com/gokulkrishnan2005/19CS301-Module5/blob/main/17.png)
 
### RESULT
Thus the  python Program to Calculated Division, sub & Multiplication using Multiple Inheritance was implemented and executed successfully.



Exp.No:5(d)	Multi-level Inheritance

### AIM
To write a Python program to Get the name, age and id of a person and display using Multilevel inheritance.
### ALGORITHM

Step 1:	  Begin the program.


Step 2:	 Define the Person class.

Step 3:	 Inside the Person class, define the __init__ method (constructor), with  two parameters: name and age.

Step 4:	 Inside the __init__ method, assign name to self.name., assign age to self.age.

Step 5:	 Define the PersonDetails class that inherits from the Person class.

Step 6:	 Inside the PersonDetails class, define the __init__ method (constructor). with three parameters: name, age, and person_id. 

Step 7:	 Inside the __init__ method, call the __init__ method of the Person class using super() to initialize name and age, assign person_id to self.person_id.

Step 8:	 Define the DisplayDetails class that inherits from the PersonDetails class.

Step 9:	 Inside the DisplayDetails class, define the __init__ method (constructor),with three parameters: name, age, and person_id.

Step 10:	Inside the __init__ method, call the __init__ method of the PersonDetails class using super() to initialize name, age, and person_id.

Step 11:	Inside the DisplayDetails class, define the show_details method.

Step 12:	Inside the show_details method, return a formatted string with self.name, self.age, and self.person_id.

Step 13:	Prompt the user to enter name (string),age (integer),person_id (integer).

Step 14:	Create an instance person of the DisplayDetails class, passing name, age, and person_id to the constructor.

Step 15:	Call the show_details method on the person object and print the result.

Step 16:	Terminate the program.

### PROGRAM
```
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

class PersonDetails(Person):
    def __init__(self, name, age, person_id):
        super().__init__(name, age)  # Call the parent class constructor
        self.person_id = person_id

class DisplayDetails(PersonDetails):
    def __init__(self, name, age, person_id):
        super().__init__(name, age, person_id)

    def show_details(self):
        return f"{self.name} {self.age} {self.person_id}"

name = input()
age = int(input())
person_id = int(input())

person = DisplayDetails(name, age, person_id)

print(person.show_details())
```
### OUTPUT
![image](https://github.com/gokulkrishnan2005/19CS301-Module5/blob/main/18.png)

 
### RESULT
Thus the python program to Get the name, age and id of a person and display using Multilevel inheritance. , was implemented and executed successfully.
