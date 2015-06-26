# Learn Python

Read Allen Downey's [Think Python](http://www.greenteapress.com/thinkpython/) for getting up to speed with Python 2.7 and computer science topics. It's completely available online, or you can buy a physical copy if you would like.

[![Think Python](img/think_python.png)](http://www.greenteapress.com/thinkpython/)

For quick and easy interactive practice with Python, many people enjoy [Codecademy's Python track](http://www.codecademy.com/en/tracks/python). There's also [Learn Python The Hard Way](http://learnpythonthehardway.org/book/) and [The Python Tutorial](https://docs.python.org/2/tutorial/).

Complete the following exercises to check your ability with Python.

These exercises are implemented with doctests, which are runnable tests inside docstrings. Fill in the function definitions. Correct solutions will make it possible to run (for example) `python -m doctest strings.py` with no messages about failures.

 * [Strings](python/strings.py)
 * [Lists](python/lists.py)


---

How are Python lists and tuples similar and different? Which will work as keys in dictionaries? Why?

Both lists and tuples are sequences of values that are indexed by integers, however unlike lists tuples are immutable. Tuples will work as keys in dictionaries. 

---


---

How are Python lists and sets similar and different? Give examples of using both. How does performance compare between lists and sets for finding an element. Why?

>Both sets and lists are 'a collection of objects. A set, however, is unordered, while a list is indexed. That means that sets elements of a set can't be searched by their their index.  `list[0]` would return the first item in the list, but doing so on a set would return a TypeError. Without an index, when searching for an element in a set, one can only check the existence of the element in the set. 

```
word = 'bookkeeper'
setex = set(word)
setex = {x for x in word}

listex = [x for x in word]

print setex
print listex
```
---


---

Describe Python's `lambda`. What is it, and what is it used for? Give at least one example, including an example of using a `lambda` in the `key` argument to `sorted`.

>`lambda` is used to create anonymous functions. If a function will only need to be accessed locally, instead of making a new function, `lambda` can be used as sort of temporary one. `lambda` is mainly used when passing a function as an argument to another function. 

I like the example of temperature conversion, taken from [here](http://www.python-course.eu/lambda.php). 

>without `lambda`:
```
def fahrenheit(T):
    return ((float(9)/5)*T + 32)
def celsius(T):
    return (float(5)/9)*(T-32)
temp = (36.5, 37, 37.5,39)

F = map(fahrenheit, temp)
C = map(celsius, F)
```
>or with `lambda`:

```
F = map(fahrenheit, temp)
C = map(celsius, F)
```

```
for name in sorted(list_family, key=lambda name: len(name)):
      print (name)
```

---


---

Explain list comprehensions. Give examples and show equivalents with `map` and `filter`. How do their capabilities compare? Also demonstrate set comprehensions and dictionary comprehensions.

REPLACE THIS TEXT WITH YOUR RESPONSE

---


Write a Markov text generator, [markov.py](python/markov.py). Your program should be called from the command line with two arguments: the name of a file containing text to read, and the number of words to generate. For example, if `chains.txt` contains the short story by Frigyes Karinthy, we could run:

```bash
./markov.py chains.txt 40
```

A possible output would be:

> show himself once more than the universe and what I often catch myself playing our well-connected game went on. Our friend was absolutely correct: nobody from the group needed this way. We never been as the Earth has the network of eternity.

There are design choices to make; feel free to experiment and shape the program as you see fit. Jeff Atwood's [Markov and You](http://blog.codinghorror.com/markov-and-you/) is a fun place to get started learning about what you're trying to make.
