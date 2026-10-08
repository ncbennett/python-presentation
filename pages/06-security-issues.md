# Security Issues

- Your code
- Your supply chain
- Your runtime environment

<!--
- For the most part, Python is a secure programming language. 
- But, like any other programming language, it inevitably has some security vulnerablities.
- There are basically three types of Python security risks: your code, your supply chain, and your runtime environment.
-->

---

# Security Issues

### Your code

- eval() and exec()
- Unsafe:

```python {lines:true}

```

- Safe:

```python {lines:true}

```

<!--
- Python's eval and exec functions execute whatever you pass to them without checking if it is valid or safe.
- If you ever take user input and pass it to one of these functions, you must check whether it is correct first.
-->

---

# Security Issues

### Your supply chain

- Dependencies

<!--
- If any of the packages you use in your project has a vulnerability, that gets passed on to you.
- You can mitigate this threat by frequently updating you dependencies.
- Most packages patch security vulnerabilities quickly.
-->

---

# Security Issues

### Your runtime environment

- Update Python to the latest version

<!--
- Old Python versions often contain security vulnerabilies.
- Make sure you're running the latest patched version.
-->
