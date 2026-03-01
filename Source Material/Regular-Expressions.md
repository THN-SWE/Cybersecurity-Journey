- I think Reg-Ex is more interesting and innovative. such a great idea. 

#### Quick History
> Fill it later.....

- Regular expressions have **two common forms: basic and extended**
-  Most commands that use regular expressions can interpret basic regular expressions.
- Extended regular expressions are not available for all commands.

#### Basic Reg-Ex

| Basic Regex Character(s) | Meaning                                                                                                                 |
| ------------------------ | ----------------------------------------------------------------------------------------------------------------------- |
| `.`                      | Any one single character                                                                                                |
| `[ ]`                    | Any one specified character                                                                                             |
| `[^ ]`                   | Not the one specified character - start of the line                                                                     |
| `*`                      | Zero or more of the previous character                                                                                  |
| `^`                      | If first character in the pattern, then pattern must be at beginning of the line to match, otherwise just a literal `^` |
| `$`                      | If last character in the pattern, then pattern must be at the end of the line to match, otherwise just a literal `$`    |

>  To Use extended Reg-Ex commands you need to use `grep -E` OR `egrep` command. 

