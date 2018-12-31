## See folder structure as tree on your mac:

Install tree app using Homebrew:
```
brew install tree
```

run `tree` on the terminal to see the complete folder structure. You can limit the recursion by passing a -L flag and specifying the maximum depth.

```
tree

tree -L 2
```

## Use ack to search your code

Install ack app using Homebrew:
```
brew install ack
```

**How to use:**
```
ack [OPTION]... PATTERN [FILES OR DIRECTORIES]

ack --js sauce
```
