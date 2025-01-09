# Groovy Null Input Handling Bug

This repository demonstrates a common, yet subtle, bug in Groovy related to handling null input in methods.  The `myMethod` function returns 0 when a null parameter is passed, which could mask a more significant issue or lead to unexpected program behavior. 

The `bug.groovy` file contains the buggy code. The `bugSolution.groovy` file provides a corrected version.

## Bug Description
The `myMethod` function implicitly handles null input by returning 0.  While seemingly harmless, this behavior can obscure errors and make debugging difficult. A more robust solution would be to either explicitly throw an exception or return a more informative value (e.g., null or a specific sentinel value).