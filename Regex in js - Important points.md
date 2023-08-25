#regex 
1. Regular expressions (regex) are patterns used to match, search, and manipulate text.
    
2. In JavaScript, regular expressions are represented by objects. You can ==create a regular expression== object using the `RegExp` constructor or by using regex literal notation, which is ==enclosed in forward slashes (`/`).==
    
3. Regular expression literals in JavaScript are ==written between two slashes (`/`)== and can include ==modifiers after the closing slash to control how the pattern is matched.==
    
4. Regular expressions have various metacharacters and special characters that allow you to define complex patterns. Examples include `.` (matches any single character except newline), `*` (matches zero or more occurrences of the preceding element), `+` (matches one or more occurrences of the preceding element), `?` (matches zero or one occurrence of the preceding element), and more.
    
5. To perform operations with regular expressions, JavaScript provides methods like `test()`, `exec()`, `match()`, `search()`, `replace()`, and `split()`.
    
6. The `test()` method returns a boolean value indicating whether a match is found or not.
    
7. The `exec()` method searches a string for a match and returns an array containing information about the match.
    
8. The `match()` method searches a string for a match and returns an array of matches.
    
9. The `search()` method searches a string for a specified pattern and returns the index of the first match.
    
10. The `replace()` method searches a string for a specified pattern, replaces it with a replacement string, and returns the modified string.
    
11. The `split()` method splits a string into an array of substrings based on a specified separator and returns the array.
    
12. Regular expressions support various modifiers or flags, such as `g` (global match), `i` (case-insensitive match), `m` (multiline match), and more.
    
13. Regular expressions can include character classes like `\d` (matches any digit), `\w` (matches any alphanumeric character), `\s` (matches any whitespace character), and more.
    
14. You can use quantifiers like `{n}` (matches exactly n occurrences), `{n,}` (matches n or more occurrences), `{n,m}` (matches between n and m occurrences), and others.
    
15. Parentheses can be used for grouping and capturing parts of a pattern. Captured groups can be referenced later using backreferences.
    
16. Regular expressions also support various predefined shorthand character classes like `\d` (digits), `\w` (word characters), `\s` (whitespace characters), `\b` (word boundaries), and more.
    
17. Regular expressions can be combined using logical operators such as `|` (OR), `[...]` (character set), and `(...)` (grouping).
    
18. JavaScript provides the `RegExp` object's properties, such as `source` (returns the text of the pattern), `flags` (returns the flags used in the regular expression), and more.