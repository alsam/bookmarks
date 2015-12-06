# julia language bookmarks
+ Julia links
    + [Julia By Example](http://samuelcolvin.github.io/JuliaByExample/)
    + [Julia HOWTO integrate equations using LaTeX in docs](https://gitter.im/MichaelHatherly/Docile.jl/archives/2015/06/10)
        + [Julia HOWTO insert Unicode symbols](http://julia.readthedocs.org/en/latest/manual/interacting-with-julia/)
    + [Introducing Julia/Arrays and tuples](https://en.wikibooks.org/wiki/Introducing_Julia/Arrays_and_tuples)
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
            + [ForwardDiff.jl github](https://github.com/JuliaDiff/ForwardDiff.jl)
                + [JSoC 2015 project: Automatic Differentiation in Julia with ForwardDiff.jl](http://julialang.org/blog/2015/10/auto-diff-in-julia/)
                + [ForwardDiff.jl docs](http://www.juliadiff.org/ForwardDiff.jl/)
                    + [ForwardDiffNumber Types](http://www.juliadiff.org/ForwardDiff.jl/types.html)
                        + [ForwardDiff contributing to](http://www.juliadiff.org/ForwardDiff.jl/contributing.html)
                + [Àlex Haro Provinciale](http://www.maia.ub.es/~alex/)
                + [Latest publications of Olivier Pironneau](http://www.ann.jussieu.fr/pironneau/publi/publications/publi.html)
            + [Automatic differentiation](https://en.wikipedia.org/wiki/Automatic_differentiation)
                + [insightful intro to AD](http://alexey.radul.name/ideas/2013/introduction-to-automatic-differentiation)
                + [/which-automatic-differentiation-tool-for-cc/](http://lingpipe-blog.com/2011/01/19/which-automatic-differentiation-tool-for-cc/)
                    + [HyperDual Numbers: Exact numeric nth derivatives](http://jliszka.github.io/2013/10/24/exact-numeric-nth-derivatives.html)
                + [Lazy Time Reversal, and Automatic Differentiation](https://karczmarczuk.users.greyc.fr/arpap/revpearl.pdf)
            + [Integration analog of automatic differentiation](http://math.stackexchange.com/questions/109070/integration-analog-of-automatic-differentiation)
                + [Risch algorithm](https://en.wikipedia.org/wiki/Risch_algorithm)
                    + [GSoC 2013 Application Chetna Gupta: Risch algorithm for symbolic integration](https://github.com/sympy/sympy/wiki/GSoC-2013-Application-Chetna-Gupta:-Risch-algorithm-for-symbolic-integration)
                    + [Q: Automatic differentiation for numerical integration](https://www.physicsforums.com/threads/automatic-differentiation-for-numerical-integration.527251/)
                    + [Derivative of definite integral](http://math.stackexchange.com/questions/716596/derivative-of-definite-integral)
                        + [Differentiation under the integral sign problem](http://math.stackexchange.com/questions/1128793/differentiation-under-the-integral-sign-problem)
                + [Chebfun—numerical computing with functions](http://www.chebfun.org/)
                + [ApproxFun - Julia package for function approximation](https://github.com/ApproxFun/ApproxFun.jl)
                    + [A practical framework for infinite-dimensional linear algebra](http://arxiv.org/pdf/1409.5529.pdf)
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
    + Iterative Solvers
        + [Iterative Solvers](https://github.com/JuliaLang/IterativeSolvers.jl)
        ```julia
        Pkg.add("IterativeSolvers")
        ```
        + [Induced Dimension Reduction method IDR(s) for solving general non-symmetric linear equations using a Krylov method, for example ordinary linear equations or Sylvester and Stein equations.](https://github.com/mschauer/IDRsSolver.jl)

    + Misc.
        + [Monadic parsers library with inheritance support](https://github.com/potan/parsers.jl)
            + [Наследование комбинаторных парсеров на Julia](http://habrahabr.ru/post/241632/)
        + [Algebraic Data Type and Pattern Matching for Julia](https://github.com/potan/adt.jl)
            + [Pattern matching с помощью макросов](http://habrahabr.ru/post/242201/)
