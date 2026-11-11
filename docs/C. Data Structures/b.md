# Lists

Lists are ordered sequences that can store different object types. Lists are identified by [] brackets. We have previously seen indexing and slicing, and these techniques work the same with lists.

You should be able to understand the code below, based on previous exercises. In this case, **len** returns the numbers of elements in the list, not the number of characters (for example, the number 10.13 would be a single element).

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig25.jpg">
<figcaption>Fig 25. Lists1.py.</figcaption>
</figure>
You can also concatenate lists.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig26.jpg">
<figcaption>Fig 26. Lists2.py.</figcaption>
</figure>

Lists can also be nested; you can have lists of lists.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig27.jpg">
<figcaption>Fig 27. Lists3.py.</figcaption>
</figure>

In previous notes I explained the term _immutable_. I demonstrated that strings are immutable. However, lists are _mutable_, individual items may be indexed and selectively edited.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig28.jpg">
<figcaption>Fig 28. Lists4.py.</figcaption>
</figure>

Lists have a range of available methods, we can edit the list in place, appending items.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig29.jpg">
<figcaption>Fig 29. Lists5.py.</figcaption>
</figure>

It can be very useful to take a string of data and create a list based on the contents of that string. For example, a comma/space delimited file (CSV) if a very normal way to exchange data. You can then iterate over the individual items; we will cover that in a later walkthrough.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig30.jpg">
<figcaption>Fig 30. StringToLists.py.</figcaption>
</figure>

## Finally

Review the methods documented [here](https://docs.python.org/3/tutorial/datastructures.html)

Experiment with some of these methods to see how they work.
