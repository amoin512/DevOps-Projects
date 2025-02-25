# To-Do List Application with Docker

This is a simple command-line To-Do List application written in python. The app allows users to manage tasks, including adding new tasks, viewing existing ones, and removing completed tasks. It creates a text file 'todo_list.txt' to store tasks persistently. Each task has a unique identifier (UUID), a task description and a deadline.

The project also includes a Dockerfile to build and run the application in a containerized environment, making it easier to deploy and run across different systems.

## Features

- Add new tasks with a unique ID, description, and deadline.
- Display all tasks currently stored in the to-do list.
- Mark tasks as completed by removing them from the list.
- Data is stored in a text file 'todo_list.txt' to persist between sessions.
- Docker containerization for easy deployment.

## Requirements

- **Docker:** Make sure Docker is installed on your system.
- **Python 3.x** (if running without Docker i.e. to test the code)

## How to Use:

1. Clone the repository to your local machine

```
git clone https://github.com/amoin512/DevOps-Projects.git
```

2. Build the Docker Image

In the project directory, run the following Docker command to build the image:

```
docker build -t todo_list_image:v1
```

This will:
- Use the `Dockerfile` to create a Docker image called `todo_list_image:v1`.
- Set up the working directory as `/app` and copy the contents of the current directory into the container.
- Run the Python script `ToDoList_Code.py` to start the application.

3. Tag the Docker Image

After building the Docker image, you can tag the image for Docker Hub:

```
docker tag todo_list_image:v1 moina512/python-todo-list-repo:latest
```

This command tags your local image `todo_list_image:v1` with the appropriate repository name and tag `moina512/python-todo-list-repo:latest`.

4. Log in to Docker Hub

```
docker login
```

You will be prompted to enter your Docker Hub username and password.

5. Push the Docker Image to Docker Hub

Push the tagged image to a Docker Hub repository:

```
docker push moina512/python-todo-list-repo:latest
```

This command uploads the image to Docker Hub under the `moina512/python-todo-list-repo` repository with the `latest` tag. You can now access this image from Docker Hub on any machine.

6. Run the Docker Container (on any machine)

Once the image is uploaded to Docker Hub, you can run the Docker container from the image with the following command:

```
docker run -it --rm moina512/python-todo-list-repo:latest
```

- The `-it` flag allows interactive mode so you can interact with the application.
- The `--rm` flag ensures the container is removed once you exit.

7. Interact with the To-To List Application

Once the container is running, the application will prmopt you with the following options:

```
    == TODO LIST ==  
    [1] show task    
    [2] add task     
    [3] complete task
    [4] exit
```

- [1] show task: Displays all tasks with their IDs, descriptions, and deadlines. 
- [2] add task: Add a new task by providing a description and deadline. The task will be assigned a unique ID.
- [3] complete task: Remove a task by entering its ID. This will mark as completed and delete it from the list.
- [4] exit: Exit the application.

8. Stop the Docker Container

To stop the container and exit the application, simply type:

```
4
```
This will exit the application and remove the container since `--rm` was used.

## Example:

Here's what interacting with the app might look like:

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