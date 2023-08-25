#regex #methods 

1. `test()`:
    
    - Method: `regex.test(str)`
    - Returns: `true` if the pattern matches the string, `false` otherwise.
    - Example: `/hello/.test("hello world")` returns `true`.
2. `exec()`:
    
    - Method: `regex.exec(str)`
    - Returns: An array containing information about the match or `null` if no match is found.
    - Example: `/hello/.exec("hello world")` returns `["hello", index: 0, input: "hello world", groups: undefined]`.
3. `match()`:
    
    - Method: `str.match(regex)`
    - Returns: An array of matches or `null` if no match is found.
    - Example: `"hello world".match(/hello/g)` returns `["hello"]`.
4. `search()`:
    
    - Method: `str.search(regex)`
    - Returns: The index of the first match or `-1` if no match is found.
    - Example: `"hello world".search(/world/)` returns `6`.
5. `replace()`:
    
    - Method: `str.replace(regex, replacement)`
    - Returns: A new string with the matched portions replaced by the specified replacement.
    - Example: `"hello world".replace(/world/, "universe")` returns `"hello universe"`.
6. `split()`:
    
    - Method: `str.split(regex)`
    - Returns: An array of sub-strings split based on the specified separator.
    - Example: `"hello world".split(/\s+/)` returns `["hello", "world"]`.