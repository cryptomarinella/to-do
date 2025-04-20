# to-do
# todo.py

tasks = []

def show_tasks():
    if not tasks:
        print("Your to-do list is empty!")
    else:
        print("Your tasks:")
        for i, task in enumerate(tasks, 1):
            print(f"{i}. {task}")

def add_task():
    task = input("Enter a task: ")
    tasks.append(task)
    print("✅ Task added.")

def remove_task():
    show_tasks()
    try:
        num = int(input("Enter task number to remove: "))
        removed = tasks.pop(num - 1)
        print(f"❌ Removed: {removed}")
    except (IndexError, ValueError):
        print("Invalid number.")

def menu():
    while True:
        print("\n1 -
