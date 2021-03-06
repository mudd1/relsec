relsec
======

Relative sectioning package for LaTeX
-------------------------------------

This is a relative sectionining package for LaTeX.
The normal LaTeX sectioning commands like `\section`,
`\subsection` and `\chapter` are replaced by `\dynsection`
whose effect depends on the use of `\leveldown` and
`\levelup` prior to the command. This makes restructuring
easier since whole passages can just be copy-and-pasted
to a new location at a different position in the
sectioning tree and just work, without having to change
all the `\section` etc. commands in the copied passage.

There is a `\gotochapterlevel` command that sets the
sectioning level to chapter for book-like document
classes and to section for article-like ones. This
allows switching back and forth between such document
classes, again without having to adapt the sectioning
commands.

`\levelup` and `\leveldown` accept an optional parameter.
So `\leveldown[2]` at section level will change to
subsubsection, just as if `\leveldown\leveldown` had
been used.

There is also an asection environment in case you prefer
`\begin{asection}` `\end{asection}` instead of loose `\leveldown` `\levelup` commands. The two types can
even be mixed although divine punishment will probably
occur.

This package uses ideas and code from answers to this
question on Stackoverflow which I found when I was fed up
from having to change my sectioning commands all the time
due to constant restructuring of my text.
http://stackoverflow.com/questions/2066119/relative-section-specification

The code is still crude and hasn't been tested with the
probably millions of combination of existing and non-existing
sectioning commands in various document classes and is
known not to make use of packages that provide new sectioning
commands such as `\subsubsubsection`.

The `\TestRelativeSectioning` macro is likely to produce one or more
error messages which is intended (testing the error messages, too)
and can just be skipped.
