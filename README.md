# wq - word quiz

wq is a small shell script to help you practice words, vocabulary or definitions in general.

All you need is a text file (txt, md, etc) in which you list the words to be tested. This could look like this:

**biological_terms.md**
```md
# Biological terms

## A
* Aldosterone - mineralocorticoid hormone compound secreted by the adrenal gland cortex
* Atavism - phenomenon in which a phenotypic trait reappears in an organism after a period of absence

## B
* Bilirubin - a molecule formed from the breakdown of red blood cells, and other cells with porphyrins
.
.
.

```

You can set the path to the file (e.g. "$HOME/Documents/biological_terms.md") in the first line of the `wq` file:

```sh
file="<path_to_default_file>"
```

In the next two lines you can set the variables `bullet` and `separator`:

```sh
bullet="*"
separator="-"
```

By default, wq expects a `*` as a bullet, but you can also take another one like `-`. The variable is needed so that wq knows which lines to include; all others, like headers or empty lines, are ignored.

By default, wq expects a `-` as a delimiter, but you can also use an en dash (`–`) or colon (`:`) or whatever.

## How to use
After downloading and setting the variables as described above, it is recommended to copy the file to /usr/local/bin:

```
$ sudo cp wq /usr/local/bin
```

After that you just have to call `wq` in the terminal and the script will pick a random word from the file.

```
$ wq
Atavism
Click enter to display the definition...
```

You think about the answer and after clicking Enter you can check if you were right.

If you call `wq` without any arguments, it will take the file that was stored in the `file` variable. But you also have the possibility to take another file as input, for example:

```
$ wq ~/Documents/spanish_vocabulary.md
```

That's it. Good luck with your practice!