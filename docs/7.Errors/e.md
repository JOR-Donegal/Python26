# Input Validation

One of the ways we intercept errors is to validate user input. Create a new programme, **validate\_integer.py**

```python
from re import A

def validate_integer():
    # Loop forever
    while True:
        try:
            user_input = int(input("Enter an integer value: "))
        except:
            # Bad value, 
            print("Error")
            continue
        else:
            print("Valid input")
            # Good value, exit the loop
            break
        finally:
            # Continue
            print("This message shows every time, regardless of the programme flow")
    

validate_integer()
```

Run this code.

Try entering the value **10**, then run the code again and enter the value **ten**.

## Exercise

I have two variables on my diesel backup generator.

* fuel in litres
* fuel\_consumption in litres per minute.

I can calculate my remaining endurance in minutes 

```python
Endurance= Fuel/(Fuel Consumption) 
```

Whenever the motor is idling, the flowmeter cannot calculate fuel flow and sets it = 0

Write a function to calculate the remaining endurance in minutes, checking and handling for divide by zero errors and for any value errors.
