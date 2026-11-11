# Build a test

I create a new file called **test\_formatter.py** and I import the **unittest** module, I also import the file I want to test, **formatter**. I create a new class, inheriting **unittest.TestCase** and create functions for my tests, in this case **test\_lower** and **test\_upper**. I add a main section and call.

```python
import unittest
import formatter

class TestFormatter(unittest.TestCase):
    def test_lower(self):
        test_text = "JOHN ORAW"
        result = formatter.convert_lower(test_text)
        self.assertEqual(result, "john oraw")

    def test_upper(self):
        test_text = "John ORaw"
        result = formatter.convert_upper(test_text)
        self.assertEqual(result, "JOHN ORAW")

if __name__ =="__main__":
    unittest.main()

```

I need to run the test from the command prompt; it passes!

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig43.jpg">
<figcaption>Fig 43. Formatter output.</figcaption>
</figure>

Note that **-m** runs a library module (unittest) as a script.
