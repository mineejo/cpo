# Output format - character, program, output (CPO)

<p align="center">
  <img alt="Example" src="./assets/example.svg"/>
</p>

This format tries to standardize the console data output for a project. It is simple and informative at the same time. It is not a log format, but for information like any error where the log is redundant and the raw output is not properly thrown.

## Basic design

<p align="center">
  <img alt="Example" src="./assets/design.svg"/>
</p>

### Rules

1. The `STARTCHARACTER` is optional
2. There must be a space after the `STARTCHARACTER`
3. The `PROGRAM` must be written with capital letters
4. There must be a colon a space after `PROGRAM`
5. Separators, such as spaces or colons, should be the color of a text
6. Keywords should be highlighted or underlined
7. `PROGRAM` can contain spaces

You can check your output using a regular expression.
The expression does not analyze design subtleties!

```regexp
/(^.( ))?([A-Z-0-9 ]+(:)( ))(.*)/gm
```

## FAQ

### Why use it?

By choosing CPO, you can save time and effort by not thinking about another beautiful design that won't seem so beautiful tomorrow.

### How to use it?

CPO is the set of rules by which data is formatted. You don't need anything other
than the way the data is output to the console. But you can use third-party
packages for ASCII colors, etc. for convenience.
