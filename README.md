# go-vte
This is a binding for libvte

The binding acts as an extension to github.com/gotk3/gotk3/gtk

This is a fork based on napsy/go-vte, it aims to be the most complete binding for libtve.

Work in progress!

## Environment variables

There is currently no official TERM value that denotes truecolor support, because terminfo/termcap does not
have a standard entry for 24-bit color. You should set the following environment variables to take advantage
of all VTE features:

```bash
export TERM=xterm-256color
export COLORTERM=truecolor
```


## Example


```go
term, err := vte.TerminalNew()
if err != nil {
	log.Fatal("Unable to create terminal:", err)
}
wd, _ := os.Getwd()
term.SpawnAsyncSimple(wd, []string{"/bin/bash"}, []string{"TERM=xterm"})
```
