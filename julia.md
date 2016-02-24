# julia language bookmarks
+ Julia links
    + [Julia By Example](http://samuelcolvin.github.io/JuliaByExample/)
    + [Julia 0.5 milestones](https://github.com/JuliaLang/julia/milestones/0.5.0)
        + [Arraypocalypse Now (0.5 release)](https://github.com/JuliaLang/julia/issues/13157)
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
    + [Julia automatic differentiation](https://github.com/alsam/bookmarks/blob/master/AD.md)

    + [Group of pkgs for function approx.](https://github.com/ApproxFun)
        + [Julia package for function approximation](https://github.com/ApproxFun/ApproxFun.jl)
        + [Julia package for solving singular integral equations and Riemann–Hilbert problems](https://github.com/ApproxFun/SingularIntegralEquations.jl)

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
        Pkg.add("ParallelAccelerator")
        ```

        + [Induced Dimension Reduction method IDR(s) for solving general non-symmetric linear equations using a Krylov method, for example ordinary linear equations or Sylvester and Stein equations.](https://github.com/mschauer/IDRsSolver.jl)
    
    + High Performance
        + [The ParallelAccelerator package, part of the High Performance Scripting project at Intel Labs](https://github.com/IntelLabs/ParallelAccelerator.jl)
            + [talk on Prospect and ParallelAccelerator.jl at SPLASH-I 2015](http://composition.al/blog/2015/10/31/my-talk-on-prospect-and-parallel-accelerator-jl-at-splash-i-2015/)
            + [laplace-3d.jl](https://github.com/IntelLabs/ParallelAccelerator.jl/blob/master/examples/laplace-3d/laplace-3d.jl)

    + Misc.
        + [Monadic parsers library with inheritance support](https://github.com/potan/parsers.jl)
            + [Наследование комбинаторных парсеров на Julia](http://habrahabr.ru/post/241632/)
        + [Algebraic Data Type and Pattern Matching for Julia](https://github.com/potan/adt.jl)
            + [Pattern matching с помощью макросов](http://habrahabr.ru/post/242201/)

        + [Joining regular expressions in julia](http://stackoverflow.com/questions/20478823/joining-regular-expressions-in-julia)

        + [Multidimensional Array Comprehension in Julia](http://stackoverflow.com/questions/19347799/multidimensional-array-comprehension-in-julia)

        + [Efficient filtering and linear algebra routines for multidimensional arrays](https://github.com/timholy/AxisAlgorithms.jl)

        + [Arrowhead and Diagonal-plus-rank-one Eigenvalue Solvers](https://github.com/ivanslapnicar/Arrowhead.jl)

        + [Jacobi polynomials and Gauss quadrature related functions](https://github.com/pjabardo/Jacobi.jl)

        + Unums
            + [Unums.jl](https://github.com/tbreloff/Unums.jl/wiki/Unum-Summary-%28in-progress%29)
            + [Julia Implementation of Unums - (seems more mature)](https://github.com/REX-Computing/unumjl)
            + [Experimental Unums](https://github.com/simonbyrne/UnumX.jl)
        
```julia
julia> x = ["a",
       "b",
       ]
2-element Array{ASCIIString,1}:
 "a"
 "b"
julia> d = Dict{ASCIIString, Int}([(xx, 0)  for xx in x])
Dict{ASCIIString,Int64} with 2 entries:
  "b" => 0
  "a" => 0
```

        + [fix lowering bug in let-bound functions](https://github.com/JuliaLang/julia/commit/debf46747905ea33ff1deb07c20031b900da76d4)
```julia
 @test isequal([1,2,3], [a for (a,b) in enumerate(2:4)])
 @test isequal([2,3,4], [b for (a,b) in enumerate(2:4)])
 
+# comprehension in let-bound function
+let x⊙y = sum([x[i]*y[i] for i=1:length(x)])
+    @test [1,2] ⊙ [3,4] == 11
+end
+
 @test_throws DomainError (10.^[-1])[1] == 0.1
 @test (10.^[-1.])[1] == 0.1

```
