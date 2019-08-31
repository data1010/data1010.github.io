---
layout: page
title: Submitting homework
---

Homework submissions will be done in two steps: 

1. Submitting to GitHub classroom.
2. Submitting to Gradescope.

The former submission will have all of the files relevant to generate your work, and the second will contain only the final product. We're using Gradescope because it provides effective tools for grading (for us) and viewing grades (for you).  

## Jupyter notebooks

You will write your submission in a Jupyter notebook. 

* Include text and math expressions using Jupyter's markdown cells (and you can generate TeX code for math expressions using a combination of [Mathpix](https://mathpix.com) and [Symbolab](https://www.symbolab.com), or using [MathKey](https://mathkey-app.com) for iOS). 
* Generate figures using code by executing code in the Jupyter notebook. 
* For non-programatically generated figures (like geometric sketches or flowcharts), we recommend using [Ipe](http://ipe.otfried.org). [Here's](docs/videos/ipe-example.mp4) a video demonstrating Ipe's basic functionality. To include a figure in a Jupyter notebook, put the figure file in the same directory as the notebook and use a Markdown cell with either Markdown (`![alt text](figure-file-name.png)`) or HTML code for figures `<img src="figure-file-name.png" alt="alt text" width="120mm">`. The latter approach allows you to control the size of the figure. You can also make it float to the right using `<img style="float: right;" src="whatever.jpg">`, which can be helpful for achieving a better use of space when an image is not very wide

To export your notebook to PDF, put a Markdown cell containing the text `\newpage` after each problem (to ensure that each problem starts on a new page). Then go to "File > Export Notebook As... > Export Notebook to PDF". Upload the resulting PDF file to Gradescope and map the problem numbers to the pages of your submission.

## Guidelines

* The idea is to use Jupyter as a format for producing a document that is meant to be read. Don't let the format encourage you to submit a scratch computation session.
* It's important to practice making your explanations as clear as possible. Bear in mind a classmate (or yourself, a few weeks from now!) as the intended reader. Provide enough context that you can follow along reasonably well without having to remember a lot of class-specific information.
* You can hide messy code that you feel isn't important to the story in a separate `.jl` file and `include` it in your notebook. Similarly, you can gloss over by-hand calculations which are routine relative to the overall difficulty of the problem. This will involve some judgement calls on your part, but that kind of judgement is a good thing to exercise.
* Long cell output should be truncated or omitted (put a semicolon at the end of the last line in the cell).