---
layout: page
title: Getting Started
---

This page includes instructions for getting started with DATA 1010, whether you're enrolled in the course or not. For those who are enrolled, there are additional instructions available on the [internal site](https://sites.google.com/view/data1010).

## Downloading Julia

We're going to use [Julia](https://julialang.org) in the course, and I recommend that you get it installed locally. There will also be a JupyterHub instance so you can run it in the cloud, in case you run into issues with your local installation.

Download the latest version of Julia from [https://julialang.org/downloads](http://julialang.org/downloads). Note that you should use the standard download link you see on that page, rather than JuliaPro or the Conda distribution or whatever.

Once you've downloaded and installed the Julia application, you'll want to make the `julia` executable visible to your system. To do this, follow the platform-specific instructions [here](https://julialang.org/downloads/platform/). 

## JupyterLab

We're primarily going to interact with Julia through JupyterLab. To get started with JupyterLab, type `julia` at your command line (after installation and setup) to open a Julia REPL. Then run

```
using Pkg; Pkg.add("IJulia")
using IJulia
jupyterlab()
```

to install the Julia-Jupyter interface and open a Jupyter Lab session in your browser. After the first time you do this, you can either run the last two lines above in a Julia REPL, or you can run `jupyter lab` from the command line if you have Anaconda installed (which you will for DATA 1030 or DATA 1050). 

## Git

To get the course notebooks on your machine, use your command line application (Terminal on macOS) to navigate to wherever you want to store the files and do  

```
git clone https://github.com/data1010/problem-sets.git
```

Try running that command to see if you have Git. If you don't, you'll need to [install it](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). After you've cloned the repo, you can navigate back to the folder and run `git pull` from the command line to retrieve any updates which might have been pushed to the repo on GitHub.

If you need an overview of command line tools and Git, check out the [Utilities](https://mathigon.org/course/data-science-utilities/introduction) course on Data Gymnasia. I recommend using WSL2 (Windows Subsystem for Linux) if you're on Windows, because that way your command line will work the same way it works for folks on macOS and Linux.

## Julia packages

Each notebook we'll use in the course will include two files in its directory, one called `Project.toml` and the other called `Manifest.toml`. These files contain information about which package versions should be used to ensure that the notebook runs correctly. Running `using Pkg; Pkg.activate(".")` in the notebook will point the Julia runtime to these correct package versions. This process will download and install packages if they're not already present on your system.

---

## Troubleshooting

If you have any trouble with package installations, here are some
tips: 

1. If you're having trouble with a package, you can try rebuilding
   it by doing `Pkg.build("PackageName")`, and you can also
   `Pkg.rm("PackageName"); Pkg.add("PackageName")` to remove it
   and add it back. 
1. You can do `using PyCall; PyCall.python` to see which Python executable your installation is using.
1. If your error message includes something about GR, you might need to rebuild your GR package or use PyPlot instead (these are both _backends_ for Plots, meaning that they are used to generate the figures corresponding to your Plots commands). To rebuild GR, try `Pkg.update(); ENV["GRDIR"] = ""; Pkg.build("GR")`. To switch to PyPlot, try `Pkg.add("PyPlot"); Pkg.add("LaTeXStrings"); using
   Plots; pyplot()`.
1. Try googling the error message. Other folks have probably had similar issues, and sometimes the fix is pretty easy. 

---

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
3. Run `ls` to see if there is a `config` folder already there. If not, make one with `mkdir config`. 
4. Run `cd config`
5. Run `emacs startup.jl` to create a `startup.jl` file and open an editor to put content into it. 
6. Type `using Statistics, LinearAlgebra` and then save the file with `Ctrl-x Ctrl-s` (hold control and press `x`, then release and press `s`)
7. Close the editor with `Ctrl-x Ctrl-c`

## Instructions for enrolled students

Several other steps are necessary for those who are enrolled in the course. Please visit the [internal site](https://sites.google.com/view/data1010) for that information. 