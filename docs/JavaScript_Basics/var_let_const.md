## DIFFERENCE BETWEEN VAR,LET AND CONST

###### VAR

* The scope of a variable declared with var is its current execution context.
* The scope is either the enclosing function or, for variables declared outside any function,the scope is global.
* var variables can be re-declared and updated.

* **Example**:

    ```
    var greeter = "hey hi";

    if (times > 3) {
        var greeter = "say Hello instead"; 
    }

    console.log(greeter) //"say Hello instead"**
    ```

###### LET

* let is block scoped
* A block is chunk of code bounded by {}.
* A block lives in curly braces.Anything within curly braces is a block.So a variable declared in a block with the let is only available for use within that block

* **Example**:

    ```
    let greeting = "say Hi";
    
    if (true) {
        let greeting = "say Hello instead";
        console.log(greeting); //"say Hello instead"
    }
    
    console.log(greeting); //"say Hi"
    ```
    
###### CONST

* Variables declared with the const maintain constant values. const declarations share some similarities with let declarations.
* const declarations are block scoped.
* const cannot be updated or re-declared

* **Example**: 
  ```
  const greeting = "say Hi";
  greeting = "say Hello instead"; //error : Assignment to constant variable.
  const greeting = "say Hello instead"; //error : Identifier 'greeting' has already been declared
  ```

## KEY POINTS:

### VAR
* var variables can be re-declared and updated.
* **HOISTING OF VAR**
  * Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution.
    What this means is that if we do this:
    
    ```
    console.log (greeter);
    var greeter = "say hello"
    ```
    **It is interpreted is:**
    
    ```
    var greeter;
    console.log(greeter); //greeter is undefined
    greeter = "say hello"
    ```
    ###### So var variables are hoisted to the top of its scope and initialized with a value of undefined.

### LET
* let can be updated but not re-declared.
* **HOISTING OF LET**
  
  * Just like var, let declarations are hoisted to the top. Unlike var which is initialized as undefined, 
    the let keyword is not initialized. So if you try to use a let variable before declaration, you'll get a Reference Error.


### CONST
* const cannot be updated or re-declared.
* **HOISTING OF CONST**

  * Just like let, const declarations are hoisted to the top but are not initialized.
