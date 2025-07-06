# go-vte
This is a binding for libvte

The binding acts as an extension to github.com/gotk3/gotk3/gtk

This is a fork based on napsy/go-vte, it aims to be the most complete binding for libtve.

Work in progress!

## Example


```go
term, err := vte.TerminalNew()
if err != nil {
	log.Fatal("Unable to create terminal:", err)
}
wd, _ := os.Getwd()
term.SpawnAsyncSimple(wd, []string{"/bin/bash"}, []string{"TERM=xterm"})
```
