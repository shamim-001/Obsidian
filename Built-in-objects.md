#js-concept #built-in-objects 
JavaScript built-in objects are accessible regardless of the contents of the window and operate independently of the page that your browser has loaded.

## Introduction

- JavaScript Built-in objects have nothing to do with the Window or DOM object models.
- JavaScript built in objects can be used for basic data processing.
- Array, String, and **Date/Time** are all JavaScript Built-in Objects.
- A JavaScript Built-in object is a set of named values in JavaScript.

**Javascript Built in Objects are divided into two groups.**

1. Standard Objects
2. Other Built-in objects

![classification of built in objects in JavaScript](https://scaler.com/topics/images/javascript-built-in-objects-1.webp)

## Standard Objects by Category

**Standard Built-in Objects**: The terminology "standard built-in objects" (also known as "global built-in objects") should not be confused with "standard objects." Objects in the global scope are referred to as "standard objects" in this context.

In the global scope, this operator can be used to access the standard object. The global scope, in reality, is made of the properties of the standard object, including any inherited properties.

![standard built-in objects](https://scaler.com/topics/images/standard-built-in-objects.webp)

### Numbers and Dates:

These foundation objects represent numbers, dates, and mathematical calculations.

![numbers and dates in built in objects](https://scaler.com/topics/images/numbers-and-dates-in-built-in-objects.webp)

**1. Number:**

- The Number objects represents numerical date, either integers or floating-point numbers.
- Number objects are created using the Number() constructor and contains Constants and methods.
- Number() function can convert values of different types to numbers.

**Syntax**:

```javascript
var num = new number(value);
```

**Properties of Number object**:

|Properties|Description|
|---|---|
|Constructor|The function that created the Number object is returned.|
|MAX VALUE|In JavaScript, this method returns the smallest number value possible.|
|MIN VALUE|In JavaScript, this method returns the smallest feasible numerical value.|
|NEGATIVE INFINITY|Negative infinity's value is represented.|
|POSITIVE INFINITY|Represent the value of infinity.|
|Prototype|An object's properties and methods can be added.|

**Methods of Number object**:

|Method()|Description|
|---|---|
|toExponential()|A number is converted to exponential notation.|
|toFixed()|Formats a number to the right of the decimal point with a given amount of digits.|
|toLocaleString()|Returns a string value version of the current number in a format that varies depending on the locale settings of the browser.|
|toPrecision()|Defines how many total digits a number should be displayed with.|
|toString()|The string representation of the number's value is returned.|
|valueOf()|Returns the value of the number.|

**2. BigInt:**

- BigInt is a primitive wrapper object for representing and manipulating primitive bigint values that are too large for the number primitive to handle.
- A BigInt objects are created using the BigInt() constructor.
- A BigInt value, sometimes known as just a BigInt, is a bigint primitive that can be generated by appending n to the end of an integer literal or by invoking the BigInt() function Object and passing it an integer or string value.

**Properties of BigInt object**:

|Properties|Description|
|---|---|
|Constructor|The function that created the BigInt object is returned.|
|Prototype|An object's properties and methods can be added.|

**Methods of BigInt object**:

|Method()|Description|
|---|---|
|asIntN()|Clamps and returns a signed integer value from a BigInt value.|
|asUintN()|Returns a BigInt value that has been clamped to an unsigned integer value.|
|toLocaleString()|This BigInt value is returned as a string with a language-sensitive representation. Overrides the Object.prototype.toLocaleString() method.|
|toString()|This BigInt value is represented as a string in the specified radix (base). Overrides the Object.prototype.toString() method.|
|valueOf()|Returns this BigInt value.|

**3. Math:**

- The Math object is used to execute simple and complicated arithmetic operations on Number values. It isn't even a function object.
- A Math objects are created using the Math() constructor.
- There are no constructors on the Math object. All of the Math object's methods and properties are static, meaning they are member functions of the Math object. There is no method to generate a Math object instance.

**Properties of Math object**:

|Properties|Description|
|---|---|
|PI|Pi's value, approximately 3.14159.|
|E|This property is utilized for the natural logarithm e's base, approximately 2.718.|
|LN2|The natural logarithm of 2 has this property, approximately 0.693.|
|LN10|The Natural logarithm of 10 has this property, approximately 2.303.|
|LOG2E|This property is used to calculate the base 2 logarithm of e, approximately 1.443 .|
|LOG10E|This property is used to calculate the base 10 logarithm of e, approximately 0.434 .|
|SQRT2|This property is used to calculate the square root of 2, approximately 1.414.|
|SQRT1_2|This property is used to calculate the square root of ½, approximately 0.707|

**Methods of Math object**:

|Method()|Description|
|---|---|
|max(x,y)|The largest of x and y is returned.|
|min(x,y)|The least of x and y is returned.|
|round(x)|The nearest integer is returned.|
|ceil(x)|Rounds up. The lowest integer greater than or equal to x is returned.|
|floor(x)|Rounds down. The greatest integer less than or equal to x is returned.|
|exp(x)|Returns e^x, with x being the argument and e being Euler's constant (2.718..., the natural logarithm's base).|
|pow(x,y)|Returns x^y|
|abs(x)|Returns absolute value of x.|
|random()|Returns an integer between 0 and 1 that is pseudo-random.|
|sqrt(x)|Returns square root of x.|
|sin(x)|Returns sin of x (x is in radians).|
|cos(x)|Returns cosine of x (x is in radians).|
|tan(x)|Returns tangent of x (x is in radians).|
|sinh(x)|Returns the hyperbolic sine of x (x is in radians).|
|cosh(x)|Returns the hyperbolic cosine of x (x is in radians).|
|tanh(x)|Returns the hyperbolic tangent of x (x is in radians).|

**4. Date:**

- When users require access to the present date and time, as well as previous and future dates and times. The Date object in JavaScript provides support for working with dates and times.
- A Date objects are created using the Date() constructor.
- The Date object abstracts dates and times in a system-independent way.
- Dates can be compared and converted to a readable string format as well. Millisecond precision is used to indicate a date.

**Syntax**:

```javascript
var today = new Date( );
```

**Properties of Date object**:

|Properties|Description|
|---|---|
|Constructor|The function that created the Date object is returned.|
|Prototype|An object's properties and methods can be added.|

**Methods of Date object**:

|Method()|Description|
|---|---|
|Date()|Returns the current date and time.|
|getDate()|The day of the month for the specified date is returned.|
|getDay()|The day of the week for the specified date is returned.|
|getFullYear()|The year of the specified date is returned.|
|getHours()|Returns the hour in local time for the specified date.|
|getMinutes()|According to local time, returns the minutes (0–59) in the specified date.|
|getSeconds()|According to local time, returns the seconds (0–59) in the specified date.|
|getMilliseconds()|According to local time, this function returns the milliseconds in the specified date.|

### Text Processing:

These objects represent strings and allow them to be manipulated.

![JS built in objects text processing](https://scaler.com/topics/images/js-built-in-objects-text-processing.webp)

**1. String:**

- In JavaScript, instances of the String object are used to represent all strings. A member of global objects, String is a wrapper class.
- A String objects are created using the String() constructor.
- It's used to do things like determining how long a string is, searching for specific characters inside it, extracting a substring, and so on.
- Single quotes(' ') or double quotes(" ") are used to enclose string literals.

**Syntax**:

```javascript
var variable_name = new String(string);
```

**Properties of String object**:

|Properties|Description|
|---|---|
|Length|The length of a string is returned.|
|Constructor|The function that created the String object is returned.|
|Prototype|An object's properties and methods can be added.|

**Methods of String object**:

|Method()|Description|
|---|---|
|charAt()|The character at the specified position is returned.|
|toLowerString()|This method converts all character of a string to lowercase.|
|toUpperString()|This method converts all characters of a string to uppercase.|
|concat()|This function joins two or more strings together.|
|indexOf(searchtext, index)|Searches for the provided string from the beginning of the string.|
|lastIndexof(searchtext, index)|Searches for the provided string from the end of the string.|
|raw()|Returns a string constructed from a template string in its raw form.|

**2. RegExp:**

- The RegExp object is used to validate a character pattern.
- A RegExp objects are created using the RegExp() constructor.
- RegExp defines methods for performing powerful pattern matching and search and replace functions on text using regular expressions.
- The following methods can be used to define regular expressions.
    - Using RegExp() Constructor: var RegularExpression = new RegExp(“pattern”,”flag”);
    - Using Literal: var RegularExpression = /pattern/flag;

Pattern: A string describing the regular expression's or another regular expression's pattern.  
Flag: An optional string comprising any of the "g", "I", and "m" characteristics, which respectively specify global, case-insensitive, and multiple matches.

**Properties of RegExp object**:

|Properties|Description|
|---|---|
|Constructor|The function that created the RegExp object is returned.|
|Global|Checks if the "g" modifier is set.|
|ignoreCase|Checks if the I modifier is set.|
|lastIndex|Sets the index at which the next match will begin.|
|multiline|Checks if the "m" modifier is set.|
|source|The RegExp pattern's text is returned.|
|sticky|Whether the search is sticky or not.|
|unicode|Whether Unicode features are enabled or not.|

**Methods of RegExp object**:

|Method()|Description|
|---|---|
|exec()|This function looks for a match in a string and Then first match is returned.|
|test()|This function looks for a match in a string. True or false is returned.|
|toSource()|The specified object is represented by an object literal.|
|toString()|The regular expression's string value is returned.|
|compile()|During the execution of a script, recompiles a regular expression.|

### Fundamental Objects:

These are the foundational, fundamental objects that all other objects are built upon. General objects, booleans, functions, and symbols are all included.

![fundamental objects](https://scaler.com/topics/images/fundamental-objects.webp)

**1. Object:**

- One of JavaScript's data types is represented by the Object class. It stores a variety of keyed collections as well as more complex entities. The Object() constructor or the object initializer / literal syntax can be used to build objects.
- A Object objects are created using the Object() constructor.
- Object operates exactly like a new Object() when invoked in a non-constructor context.

The Object constructor constructs an object wrapper for the given value.

- When the value is null or undefined, it will create and return an empty object.
- If the value already exists as an object, it will return it.
- Otherwise, it will return an object of the value's Type.

**Properties of Object object**:

|Properties|Description|
|---|---|
|Constructor|Specifies the function that builds the prototype of an object.|
|proto|This property refers to the object that was used as a prototype when the object was created.|

**Methods of Object object**:

|Method()|Description|
|---|---|
|assign()|Copies all enumerable own properties' values from one or more source objects to a target object.|
|create()|The prototype object and its properties are used to create a new object.|
|entries()|Returns an array containing all of the [key, value] pairs of the enumerable string properties of a specified object.|
|freeze()|An object is frozen. Its properties can't be changed or deleted by other code.|
|is()|When two values are compared, it is determined whether they are the same. All NaN values are equated in this function (which differs from both Abstract Equality Comparison and Strict Equality Comparison).|
|keys()|Returns an array containing the names of all the enumerable string properties of the specified object.|
|seal()|Prevents other code from deleting an object's properties.|
|toString()|Returns the object's string representation.|
|values()|Returns an array holding the values for all of the enumerable string properties of a specified object.|

**2. Function:**

- A Function object is the basis of every JavaScript function.
- A Function objects are created using the Function() constructor.
- The Function constructor is used to create functions that only run in the global scope.

**Properties of Function object**:

|Properties|Description|
|---|---|
|length|The number of arguments the function expects is specified here.|
|displayName|The function's displayed name.|
|caller|The function that called the one that is currently running. This property is no longer used and is only used for non-strict functions.|
|name|The name of the function.|
|arguments|The arguments passed to a function are represented as an array. As a Function property, this is deprecated.|

**Methods of Function object**:

|Method()|Description|
|---|---|
|toString()|Returns a string containing the function's source code. Overrides the Object.prototype.toString method.|
|call(thisArg[, arg1, arg2, ...argN])|This is set to the specified value when a function is called. Arguments can be passed in their current state.|
|bind(thisArg[, arg1[, arg2[, ...argN]]])|Creates a new function whose this is set to the specified thisArg when it is called. If the newly-bound function is called, a given sequence of arguments can be prepended to the arguments.|
|apply(thisArg [, argsArray])|ThisArg is set to the given thisArg when a function is called. Array objects can be used to pass arguments.|

**3. Boolean:**

- The Boolean object is a wrapper class for global objects and a member of them.
- A Boolean objects are created using the Boolean() constructor.
- It converts a non-Boolean value into a Boolean value (true or false).
- The object is set to false if it has no initial value or if it is 0, -0, null, "", false, undefined, or NaN. Otherwise, it's true (even with the string "false")

We can create Boolean object by using below methods:

- By using Boolean Literal Notation: var bool = true;
- By using Boolean Object as Function: var bool = Boolean(true);
- By using Testable Expressions: if(true) {………….}

**Properties of Boolean object**:

|Properties|Description|
|---|---|
|Constructor|The function that created the Boolean object is returned.|
|Prototype|An object’s properties and methods can be added.|

**Methods of Boolean object**:

|Method()|Description|
|---|---|
|toSource()|The source of the Boolean object is returned as a string; you can use this string to create an equivalent object.|
|valueOf()|The primitive value of the Boolean object is returned.|
|toString()|Depending on the object's value, returns a string that is either "true" or "false."|

**4. Symbol:**

- Symbols are frequently used to add unique property keys to an object that won't conflict with keys added by other code and that are hidden from any mechanisms used by other code to access the object.
- A Symbol object are created using the Symbol() constructor.
- We write Symbol() with an optional string as its description to create a new primitive Symbol

**Properties of Symbol object**:

|Properties|Description|
|---|---|
|asyncIterator|A method that returns an object's default AsyncIterator.  Used by for await...of.|
|hasInstance|A method for checking if a constructor object recognizes an object as an instance. Used by instanceof.|
|match|A technique for determining if an object may be used as a regular expression by matching it against a string.|
|species|A constructor function for creating derived objects.|
|toPrimitive|A method for converting a primitive value from an object.|
|unscopables|An object value whose own and inherited property names are not included in the related object's with environment bindings.|
|search|The index within a string that matches the regular expression is returned by this method. Used by String.prototype.search().|
|split|A method for splitting a string at indices matching a regular expression. Used by String.prototype.split().|
|matchAll|A method that returns an iterator containing regular expression matches against a string. Used by String.prototype.matchAll().|

**Methods of Symbol object**:

|Method()|Description|
|---|---|
|for(key)|If any existing Symbols with the specified key are identified, they are returned. If not, a new Symbol with key is created in the global Symbol registry.|
|keyFor(sym)|Retrieves a shared Symbol key for the specified Symbol from the global Symbol registry.|
|toString()|Returns a string giving the Symbol's description. Overrides the Object.prototype.toString() method.|

## Conclusion

- Standard JavaScript Built in objects can be used for basic data processing.
- There are mainly two types of JavaScript Built in Objects: Standard Built-in Objects and other Built-in Objects.
- Javascript Built-in objects includes properties and methods.
- Except for primitives, all JavaScript values are objects.