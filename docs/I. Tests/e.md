# Test a test

Next, I force an error. I edit **test\_formatter.py** and mangle the test string.

```python
def test_upper(self):
    test_text = "John ORaw"
    result = formatter.convert_upper(test_text)
    self.assertEqual(result, "JoHN ORAW")
```

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig44.jpg">
<figcaption>Fig 44. Formatter output.</figcaption>
</figure>

The test failed as expected and the location of the error was pointed out to me. There are many different test types you could use in unittest, look through and understand the flexibility you have.

