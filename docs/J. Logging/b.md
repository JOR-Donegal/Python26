# Time

I am creating a first python file called _mytime.py_ for this exercise. There are several standard libraries we can use in Python to handle time.

The module _datetime_ is one of the most used. I am going to let you [read](https://docs.python.org/3/library/datetime.html.) the detail, rather than explaining everything. here.

```python
from datetime import datetime as dt
# Get the current time, returns a value like 2022-10-09 17:46:45.151666
today = dt.now()
print(today)
# Get Unix time, returns a value like 1665566809.057217
unix_epoch_time = dt.timestamp(today)
print(unix_epoch_time)

```

Once you have read the detail, you should be able to calculate things like _timedelta_, the difference between two times.

The **strftime()** method is handy for making useful strings from the datetime object.

Rather than using a function to return the weekday, I can use

```python
weekday = dt.now().strftime("%A") 
```

Similarly, to get a month, I can use

```python
month = dt.now().strftime("%B")
```

Hours, minutes, etc. all have their own codes available.

## Exercise

Add to the code above and print human readable values for current time (hours, minutes, seconds) and date (year, month, day).
