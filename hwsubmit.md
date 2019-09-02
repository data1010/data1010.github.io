---
layout: page
title: Submitting homework
---

Homework submissions will be done in two steps: 

1. Submitting to GitHub classroom.
2. Submitting to Gradescope.

The former submission will have all of the files relevant to generate your work, and the second will contain only the final product. We're using Gradescope because it provides effective tools for grading (for us) and viewing grades (for you).  

## Jupyter notebooks

We'll be writing up our homework submissions in a Jupyter notebook. 

* Include text and math expressions using Jupyter's markdown cells (and you can generate TeX code for math expressions using a combination of [Mathpix](https://mathpix.com) and [Symbolab](https://www.symbolab.com), or using [MathKey](https://mathkey-app.com) for iOS). 
* Generate figures using code by executing code in the Jupyter notebook. 
* For non-programatically generated figures (like geometric sketches or flowcharts), we recommend using [Ipe](http://ipe.otfried.org). [Here's](docs/videos/ipe-example.mp4) a video demonstrating Ipe's basic functionality. To include a figure in a Jupyter notebook, save the figure as a PDF and drag it from your computer to the Jupyter Lab file viewer in the same directory as the notebook. Then use a Markdown cell with the Markdown image syntax (`![alt text](figure-file-name.pdf)`). 
* If you have a raster image to include, use png instead of jpg. Also, you can specify image size in [curly braces](https://pandoc.org/MANUAL.html) at the end of the Markdown image code: `![alt-text](figure-file-name.pdf){ width=50% }`. This will not render correctly in the notebook, but it does render correctly when the notebook is exported to PDF. 

To export your notebook to PDF, put a Markdown cell containing the text `\newpage` after each problem (to ensure that each problem starts on a new page). Then go to "File > Export Notebook As... > Export Notebook to PDF". Upload the resulting PDF file to Gradescope and map the problem numbers to the pages of your submission.

## Guidelines

* The idea is to use Jupyter as a format for producing a document that is meant to be read. Don't let the format encourage you to submit a scratch computation session.
* It's important to practice making your explanations as clear as possible. Bear in mind a classmate (or yourself, a few weeks from now!) as the intended reader. Provide enough context that you can follow along reasonably well without having to remember a lot of class-specific information.
* You can hide messy code that you feel isn't important to the story in a separate `.jl` file and `include` it in your notebook. Similarly, you can gloss over by-hand calculations which are routine relative to the overall difficulty of the problem. This will involve some judgement calls on your part, but that kind of judgement is a good thing to exercise.
* Long cell output should be truncated or omitted (put a semicolon at the end of the last line in the cell).