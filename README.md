# xio

Go Package tha can convert any value of interface io.Writer into a full
writer supporting Write, WriteString and WriteByte method.

It can be used as follows:

```go
h := sha256.New()
w := xio.WrapWriter(h)
w.WriteString("Hello, world!")
fmt.Printf("hash value %x\n", h.Sum(nil))
```
