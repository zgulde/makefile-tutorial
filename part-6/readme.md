# More Variables and Builtin Functions

Here we define two new variables, `MD_FILES` and `HTML_FILES`. `MD_FILES`
contains all the markdown files in the directory, and `HTML_FILES` contains the
names of all the target html files.

We used the built-in `shell` function to define the `MD_FILES` variable. The
`shell` function runs a shell command and returns the command's output. In this
case, we ran a command that output the names of all the files with the `.md`
file extension.

We used the `patsubst` command to generate a list of output html files. The
arguments to `patsubst` say that we want to replace the `md` extension with
`html` for every value in the `MD_FILES` variable.

Lastly we updated the `all` target to depend on the `HTML_FILES` variable. These
modifications make it so that our Makefile will work for any markdown files we
place in the directory, so we don't have to hardcode any file names.

## Try It Out

1. Create a file named `index.md` and write some markdown in it.
1. Run `make all`.
1. Create a file named `one.md` and write some markdown in it.
1. Run `make all`.
1. Notice that you didn't need to update the Makefile, even as you add more
   markdown files.
