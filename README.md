# Resource Management Project Readme

## Overview
This Java program implements a resource management system that allocates budget to different university departments based on their needs and priorities. The system uses a priority queue data structure to manage departments and their budget requests.

## Files
* `Driver.java`: Contains the main method that executes test cases with different files and budgets
* `ResourceManagement.java`: Contains the main logic for budget allocation and item selection
* `TestCase1/` and `TestCase2/`: Directories containing test files for different departments

## Data Structures
The program uses the following data structures:
* `PriorityQueue<Department>`: To store departments based on priority
* `Queue<Item>`: To store items desired, received, and removed for each department

## Classes
1. **ResourceManagement**: Main class that handles budget allocation
   * Fields: departmentPQ, remainingBudget, budget
   * Methods: Constructor, printSummary(), printName()
2. **Department**: Represents a university department
   * Fields: name, priority, itemsDesired, itemsReceived, itemsRemoved
   * Methods: Constructor, compareTo(), equals(), toString()
3. **Item**: Represents an item to be purchased
   * Fields: name, price
   * Methods: Constructor, toString()

## Algorithm
The budget allocation algorithm works as follows:
1. Create a department for each input file
2. For each department, parse items and add them to the itemsDesired queue
3. Use a priority queue to track which department gets the next item purchase
4. The priority is determined by how much has been spent on each department so far
5. Departments with less money spent get higher priority
6. Continue until the budget is depleted or no items can be purchased

## File Format
Each department file follows this format:
* First line: Department name
* Subsequent pairs of lines: Item name followed by price

## To-Do
The following functions need to be implemented:
* ResourceManagement constructor
* printSummary() method
* Department constructor
* printName() method (add your name)

## How to Run
Compile and run Driver.java:
```
javac Driver.java
java Driver
```

## Evaluation:
The program will test the implementation with three different test cases:

1. Test case with budget = $41850.00
2. Test case with budget = $0.01
3. Test case with budget = $27961.10