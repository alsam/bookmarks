# numerical linear algebra and more for PDE

+ [CFD](https://github.com/alsam/bookmarks/blob/master/hpc.md#CFD)

+ BLAS + LAPACK (OpenBLAS + FLAME + ATLAS + MAGMA + KBLAS) and friends
    + [C++ tensors with broadcasting and lazy computing](https://github.com/QuantStack/xtensor)
        + [xtensor](http://quantstack.net/xtensor)
        + [The x template library](https://github.com/QuantStack/xtl)
    + [Benchmarking Single- and Multi-Core BLAS Implementations and GPUs for use with R](http://cran.r-project.org/web/packages/gcbd/vignettes/gcbd.pdf)
    + [OpenBLAS: An optimized BLAS library](http://www.openblas.net/)
        + [OpenBLAS github](https://github.com/xianyi/OpenBLAS)
        + [tester for BLAS libraries including OpenBLAS and Intel MKL](https://github.com/xianyi/BLAS-Tester)
        + [Vector Math Library](https://github.com/xianyi/OpenVML)
    + [BLIS (flame)](https://code.google.com/p/blis/)
        + [github repo for BLIS](https://github.com/flame/blis)
        + [github repo for FLAME](https://github.com/flame/libflame)
    + [**M**atrix **T**emplate **L**ibrary 4](http://new.simunova.com/en/mtl4/)
    + [GEMM: From Pure C to SSE Optimized Micro Kernels](http://apfel.mathematik.uni-ulm.de/~lehn/sghpc/gemm/index.html)
        [ulmBLAS: parent of the above link](https://github.com/michael-lehn/ulmBLAS)
    + [GEMV kernel](http://math-atlas.sourceforge.net/devel/atlas_contrib/node46.html)
    + [GPU Accelerated Memory-bound Linear Algebra Kernels" KBLAS + KSPARSE](https://www.hpc.kaust.edu.sa/training/2015/nvidia/materials/ahmad_Gday2015.pdf)
        + [PhD thesis 4 KBLAS+KSPARSE](http://repository.kaust.edu.sa/kaust/bitstream/10754/346955/1/Ahmad_Thesis_Final.pdf)
        + [KBLAS: An Optimized Library for Dense Matrix-Vector Multiplication on GPU Accelerators](http://arxiv.org/pdf/1410.1726.pdf)
        + [KBLAS: download](http://ecrc.kaust.edu.sa/Pages/Res-kblas.aspx)
        + [KSPARSE: download](http://ecrc.kaust.edu.sa/Pages/ksparse.aspx)
        + [bhSPARSE: A Sparse BLAS Library](https://github.com/bhSPARSE/bhSPARSE)
        + [fmmtl: FMM Template Library -- a structured dense matrix algorithms library, GPU accelerated, Simon Layton is a coauthor](https://github.com/ccecka/fmmtl)
        + [LAMA -- Library for Accelerated Math Applications -- GPU accelerated](http://www.libama.org/overview.html)
            + [sourceforge project for LAMA](http://sourceforge.net/projects/libama/)
    + [blaze-lib -- A high performance C++ math library -- claims to be the fastest, supports AVX](https://bitbucket.org/blaze-lib/blaze)
        + [wiki link compares blaze vs. other C++ libraries](http://code.google.com/p/blaze-lib/wiki/Benchmarks)
    + [The Numerical Template Toolbox - C++ Scientific Computing Made Easy](https://github.com/jfalcou/nt2)
        + [The Numerical Template Toolbox - C++ Scientific Computing Made Easy docs](http://nt2.numscale.com/doc/html/)
    + [SIMD Vector Classes for C++](https://github.com/VcDevel/Vc)
    + [EVE - the Expressive Vector Engine](https://github.com/jfalcou/eve)
    + [High-Performance Matrix-Matrix Multiplications of
Very Small Matrices](https://hal.archives-ouvertes.fr/hal-01409286/document)
    + [AUGEM: Automatically generate high performance Dense Linear Algebra kernels on x86 CPUs](https://github.com/Ewenwan/MVision/blob/master/CNN/HighPerformanceComputing/doc/AUGEM%20automatically%20generate%20high%20performance%20dense%20linear%20algebra%20kernels%20on%20x86%20CPUs.pdf)
    + [psBLAS -- Parallel Sparse Basic Linear Algebra Subroutines -- Fortran2003](http://www.ce.uniroma2.it/psblas/)
    + [Ginkgo is a high-performance linear algebra library for manycore systems, with a focus on sparse solution of linear systems. It is implemented using modern C++ (you will need at least C++14 compliant compiler to build it), with GPU kernels implemented in CUDA and HIP](https://github.com/ginkgo-project/ginkgo)
        + [ginkgo: getting started](https://github.com/ginkgo-project/ginkgo/wiki/Tutorial-1:-Getting-Started)    
        tl;dr    
        ```sh
        git clone https://github.com/ginkgo-project/ginkgo.git
        cd ginkgo
        mkdir build
        cd build
        ccmake ..
        make -j4
        ```
    + [GraphBLAS Repositories dedicated to Graphs in the Language of Linear Algebra](https://github.com/GraphBLAS)
        + [GraphBLAS Pointers](https://github.com/GraphBLAS/GraphBLAS-Pointers)
        + [	GraphBLAS  ycombinator](https://news.ycombinator.com/item?id=32844130)
        + [SuiteSparse:GraphBLAS, Timothy A. Davis, (c) 2017-2023, All Rights Reserved.](https://github.com/DrTimothyAldenDavis/GraphBLAS)
        + [ibmgraphblas](https://github.com/IBM/ibmgraphblas)
        + [GraphBLAS Template Library (GBTL), v. 3.0](https://github.com/cmu-sei/gbtl)
        + Rust wrappers to GraphBLAS
            + [graphblas_sparse_linear_algebra](https://crates.io/crates/graphblas_sparse_linear_algebra)
                + [graphblas_sparse_linear_algebra](https://github.com/code-sam/graphblas_sparse_linear_algebra)
            + [rustgraphblas](https://github.com/fabianmurariu/rustgraphblas)

    + [Elemental is a modern C++ library for distributed-memory dense and sparse-direct linear algebra and optimization.](https://github.com/elemental/Elemental)
        + [Elemental.jl](https://github.com/JuliaParallel/Elemental.jl)
    + [Recommendations for a usable, fast C++ matrix library?](https://scicomp.stackexchange.com/questions/351/recommendations-for-a-usable-fast-c-matrix-library)

    + [The Tensor Algebra Compiler (taco) computes sparse tensor expressions on CPUs and GPUs](https://github.com/tensor-compiler/taco)
        + [A fast and versatile library for linear and tensor algebra](http://tensor-compiler.org/)
    + [amgcl : C++ library for solving large sparse linear systems with algebraic multigrid method](https://github.com/ddemidov/amgcl)
        + [amgl docs : AMGCL is a header-only C++ library for solving large sparse linear systems with algebraic multigrid (AMG) method](https://amgcl.readthedocs.io/en/latest/)
            + [amgl issue : MPI & preconditioner+solver setup](https://github.com/ddemidov/amgcl/issues/107)


+ [The Amazing Performance of C++17 Parallel Algorithms, is it Possible?](https://www.bfilipek.com/2018/11/parallel-alg-perf.html?m=1)

+ SIMD
    + [The C++ scientist](http://jmabille.github.io/)


+ [Spectra - C++ Library For Large Scale Eigenvalue Problems](http://yixuan.cos.name/spectra/)
    + [A header-only C++ library for large scale eigenvalue problems](https://github.com/yixuan/spectra)
        + [Spectra C++ Library For Large Scale Eigenvalue Problems](https://spectralib.org/)
    + [Spectra Performance](http://yixuan.cos.name/spectra/performance.html)

+ Dimension Reduction
    + [A flexible and efficient С++ template library for dimension reduction](https://github.com/lisitsyn/tapkee)
        + [Tapkee an efficient dimension reduction library](http://tapkee.lisitsyn.me/)

+ [Wavelet and Multiscale Library](https://wavelet-and-multiscale-library.github.io/)
    + [The Marburg Software Library is a collection of wavelet based c++ algorithms to solve multivariate partial differential equations.](https://github.com/wavelet-and-multiscale-library/Marburg_Software_Library)
    + [Parallel adaptive wavelet collocation method for PDEs](https://www.skoltech.ru/app/data/uploads/sites/19/2017/02/JCP_2015.pdf)
    + [Wavelet methods in computational fluid dynamics](https://hal.archives-ouvertes.fr/hal-01024632/document)

+ BEM - **B**oundary **E**lement **L**ibrary
    + [Curated list of Hierarchical Matrices (H-Matrices) libraries](https://github.com/gchavez2/awesome-hierarchical-matrices)
    + [BEM++ is an open-source Galerkin boundary element library that handles Laplace, Helmholtz and Maxwell problems on bounded and unbounded domains](http://www.bempp.org/)
        + [BEM++ github repo](https://github.com/bempp/bempp)
            + [Bempp-rs is an (in early development) boundary element library written in Rust with a Python interface](https://github.com/bempp/bempp-rs)
            + [ExaFMM: a high-performance fast multipole method library with C++ and Python interfaces](https://github.com/JoshuaTetzner/exafmm-t/tree/feature/c_interface)
            + [BEM++ fork](https://github.com/UCL/bempp)
    + [Boundary Element Template Library](http://www.sam.math.ethz.ch/betl/)
    + [HyENA - HyENA stands for [Hy]perbolic and [E]lliptic [N]umerical [A]nalysis and is a C++ library](http://portal.tugraz.at/portal/page/portal/Files/i2610/files/Forschung/Software/HyENA/html/index.html)
    + [Obtaining the source code for NiHu](https://last.hit.bme.hu/nihu/a06431.html)
    tl;dr
    ```c++
    git clone -b release_2.0 git://last.hit.bme.hu/toolbox/nihu.git
    ```
    + [Formulating various BEM problems with an open source C++ BEM template library](http://pub.dega-akustik.de/DAGA_2014/data/articles/000368.pdf)
    + [fmm-bem-relaxed](https://github.com/barbagroup/fmm-bem-relaxed)
    + [SCUFF-EM](https://github.com/HomerReid/scuff-em/)
        + [PhD Thesis on SCUFF-EM](http://homerreid.dyndns.org/research/memos/Thesis.pdf)

    + Hierarchical matrices
        + [H2Lib is an open source software library for hierarchical matrices and H²-matrices](http://h2lib.org/)
            + [H2Lib public github repository](https://github.com/H2Lib/H2Lib)
        + [AHMED - Another software library on hierarchical matrices for elliptic differential equations github repository](https://github.com/xantares/ahmed)
            + [AHMED presentation](http://www.uni-graz.at/~haasegu/Lectures/HPC-II/SS14/ahmed.pdf)

+ [The C++ Standards Library for Concurrency and Parallelism http://stellar-group.org/libraries/hpx](https://github.com/STEllAR-GROUP/hpx)
    + [HPX (High Performance ParalleX) is a general purpose C++ runtime system for parallel and distributed applications of any scale](http://stellar-group.org/libraries/hpx)
    + [HPX — рантайм-система для параллельных и распределенных вычислений](https://corehard.by/2016/02/15/conf2016-hpx/)

+  Automatic Differentiation: mostly Julia, C++, Haskell. Scala as well
    + CasADi framework for nonlinear optimization
        + [CasADi framework for nonlinear optimization](https://web.casadi.org/)
        + [CasADi is a symbolic framework for numeric optimization implementing automatic differentiation in forward and reverse modes on sparse matrix-valued computational graphs](https://github.com/casadi/casadi)
        + [CasADi FAQ](https://github.com/casadi/casadi/wiki/FAQ)
        + [CasADi docs](https://web.casadi.org/docs/)
        + [tipsandtricks for CasADi](https://github.com/casadi/casadi/wiki/tipsandtricks)
    + [automatic-differentiation](http://rodrigo.ebrmx.com/github_/topics/automatic-differentiation)
        + [Tensors and differentiable operations (like TensorFlow) in Rust https://docs.rs/autograd/](http://rodrigo.ebrmx.com/github_/raskr/rust-autograd)
        + [Kotlin𝛁: Differentiable Functional Programming with Algebraic Data Types https://github.com/breandan/kotlingrad](http://rodrigo.ebrmx.com/github_/breandan/kotlingrad)
    + [JuliaDiff Differentiation tools in Julia](http://www.juliadiff.org/)
        + [ForwardDiff.jl github](https://github.com/JuliaDiff/ForwardDiff.jl)
            + [JSoC 2015 project: Automatic Differentiation in Julia with ForwardDiff.jl](http://julialang.org/blog/2015/10/auto-diff-in-julia/)
            + [ForwardDiff.jl docs](http://www.juliadiff.org/ForwardDiff.jl/)
                + [ForwardDiffNumber Types](http://www.juliadiff.org/ForwardDiff.jl/types.html)
                    + [ForwardDiff contributing to](http://www.juliadiff.org/ForwardDiff.jl/contributing.html)
            + [Julia automatic differentiation with source code transformation](https://github.com/gaika/AutoDiffSource.jl)
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
    
    + Haskell Automatic Differentiation
        + [What is automatic differentiation, and why does it work?](http://conal.net/blog/posts/what-is-automatic-differentiation-and-why-does-it-work)
    
    + [Why Automatic Differentiation Won’t Cure Your Calculus Blues](http://accu.org/index.php/journals/1932)
    
    + [Automatic Differentiation in Computational Science : presentation](http://science.energy.gov/~/media/ascr/ascac/pdf/meetings/nov10/Norris.pdf)
    
    + Reviews of AD including computational cost of FAD/BAD
        + [A Hitchhiker's Guide to Automatic Differentiation - up-to-date - all you have to know about AD, Haskell focused](http://arxiv.org/abs/1411.0583)
            + [Dr Philipp Hoffmann personalia](https://www.maynoothuniversity.ie/people/philipp-hoffmann)
                + [National University of Ireland Maynooth Brain and Computation Lab](http://bcl.hamilton.ie/software/)
                    + [Hype: Compositional Machine Learning and Hyperparameter Optimization](http://hypelib.github.io/Hype/)
        + [Automatic differentiation in machine learning: a survey contains estimation for number of operations](http://arxiv.org/pdf/1502.05767.pdf)
        + [AD and Sparse Matrices (Computational Complexity of Forward Mode AD)](http://www.numerical.rl.ac.uk/people/hsd/jkr/talks/forth.pdf)
        + [Towards a Computer Algebra System with Automatic Differentiation for use with Object-Oriented modelling languages (the paper describes DAG representation for representing optimization problem)](http://www.ep.liu.se/ecp/047/011/ecp4710011.pdf)
        + [Non-smooth Optimization and Automatic Differentiation (skript of the lecture)](http://www.math.hu-berlin.de/~bosse/Downloads/NonsmoothSkript.pdf)
        + [PhD Thesis A Small-Perturbation Automatic-Differentiation (SPAD) Method for Evaluating Uncertainty in Computational Electromagnetics](https://etd.ohiolink.edu/!etd.send_file?accession=osu1354742230&disposition=inline)
        + [Reverse-Mode AD in a Functional Framework: Lambda the Ultimate Backpropagator](http://www.bcl.hamilton.ie/~barak/papers/toplas-reverse.pdf)
            + [Barak A. Pearlmutter publications](http://www.bcl.hamilton.ie/~barak/publications.html)
            + [Jeffrey Mark Siskind's Software](https://engineering.purdue.edu/~qobi/software.html)
        + [A simple explanation of reverse-mode automatic differentiation](https://justindomke.wordpress.com/2009/03/24/a-simple-explanation-of-reverse-mode-automatic-differentiation/)
            + [Automatic Differentiation: The most criminally underused tool in the potential machine learning toolbox?](https://justindomke.wordpress.com/2009/02/17/automatic-differentiation-the-most-criminally-underused-tool-in-the-potential-machine-learning-toolbox/)
            + [Review and Unification of Methods for Computing Derivatives of Multidisciplinary Computational Models](http://mdolab.engin.umich.edu/sites/default/files/Martins-Hwang-2013-AIAAJ-derivatives.pdf)
    
    + Applications of AD to Real World
        + [Efficient Hessian Calculations using Automatic Differentiation and the Adjoint Method](http://academic.udayton.edu/MarkusRumpfkeil/Documents/AIAA2010-1268.pdf)
        + [Automatic Differentiation Adjoint of the Reynolds-Averaged Navier–Stokes Equations with a Turbulence Model AIAA 2013-2581](http://deepblue.lib.umich.edu/bitstream/handle/2027.42/106452/AIAA2013-2581.pdf?sequence=1)
        + AD for Optimization
            + [Ceres Solver : can solve bounds constrained robustified non-linear least squares problems](http://ceres-solver.org/nnls_tutorial.html)
    
    + [AD in Haskell](https://wiki.haskell.org/Automatic_Differentiation)
    
    + [CS267 Project Report Towards Parallel Automatic Differentiation](http://www.cs.berkeley.edu/~agearh/cs267.sp10/files/Report-autodiff-Chenjie_Gu.pdf)
    
    + Autograd
        + [autograd: Efficiently computes derivatives of numpy code](https://github.com/HIPS/autograd)
        + [Autograd automatically differentiates native Torch code. Inspired by the original Python version](https://github.com/twitter/torch-autograd)
    
    + Backup
        + [fast automatic differentiation jacobians by compact lu factorization](https://orca-mwe.cf.ac.uk/49127/1/Pryce%202008.pdf)

+ Unum
    + [What are the biggest challenges in scientific computing?](https://www.quora.com/What-are-the-biggest-challenges-in-scientific-computing)
        + [John Gustafson presents: Beyond Floating Point – Next Generation Computer Arithmetic](http://insidehpc.com/2017/02/john-gustafson-presents-beyond-floating-point-next-generation-computer-arithmetic/)
                + [(former Unum)Create RUST posit arithmetic library based on 21 February 2017 Posit Arithmetic by John L. Gustafson - Beating Floating Point at its Own Game](https://users.rust-lang.org/t/create-rust-posit-arithmetic-library-based-on-21-february-2017-posit-arithmetic-by-john-l-gustafson-beating-floating-point-at-its-own-game/10077/3)
            + [UNUM ... a better alternative to IEEE Floating Point?](https://www.reddit.com/comments/2ckk5u)
            + [The Evils of Floating Point, and the Joys of Unum](http://vrworld.com/2015/03/24/the-evils-of-floating-point-and-the-joys-of-unum/)
            + [John Gustafson (scientist)](https://en.wikipedia.org/wiki/John_Gustafson_%28scientist%29)
            + [Unum Computing: An Energy Efficient and Massively Parallel Approach to Numerics](https://news.ycombinator.com/item?id=9943589)
                + [Unum Computing slideshare](http://www.slideshare.net/insideHPC/unum-computing-an-energy-efficient-and-massively-parallel-approach-to-valid-numerics)
                + [Unum Computing Is A Breakthrough ... A Game Changer](http://www.amazon.com/The-End-Error-Computing-Computational/product-reviews/1482239868)
                + [Handbook of Floating-Point Arithmetic](http://www.amazon.com/Handbook-Floating-Point-Arithmetic-Jean-Michel-Muller/dp/081764704X/ref=cm_cr_pr_product_sims?ie=UTF8)
                + [Rump's Royal Pain](http://arith22.gforge.inria.fr/slides/06-gustafson.pdf)
                + [Official Blog - SSRLabs for UNUMs implemented in hardware](http://www.ssrlabs.com/blog.html#articleOne)
            + [Unums.jl](https://github.com/tbreloff/Unums.jl/wiki/Unum-Summary-%28in-progress%29)
            + [Julia Implementation of Unums - (seems more mature)](https://github.com/REX-Computing/unumjl)
            + [unum - Rust library for unums, a placeholder @Jan 4, 2016](https://github.com/eddyb/unum)
            ```julia
            julia> f(x,y) = 333.75*y^6 + x^2*(11*x^2*y^2-y^6-121*y^4-2)+5.5*y^8+x/(2*y)
            f (generic function with 1 method)

            julia> f(77617,33096)
            1.64176022256015e21

            julia> f(Rational(77617,1),Rational(33096,1))
            ERROR: OverflowError()
             in * at rational.jl:188
             in power_by_squaring at intfuncs.jl:96
             in f at none:1
            
            julia> f(Rational(BigInt(77617),1),Rational(BigInt(33096),1))
            -8.273960599468213681411650954798162919990331157843848199178148416727096930142628e-01

            julia> f(77617.0,33096.0)
            -1.1805916207174113e21

            julia> f(BigFloat(77617),BigFloat(33096))
            -8.273960599468213681411650954798162919990331157843848199178148416727096930142628e-01
            ```

            + [(more or less) accurate floating point algorithms](https://crates.io/crates/accurate)

            + [unum in D](https://github.com/lionello/unumd)
                + [Unums.jl](https://github.com/tbreloff/Unums.jl/wiki/Unum-Summary-%28in-progress%29)
                + [Julia Implementation of Unums - (seems more mature)](https://github.com/REX-Computing/unumjl)
                + [Experimental Unums](https://github.com/simonbyrne/UnumX.jl)

            + [PosIt(new Unum) in C, C++]
                + [Unum & Posit](https://posithub.org/)
                    + [Toward Floating-Point Run-time Variable Precision in CPU](https://tel.archives-ouvertes.fr/tel-03586720/document)
                    + [PERCIVAL: Open-Source Posit RISC-V Core with Quire Capability](https://github.com/artecs-group/PERCIVAL)
                + [SoftPosit](https://gitlab.com/cerlane/SoftPosit)
                    + [Berkeley SoftFloat](http://www.jhauser.us/arithmetic/SoftFloat.html)
                + [Universal Number Arithmetic in C++](https://github.com/stillwater-sc/universal)

    + Automatic Fortran to C++ conversion
        + [Automatic Fortran to C++ conversion with FABLE](https://scfbm.biomedcentral.com/articles/10.1186/1751-0473-7-5)

    + Promising Languages for Scientific Computing (besides Julia)
        + [Polyglot Programming : review several candidate languages, namely C, C++, Fortran, Cython, Numba, Nim, Rust, D, Chapel and Julia](http://stash.artec-group.com:7990/projects/LSL/repos/mover/pull-requests/12/overview)
        + [SciLua: Scientific Computing with LuaJIT](http://scilua.org/)
        + [Chapel Quickstart Instructions](http://chapel.cray.com/docs/latest/usingchapel/QUICKSTART.html)
            tl;dr
            ```sh
            source util/quickstart/setchplenv.bash
            make
            make check
            chpl -o hello examples/hello.chpl
            ```
    + [linear algebra library Eigen](http://eigen.tuxfamily.org/)
        + [Eigen Cheat sheet](https://gist.github.com/gocarlos/c91237b02c120c6319612e42fa196d77)
        + [Eigen Aliasing](https://eigen.tuxfamily.org/dox-devel/group__TopicAliasing.html)
        + [Eigen 3.2.92 : Bug 1221: disable gcc 6 warning: ignoring attributes on template argument](https://bitbucket.org/eigen/eigen/commits/ad10b2383e48)
        + [Eigen disable GCC diagnostic ignored "-Wignored-attributes" has already merged](https://github.com/RLovelett/eigen/blob/master/Eigen/src/Core/util/DisableStupidWarnings.h)
        + [An evaluation of the Eigen linear algebra library for use in the aither CFD solver](https://github.com/mnucci32/eigenVsAither)
        + [A look at the performance of expression templates in C++: Eigen vs Blaze vs Fastor vs Armadillo vs XTensor](https://romanpoya.medium.com/a-look-at-the-performance-of-expression-templates-in-c-eigen-vs-blaze-vs-fastor-vs-armadillo-vs-2474ed38d982)
        + [How should I initialize the contents of a large matrix in Eigen?](https://stackoverflow.com/questions/27005322/how-should-i-initialize-the-contents-of-a-large-matrix-in-eigen)

+ [AeroSandbox](https://github.com/peterdsharpe/AeroSandbox)
