#regex #characters 

1. `.` (dot):
    - Matches any single character except newline.
    - Example: `/h.t/` matches "hat", "hot", "hit", etc.
2. `*` (asterisk):
    - Matches zero or more occurrences of the preceding element.
    - Example: `/go*d/` matches "gd", "god", "good", "gooood", etc.
3. `+` (plus):
    - Matches one or more occurrences of the preceding element.
    - Example: `/go+d/` matches "god", "good", "gooood", etc. but not "gd".
4. `?` (question mark):
    - Matches zero or one occurrence of the preceding element.
    - Example: `/go?d/` matches "gd" and "god" but not "good".
5. `[]` (square brackets):
    - Matches any single character from the specified set of characters.
    - Example: `/[aeiou]/` matches any vowel character.
6. `[^]` (caret inside square brackets):
    - Matches any single character not in the specified set of characters.
    - Example: `/[^aeiou]/` matches any non-vowel character.
7. `\` (backslash):
    - Escapes a special character, allowing you to use it as a literal character.
    - Example: `/\./` matches a literal dot (.), not any character.
8. `|` (pipe):
    
    - Acts as an OR operator, matching either the pattern on the left or the pattern on the right.
    - Example: `/cat|dog/` matches either "cat" or "dog".
9. `()` (parentheses):
    
    - Groups expressions together and captures the matched text for later use.
    - Example: `/(ab)+/` matches "ab", "abab", "ababab", etc.
10. `^` (caret):
    
    - Matches the beginning of a line or string.
    - Example: `/^hello/` matches "hello" at the beginning of a line or string.
11. `$` (dollar sign):
    
    - Matches the end of a line or string.
    - Example: `/world$/` matches "world" at the end of a line or string.
12. `{n}` (curly braces):
    
    - Matches exactly `n` occurrences of the preceding element.
    - Example: `/a{3}/` matches "aaa" but not "aa".
13. `{n,}` (curly braces with a comma):
    
    - Matches `n` or more occurrences of the preceding element.
    - Example: `/a{2,}/` matches "aa", "aaa", "aaaa", etc.
14. `{n,m}` (curly braces with comma-separated values):
    
    - Matches between `n` and `m` occurrences of the preceding element.
    - Example: `/a{2,4}/` matches "aa", "aaa", or "aaaa" but not "a" or "aaaaa".