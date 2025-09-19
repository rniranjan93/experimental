# C Programming Coding Guidelines

This document lists the coding guidelines that shall be followed when writing software programs using C. The suggested examples provided in this document are related to a generic C library.

## 1. Names

Names should give useful information of the variable or function.

### 1.1 Variables

- Use meaningful names
- Important API level and global variables shall be prefixed with `lib_`
- Use underscores to separate words in a name
- Stick to lower case
- Local variable names can be shorter and their purpose can be explained with comments
- Place the `*` close to the variable name not pointer type
- Include units in variable names – eg: `timeout_msecs`
- Pointers shall be prefixed with `p_` & function pointers shall be suffixed with `_fp`
- Use `const` keyword everywhere applicable

### 1.2 Functions

- Prefix all the interface APIs with `lib_`
- Sometimes, concrete module level interface APIs can be prefixed with `modulename_`
- Make function names as verbs that perform an action to distinguish them from data objects. For Example: Use `check_for_errors()` instead of `error_check()`
- Function parameter order: inputs, then outputs

### 1.3 Macros and Global Constants

- Use upper case with "_" separators
- Important API level and global variables/macros/constants shall be prefixed with `lib_`
- Wrap the macro expression in parenthesis to avoid wrong order of operations
- In case a macro definition is quite big, consider using an inline function provided there are no performance side-effects

### 1.4 Enums

- Use upper case with "_" separators for all the labels
- Important API level and global enums shall be prefixed with `lib_`

### 1.5 Structures

- Use lower case with "_" separators for the structure names
- Important API level structures shall be prefixed with `lib_`
- Organize the member variables in the structure in the decreasing order of their sizes to minimize memory alignment issues

## 2. Formatting

- Maintain 80 chars a line
- Use the braces form where the open brace starts in the new lineExpand commentComment on line R49ResolvedCode has comments. Press enter to view.
- For one-liner if or loop constructs, it can be in the same line
- Always enclose if or loop constructs with curly braces. Add comments to the closing braces only for multi-line blocks or complex/nested structures where the closing brace's purpose might be unclear
- Variable declarations shall be followed by a new line to separate them from the rest of the code
- No space should be added after the type and the variable when typecasting it
- Always initialize the variables
- Use header file guards to avoid multiple inclusions
- One statement per line
- One variable defined per line
- Try to avoid goto statements. But, when it is really necessary, write good comments and place the label to the left of the code that follows
- Leave a space between if/while & (
- System headers followed by project specific headers

## 3. Comments

- Write a brief comment (in doxygen style) at the start of each source file about the overall purpose of the file
- Write comments (in doxygen style) for each function providing details about what the function does, what are its arguments along with the possible values/range of arguments and their meanings, and what are the return values/codes of this function
- Write comments (in doxygen style) for macros and enums
- Write comments (in doxygen style) for important variables including the global variable
- Write comments (in doxygen style) for important structures
- Write comments for every `#endif`
- Write elaborate comments for function or code section in a function that needs explanation about the algorithmic steps or strategies adopted
- Comments shall not exceed 80 chars
