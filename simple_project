import 'dart:io';

void main(){
  List<String> tasks = [];
  bool isRunning = true;

  while(isRunning){
    print('\nSimple To-Do List Application');
    print('a. Add a task');
    print('b. View all task');
    print('c. Mark a task as completed');
    print('d. Delete a task');
    print('e. Exit');
    print('Enter your choice: ');

    var choice = stdin.readLineSync();
    if (choice != null){
      print("You entered: $choice");
    }
    else{
      print("You entered: null!");
    }
    switch (choice){
        case "a":
          addTask(tasks);
          break;
        case "b":
          viewTasks(tasks);
          break;
        case "c":
          markTaskAsCompleted(tasks);
          break;
        case "d":
          deleteTask(tasks);
          break;
        case "e":
          isRunning = false;
          print('Thank you for using the application');
          break;
       default:
          print('Invalid choice. Please try again.');   
    }
  }
}

  void addTask( List<String> tasks){
    print("Enter the task:");
    String? task = stdin.readLineSync();
    if (task != null && task.isNotEmpty){
      tasks.add(task);
      print("Task added.");
    } else {
      print("Invalid task. Please try again.");
    }
  }
  
  void viewTasks(List<String> tasks){
    if (tasks.isEmpty){
      print('No task available.');
    } else {
      print('\nTasks:');
      for (int i = 0; i < tasks.length; i++){
        print('${i + 1}. ${tasks[i]}');
      }
    }
  }
  
  void markTaskAsCompleted(List<String> tasks){
    if (tasks.isEmpty){
      print('No tasks available.');
    } else {
      print('Enter the task number to mark as completed:');
      String? input = stdin.readLineSync();
      int? taskNumber = int.tryParse(input ?? '');

    if(taskNumber != null && taskNumber > 0 && taskNumber <= tasks.length){
      tasks[taskNumber - 1] += ' (completed)';
      print('Task marked as completed.');
    } else {
      print('Invalid task number. Please try again.');
      }
    }
  }

  void deleteTask(List<String> tasks){
    if (tasks.isEmpty){
      print('No tasks available.');
    } else {
      print('Enter the task number to delete:');
      String? input = stdin.readLineSync();
      int? taskNumber = int.tryParse(input ?? '');

    if(taskNumber != null && taskNumber > 0 && taskNumber <= tasks.length){
      tasks.removeAt(taskNumber - 1);
      print('Task deleted.');
    } else {
      print('Invalid task number. Please try again.');
      }
    }
  }
