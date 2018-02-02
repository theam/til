Roberto Diaz

# Delete all merged branches in git #
We are always working with pull request and normally we forget to delete branches when they are already merged. In this situation a glorious lush tree is created 🙈. Here is a simple recipe to trip all the branches and maintain your repo tree as clean as possible:

```
git branch -r --merged | egrep -v "(^\*|master|dev)" | sed 's/origin\///' | xargs -n 1 git push --delete origin
```
