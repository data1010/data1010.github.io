---
layout: page
title: Submitting homework
---

## Jupyter notebooks

We'll be writing up our homework submissions in a Jupyter notebook.

* Include text and math expressions using Jupyter's markdown cells (and you can generate TeX code for math expressions using a combination of [Mathpix](https://mathpix.com) and [Symbolab](https://www.symbolab.com), or using [MathKey](https://mathkey-app.com) for iOS). Another excellent math equation editor is [LyX](https://www.lyx.org).
* Generate figures from code by executing code in the Jupyter notebook.
* For non-programmatically generated figures (like geometric sketches or flowcharts), I highly recommend using [Ipe](http://ipe.otfried.org). [Here's](docs/videos/ipe-example.mp4) a video demonstrating Ipe's basic functionality. To include a figure in a Jupyter notebook, take a screenshot and then drag the image into the pane in your Juptyer notebook where the files are. From there you can drag it to a Markdown cell in the Jupyter notebook, and the Jupyter lab will automatically insert the relevant code to put the image in at that point in the document. If you want to use math expressions in your Ipe images, I recommend [TinyTeX](https://yihui.name/tinytex/) if you're pretty savvy and/or concerned about hard drive space, or [MacTeX](http://www.tug.org/mactex/) or [MikTeX](https://miktex.org) (Windows) otherwise.
* Export should be done in the following way: Select File > Export Notebook As... and choose the HTML option. Then move the downloaded HTML back into the same directory as the Jupyter notebook (so that your browser will pickup any images you've included in the notebook), and use your browser's print dialogue to save as PDF. (It might also work fine to export to PDF directly from Jupyter, but most likely you're going to encounter issues if you  try to do that.)

## Guidelines

* The idea is to use Jupyter as a format for producing a document that is meant to be read. Don't let the format encourage you to submit a scratch computation session.
* It's important to practice making your explanations as clear as possible. Bear in mind a classmate (or yourself, a few weeks from now!) as the intended reader. Provide enough context that you can follow along reasonably well without having to remember a lot of class-specific information.
* You can hide messy code that you feel isn't important to the story in a separate `.jl` file and `include` it in your notebook. Similarly, you can gloss over by-hand calculations which are routine relative to the overall difficulty of the problem. This will involve some judgement calls on your part, but that kind of judgement is a good thing to exercise.
* Long cell output should be truncated or omitted (put a semicolon at the end of the last line in the cell).

## Reflections

As of October 21, we're introducing a new optional component to the course, called *Homework Reflections*. There are at least three goals here:

1. To give you a chance to benefit from looking back at what you missed (or didn't miss) on a HW assignment and expanding on what you learned from the experience.
2. To facilitate more collaboration between students.
3. To give you a chance to earn more points.

Here are the rules/instructions:

1. You must form a group of exactly 4 or 5 students. To facilitate the formation of these groups, please use [this workspace](https://tables.area120.google.com/workspace/aakEOfWt2sQ6pGRXx7DOe9) in Google Tables. You can create a new row to start a new group, or you can join an existing group by adding yourself to the "People" column. Once you reach a group size or 4 or 5, you can use the comment thread (available at the extreme left end of the row) to communicate a Zoom link and coordinate a time to meet.
2. You must hold a videoconference (or in-person, if in the same COVID pod) meeting attended by all of the students in the group. This meeting will include a decision about which homework assignment the group is going to submit a reflection for, as well as a discussion of each question. Your goal is to identify which questions had the most interesting/important emergent ideas or misconceptions.
3. The group members will collaborate (asynchronously in most cases, though synchronous is OK too) to produce a document which expounds the aforementioned points. As with the homework, your goal here is going to be to write something that's interesting and useful for another person to read. You want to include pictures, code, etc. You can copy snippets from the homework as appropriate, but the overarching narrative voice should be one of reflection. It's not OK for it to read like a list of whatever was submitted originally on the homework by the group members, with brief comments at the end about what folks missed.

  To facilitate asynchronous collaboration, I recommend using either Google Docs (for basic word processing features) or [CoCalc](https://cocalc.com) (for real-time collaboration on a full-fledged Jupyter notebook).

  Without being overly prescriptive regarding scope, a good guideline is that the new text (beyond anything copied from an assignment or original submission) should amount to a page or more of text. A better guideline is to write an amount of text that you would want to read if you were aiming to learn about what folks found interesting/challenging in the assignment.

4. Once your document is ready, one person can export it to PDF and submit it [here](https://tables.area120.google.com/authform/a1yGoUYHTaZ95pf-sukksX/t/aYBhTUc0SgK7re66igbOJWa6aulcE1_oP9uYUrIOfkhE91zNePzpS7X3LS69GArk1n).
5. Upon submission, the group will self-assign a score. You can give yourself as many as 10 points (for an excellent job) or as few as 5 (for meeting the basic requirements). Your self-assigned score may be reviewed, but you are encouraged to assess yourself fairly. These points will affect the grade of each group member in exactly the same way as if they were added directly to the score of the corresponding homework. E.g., if you had a 94, you will effectively have a 104 (though these points will be added downstream in the grading pipeline, not directly in Gradescope).
6. You can submit a reflection on any homework at any time. Furthermore, you can collaborate with different groups on different assignments. However, each student may submit at most two reflections per week. To receive credit, a submission must be received by midnight on the last day of class.

### Reflection example

Here's an example of a good, brief reflection on a short exercise:

(Homework 4, Problem 4a). This exercise asks us to show that sampling uniformly from unit square is the same as sampling two independent random variables uniformly from the unit interval and combining them to form a tuple. This was actually an easy question to miss because of its simplicity. It's easy to think of the fact being asked about as self-evidence, but it isn't because the validity of the statement depends on the independence of the two components, and that has to be accounted for somehow. In fact, the problem relies on the "independence means multiply" concept: the key point is to observe that the unit density on the square factors as a product of the unit interval density of x times the unit interval density of y. In short, 1 times 1 equals 1!
