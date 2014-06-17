auto-enca
=========

Automatically detect coding system with Enca (by Dmitriyi Paduchikh)

## Usage

To get this function working, put the file at some place in your
load-path, compile, and add something like this into .emacs:

```lisp
(setenv "ENCAOPT" "-L russian")
(when (load "auto-enca" 'noerror)
  (modify-coding-system-alist 'file "" 'enca-detect-coding))
```
