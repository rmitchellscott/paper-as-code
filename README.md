# Paper as Code
## What Even Is This?
I've been doing some bookbinding lately and have created a couple typesets in LaTex. After finally unpacking my fountain pens after my move, I want to bind some blank (or not-quite so blank) notebooks! I'm a bit picky about lines, etc on my paper, have a perfectly good laser printer in my basement, and with a little bit of Google-fu, can have passable LaTex to generate what I want!
## How Will You Bind This?
Good question! The first step is to create LaTex files to generate a page of paper for my noteboo- we better back up. Let's define a few terms:
- page : Single sided page of a notebook (half-letter or A5 for example)
- sheet : single piece of original paper (letter or A4 for example)
- signature: a collection of sheets folded together (2-8 sheets, depends on the binding/binder)

And now for some quick math: I have 50 sheets of A4 paper. If I fold this paper in half (you should be using short-grain paper for this btw), I will have 4 pages per sheet to make a notebook of 200 pages. Since 5 divides evenly into 50, let's say I'll have 10 signatures of 5 sheets. I can sew all these together, spend around 10 hours of time binding it (and like 40 hours waiting for glue to dry...) and hey, I'll have my very own custom notebook of paper! I can even use _good_ paper to make using fountain pens on it nice.

Okay, where were we? Yeah, a PDF of all of the A5/half-letter pages. We'll need to do some more work to those in order to get them ready to print and bind. Luckily, [this](https://momijizukamori.github.io/bookbinder-js) project exists to do the imposition into signatures. This will take our collection of single pages and lay them out into two-page-per-side (four-pages-total) sheets, in the proper order to fold and sew. 

## Styles
So far I've created the following styles:
- 5.8mm lined - This is somewhat narrower than even narrow-ruled paper. Wide-ruled paper is 8.7mm between the lines, college ruled is 7.1mm, narrow ruled is 6.4mm. Yeah, I'm using metric. I use metric for all my bookbinding, tiny fractions suck. 5.8mm though, that's what the Lined Small template on my Remarkable 2 e-ink tablet is, and I think I like that.
- 5mm dot - This is a 5mm dot grid. This seems to be the standard for this sort of graph paper. 

All of these at this point have 1cm margins, with an extra 5mm in the "gutter" between pages. This is to account for the spine when binding. I haven't bound one of these yet, so this is subject to change. These values are more hard-coded than I'd like in the .tex files, I'm still pretty noobish at LaTeX, so I hope to make these more user-friendly to change in the future. 
