---
layout: page
title: Submitting homework
---

## Jupyter notebooks

We'll be writing up our homework submissions in a Jupyter notebook.

* Include text and math expressions using Jupyter's markdown cells (and you can generate TeX code for math expressions using a combination of [Mathpix](https://mathpix.com) and [Symbolab](https://www.symbolab.com), or using [MathKey](https://mathkey-app.com) for iOS).
* Generate figures from code by executing code in the Jupyter notebook.
* For non-programmatically generated figures (like geometric sketches or flowcharts), I highly recommend using [Ipe](http://ipe.otfried.org). [Here's](docs/videos/ipe-example.mp4) a video demonstrating Ipe's basic functionality. To include a figure in a Jupyter notebook, take a screenshot and then drag the image into the pane in your Juptyer notebook where the files are. From there you can drag it to a Markdown cell in the Jupyter notebook, and the Jupyter lab will automatically insert the relevant code to put the image in at that point in the document. If you want to use math expressions in your Ipe images, I recommend [TinyTeX](https://yihui.name/tinytex/) if you're pretty savvy and/or concerned about hard drive space, or [MacTeX](http://www.tug.org/mactex/) or [MikTeX](https://miktex.org) (Windows) otherwise.
* You can zip the notebook's enclosing folder and submit that directly on Gradescope (on macOS, right click on the folder and select "Compress") under the appropriate assignment listing.

## Guidelines

* The idea is to use Jupyter as a format for producing a document that is meant to be read. Don't let the format encourage you to submit a scratch computation session.
* It's important to practice making your explanations as clear as possible. Bear in mind a classmate (or yourself, a few weeks from now!) as the intended reader. Provide enough context that you can follow along reasonably well without having to remember a lot of class-specific information.
* You can hide messy code that you feel isn't important to the story in a separate `.jl` file and `include` it in your notebook. Similarly, you can gloss over by-hand calculations which are routine relative to the overall difficulty of the problem. This will involve some judgement calls on your part, but that kind of judgement is a good thing to exercise.
* Long cell output should be truncated or omitted (put a semicolon at the end of the last line in the cell).
