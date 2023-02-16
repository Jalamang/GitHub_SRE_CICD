### 1. What is Python and what are its features?

 ```Python is an object-oriented programming language that is designed in C. By nature, it is a high-level programming language that allows for the creation of both simple as well as complex operations. Along with this Python comes inbuilt with a wide array of modules as well as libraries which allows it to support many different programming languages like Java, C, C++, and JSON.```

 ```Easy to Code, Open Source and Free, Support for GUI, Object-Oriented Approach, High-Level, Language Highly Portable, Support for Other Languages, Highly Dynamic```

### 2. Explain the difference between Python 2 and Python 3.
 ```- The key difference is the replacement of the ***print keyword** in Python 2.x with the print() function in Python 3.x.```

 ```- Division operator (7 / 5) (Output in Python 2.x  1 and Python 3.x is 1.4)```

```- long- holds long integers(exists in Python 2.x, deprecated in Python 3.x).```

### 3. What are the built-in data types in Python?
- Numeric data types: int, float, complex
- String data types: str
- Sequence ty pes: list, tuple, range
- Binary types: bytes, bytearray, memoryview
- Mapping data type: dict
- Boolean type: bool
- Set data types: set, frozenset

### 4. What is the difference between a tuple and a list in Python?
- 1  Lists are mutable	    Tuples are immutable
- 2	The implication of iterations is Time-consuming	  -  The implication of iterations is comparatively Faster
- 3	The list is better for performing operations, such as insertion and deletion.	  -      Tuple data type is appropriate for accessing the elements
- 4	Lists consume more memory	-    Tuple consumes less memory as compared to the list
- 5	Lists have several built-in methods	  -  Tuple does not have many built-in methods.
- 6	The unexpected changes and errors are more likely to occur	-    In tuple, it is hard to take place.

### 5. How do you create a dictionary in Python?

    ```dictionary_name = {key: value}
    ```

### 6. What is a generator in Python?
- Generator function use the yield keyword instead of return

- So a generator function returns an generator object that is iterable
- 
```def simpleGeneratorFun():```
    ```yield 7 yield 17 yield 8```

```for value in simpleGeneratorFun(): print(value)```

### 7. What are the different types of loops in Python and when would you use each one?
 
   - A for loop in Python is used to iterate over a sequence (list, tuple, set, dictionary, and string).
  - The while loop is used to execute a set of statements as long as a condition is true.
  - If a loop exists inside the body of another loop, it is called a nested loop.

### 8. What is a decorator in Python?
    # In Python, a decorator is a design pattern that allows you to modify the functionality of a function by wrapping it in another function.

    # The outer function is called the decorator, which takes the original function as an argument and returns a modified version of it.
def outer(x):
    def inner(y):
        return x + y
    return inner

add_five = outer(5)
result = add_five(6)
print(result)  # prints 11


### 9. How do you handle exceptions in Python?
```
try:
    print('try block')
    x=int(input('Enter a number: '))
    y=int(input('Enter another number: '))
    z=x/y
except ZeroDivisionError:
    print("except ZeroDivisionError block")
    print("Division by 0 not accepted")
else:
    print("else block")
    print("Division = ", z)
finally:
    print("finally block")
    x=0
    y=0
print ("Out of try, except, else and finally blocks." )
```
```
try:
    x=int(input('Enter a number upto 100: '))
    if x > 100:
        raise ValueError(x)
except ValueError:
    print(x, "is out of allowed range")
else:
    print(x, "is within the allowed range")
```

### 10. What is the difference between a module and a package in Python?
   - The module is a simple Python file that contains collections of functions and global variables and with having a .py extension file. It is an executable file and to organize all the modules we have the concept called Package in Python.

### 11. What is PEP 8 and why is it important?
    - Readability - Naming convention 

### 12. How do you debug Python code?
   - Debugging in Python is facilitated by pdb module (python debugger) which comes built-in to the Python standard library.
```
import pdb

def addition(a, b):
	answer = a * b
	return answer


pdb.set_trace()
x = input("Enter first number : ")
y = input("Enter second number : ")
sum = addition(x, y)
print(sum)
```
### 13. How would you reverse a string in Python?
``` 
Slicing [::-1] 
range(len(str) - 1, -1), 
for loop (str = i str = i + str)
```

### 14. What are the advantages of using NumPy over regular Python lists?
- NumPy is the de-facto Python library for N-dimensional arrays manipulation and computational computing. It is open-source, easy to use, memory friendly, and lightning-fast.
- NumPy provides fast and efficient operations on arrays of homogeneous data.
  
- Python lists store a collection of ordered, alterable data objects, 
- NumPy arrays only store a single type of object. So, we can say that NumPy arrays live under the lists’ umbrella.

### 15. What are the different types of inheritance in Python?
- Single inheritance enables a derived class to inherit properties from a single parent class, thus enabling code reusability and the addition of new features to existing code.


