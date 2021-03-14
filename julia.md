# julia language bookmarks
+ Julia links
    + [Краткое описание языка програм-мирования Julia и некоторые при-меры его использования](http://www.ihed.ras.ru/~thermo/Julia/Brief%20description%20of%20Julia%20language.pdf)
    + [Hands-On Design Patterns and Best Practices with Julia](https://www.packtpub.com/product/hands-on-design-patterns-and-best-practices-with-julia/9781838648817)
    + [Julia By Example](http://samuelcolvin.github.io/JuliaByExample/)
    + [Beautiful Julia: Cool Language Constructs and Tricks for Beginners](http://blog.translusion.com/posts/beautiful-julia/)
    + [Tricks in Julia](http://blog.translusion.com/posts/julia-tricks/)
    + [Julia for Numerical Computation in MIT Courses](https://github.com/stevengj/julia-mit)
    + [My New Workflow with Julia 1.0](https://erik-engheim.medium.com/my-new-workflow-with-julia-1-0-99711103d97c)
    + [Tutorial on precompilation](https://julialang.org/blog/2021/01/precompile_tutorial/)
        + [Force precompile and startup times](https://www.reddit.com/r/Julia/comments/9wkmzk/force_precompile_and_startup_times/)
        + [Why julia takes long time to import a package?](https://stackoverflow.com/questions/62752978/why-julia-takes-long-time-to-import-a-package)
        + [Creating a sysimage for fast plotting with Plots.jl](https://julialang.github.io/PackageCompiler.jl/dev/examples/plots/)
        + [PackageCompiler](https://github.com/JuliaLang/PackageCompiler.jl)
        + [SnoopCompile](https://github.com/timholy/SnoopCompile.jl)
            + [Producing precompile directives automatically](https://timholy.github.io/SnoopCompile.jl/stable/snoopi/#auto-1)
        + [Precompile a script?](https://discourse.julialang.org/t/precompile-a-script/5364)
    + [Julia 0.5 milestones](https://github.com/JuliaLang/julia/milestones/0.5.0)
        + [Arraypocalypse Now (0.5 release)](https://github.com/JuliaLang/julia/issues/13157)
    + [Julia HOWTO integrate equations using LaTeX in docs](https://gitter.im/MichaelHatherly/Docile.jl/archives/2015/06/10)
        + [Julia HOWTO insert Unicode symbols](http://julia.readthedocs.org/en/latest/manual/interacting-with-julia/)
    + Switch to modern Julia
        + [Difference between Set{Int}() and BitSet()](https://discourse.julialang.org/t/difference-between-set-int-and-bitset/27737)
        + [Pkg](https://docs.julialang.org/en/v1/stdlib/Pkg/index.html)
        + [immutable vs struct and type vs mutable struct in Julia](https://stackoverflow.com/questions/46863422/immutable-vs-struct-and-type-vs-mutable-struct-in-julia)
        + [What is the difference between `using` and `import` in Julia when building a module?](https://stackoverflow.com/questions/27086159/what-is-the-difference-between-using-and-import-in-julia-when-building-a-mod)
        + [Pkg Fails to clone git repository on Arch related distros](https://github.com/JuliaLang/Pkg.jl/issues/1013)
        ```sh
        git clone https://github.com/JuliaRegistries/General.git ~/.julia/registries/General
        ```
        + [Discussion: Plans for Julia as a general-purpose language?](https://discourse.julialang.org/t/discussion-plans-for-julia-as-a-general-purpose-language/30861/30)

    + [Introducing Julia/Arrays and tuples](https://en.wikibooks.org/wiki/Introducing_Julia/Arrays_and_tuples)
        + [Multidimensional algorithms and iteration](http://julialang.org/blog/2016/02/iteration)
        + [Multi-dimensional arrays with arbitrary upper and lower bounds that can be fixed or flexible](https://github.com/eschnett/FlexibleArrays.jl)
    + [Compiling Julia for NVIDIA GPUs](http://blog.maleadt.net/2015/01/15/julia-cuda/)
    + [phdthesis\title{Abstraction in Technical Computing}\author{Jeffrey Werner Bezanson}](https://github.com/JeffBezanson/phdthesis/blob/master/main.pdf)

    + Julia Groups  
        + [JuliaML](https://github.com/JuliaML)
            + [Machine Learning in Julia : a discourse](https://discourse.julialang.org/c/domain/ML/24)
            + [Should Flux be as fast as TensorFlow on CPUs?](https://www.reddit.com/r/Julia/comments/bsc68h/should_flux_be_as_fast_as_tensorflow_on_cpus/)
            + [Differentiable Programming with Julia by Mike Innes](https://www.youtube.com/watch?reload=9&v=LjWzgTPFu14&feature=youtu.be)
        + [JuliaArrays](https://github.com/JuliaArrays)
            + [Various improvements #26](https://github.com/JuliaArrays/OffsetArrays.jl/pull/26)
            + [move OffsetArrays to JuliaArrays](https://github.com/JuliaLang/METADATA.jl/pull/8884)
        + [JuliaApproximation](https://github.com/JuliaApproximation)
        + [Julia Arbitrary Precision](https://github.com/JuliaArbTypes)
            + [Much faster than BigFloat at precisions up to 3,500 bits (1050 digits)](https://github.com/JuliaArbTypes/ArbFloats.jl)
        + [Parallel Julia](https://github.com/JuliaParallel)
        + [JuliaGPU - GPU Computing for Julia](https://github.com/JuliaGPU)
        + [Julia Statistics - Statistics and Machine Learning made easy in Julia](https://github.com/JuliaStats)
        + [JuliaPlots - Data visualization in Julia using Plots.jl](https://github.com/JuliaPlots)
        + [JuliaGraphics](https://github.com/JuliaGraphics)
            + [Julia and OpenGL](https://www.reddit.com/r/Julia/comments/bfaxmu/example_julia_and_opengl/)
            + [CImGui](https://github.com/Gnimuc/CImGui.jl)
        + [JuliaQuantum](http://juliaquantum.github.io/)
            + [news](http://juliaquantum.github.io/news/)
            + [GSoC2015:Community Bonding Period Updates](http://juliaquantum.github.io/news/2015/04/JuliaQuantum-and-GSoC2015)
            + [Julia Libraries for Quantum Science and Technology](https://github.com/JuliaQuantum)
            + [QuDynamics.jl](https://github.com/JuliaQuantum/QuDynamics.jl)
        + [Julia Math](https://github.com/JuliaMath)
            + [Julia DiffEq](https://github.com/JuliaDiffEq)
            + [JuliaOpt](https://github.com/JuliaOpt)
                + [JuliaSmoothOptimizers](https://github.com/JuliaSmoothOptimizers)
            + [Julia Homotopy Continuation](https://github.com/JuliaHomotopyContinuation)
                + [A package for construction of polynomial homotopies](https://github.com/JuliaHomotopyContinuation/Homotopies.jl)

    + Translating from Fortran to Julia
        + [Julia equivalent of Fortran common blocks or, even better, Fortran 90 Modules](https://groups.google.com/forum/#!topic/julia-users/-bzuOUTeMX4)
        + Julia (sub)arrays performance
            + OffsetArrays
                + [github repo for OffsetArrays](https://github.com/alsam/OffsetArrays.jl)
                + [Tag OffsetArrays v0.1.0 (retry) #5417](https://github.com/JuliaLang/METADATA.jl/pull/5417)
                + [Performance of OffsetArrays](https://github.com/JuliaArrays/OffsetArrays.jl/issues/28)
                + [`diagm` doesn't work](https://github.com/JuliaArrays/OffsetArrays.jl/issues/25#issuecomment-335560525)
        + [Generalizing AbstractArrays: opportunities and challenges](http://julialang.org/blog/2016/03/arrays-iteration)
        + [RFC: Give AbstractArrays smart and performant indexing behaviors for free #10525](https://github.com/JuliaLang/julia/pull/10525)
        + [room for performance improvement for SubArray #5117](https://github.com/JuliaLang/julia/issues/5117)
        + [Fortran-like arrays such as FArray(Float64, -1:1,-7:7,-128:512)](https://groups.google.com/forum/#!topic/julia-dev/NOF6MA6tb9Y)
        + [Docs » Documentation of Julia’s Internals » SubArrays](http://julia.readthedocs.org/en/latest/devdocs/subarrays/)
        + [JuliaLang/ArrayViews.jl :> A Julia package to explore a new system of array views](https://github.com/JuliaLang/ArrayViews.jl)
        + `goto` and `label`
            + [@goto and @label](http://stackoverflow.com/documentation/julia-lang/5564/goto-and-label)

    + Julia closures aka lambdas performance
        + [anonymous function calls have a huge overhead #1864](https://github.com/JuliaLang/julia/issues/1864)
            + [from here: reddit: Rust and Julia comparison](http://www.reddit.com/r/rust/comments/27jk63/rust_and_julia_comparison/)
            + [see also: length, numel, count, strlen #1939 summary `numel` -> `length`](https://github.com/JuliaLang/julia/issues/1939)
    + [Julia automatic differentiation](https://github.com/alsam/bookmarks/blob/master/AD.md)

    + CAS in Julia - Symbolic Computations
        + [JuliaSymbolics Roadmap: A Modern Computer Algebra System for a Modern Language](https://juliasymbolics.org/roadmap/)
        + [Symbolic Computations in Julia using Maxima](https://github.com/nsmith5/Maxima.jl)

    + [Group of pkgs for function approx.](https://github.com/ApproxFun)
        + [Julia package for function approximation](https://github.com/ApproxFun/ApproxFun.jl)
        + [Julia package for solving singular integral equations and Riemann–Hilbert problems](https://github.com/ApproxFun/SingularIntegralEquations.jl)

    + Computer Vision
        + [The OpenCV (C++) interface for Julia](https://github.com/maxruby/OpenCV.jl)
        + [Julia packages for image processing](https://github.com/JuliaImages)

    + Graphics
        + [Powerful convenience for Julia visualizations and data analysis http://docs.juliaplots.org](https://github.com/JuliaPlots/Plots.jl)
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
            + JSON to work with 0.5
                + [Fix JSON.parse with dicttype specified #137 ](https://github.com/JuliaLang/JSON.jl/pull/137)
        + [PGFPlots](http://nbviewer.jupyter.org/github/sisl/PGFPlots.jl/blob/master/doc/PGFPlots.ipynb)
        ```julia
        using PGFPlots
        a=Axis([
           Plots.Linear(sin, (0,10), legendentry=L"$\sin(x)$"),
           Plots.Linear(x->sqrt(2*x), (0,10), legendentry=L"$\sqrt{2x}$")
           ], legendPos="north west")
        save("t.pdf",a)
        save("t1.tex",a)
        ```

    + Iterative Solvers
        + [Iterative Solvers](https://github.com/JuliaLang/IterativeSolvers.jl)
        ```julia
        Pkg.add("IterativeSolvers")
        Pkg.add("ParallelAccelerator")
        ```

        + [Induced Dimension Reduction method IDR(s) for solving general non-symmetric linear equations using a Krylov method, for example ordinary linear equations or Sylvester and Stein equations.](https://github.com/mschauer/IDRsSolver.jl)
    
    + High Performance
        + [[ANN] LoopVectorization](https://discourse.julialang.org/t/ann-loopvectorization/32843)
        + [The ParallelAccelerator package, part of the High Performance Scripting project at Intel Labs](https://github.com/IntelLabs/ParallelAccelerator.jl)
            + [talk on Prospect and ParallelAccelerator.jl at SPLASH-I 2015](http://composition.al/blog/2015/10/31/my-talk-on-prospect-and-parallel-accelerator-jl-at-splash-i-2015/)
            + [laplace-3d.jl](https://github.com/IntelLabs/ParallelAccelerator.jl/blob/master/examples/laplace-3d/laplace-3d.jl)
        + [The 3rd annual JuliaCon 2016 (MIT) | Introduction to Writing High Performance Julia | Arch D. Robison](https://www.youtube.com/watch?v=szE4txAD8mk&list=PLP8iPy9hna6SQPwZUDtAM59-wPzCPyD_S&index=25)

    + [DiffEqFlux.jl – A Julia Library for Neural Differential Equations](https://julialang.org/blog/2019/01/fluxdiffeq)
        + [Relax! Flux is the ML library that doesn't make you tensor https://fluxml.ai/](https://github.com/FluxML/Flux.jl)

    + Misc.
        + [Julia vs. Python: Which is best for data science?](https://www.infoworld.com/article/3241107/julia-vs-python-which-is-best-for-data-science.html#:~:text=Although%20Julia%20is%20purpose%2Dbuilt,uses%20zero%2Dbased%20array%20indexing.)
        + [ScientificTypes](https://github.com/alan-turing-institute/ScientificTypes.jl)
        + [The Serious Downsides To The Julia Language In 1.0.3](https://towardsdatascience.com/the-serious-downsides-to-the-julia-language-in-1-0-3-e295bc4b4755)
        + [TensorFlow.jl: A Julia Front End to the TensorFlow World (TF Dev Summit '19)](https://www.youtube.com/watch?v=n2MwJ1guGVQ)
        + [A Comparison Between Differential Equation Solver Suites In MATLAB, R, Julia, Python, C, Mathematica, Maple, and Fortran](http://www.stochasticlifestyle.com/comparison-differential-equation-solver-suites-matlab-r-julia-python-c-fortran/)
        + [Monadic parsers library with inheritance support](https://github.com/potan/parsers.jl)
            + [Наследование комбинаторных парсеров на Julia](http://habrahabr.ru/post/241632/)
        + [Algebraic Data Type and Pattern Matching for Julia](https://github.com/potan/adt.jl)
            + [Pattern matching с помощью макросов](http://habrahabr.ru/post/242201/)

        + [Joining regular expressions in julia](http://stackoverflow.com/questions/20478823/joining-regular-expressions-in-julia)

        + [Multidimensional Array Comprehension in Julia](http://stackoverflow.com/questions/19347799/multidimensional-array-comprehension-in-julia)

        + [Efficient filtering and linear algebra routines for multidimensional arrays](https://github.com/timholy/AxisAlgorithms.jl)

        + [Arrowhead and Diagonal-plus-rank-one Eigenvalue Solvers](https://github.com/ivanslapnicar/Arrowhead.jl)

        + [Jacobi polynomials and Gauss quadrature related functions](https://github.com/pjabardo/Jacobi.jl)

        + [Singular Value Decomposition for generic number types](https://github.com/simonbyrne/GenericSVD.jl)

        + [How To Automate Julia Documentation With Documenter.jl](https://towardsdatascience.com/how-to-automate-julia-documentation-with-documenter-jl-21a44d4a188f)

        + Unums
            + [Unums.jl](https://github.com/tbreloff/Unums.jl/wiki/Unum-Summary-%28in-progress%29)
            + [Julia Implementation of Unums - (seems more mature)](https://github.com/REX-Computing/unumjl)
            + [Experimental Unums](https://github.com/simonbyrne/UnumX.jl)

        + [JuliaEditorSupport/deoplete-julia](https://github.com/JuliaEditorSupport/deoplete-julia)
        
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

+ Selected issues
    + [Precompile error when using Plots.jl](https://github.com/tbreloff/Plots.jl/issues/545)
    + [A case/switch statement for Julia](https://github.com/JuliaLang/julia/issues/18285)
    + [JuliaCon 2016 | Accelerating Julia Kernels with ArrayFire.jl](https://www.youtube.com/watch?list=PLP8iPy9hna6SQPwZUDtAM59-wPzCPyD_S&v=2f32XSMYlDk)

+ [ITensor](https://itensor.org/)
    + [ITensors.jl](https://github.com/ITensor/ITensors.jl)
    + [An efficient and flexible C++ library for performing tensor network calculations](https://github.com/ITensor/ITensor)


+ [Should I use Chapel or Julia for my next project?](https://www.dursi.ca/post/julia-vs-chapel.html)

+ [Хочу все знать. Язык Julia](https://geekbrains.ru/posts/julia_lang)

+ [Metatheory.jl is a general purpose metaprogramming and algebraic computation library for the Julia programming language, designed to take advantage of the powerful reflection capabilities to bridge the gap between symbolic mathematics, abstract interpretation, equational reasoning, optimization, composable compiler transforms, and advanced homoiconic pattern matching features](https://github.com/0x0f0f0f/Metatheory.jl) 

+ JuliaCon 2019
    + [JuliaCon 2019 | What's Bad About Julia | Jeff Bezanson](https://www.youtube.com/watch?v=TPuJsgyu87U&feature=youtu.be)
    + [JuliaCon 2019 | How We Wrote a Textbook using Julia](https://www.youtube.com/watch?v=ofWy5kaZU3g&feature=youtu.be)
        + [Tufte Algorithms Book Template](https://github.com/sisl/tufte_algorithms_book.git)
    + [JuliaCon 2019 | If Runtime isn't Funtime: Controlling Compile-time Execution | Nathan Daly](https://www.youtube.com/watch?v=JCFej--XER0)
        + [JuliaCon2019 Talk "If Runtime isn't Funtime: Controlling Compile-time Execution"](https://github.hillwoodhome.net/NHDaly/juliaCon2019-If_Runtime_isn-t_Funtime-Slides)

+ JuliaCon 2020
    + [Dispatching Design Patterns (video)](https://www.youtube.com/watch?v=n-E-1-A_rZM)
        + [Dispatching Design Patterns](https://github.com/ninjaaron/dispatching-design-patterns)
            + [Object Orientation and Polymorphism in Julia](https://github.com/ninjaaron/oo-and-polymorphism-in-julia)

+ [MIT Computational Thinking Spring 2021. 6.S083 / 18.S191 / 22.S092](https://www.youtube.com/watch?reload=9&v=uZYVjDDZW9A&feature=youtu.be)

+ [PDE Solvers in Julia](https://discourse.julialang.org/t/pde-solvers-in-julia/24416)
    + [CFD Julia: A Learning Module Structuring an Introductory Course on Computational Fluid Dynamics](https://www.mdpi.com/2311-5521/4/3/159/htm)
        + [CFD_Julia](https://github.com/surajp92/CFD_Julia)
        + [Building blocks of spectral methods for Julia](https://github.com/tpapp/SpectralKit.jl)
        + [A library of functions for polynomial bases used in spectral element methods](https://github.com/ranocha/PolynomialBases.jl)
        + [Julia translation and modification of MATLAB scripts that accompany the text on Nodal Disontinuous Galerkin methods](https://github.com/bendudson/NodalDG.jl)
        + [Gridap provides a set of tools for the grid-based approximation of partial differential equations (PDEs) written in the Julia programming language](https://github.com/gridap/Gridap.jl)
            + [Solving partial differential equations in Julia with Gridap.jl](https://pretalx.com/juliacon2020/talk/DVSD7Q/)
        + [VisClaw.jl](https://github.com/hydrocoast/VisClaw.jl)
    + [JuliaCon 2018 | Solving Partial Differential Equations with Julia | Chris Rackauckas](https://www.youtube.com/watch?time_continue=3&v=okGybBmihOE&feature=emb_title)
    + [Benchmarking Julia on a PDE: the Kuramoto-Sivashinksy equation](https://github.com/johnfgibson/julia-pde-benchmark/blob/master/1-Kuramoto-Sivashinksy-benchmark.ipynb)
    + [Julia debugger](https://github.com/JuliaDebug/Debugger.jl)    
        tl;dr    
        ```julia
        using Debugger

        function foo(n)
            x = n+1
            ((BigInt[1 1; 1 0])^x)[2,1]
        end

        @enter foo(20)
        ```
