# More Variables

In this make file we define our own variable, `PANDOC` that contains out pandoc
command and two flags. Inside of our recipe we can reference this variable so
that we don't duplicate the flags we are using with pandoc.

Makefile variables are created and assigned to with `:=`, and are referenced
with a dollar sign and parenthesis around the variable name. Variables can be
referenced anywhere in the Makefile, within rules, or they can be used within
another variable definition.

## Try It Out

1. Run `make index.html` and observe the output. Notice how the `PANDOC`
   variable is used.
1. Create a variable named `PANDOC_FLAGS` that contains the command line
   arguments passed to the pandoc command. Add another pandoc flag to this
   variable (you can view all the availble pandoc flags by running `pandoc
   --help`).
1. Reference this variable inside of the recipe.
1. Delete `index.html` and run `make index.html` again. Make sure the variable
   is used the right way.
1. Update your definition of the `PANDOC` variable to include the `PANDOC_FLAGS`
   variable, and remove the reference to `PANDOC_FLAGS` in the recipe. This way
   we only have to reference one variable in the recipe.
1. Remove `index.html` and re-run `make index.html` to ensure everything still
   works as intended.
