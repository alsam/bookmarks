# julia language bookmarks
+ Julia links
    + [Julia By Example](http://samuelcolvin.github.io/JuliaByExample/)
    + [Julia HOWTO integrate equations using LaTeX in docs](https://gitter.im/MichaelHatherly/Docile.jl/archives/2015/06/10)
        + [Julia HOWTO insert Unicode symbols](http://julia.readthedocs.org/en/latest/manual/interacting-with-julia/)
    + [Compiling Julia for NVIDIA GPUs](http://blog.maleadt.net/2015/01/15/julia-cuda/)
    + [phdthesis\title{Abstraction in Technical Computing}\author{Jeffrey Werner Bezanson}](https://github.com/JeffBezanson/phdthesis/blob/master/main.pdf)
    + [JuliaQuantum](http://juliaquantum.github.io/)
        + [news](http://juliaquantum.github.io/news/)
        + [GSoC2015:Community Bonding Period Updates](http://juliaquantum.github.io/news/2015/04/JuliaQuantum-and-GSoC2015/)
        + [Julia Libraries for Quantum Science and Technology](https://github.com/JuliaQuantum)
        + [QuDynamics.jl](https://github.com/JuliaQuantum/QuDynamics.jl)
    + Julia (sub)arrays performance
        + [RFC: Give AbstractArrays smart and performant indexing behaviors for free #10525](https://github.com/JuliaLang/julia/pull/10525)
        + [room for performance improvement for SubArray #5117](https://github.com/JuliaLang/julia/issues/5117)
        + [Fortran-like arrays such as FArray(Float64, -1:1,-7:7,-128:512)](https://groups.google.com/forum/#!topic/julia-dev/NOF6MA6tb9Y)
        + [Docs » Documentation of Julia’s Internals » SubArrays](http://julia.readthedocs.org/en/latest/devdocs/subarrays/)
        + [JuliaLang/ArrayViews.jl :> A Julia package to explore a new system of array views](https://github.com/JuliaLang/ArrayViews.jl)
    + Julia closures aka lambdas performance
        + [anonymous function calls have a huge overhead #1864](https://github.com/JuliaLang/julia/issues/1864)
            + [from here: reddit: Rust and Julia comparison](http://www.reddit.com/r/rust/comments/27jk63/rust_and_julia_comparison/)
            + [see also: length, numel, count, strlen #1939 summary `numel` -> `length`](https://github.com/JuliaLang/julia/issues/1939)
    + Julia automatic differention
        + [JuliaDiff Differentiation tools in Julia](http://www.juliadiff.org/)
            + [Automatic differentiation](https://en.wikipedia.org/wiki/Automatic_differentiation)
                + [/which-automatic-differentiation-tool-for-cc/](http://lingpipe-blog.com/2011/01/19/which-automatic-differentiation-tool-for-cc/)
            + [Symbolic math with julia](http://mth229.github.io/symbolic.html)
    + Gadfly
        + [latex axis labels in Gadfly](https://groups.google.com/forum/#!topic/julia-users/4QY2hzaR_EI)
        + [MathJax/LaTeX/Some sort of thing like that for labels/titles #356](https://github.com/dcjones/Gadfly.jl/issues/356)
        + [PGFPlots backend #152](https://github.com/dcjones/Gadfly.jl/issues/152)
            + [PGFPlots – Plotting in LaTeX](http://pgfplots.sourceforge.net/pgfplots_talk_FTUG_2012_final.pdf)
            + [Public Fonts for Minority Languages of Russia](http://www.paratype.com/public/)
            + ```sh
                fc-cache -fv
                xelatex Int_J1_tex.tex
              ```
