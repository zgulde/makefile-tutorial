# Adding More Structure

We added two variables, `SRC_DIR` and `OUTPUT_DIR` that contain directory names
where we will store our markdown source files, and the output html files,
respectively.

We updated the `HTML_FILES` variable definition so that all of the html file
names have the correct output directory in them.

We updated our target and prerequisites to include the directory names.

We added a line to our recipe to convert html files to markdown files that uses
the `dir` make function to get the name of the directory that the target that is
currently being made resides in. We first ensure this directory is created
before trying to create an html file inside of it. We start this line with an
`@` sign to stop make from outputting the command when it is run.

## Try It Out

1. Run `make all`. Do you see the `mkdir` command in the output of `make all`?
1. Create more markdown files inside of `src`, then run `make all` to see the
   corresponding html files created.
1. Create a subdirectory inside of `src` that contains more markdown files. Run
   `make all` and observe the results.
