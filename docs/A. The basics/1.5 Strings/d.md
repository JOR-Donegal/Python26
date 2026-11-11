# Escape Sequences

We have already seen the print function.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig14.jpg">
<figcaption>Fig 14. Simple print 1.</figcaption>
</figure>

Normally, it inserts a line feed by default.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig15.jpg">
<figcaption>Fig 15. Simple print 2.</figcaption>
</figure>

The default value of the end parameter of the print function is \n, so a new line character is appended to the string.

We could suppress this.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig16.jpg">
<figcaption>Fig 16. Print with suppressed ending.</figcaption>
</figure>

Or we could include an escape sequence \n to do a multi-line print command on one line of code.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig17.jpg">
<figcaption>Fig 17. Print with escape.</figcaption>
</figure>

Escape sequences tell Python that the following character is a control character, not a letter.

In this example, I use \n to tell Python I want a new line. I could use **\t** to insert a tab character.
