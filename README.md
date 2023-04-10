# Output format - character, program, output (CPO)

<center>
    <img alt="Example" src="./assets/example.svg"/>
</center>

This format tries to standardize the console data output for the project. It is simple and informative at the same time. It is not a log format, but for information like any error where the log is redundant and the raw output is not properly thrown.

## Basic design

<center>
    <img alt="Example" src="./assets/design.svg"/>
</center>

1. The `STARTCHARACTER` is optional
2. There must be a space after the `STARTCHARACTER`
3. The `PROGRAM` must be written with capital letters
4. There must be a colon a space after `PROGRAM`
5. Separators, such as spaces or colons, should be the color of a text
6. Keywords should be highlighted or underlined

You can check your output using a regular expression.
The expression does not analyze design subtleties!

```regexp
/(^.( ))?([A-Z-0-9]+(:)( ))(.*)/gm
```
