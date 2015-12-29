# numerical linear algebra and more for PDE

+ BLAS + LAPACK (OpenBLAS + FLAME + ATLAS + MAGMA + KBLAS) and friends
    + [Benchmarking Single- and Multi-Core BLAS Implementations and GPUs for use with R](http://cran.r-project.org/web/packages/gcbd/vignettes/gcbd.pdf)
    + [OpenBLAS: An optimized BLAS library](http://www.openblas.net/)
        + [OpenBLAS github](https://github.com/xianyi/OpenBLAS)
        + [tester for BLAS libraries including OpenBLAS and Intel MKL](https://github.com/xianyi/BLAS-Tester)
        + [Vector Math Library](https://github.com/xianyi/OpenVML)
    + [BLIS (flame)](https://code.google.com/p/blis/)
        + [github repo for BLIS](https://github.com/flame/blis)
        + [github repo for FLAME](https://github.com/flame/libflame)
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
    + [psBLAS -- Parallel Sparse Basic Linear Algebra Subroutines -- Fortran2003](http://www.ce.uniroma2.it/psblas/)

+ [Spectra - C++ Library For Large Scale Eigenvalue Problems](http://yixuan.cos.name/spectra/)
    + [A header-only C++ library for large scale eigenvalue problems](https://github.com/yixuan/spectra)
    + [Spectra Performance](http://yixuan.cos.name/spectra/performance.html)

+ Hierarchical matrices
    + [H2Lib is an open source software library for hierarchical matrices and H²-matrices](http://h2lib.org/)
        + [H2Lib public github repository](https://github.com/H2Lib/H2Lib)
    + [AHMED - Another software library on hierarchical matrices for elliptic differential equations github repository](https://github.com/xantares/ahmed)
        + [AHMED presentation](http://www.uni-graz.at/~haasegu/Lectures/HPC-II/SS14/ahmed.pdf)
    + [BEM++ is an open-source Galerkin boundary element library that handles Laplace, Helmholtz and Maxwell problems on bounded and unbounded domains](http://www.bempp.org/)
        + [BEM++ github repo](https://github.com/bempp/bempp)
            + [BEM++ fork](https://github.com/UCL/bempp)
    + [Boundary Element Template Library](http://www.sam.math.ethz.ch/betl/)
    + [HyENA - HyENA stands for [Hy]perbolic and [E]lliptic [N]umerical [A]nalysis and is a C++ library](http://portal.tugraz.at/portal/page/portal/Files/i2610/files/Forschung/Software/HyENA/html/index.html)

+ Unam
    + [What are the biggest challenges in scientific computing?](https://www.quora.com/What-are-the-biggest-challenges-in-scientific-computing)
        + [UNUM ... a better alternative to IEEE Floating Point?](https://www.reddit.com/comments/2ckk5u)
        + [The Evils of Floating Point, and the Joys of Unum](http://vrworld.com/2015/03/24/the-evils-of-floating-point-and-the-joys-of-unum/)
        + [John Gustafson (scientist)](https://en.wikipedia.org/wiki/John_Gustafson_%28scientist%29)
        + [Unum Computing: An Energy Efficient and Massively Parallel Approach to Numerics](https://news.ycombinator.com/item?id=9943589)
            + [Unum Computing slideshare](http://www.slideshare.net/insideHPC/unum-computing-an-energy-efficient-and-massively-parallel-approach-to-valid-numerics)
            + [Unum Computing Is A Breakthrough ... A Game Changer](http://www.amazon.com/The-End-Error-Computing-Computational/product-reviews/1482239868)
            + [Handbook of Floating-Point Arithmetic](http://www.amazon.com/Handbook-Floating-Point-Arithmetic-Jean-Michel-Muller/dp/081764704X/ref=cm_cr_pr_product_sims?ie=UTF8)
            + [Rump's Royal Pain](http://arith22.gforge.inria.fr/slides/06-gustafson.pdf)
        + [Unums.jl](https://github.com/tbreloff/Unums.jl/wiki/Unum-Summary-%28in-progress%29)
        ```jlcon
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
