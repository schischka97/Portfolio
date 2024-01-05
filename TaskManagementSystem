class TaskManagementSystem:
    def __init__(self):
        self.tasks = []

    def add_task(self, name, priority=False):   #add tasks to list
        task = {
            'name': name,
            'priority': priority
        }
        self.tasks.append(task)

    def update_task(self, name, priority):      #update priority of tasks
        task = self.find_task(name)
        if task:
            task['priority'] = priority
        else:
            print(f"Task '{name}' not found.")

    def delete_task(self, name):                 #delete tasks from list
        task = self.find_task(name)
        if task:
            self.tasks.remove(task)
        else:
            print(f"Task '{name}' not found.")

    def prioritize_task(self):                  #orders priority tasks to the top of the list
        self.tasks.sort(key=lambda x: not x['priority'])

    def find_task(self, name):                   #search for task by name
        for task in self.tasks:
            if task['name'] == name:
                return task
        return None

    def display_tasks(self):                     #prints task
        print("\nTask List:")
        for task in self.tasks:
            print(f"Task: {task['name']}, priority: {task['priority']}")


task_manager = TaskManagementSystem()
