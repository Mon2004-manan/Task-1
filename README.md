# Task-1
Codesoft Task 1 
def main():
  tasks = []

  while True:
    print("1. Add Task")
    print("2. View Tasks")
    print("3. Mark Task Done")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == '1':
      task = input("Enter task: ")
      tasks.append(task)
      print("Task added!")
    elif choice == '2':
      if not tasks:
        print("No tasks added yet!")
      else:
        print("Tasks:")
        for i, task in enumerate(tasks):
          print(f"{i+1}. {task}")
    elif choice == '3':
      if not tasks:
        print("No tasks to mark as done!")
      else:
        print("Tasks:")
        for i, task in enumerate(tasks):
          print(f"{i+1}. {task}")
        task_number = int(input("Enter task number to mark done: ")) - 1
        if task_number < 0 or task_number >= len(tasks):
          print("Invalid task number!")
        else:
          tasks.pop(task_number)
          print("Task marked as done!")
    elif choice == '4':
      print("Exiting...")
      break
    else:
      print("Invalid choice!")

if __name__ == "__main__":
  main()
