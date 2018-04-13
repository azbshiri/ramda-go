# ramda-go
An implemenation of ramda library for Go programmers.


# Installation
```
$ go get github.com/azbshiri/ramda
```

# Logic
```go
import "github.com/azbshiri/ramda"

func main() {
		waterTemp := ramda.NewCond(ramda.Cond{
			Equals(0), Always("water freezes at 0°C"),
			Equals(100), Always("water boils at 100°C"),
			T(), Always("nothing special happens at %d°C"),
		})
    
    fmt.Println(waterTemp(0)) // water freezes at 0°C
    fmt.Println(waterTemp(100)) // water boils at 100°C
    fmt.Println(waterTemp(50)) // nothing special happens at 50°C
    fmt.Println(waterTemp(70)) // nothing special happens at 70°C
}
```

# Slice
```go
import "github.com/azbshiri/ramda"

func main() {
    fmt.Println(ramda.Head([]string{"a", "b"})) // a
    fmt.Println(ramda.Head([]int{1, 2, 3})) // 1
}
```

```go
import "github.com/azbshiri/ramda"

func main() {
    fmt.Println(ramda.Tail([]string{"a", "b"})) // b
    fmt.Println(ramda.Tail([]int{1, 2, 3})) // 3
}
```

# TODO
[ ] Add exmaples in comments
[ ] Implement all functions in Ramda.js
