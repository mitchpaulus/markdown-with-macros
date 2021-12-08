# Markdown with Macros

I've found the need that I want the benefit of macros like Latex, but
with the simplicity and convertibility of Markdown. So I'm embarking on
writing a compiler that will take a superset of Markdown and turn it
into plain Markdown.

## Macros

May help to review the current escapable characters:

```
\   backslash
`   backtick
*   asterisk
_   underscore
{}  curly braces
[]  square brackets
()  parentheses
#   hash mark
+   plus sign
-   minus sign (hyphen)
.   dot
!   exclamation mark
```

I'm thinking an individual trigger character, non-ASCII, would work
well. I've liked the λ character for this purpose.

```
λ macroname param1 param2 "Macro string"
```

The second requirement would be an ability to specify the replacements
in text. Here we need some sort of boundary characters, similar to
quotes for strings.

