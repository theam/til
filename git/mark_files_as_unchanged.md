Roberto Diaz

# Mark Changed Files as Unchanged

Sometime you have files from a git repo that you modify in your local but you don't want to push your changes. There is
a simple way to tell git to ignore the changes done in those files with the following command:

```
git update-index --assume-unchanged gradle.properties
```
