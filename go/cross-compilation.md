# Cross Compilation with Go

Cross compilation in go relies on two environment variables to be set.

To compile something for OS X, do the following:
```bash
$ env GOOS=darwin GOARCH=386 go build hello.go
```

For a Raspberry Pi for example, do this:
```bash
$ env GOOS=linux GOARCH=arm go build hello.go
```

Setting `GOARM=7` is optional, see the last paragraph [here](http://dave.cheney.net/2015/08/22/cross-compilation-with-go-1-5).

For possible combinations of `GOOS` and `GOARCH` see [here](https://golang.org/doc/install/source#environment)
