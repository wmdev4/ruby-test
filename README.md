Write a program which, given a dictionary, generates two output files, "sequences" and "words".

"sequences" should contain every unique sequence of four *letters* that appear in exactly one word of the dictionary, one sequence per line. Casing should not create a unique sequence. Numbers and special characters should not create a unique sequence.

'words' should contain the corresponding words that contain the sequences, in the same order, again one per line.

For example, given the trivial dictionary containing only

```
arrows
carrots
give
me
```

The outputs should be:

```
'sequences'             'words'

carr                    carrots
give                    give
rots                    carrots
rows                    arrows
rrot                    carrots
rrow                    arrows
```

'arro' does not appear in the output, since it is found in more than one word.

For the final solution, use the following dictionary file: 
