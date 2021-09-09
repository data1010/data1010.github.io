---
layout: page
title: Getting Started
---

This page includes instructions for getting started with DATA 1010.

## Downloading Julia

We're going to use [Julia](https://julialang.org) in the course, and I recommend that you get it installed locally. You can also the web-based Prismia version, but there is some delay in starting up your instance, and you will likely find that you prefer the experience of a locally installed version.

Download the latest version of Julia from [https://julialang.org/downloads](http://julialang.org/downloads). Note that you should use the standard download link you see on that page, rather than JuliaPro or the Conda distribution or whatever.

Once you've downloaded and installed the Julia application, you'll want to make the `julia` executable visible to your system. To do this, follow the platform-specific instructions [here](https://julialang.org/downloads/platform/). (For macOS users, there's a chance you might not already have a `/usr/local/bin` directory; if that's the case, then you'll get an error when you run the `ln -s` command suggested on the Julia website. If that's the case, do `mkdir -p /usr/local/bin` and then run the `ln -s` command again. If you get a permissions error, re-run the same command but with `sudo ` prepended. You'll be able to enter your password to override the permissions restriction. To avoid similar problems in the future, you might also want to change your permissions on your `/usr/local` directory by doing `sudo chown -R $(whoami) /usr/local`).

## JupyterLab

We're primarily going to interact with Julia through JupyterLab. To get started with JupyterLab, type `julia` at your command line (after installation and setup) to open a Julia REPL. Then run

```
using Pkg; Pkg.add("IJulia")
using IJulia
jupyterlab()
```

to install the Julia-Jupyter interface and open a Jupyter Lab session in your browser. After the first time you do this, you can either run the last two lines above in a Julia REPL, or you can run `jupyter lab` from the command line if you have Anaconda installed (which you will for DATA 1030 or DATA 1050).

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
5. Run `vi startup.jl` to create a `startup.jl` file and open an editor to put content into it.
6. Type `i` to insert text, and then type `using Statistics, LinearAlgebra`.
7. Save the file by pressing escape, then `:wq`, and then enter.
