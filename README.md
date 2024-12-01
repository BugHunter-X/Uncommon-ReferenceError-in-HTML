# Uncommon ReferenceError in HTML
This repository demonstrates an uncommon way a `ReferenceError` can occur in HTML due to inline JavaScript attempting to use an undeclared variable.  This can be confusing to debug as it might not be immediately obvious which variable is causing the problem, especially in larger HTML files.

## Bug Description
The bug is caused by the following line of inline JavaScript:
```javascript
document.getElementById("myParagraph").innerHTML = someVariableThatDoesNotExist;
```
The variable `someVariableThatDoesNotExist` has not been declared, leading to a `ReferenceError` when the JavaScript is executed.

## Solution
The solution is to declare and initialize the variable before using it: