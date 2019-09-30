---
title: "The Wall of Text"
published: true
---
Coming back to university for my second year of study, I decided to warm
up by revivng an old project I couldn't quite get working a few years ago.
The Wall of Text is inspired by the [Library of Babel](https://libraryofbabel.info)
- its essentially just a simpler version of the same thing.

The idea behind the Wall of Text is simple. Its a long paragraph, made up
of lots of lines of text. Each line is 140 characters long, and the Wall
contains every possible 140-character line that can be constructed from
a set of 95 characters. The user can print a chosen number of lines from
a chosen starting line, or get for the line number of any word, phrase
or sentence(s) they can think of (under 140 characters).

In other words, it's the sum of all human knowledge, plus a lot of gibberish.
But if you do happen to find the winning lottery numbers, or the cure for any
deadly diseases, please let me know.

The trick (because of course there's a trick) is more or less just base
conversion. The Wall of Text isn't stored anywhere. The lines are logically
ordered such that the mapping from a line number to its contents is essentially
just a conversion from a decimal number to a base 95 number.

There are a few of quirks which make this a little different to a simple base
conversion. First, while the content of a line is just a well-disguised base
95 number, the line's number isn't equivalent to the decimal number the line
represents. Each line number is offset by 1 (the first line contains the base
95 number 0, etc). The goal is essentially to produce every base 95 number up
to a certain length, so making line 1 represent the decimal number 1 would skip
the decimal number 0!

The second quirk is that the base 95 numbers contained in the lines are actually flipped - the smallest units
are on the left, and the largest units are on the right. On top of this, the
digits used in my implementation are ordered a little unusually - whitespace
represents the decimal number 0, followed by letters, *then* base 10 digits, and finally symbols.

Finally, because every line must contain 140 characters, shorter base 95 numbers
contain whitespace at the end, to fill the remaining space. Because whitespace represents the
decimal number 0, this is logically consistent with a number system with flipped
digits- a base 95 number with some amount of whitespace at the end, under my system, is
equivalent to a decimal number with some number of zeroes at the front.

The last three points serve to place common search terms much earlier in the Wall. For example, there
exists a line in the Wall containing the word "Luke" followed by 136 whitespace characters. If we
were to search for the word "Luke", this is probably the line we'd want (as opposed to a line with
136 whitespace characters at the front and then the word "Luke", or one with the word "Luke" jammed
somewhere between the whitespace). By making whitespace represent 0, and by making the leftmost
digits the smallest, the earliest lines of the wall are populated by short sequences of characters,
like "Luke", and the complexities of the lines grow as you move down. Furthermore, because letters are the most
important characters, they're the smallest digits (besides whitespace), so that they appear earliest in the wall.
Similarly, symbols are deemed unimportant and less likely to be used frequently, so they're the largest digits.
Compared to the previous measures, this one is fairly negligible, but is still useful in presenting more
manageable line numbers when searching for lines.

If you couldn't tell already, this is a bit difficult to explain, so I'd recommend just trying it out. Starting
from line 1 and printing the first thousand or so lines, it should become pretty obvious what's going on
and why certain details deviate from your typical base conversion. It's also worth noting that, by editing
two variables in the code, you can change the set of allowed characters and the length of each line, and everything should work.
This was a fun project, and I may expand on it in the future somehow. But for now, it's fairly complete, and I'm happy with where it is.

Thanks for reading,

Luke

---

Check out the Wall of Text [here](https://github.com/lukeshorejones/wall-of-text).
