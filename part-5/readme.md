# Phony Targets

We can define "phony" targets in our makefile. These are targets that arent
actually files, but serve as a way to group files, or name certain bits of
logic.

Here we define two new targets:

- `all` is dependent on three html files. When we ask make to build the `all`
  target, it will realize that it needs to build each of the html targets, and
  will do so. Notice that this rule only specifies a target and prerequisites
  without a recipe.
- `clean` runs a shell command that removes all of the built html files.

## Try It Out

1. Run `make all`. What happens on subsequent invocations of `make all`? What if
   you modify one of the markdown files, then run it? What if you modify
   multiple markdown files then run it?
1. Run `make clean`. What happens on subsequent invocations of `make clean`?
1. Run `make clean all`. What happens?
1. Run `make all clean`. What happens?
1. Create a target named `help`. Within this target, use the shell `echo`
   command to print out a message that explains (briefly) how to use this
   makefile.
1. Run `make help` to see your help message. Notice that each command is shown
   before it is run. You can supress this behavior by adding a `@` before the
   command within the rule's recipe.
1. What happens if you run `make help all`? `make clean help all`?
1. Create a file named `three.md` and write some markdown in it. Modify the
   Makefile to render `three.html` as well.

