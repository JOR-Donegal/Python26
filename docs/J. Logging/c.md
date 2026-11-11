# System Logfiles

SYSLOG is a standard for message logging and is used by almost every system type, do a search for RFC 5424 and review. Python's logging library serves a similar function, with 5 debug levels.

Create a new file as **system\_logging.py**

````python
import logging

logging.debug('Debug message')
logging.info('Information message')
logging.warning('Warning message')
logging.error('Error message')
logging.critical('Critical message')
````

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig45.jpg">
<figcaption>Fig 45. System logging output.</figcaption>
</figure>

The format is Level, Logger, Message. The name of the default logger is **root**.

You can set the default logging level after the import statement.

```python
logging.basicConfig(level=logging.DEBUG)
```

Now everything at DEBUG or above will be logged (basically, everything!).

To log to a file, with formatted data, try the following.

```python
import logging
from datetime import datetime

# Get the date and time and use as a filename
now = datetime.now()
file_name = '%0.4d%0.2d%0.2d-%0.2d%0.2d%0.2d' % (now.year, now.month, now.day, now.hour, now.minute, now.second)

# Set logging to that file
logging.basicConfig(filename=file_name, filemode='w', format='%(name)s - %(levelname)s - %(message)s')

logging.debug('Debug message')
logging.info('Information message')
logging.warning('Warning message')
logging.error('Error message')
logging.critical('Critical message')
```

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig46.jpg">
<figcaption>Fig 46. System logging output.</figcaption>
</figure>

There are many attributes which can be included.

On large structured projects, the logging design is complex and I have only scratched the surface here!