- single inheritance

- Base class
```
class Parent:
	def func1(self):
		print("This function is in parent class.")

- Derived class

class Child(Parent):
	def func2(self):
		print("This function is in child class.")

- Driver's code
object = Child()
object.func1()
object.func2()
```


- multiple inheritance

- Base class1
  ```
class Mother:
	mothername = ""

	def mother(self):
		print(self.mothername)


- In multilevel inheritance, features of the base class and the derived class are further inherited into the new derived class. This is similar to a relationship representing a child and a grandfather.

- Multilevel inheritance

- Base class

```
class Grandfather:

	def __init__(self, grandfathername):
		self.grandfathername = grandfathername

- Intermediate class
- 
class Father(Grandfather):
	def __init__(self, fathername, grandfathername):
		self.fathername = fathername

		# invoking constructor of Grandfather class
		Grandfather.__init__(self, grandfathername)

- Derived class

class Son(Father):
	def __init__(self, sonname, fathername, grandfathername):
		self.sonname = sonname

		# invoking constructor of Father class
		Father.__init__(self, fathername, grandfathername)

	def print_name(self):
		print('Grandfather name :', self.grandfathername)
		print("Father name :", self.fathername)
		print("Son name :", self.sonname)

- Driver code
s1 = Son('Prince', 'Rampal', 'Lal mani')
print(s1.grandfathername)
s1.print_name()
```

- When a class can be derived from more than one base class this type of inheritance is called multiple inheritances. In multiple inheritances, all the features of the base classes are inherited into the derived class.

- Multiple inheritances
```
class Father:
	fathername = ""

	def father(self):
		print(self.fathername)

- Derived class

class Son(Mother, Father):
	def parents(self):
		print("Father :", self.fathername)
		print("Mother :", self.mothername)

- Driver's code
s1 = Son()
s1.fathername = "RAM"
s1.mothername = "SITA"
s1.parents()
```

- Hierarchical inheritance

- Base class
```
class Parent:
	def func1(self):
		print("This function is in parent class.")

- Derived class1

class Child1(Parent):
	def func2(self):
		print("This function is in child 1.")

- Derived class2

class Child2(Parent):
	def func3(self):
		print("This function is in child 2.")

- Driver's code
object1 = Child1()
object2 = Child2()
object1.func1()
object1.func2()
object2.func1()
object2.func3()
```
- When more than one derived class are created from a single base this type of inheritance is called hierarchical inheritance. In this program, we have a parent (base) class and two child (derived) classes.

- Hybrid inheritance
```
class School:
	def func1(self):
		print("This function is in school.")

class Student1(School):
	def func2(self):
		print("This function is in student 1. ")

class Student2(School):
	def func3(self):
		print("This function is in student 2.")

class Student3(Student1, School):
	def func4(self):
		print("This function is in student 3.")

- Driver's code

object = Student3()
object.func1()
object.func2()
```

### 16. How do you implement a linked list in Python?
- Python program for traversal of a linked list
#### Node class

```
class Node:

	- Function to initialise the node object
	def __init__(self, data):
		self.data = data # Assign data
		self.next = None # Initialize next as null


- Linked List class contains a Node object
class LinkedList:

	- Function to initialize head
	def __init__(self):
		self.head = None

	- This function prints contents of linked list
	 starting from head
	def printList(self):
		temp = self.head
		while (temp):
			print(temp.data)
			temp = temp.next


- Code execution starts here
if __name__ == '__main__':

	- Start with the empty list
	llist = LinkedList()

	llist.head = Node(1)
	second = Node(2)
	third = Node(3)

	llist.head.next = second 
    - Link first node with second

	second.next = third 
    - Link second node with the third node

	llist.printList()
```

### 17. What is the difference between deep and shallow copying in Python?

- A shallow copy creates a new variable that shares the reference of the original object
- A deep copy creates a new compound object before inserting copies of the items found in the original into it in a recursive manner. 

- It means that any changes made using deep copy, the changes do not reflect in the original object which is the opposite for shallow

### 18. What are the benefits of using a virtual environment in Python?

- A virtual environment is a tool that helps to keep dependencies required by different projects separate by creating isolated python virtual environments for them.
  
- By default very project on your system will use these same directories to store and retrieve site packages (third-party libraries).
 
- It is generally good to have one new virtual environment for every Python-based project you work on. So the dependencies of every project are isolated from the system and each other.

### 19. Explain the difference between *args and **kwargs in Python.
  - *args allows you to pass the desired number of arguments to the function. Args generally means arguments in this case. Let’s see an example.
```
def demo(*args):
    print(args)
 Call the function again, this time with 6 arguments
    demo("Humpty", "Dumpty", "Sat", "On", "A", "Wall") #Output ('Humpty', 'Dumpty', 'Sat', 'On', 'The', 'Wall')
