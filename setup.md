
# Julia setup

## Download

You can download Julia from http://julialang.org/downloads. I
recommend Julia 1.0.1 for this class. Also, use the standard download
link you see on that page, rather than JuliaPro or any other
distribution.

## Julia and Python

If you have Anaconda installed on your machine, you will want to
point the IJulia and PyCall packages to your Anaconda executables so
that it doesn't install its own versions (replace `sswatson` with your
own username on your machine---also, you will want to check that you
have Anaconda installed in the same place I do). You have to re-build
the packages after updating the `ENV` dictionary.

**Step 1.** _Find your Anaconda Python executable._ Launch an Anaconda
Python session and from within that session run 

```python
import sys
sys.executable
```

Make note of this path. 

**Step 2.** _Find your Jupyter executable_. On a Mac, run `which
jupyter` from a Terminal session get the path of your Jupyter
executable. It's probably somewhere like
`/Users/sswatson/anaconda3/bin/jupyter`. On Windows, it's probably
somewhere like `C:/Users/sswatson/Anaconda3/Scripts/jupyter`. You can
check this by starting Command Prompt, typing `cd Ana` and
pressing tab to see if it autocompletes to `cd Anaconda3`. Then start
typing `Scripts` and hit tab again to see that it completes to
`Scripts`. 

**Step 3.** _[Download Julia](https://julialang.org/downloads/) and run
the following from a Julia session._ Replace the Jupyter and Python
paths below with what you found in Steps 1 and 2. 

```julia
using Pkg
ENV["JUPYTER"] = "/Users/sswatson/anaconda3/bin/jupyter"
Pkg.build("IJulia")
ENV["PYTHON"] = "/Users/sswatson/anaconda3/bin/python"
Pkg.build("PyCall")
```

**Step 4.** We will also be using the `Plots` package and a few
others, so you can go ahead and run 
```julia
Pkg.add("Plots")
Pkg.add("Images")
Pkg.add("Colors")
```
If you don't install these now, you can install them later. 

## Troubleshooting

If you have any trouble with the above installation, here are some
tips: 

1. If you're having trouble with a package, you can try rebuilding
   it by doing `Pkg.build("PackageName")`, and you can also
   `Pkg.rm("PackageName"); Pkg.add("PackageName")` to remove it
   and add it back. 
1. Do `using PyCall; PyCall.python` to see which Python executable
   your installation is using. You want it to be in a directory with
   `Anaconda3` or `anaconda3` in the path string. 
1. If your error message includes something about GR, you might need
   to rebuild your GR package or use PyPlot instead (these are both
   _backends_ for Plots, meaning that they are used to generate the
   figures corresponding to your Plots commands). To rebuild GR, try
   `Pkg.update(); ENV["GRDIR"] = ""; Pkg.build("GR")`. To switch to
   PyPlot, try `Pkg.add("PyPlot"); Pkg.add("LaTeXStrings"); using
   Plots; pyplot()`.
1. Try googling the error message. Other folks have probably had
    similar issues, and sometimes the fix is pretty easy. 
1. If you have Windows 7, there are instructions on the downloads
   page for stuff you have to do for Julia to work. One of these is
   the Windows Management Framework, which is necessary for Julia to
   be able to download binaries for its packages. 

## Getting started

You should complete the _Programming in Julia_ edX module to get
oriented.

## startup.jl

If you don't want to have to run `using Statistics, LinearAlgebra` in
every session, you can put these lines in your `startup.jl` file. The
code in this file is loaded every time you run Julia. 

The instructions below are for macOS/Linux. The same idea applies if
you're using Windows, but the navigation commands are different. The
basic idea is to put a `startup.jl` file in `~/.julia/config/`, where
`~` represents whatever the home directory is on your system. 

1. Open a Terminal session 
2. Run `cd ~/.julia/`
3. Run `ls` to see if there is a `config` folder already there. If
   not, make one with `mkdir config`. 
4. Run `cd config`
5. Run `emacs startup.jl` to create a `startup.jl` file and open an
   editor to put content into it. 
6. Type `using Statistics, LinearAlgebra` and then save the file with
   `Ctrl-x Ctrl-s` (hold control and press `x`, then release and press
   `s`)
7. Close the editor with `Ctrl-x Ctrl-c`
