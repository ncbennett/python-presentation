# Security Issues

- Your code
- Your supply chain
- Your runtime environment

<!--
- For the most part, Python is a secure programming language. 
- But, like any other programming language, it inevitably has some security vulnerablities.
- There are basically three groups of Python security risks: your code, your supply chain, and your runtime environment.
-->

---


# Security Issues

### Your Code

**Unsafe:**

```python {lines:true}
age = eval(input("Enter your age: "))
```

**Safe:**

```python {lines:true}
age = int(input("Enter your age: "))
```

<!--
- Python has two particularly powerful built-in functions, eval() and exec(), that execute Python code.
- However, they don't check if that code is valid or safe, so passing untrusted user input to either function could cause vulnerabilites.
- In this example, eval() treats the user's input as Python code.
- The correct method would be to use int() to attempt to convert the input into an integer without executing it as Python code.
- While this could lead to a ValueError, it could be handled gracefully.
-->

---


# Security Issues

### Your Supply Chain

<v-clicks>

- Vulnerable or malicious dependencies
- Regularly update dependencies
- Audit packages for vulnerabilities

</v-clicks>

<!--
- Python has a huge third-party package ecosystem, but the use of external code will always expose you to security risks.
- A vulnerability in one of your dependencies, including its own dependencies, could cause your app to become vulnerable.
- Attackers can also publish malicious packages, sometimes using names similar to popular packages, to try to trick users to download them.
- To reduce these risks, use trustworthy packages, keep dependencies updated, and scan for known vulnerabilities.
- Tools like pip-audit can identify known vulnerabilities in installed Python packages.
-->

---


# Security Issues

### Your Runtime Environment

<v-clicks>

- Keep Python updated
- Use supported Python versions

</v-clicks>

<!--
- Python can contain security vulnerabilities, just like any other language runtime.
- Supported versions receive security patches, while end-of-life versions no longer receive them.
- You should keep both Python updated.
-->