```

 - **kwargs stands for keyword arguments. The only difference from args is that it uses keywords and returns the values in the form of a dictionary. Now, let’s write a normal function and pass arguments through args and kwargs
``
def demo(**kwargs):
    print(kwargs)

    demo(name="Humpty", location="Wall")  #Output {'name': 'Humpty', 'location': 'Wall'}
```

### 20. How do you check if a string is a palindrome in Python?
  - A palindrome is a sequence of the word, phrases, or numbers that read the same backward as forward.
```
def isPalindrome(string): 
    if(string == string[::-1]): 
        return "The string is a palindrome. 
    else: 
        return "The string is not a palindrome.
``` 
```
Enter input string 
string = input ("Enter string: ") 
 
print(isPalindrome(string)) 
```

### Programming questions:

   - factorial of a number.
```
    def fact(n):
        if n == 1 or n == 0:
            return 1
        else:
            return n * fact(n - 1)
```
### Write a Python function to check if a number is prime.
```
    def checkPrime(n):
        if n == 0 or n == 1:
            return f"{n} is not prime"

        for num in range(2, n + 1):
            if n % num == 0:
                return f"{n} is not prime"
        else:
            return f"{n} is prime"
```
### Write a Python function to check if a string is a palindrome.
```
    def checkPalindrome(text):
        for i in range(len(text)//2 + 1):
            if(text[i] != text[len(text) - 1 - i]):
                return f"{text} is not a palindrome"
        else:
            return f"{text} is a palindrome"
                
    checkPalindrome('MALAYALAM')
```
#### Write a Python program to check if two strings are anagrams.
```
    def CheckAnagram(s1, s2):
    
        if sorted(s1) == sorted(s2):
            return True
        else:
            return False
    
    CheckAnagram('restful', 'fluster')
```
### Write a Python program to reverse a string.
```
    def reverseString(string):
        return string[::-1]
```
### Write a Python program to sort a list of integers.
```
    def SortAList(myList):
        return sorted(myList)
    SortAList([1, 9,13, 112, 7, 9, 105])   
```
### Write a Python program to find the common elements between two lists.
```
    def  CommonElements(listA, listB):
        commonList = []
        for el in listA:
            if el in listB:
                commonList.append(el)
        return commonList
        
    CommonElements([9, 13, 7, 9, 10], [1, 9,13, 112, 7, 9, 105])  
```
### Write a Python function to find the maximum and minimum elements in a list.
```
    def maxAndMin(myList):
        return (max(myList), min(myList))
```    
# Write a Python program to remove duplicates from a list.
```
    def RemoveDuplicatesV1(myList):
        uniqueValues = []
        i = 0
        for el in myList:
            if el in uniqueValues:
                pass
            else:
                uniqueValues.append(el)
                
        return uniqueValues
            

    RemoveDuplicatesV2([105, 2, 2, 7,1, 9,13, 112, 7, 9, 105])
```
# Write a Python program to find the second largest number in a list.
```
    def SecondLargest(myList):
        mySortedList = sorted(myList)
        return mySortedList[-2]

    SecondLargest([105, 7,1, 9,13, 112])
```

### Write a Python program to calculate the average of a list of numbers.
```
    def TotalV1(myList):
        return sum(myList)/len(myList)

    def TotalV2(myList):
        total = 0
        for num in myList:
            total += num
        return total//len(myList)

    TotalV2([1,3,7,11])
```
### Write a Python function to check if a string is a valid IP address.

```
    def validateOctet(octet):
        
        if len(octet) > 1 and octet[0] == '0':
                return False
        else:
            if octet.isdigit() is False:
                return False
            else:
                return True
```    
 
```  
    def CheckValidIP(ip):
            ipList = ip.split('.')
            
            if len(ipList) != 4:
                return f'{ip} is an invalid IP address!'

            for octet in ipList:
                if validateOctet(octet) is False or int(octet) < 0 or int(octet) > 255:
                    return f'{ip} is not a valid IP address!'

            else: 
                return f'{ip} is a valid IP address!'
          
```

### Write a Python program to generate all permutations of a list.
import itertools

```
    def listOfPermutation(*args):
        return list(itertools.permutations(args))

    listOfPermutation([2,5,7])
```

### Write a Python function to check if a given year is a leap year.

```
     def LeapYear(year):
        if year % 4 == 0 and year % 100 != 0 or year % 400:
            return f'{year} is a lear year'
        else:
            return f'{year} is not a lear year'
```
### Write a Python program to find the most frequent element in a list.

```
    def MostFrequent(arr):
        
        mostRepeated = 0
        element = 0
        myDict = {}
        for el in arr:
            myDict[el] = myDict.get(el, 0) + 1
    
        for key in myDict:
            if myDict[key] > mostRepeated:
                mostRepeated = myDict[key]
                element = key
            else:
                pass
        return element
```