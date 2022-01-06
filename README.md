# The Go Programming Language

This fork of the go programming language adds a new `until` statement to it as described in this post: [Go compiler internals: adding a new statement to Go - Part 1](https://eli.thegreenplace.net/2019/go-compiler-internals-adding-a-new-statement-to-go-part-1/). Although due to some refactoring in the go compiler, I had to do some major changes, but Eli's post was instrumental and I couldn't have done it without his post.

This is an example of how you'd use this new statement:

```go
package main

import "fmt"

func main() {
  i := 4
  until i == 0 {
    i--
    fmt.Println("Hello, until!")
  }
}
```

To compile and run this version of the compiler you can go to `src` folder that's inside the root of where you cloned the repo and run this command:

```
./make.bash
```

If everything goes well to run a program using this compiler you had to do this:

```
<clone folder>/go/bin/go run untilstmt.go
```

And that's it! I plan to make a blog post and add a `do while` instead!
