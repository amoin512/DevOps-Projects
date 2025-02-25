# To-Do List Application

This is a simple command-line To-Do List application written in python. The app allows users to manage tasks, including adding new tasks, viewing existing ones, and removing completed tasks. It creates a text file 'todo_list.txt' to store tasks persistently. Each task has a unique identifier (UUID), a task description and a deadline.

## Features

- Add new tasks with a unique ID, description, and deadline.
- Display all tasks currently stored in the to-do list.
- Mark tasks as completed by removing them from the list.
- Data is stored in a text file 'todo_list.txt' to persist between sessions.

## Requirements

- Python 3.x

## How to Use:

1. Clone the repository to your local machine:

```
git clone https://github.com/amoin512/DevOps-Projects/blob/430a60c577cc04501c6a746c6134e3f17d00a838/Project-1_ToDoList/ToDoList_Code.py
```

2. Run the application:

```
python ToDoList_Code.py
```

3. Use the following options to interact with the to-do list:

- [1] show task: Displays all tasks with their IDs, descriptions, and deadlines. 
- [2] add task: Add a new task by providing a description and deadline. The task will be assigned a unique ID.
- [3] complete task: Remove a task by entering its ID. This will mark as completed and delete it from the list.
- [4] exit: Exit the application.

4. The tasks are stored in a file named 'todo_list.txt' in the same directory as the script.

## Example:

```
    == TODO LIST ==  
    [1] show task    
    [2] add task     
    [3] complete task
    [4] exit

Your choice: 2
What is your task? Finish Homework
What is the deadline? Monday

    == TODO LIST ==  
    [1] show task    
    [2] add task     
    [3] complete task
    [4] exit

Your choice: 1
bfff8c79-f19a-4fa4-9e6a-6cd25573eac9 | Finish Homework | Monday
```

## Error Handling:

- If any error occurs while reading or writing to the file, the program will display an error message.
- Invalid menu choices with prompt user to try again.