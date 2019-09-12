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
* Generate figures from code by executing code in the Jupyter notebook. 
* For non-programatically generated figures (like geometric sketches or flowcharts), we strongly recommend using [Ipe](http://ipe.otfried.org). [Here's](docs/videos/ipe-example.mp4) a video demonstrating Ipe's basic functionality. To include a figure in a Jupyter notebook, export the file as SVG from the file menu and drag the SVG file from your computer to the Jupyter Lab file viewer in the same directory as the notebook. Then use HTML to import the file (`<img src="example.svg" width=350px>`). (Note: if you don't have any TeX installation on your machine, you'll need to download [MacTeX](http://www.tug.org/mactex/) or [MikTeX](https://miktex.org) (Windows) to be able to do math expressions in labels in Ipe. If you're concerned about download size, [TinyTeX](https://yihui.name/tinytex/) is another option, but it requires a bit more configuration and potentially some troubleshooting.)
* If you have a raster image to include, use png instead of jpg. 
* Note that you can make text float around an image like this: `<img src="set.png" style="float: right;" width=350px>`

To export your notebook to PDF, install [nteract](http://nteract.io) on your computer and put 

```
<style>
@media print
{
h2 {page-break-before:always}
}
</style>
```

at the top of your first cell (starting with HW02, we'll be including this in the starter code). This causes each problem to start on a new page. Download the notebook to your machine, and double-click the file to open it in nteract. Go to File > Export PDF. Navigate to Gradescope in your browser, upload your PDF, and map the problem numbers to the pages of your submission.

## Guidelines

* The idea is to use Jupyter as a format for producing a document that is meant to be read. Don't let the format encourage you to submit a scratch computation session.
* It's important to practice making your explanations as clear as possible. Bear in mind a classmate (or yourself, a few weeks from now!) as the intended reader. Provide enough context that you can follow along reasonably well without having to remember a lot of class-specific information.
* You can hide messy code that you feel isn't important to the story in a separate `.jl` file and `include` it in your notebook. Similarly, you can gloss over by-hand calculations which are routine relative to the overall difficulty of the problem. This will involve some judgement calls on your part, but that kind of judgement is a good thing to exercise.
* Long cell output should be truncated or omitted (put a semicolon at the end of the last line in the cell).
* If something slightly odd happens in PDF export (like a figure gets split across pages), don't worry about it. We can always look at your repo if we need to. 