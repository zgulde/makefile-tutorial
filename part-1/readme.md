# Introduction

Makefiles contain **rules** (how to convert inputs to output) that consist of
**targets** (outputs), **prerequisites** (inputs that produce the outputs), and
**recipes** (how to turn the inputs into outputs).

This make file defines a single rule. The rule specifies a target named
`index.html` and it's prerequisite is `index.md`. The recipe to produce the
target involves a pandoc command. The recipe can be multiple lines, but *every
line must be indented with a tab*.

You can use make from the command line by typing:

```
make TARGET
```

Where `TARGET` is one of the targets that is defined in your `Makefile`.

## Try It Out

1. Type `make index.html` to see the recipe run
1. Type `make index.html` again, notice that make knows that it doesn't need to
   re-create the `index.html` file, as it is already up to date
1. Make a change to the `index.md` file, then run `make index.html` again. Make
   will now notice that you made a change to the input file, and that
   `index.html` is out of date, so it will rebuild it.
1. Create a rule to convert this `readme.md` file to html. Test out the rule you
   created.
