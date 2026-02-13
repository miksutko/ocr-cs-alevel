# Modularity
- Modularity means breaking a program into **subroutines** so repeated or complex parts are handled in one place.
- A **subroutine** is a named block of code that performs a specific task.
# Function vs procedure (OCR style)
- **Function**: returns a value back to the caller.
- **Procedure**: does not return a value (it may still output/display results).
# Parameters and arguments
- **Parameters** are the named inputs in the subroutine definition.
- **Arguments** are the actual values passed in when calling it.
## Parameter passing: by value vs by reference

### Pass by value
- The subroutine receives a **copy** of the variable’s value.
- Changes inside the subroutine **do not affect** the original variable. 
### Pass by reference
- The subroutine receives the **address/reference** to the original variable.
- Changes inside the subroutine **do affect** the original variable (similar risk to globals).