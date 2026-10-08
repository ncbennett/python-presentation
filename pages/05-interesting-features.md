# Interesting Features of Python

<div v-click>

### Python Generators 

```python {lines:true}
def reverse(data):
    for index in range(len(data)-1, -1, -1):
        yield data[index]
```

</div>

<!--
- Python Generators are a particularly interesting feature of the language. 
- While they are written like normal functions, they use the yield statement to return data. 
- This small change makes a large difference in performance, however, as generators allow you to load chunks of a file in at a time.
-->

---

# Interesting Features of Python

### Python Decorators

```python {lines:true}
def changecase(func):
  def myinner():
    return func().upper()
  return myinner

@changecase
def myfunction():
  return "Hello Sally"

print(myfunction())
```

<!--
- Python Decorators are another amazing feature of Python. 
- They let you add more behavior to a function without modifying the code by taking in a function as input and returning a new function.
-->

---

# Interesting Features of Python

### Python Dictionary Comprehension

```python {lines:true}
# Some code about dictionaries.
```
<!--
- Python dictionaries are a great example of a language integrating an easy to use and highly flexible hash table as a core data type.
-->
