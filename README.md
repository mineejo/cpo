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
2. The `PROGRAM` parameter is optional if there is `STARTCHARACTER`
3. There must be a space after the `STARTCHARACTER`
4. There must be a colon a space after `PROGRAM`
5. `PROGRAM` must be written with capital letters
6. `PROGRAM` must contain spaces
7. `PROGRAM` must not contain special characters
8. Keywords should be highlighted or underlined

You can check your output using a regular expression.
The expression does not analyze design subtleties!

```regexp
/(^.( ))?([a-zA-Z-0-9 ]+(:)( ))?(.*)/gm
```

### Example

```
× STRANGE ERROR: Something's wrong...
```

```
✓ It's okay
```

## FAQ

### Why use it?

By choosing CPO, you can save time and effort by not thinking about another beautiful design that won't seem so beautiful tomorrow.

### How to use it?

CPO is the set of rules by which data is formatted. You don't need anything other
than the way the data is output to the console. But you can use third-party
packages for ASCII colors, etc. for convenience.
