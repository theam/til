Nick Tchayka

# Replace a string in all files

Sometimes, we want to replace a symbol in all files, like when doing a major rename.

It is very useful to have this simple helper command that allows doing it easily:

```bash
function replaceall {
  find ./ -type f -exec sed -i "s/$1/$2/g" {} \;
}
```
