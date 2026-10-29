# Coding with Strings

Strings are ordered sequences, so we can index and slice the string.We can use a square bracket notation to extract characters from the string, in the format \[start:stop:step].Consider the string “Greetings!” indexed from the start.

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| - | - | - | - | - | - | - | - | - | - |
| G | r | e | e | t | i | n | g | s | ! |

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig2.jpg">
<figcaption>Fig 2. Slicing.py first example.</figcaption>
</figure>

We can use forward or reverse indexing. Consider the string “Greetings!” indexed and sliced from the end.

| -10 | -9 | -8 | -7 | -6 | -5 | -4 | -3 | -2 | -1 |
| --- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| G   | r  | e  | e  | t  | i  | n  | g  | s  | !  |

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig3.jpg">
<figcaption>Fig 3. Slicing.py second example.</figcaption>
</figure>

I can also grab a single character.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig4.jpg">
<figcaption>Fig 4. Slicing.py third example.</figcaption>
</figure>

As discussed previously, strings are immutable, that means you cannot change the string. You can however slice the string and reassemble a new string with changes.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig5.jpg">
<figcaption>Fig 5. Slicing.py fourth example.</figcaption>
</figure>

You cannot add a string and a number, they are different types. Examine the code below.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig6.jpg">
<figcaption>Fig 6. Slicing.py fourth example.</figcaption>
</figure>
