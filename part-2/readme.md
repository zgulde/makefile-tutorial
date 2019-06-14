# Variables

Variables in a make file start with a dollar sign. To include a single dollar
sign inside of a recipe command, use two dollar signs together (`$$`).

In this make file we are using two special variables:

- `$@` contains the name of the target (mnemonic: the @ sign looks like a
  target)
- `$<` contains the name of the prerequisite, or input (mnemonic: the < sign
  looks like it is feeding something *in*)

## Try It Out

1. Run `make index.html` and make sure it works as intended.
1. Create a file named `ond.md` and write some markdown in it.
1. Create a rule for converting `one.md` to `one.html`. Use make variables in
   this recipe.
1. Run the make command necessary to test out your new target
