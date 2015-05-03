# bookmarks

*Looking for something else? Take a look at the [awesome collection of other awesome lists](https://github.com/sindresorhus/awesome).*

+ CFD
    + [What are possible methods to solve compressible Euler equations](http://scicomp.stackexchange.com/questions/283/what-are-possible-methods-to-solve-compressible-euler-equations/305#305 What are possible methods to solve compressible Euler equations)
    + [I do like CFD, VOL.1, Second Edition](http://www.cfdbooks.com/cfdbooks.html)
    + [Free CFD Codes](http://www.cfdbooks.com/cfdcodes.html)
    + [Hydrodynamics in OpenCL](http://christopheremoore.net/hydrodynamics-cl/)
        + [Roe, HLL, HLLC, Burgers Scheme; 1D, 2D, 3D; Euler Equation, (~Maxwell), (~MHD), ADM Solver in OpenCL](https://github.com/thenumbernine/HydrodynamicsGPU)
    + [Implementing the discontinuous Galerkin method in CUDA](https://github.com/martyfuhry/DGCUDA)
        + [Marty Fuhry's Homepage](http://www.martyfuhry.blogspot.co.uk/p/another-page.html)
            + [Master's Thesis: An Implementation of the Discontinuous Galerkin Method on Graphics Processing Units, defended May, 2013](https://www.dropbox.com/s/w205x0ppyc15ylt/Fuhry_Martin.pdf)
    + [SU2](http://su2.stanford.edu/)
        + [github repo for SU2](https://github.com/su2code/SU2)
    + [HiFiLES: High Fidelity Large Eddy Simulation](https://hifiles.stanford.edu/)
        + [github repo for HiFiLES](https://github.com/HiFiLES/HiFiLES-solver)
    + [PyWENO + PyPFASST](https://github.com/memmett)
    + [Clawpack Repositories](https://github.com/clawpack/)

+ CPU, GPU & DRAM Architecture Simulators
    + [GPGPU-Sim](http://www.gpgpu-sim.org/)
    + [Integrated gem5 + GPGPU-Sim Simulator](http://cpu-gpu-sim.ece.wisc.edu/)
        + [Getting gem5](http://www.m5sim.org/Download)
    + [SimpleScalar LLC](http://www.simplescalar.com/)
        + [SimpleScalar LLC Intro](http://www.ecs.umass.edu/ece/koren/architecture/Simplescalar/SimpleScalar_introduction.htm)
            + [Todd Austin : the author](http://web.eecs.umich.edu/~taustin/)
    + [DRAMSim2](http://www.eng.umd.edu/~blj/dramsim/)
        + [github repos for DRAMSim2 etc. from University of Maryland](https://github.com/dramninjasUMD)
    + [Chisel: Constructing Hardware in a Scala Embedded Language](https://chisel.eecs.berkeley.edu/)
        + [UC Berkeley Architecture Research](https://github.com/ucb-bar)
            + [The RISC-V Instruction Set Architecture](http://riscv.org)
            + [Rocket Microarchitectural Implementation of RISC-V ISA](https://github.com/ucb-bar/rocket)
            + [Rocket uncore: L2 cache, etc.](https://github.com/ucb-bar/uncore)

+ DSLs targeting GPU
    + [CARP: Correct and Efficient Accelerator Programming](http://carp.doc.ic.ac.uk/external/news.php)
        + [CARP dessimination](http://carp.doc.ic.ac.uk/external/dissemination.php)
    + [Framework for performance-portable parallel computations on unstructured meshes](https://github.com/OP2/PyOP2)
        + [OP2: Developing an open-source framework for the execution of unstructured grid applications](http://www.oerc.ox.ac.uk/projects/op2)
    + [Copperhead Data Parallel Python](https://copperhead.github.io/)
        + [github CU copperhead](https://github.com/copperhead)
    + [Delite](https://github.com/stanford-ppl/Delite)
    + [Scalan](https://github.com/scalan)
        + [Scalan Community Edition](https://github.com/scalan/scalan-ce)

    + CUDA kernels generation using C++ expression templates technique
        + CU++ -- an interesting approach
            + [CU++, An Object Oriented Tool for CFD Applications: GTC 2012](http://on-demand.gputechconf.com/gtc/2012/presentations/S0264-CU++-An-Object-Oriented-Framework-for-CFD-CFD-Apps.pdf)
            + [CU++(ET) / UGC- CUDA With C++ Expression Templates with the Unified GPU-CPU Compiler](http://w3.uwyo.edu/~dchandar/CU++.html)
            + [A Hybrid Multi-GPU/CPU Computational Framework](http://scientific-sims.com/cfdlab/Dimitri_Mavriplis/HOME/NEW_PAPERS/Chandar.2013-2855.pdf)
        + VexCL is a C++ vector expression template library for OpenCL/CUDA
            + [VexCL is a C++ vector expression template library for OpenCL/CUDA](https://github.com/ddemidov/vexcl)
            + [Generating OpenCL/CUDA source code from C++ expressions in VexCL](https://isocpp.org/blog/2015/01/generating-opencl-cuda-source-code-from-c-expressions-in-vexcl)

+ Polyhedral papers intro & focused to GPU code generation
    + [Code Generation in the Polyhedral Model Is Easier Than You Think](https://hal.archives-ouvertes.fr/hal-00017260/document)
    + [Non-affine Extensions to Polyhedral Code Generation](http://cgo.org/cgo2014/wp-content/uploads/2013/05/Non-affine_Extensions_to_Polyhedral_Code_Generation.pdf)
    + [Polyhedral Code Generation In The Real World](http://icps.u-strasbg.fr/~bastoul/research/papers/VBC06-CC.pdf)
    + [The Polyhedral Model Is More Widely Applicable Than You Think](http://www.cs.ucla.edu/~pouchet/doc/cc-article.10.pdf)
    + [Generating Performance Portable Code using Rewrite Rules](http://homepages.inf.ed.ac.uk/slindley/papers/array-gpu-draft-february2015.pdf)
    + [Polyhedral Parallel Code Generation for CUDA](http://www.researchgate.net/profile/Sven_Verdoolaege/publication/256121128_Polyhedral_parallel_code_generation_for_CUDA/links/0deec52d70d531521e000000.pdf)
        + [PoCC: the Polyhedral Compiler Collection](http://web.cse.ohio-state.edu/~pouchet/software/pocc/)
            + [more Polyhedral Software and Lectures are here](http://web.cse.ohio-state.edu/~pouchet/)
        + [PPCG is a parallel code generator using the polyhedral model: CUDA and OpenCL backends](http://freecode.com/projects/ppcg)
            + [PPCG git repo](http://repo.or.cz/ppcg)

+ Scala
    + [The Neophyte's Guide to Scala](http://danielwestheide.com/scala/neophytes.html)
    + [Scala Tour](https://github.com/dcapwell/scala-tour)
      + [Scala Tour: Functor](https://github.com/dcapwell/scala-tour/blob/master/Functor.md)
      + [Scala Tour: Applicative Functor](https://github.com/dcapwell/scala-tour/blob/master/Applicative\ Functor.md)
    + [Applicative ramblings in Scala](http://patterngazer.blogspot.ru/2012/02/hello-again.html)
    + [Introduction to Category Theory in Scala](https://hseeberger.wordpress.com/2010/11/25/introduction-to-category-theory-in-scala/)
      + [Physics, Topology, Logic and Computation: A Rosetta Stone](http://math.ucr.edu/home/baez/rosetta.pdf)
      + [Applicatives are generalized functors](https://hseeberger.wordpress.com/2011/01/31/applicatives-are-generalized-functors/)
    + [Functors and things using Scala](http://tonymorris.github.io/blog/posts/functors-and-things-using-scala/index.html)
    + Number crunching in Scala
        + [Number Crunching in Scala - Chris Stucchio](https://www.chrisstucchio.com/pubs/slides/thoughtworks_scientific_2014/slides.html#1)
        + [non/spire : Powerful new number types and numeric abstractions for Scala](https://github.com/non/spire)
    + [«Перегрузка операторов» в Scala](http://habrahabr.ru/company/golovachcourses/blog/255631/)


+ [Rust links](https://github.com/alsam/bookmarks/blob/master/rust.md)

+ [Tips](https://github.com/alsam/bookmarks/blob/master/tips.md)
