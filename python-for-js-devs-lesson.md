```markdown
# Python for JavaScript Developers: Syntax and Basics

## 1. Python Syntax Basics

### 1.1 Indentation vs. Curly Braces

Python uses indentation to define code blocks, unlike JavaScript's curly braces `{}`. This makes the code more readable but requires careful attention to spacing.

Python:
```

```python
def greet(name):
    if name:
        print(f"Hello, {name}!")
    else:
        print("Hello, world!")
```

```markdown
JavaScript:
```

```javascript
function greet(name) {
  if (name) {
    console.log(`Hello, ${name}!`)
  } else {
    console.log('Hello, world!')
  }
}
```

```markdown
### 1.2 Printing Output

Python uses the `print()` function, while JavaScript uses `console.log()`.

Python:
```

```python
print("Hello, world!")
```

```markdown
JavaScript:
```

```javascript
console.log('Hello, world!')
```

```markdown
### 1.3 Comments

Single-line comments in Python start with `#`, while in JavaScript they start with `//`.

Python:
```

```python
# This is a single-line comment in Python
```

```markdown
JavaScript:
```

```javascript
// This is a single-line comment in JavaScript
```

```markdown
Multi-line comments in Python use triple quotes `'''` or `"""`, while JavaScript uses `/* */`.

Python:
```

```python
'''
This is a multi-line
comment in Python
'''
```

```markdown
JavaScript:
```

```javascript
/*
This is a multi-line
comment in JavaScript
*/
```

```markdown
## 2. Functions in Python

### 2.1 Defining Functions

Python uses the `def` keyword to define functions, while JavaScript uses the `function` keyword.

Python:
```

```python
def greet(name):
    return f"Hello, {name}!"
```

```markdown
JavaScript:
```

```javascript
function greet(name) {
  return `Hello, ${name}!`
}
```

```markdown
### 2.2 Function Parameters and Default Arguments

Both Python and JavaScript support default arguments, but the syntax differs slightly.

Python:
```

```python
def greet(name="World"):
    return f"Hello, {name}!"

print(greet())  # Output: Hello, World!
print(greet("Alice"))  # Output: Hello, Alice!
```

```markdown
JavaScript:
```

```javascript
function greet(name = 'World') {
  return `Hello, ${name}!`
}

console.log(greet()) // Output: Hello, World!
console.log(greet('Alice')) // Output: Hello, Alice!
```

```markdown
### 2.3 Return Statements

Return statements work similarly in both languages, but Python doesn't require parentheses.

Python:
```

```python
def add(a, b):
    return a + b
```

```markdown
JavaScript:
```

```javascript
function add(a, b) {
  return a + b
}
```

```markdown
### 2.4 Key Differences from JavaScript Functions

1. No `function` keyword in Python
2. Indentation defines the function body in Python, not curly braces
3. Python uses dynamic typing, so you don't need to declare parameter types

## 3. Control Flow Statements

### 3.1 Conditional Statements

Python uses `if`, `elif`, and `else`, while JavaScript uses `if`, `else if`, and `else`.

Python:
```

```python
x = 10
if x > 15:
    print("x is greater than 15")
elif x > 5:
    print("x is greater than 5 but not greater than 15")
else:
    print("x is 5 or less")
```

```markdown
JavaScript:
```

```javascript
let x = 10
if (x > 15) {
  console.log('x is greater than 15')
} else if (x > 5) {
  console.log('x is greater than 5 but not greater than 15')
} else {
  console.log('x is 5 or less')
}
```

```markdown
### 3.2 Logical Operators

Python uses `and`, `or`, and `not`, while JavaScript uses `&&`, `||`, and `!`.

Python:
```

```python
if x > 0 and x < 100:
    print("x is between 0 and 100")

if not (x < 0 or x > 100):
    print("x is between 0 and 100")
```

```markdown
JavaScript:
```

```javascript
if (x > 0 && x < 100) {
  console.log('x is between 0 and 100')
}

if (!(x < 0 || x > 100)) {
  console.log('x is between 0 and 100')
}
```

```markdown
### 3.3 Best Practices

- Use clear and descriptive variable names
- Keep indentation consistent (usually 4 spaces in Python)
- Use parentheses to group complex logical expressions for clarity

## 4. f-Strings in Python

f-Strings provide a concise and readable way to embed expressions inside string literals.

### 4.1 Basic Syntax

Python:
```

```python
name = "Alice"
age = 30
print(f"My name is {name} and I am {age} years old.")
```

```markdown
JavaScript (template literals):
```

```javascript
let name = 'Alice'
let age = 30
console.log(`My name is ${name} and I am ${age} years old.`)
```

```markdown
### 4.2 Formatting Numbers and Dates

Python has a built-in datetime module to format dates.

Python:
```

```python
import datetime

pi = 3.14159
today = datetime.date.today()

print(f"Pi is approximately {pi:.2f}")
print(f"Today's date is {today:%B %d, %Y}")
```

```markdown
JavaScript:
```

```javascript
let pi = 3.14159
let today = new Date()

console.log(`Pi is approximately ${pi.toFixed(2)}`)
console.log(
  `Today's date is ${today.toLocaleDateString('en-US', {
    month: 'long',
    day: 'numeric',
    year: 'numeric',
  })}`
)
```

```markdown
### 4.3 Comparison with Other String Formatting Methods

Python offers multiple ways to format strings:

1. f-Strings (Python 3.6+)
2. str.format() method
3. % operator (older style)

Example using different methods:
```

```python
name = "Alice"
age = 30

# f-String
print(f"{name} is {age} years old.")

# str.format()
print("{} is {} years old.".format(name, age))

# % operator
print("%s is %d years old." % (name, age))
```

```markdown
f-Strings are generally preferred for their readability and performance.

Try these [Exercises](exercises.ipynb) to test your understanding of what you've just learned.
```
