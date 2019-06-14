# Wildcards

Here we define a rule with a wildcard, `%`, that says any `.html` file is
dependent on the same file, but with a `.md` file extension. Now we can include
an arbitrary number of markdown files and convert them all at once!

## Try It Out

1. Run `make index.html`. Notice that this will work, even though we haven't
   defined an explicit rule for `index.html`.
1. Create a file named `one.md` and write some markdown in it.
1. Run `make one.html`.
1. Create a file named `two.md` and write some markdown in it.
1. Run `make two.html`.
1. Remove all the built html files.
1. Run `make one.html two.html` and observe the results.
