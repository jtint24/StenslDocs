## Statement Blocks

Statement blocks are groups of statements organized by curly braces. Many statements use statement blocks in order to control their behavior. Statement blocks must begin with the “{” character on the line of the statement which requires the block. If a variable is required to be defined inside the statement block, that is done inside parentheses on the same line as the opening brace. This declaration takes the form of the variable type followed by the variable name. If variables are declared for statement blocks, they may be used within the statements inside the statement blocks. Statement blocks must end with the “}” character on its own line or followed by additional keywords and code blocks if the statement requires them. This is to promote readability and well-formatted code. On that note, it is typical to indent inwards for the statements inside of a statement block.

Statement blocks are used to create self-contained blocks of functionality. This allows for code to be defined and used portably. Because statement blocks are self contained, anything declared inside a statement block can only be accessed or modified from within that block.

Currently, function and class declarations are not supported inside statement blocks. 

Examples of valid statement blocks are below:


```
{
  1+1
  2+2
}

{(int i)
  i=3
}
```


Note that because statement blocks can only appear where they are needed, these blocks alone are not valid Stensl code, but would be valid if attached to a corresponding statement. 
