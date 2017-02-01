Markov Sentence Generator
=========================

This is a fork [janhoy/markov-sentence-generator](https://github.com/janhoy/markov-sentence-generator) of th original project [hrs/markov-sentence-generator](https://github.com/hrs/markov-sentence-generator)

This program generates a sentence's worth of "real-looking" text using a Markov model and sample textual training input.  Given some sample text from which to build a model, the program prints out a sentence based on a Markov chain.  Use it thus:

`$ ./sentence-generator.py  filename  [chain length] [csv size] [cache size]`

 * `filename` is a file containing some training text for the sentence to imitate (one of Project Gutenberg's books fits the bill nicely)
 * `chain length` optionally represents the number of words taken into account when choosing the next word.
 * `csv size` will cause the program to output `size` rows with columns "id" and "text"
 * `cache size` will speed up csv generation by limiting number of unique sentences to `cace size`
 
> Chain length defaults to 1 (which is fastest), but increasing this may generate more realistic text, albeit slightly more slowly.
> Depending on the text, increasing the chain length past 6 or 7 words probably won't do much good -- at that point you're usually plucking out whole sentences anyway, so using a Markov model is kind of redundant.

The texts of *Portrait of the Artist as a Young Man* and *Leaves of Grass* (in `snippet.txt`) are taken from Project Gutenberg.  The usual copyright headers had to be removed so that they could serve as useful sample input, but naturally all the rights and restrictions of a Gutenberg book still apply.

January 2017
-------------
This fork provides Python3 support and fast generation of large CSV file