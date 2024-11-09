# Initialize an empty list to store tasks
tasks = []

# Main loop
while True:
    print("Options:")
    print("1. Add a task")
    print("2. Show tasks")
    print("3. Mark a task as complete")
    print("4. Exit")
    choice = input("Enter your choice: ")

    if choice == "1":
        task = input("Enter the task: ")
        tasks.append(task)
        print("Task added.")

    elif choice == "2":
        print("Your tasks:")
        for i, task in enumerate(tasks):
            print(f"{i+1}. {task}")

    elif choice == "3":
        print("Which task do you want to mark as complete?")
        for i, task in enumerate(tasks):
            print(f"{i+1}. {task}")
        task_index = int(input("Enter the task number: ")) - 1
        if task_index >= 0 and task_index < len(tasks):
            tasks[task_index] = tasks[task_index] + " (Complete)"
            print("Task marked as complete.")
        else:
            print("Invalid task number.")

    elif choice == "4":
        print("Exiting.")
        break

    else:
        print("Invalid choice. Please try again.")
      
