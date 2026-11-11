# Systematically Handling Errors

If code has been written incorrectly, the interpreter will catch this and label it as a _syntax error_. Even if your Python is syntactically correct, it may still generate errors when you try to run it. Perhaps you are running in the wrong operating system, or missing libraries?

An _exception_ is a _run time error_ which occurs during the execution of the program. In my code, I handle such events in a planned way.

There are keywords used for exception handling

**Try** is the block of code we are about to attempt to run.

**Except** is the code that runs if an error occurs and should handle the error gracefully. For example, it may report the error in detail and then resume the programme. You can have a separate Except section for each error type.

**Else** is the additional code that runs if an error does not occur.

**Finally** is the code that runs at the end, whether there is an error or not.

I am going to write a simple function to create a directory but I’m going to handle any errors in its creation. Copy the content of **detect\_working\_directory.py** to a new file **create\_directoy.py**

Add the following function.

```python
def create_directory(directory_name: str) ->bool:
    # Use try/except to catch errors
    try:
        # Create the diretory
        os.mkdir(directory_name)
        # If this worked, return True
        return True
    except:
        # Give an explicit error message
        print(f"Error creating directory {directory_name}")
        # If this did not work, return False
        return False    
```

At the end of your **if (\_\_name\_\_ == '\_\_main\_\_'):** section, with the correct indentation, add

```python
if create_directory("JOR"):
        print("Creating a directory worked")
        # Do other stuff
    else:
        print("You couldn't create a directory!")
        # Do other stuff
```

When you run the program the first time, it works. However, the second time you run the program, it fails. You already created the directory; you cannot create a directory with the same name in the same path.

The “already existing” case wasn’t really an error, we should deal with this case differently. I can modify my function to return a value if the directory already exists. Maybe I’m going to return an integer and change my calling code!

```python
def create_directory(directory_name: str)->int: 
    # Check to see if the directory already exists
    if os.path.isdir(directory_name):
        # The directory already exists
        return 2
    else:
        # Use try/except to catch errors
        try:
            # Create the directory
            os.mkdir(directory_name)
            # If this worked, return True
            return 0
        except:
            # Give an explicit error message
            print(f"Error creating directory {directory_name}")
            # If this did not work, return False
            return 1

```

There are now three possible return statuses I could have.

```python
if create_directory("JOR") == 0:
        print("Creating a directory worked")
        # Do other stuff
    elif create_directory("JOR") == 1:
        print("You couldn't create a directory!")
        # Do other stuff
    elif create_directory("JOR") == 2:
        print("Directory already existed!")
        # Do other stuff
```
