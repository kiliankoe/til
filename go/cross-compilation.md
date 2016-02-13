# Cross Compilation with Go

Cross compilation in go relies on two or three environment variables to be set.

To compile something for OS X, do the following:
```bash
$ env GOOS=darwin GOARCH=386 go build hello.go
```

For a Raspberry Pi for example, do this:
```bash
$ env GOOS=linux GOARCH=arm GOARM=7 go build hello.go
```
