# bookmarks

*Looking for something else? Take a look at the [awesome collection of other awesome lists](https://github.com/sindresorhus/awesome).*
+ [Excellent list of free programming books](https://github.com/vhf/free-programming-books)
    + [The list in English](https://github.com/vhf/free-programming-books/blob/master/free-programming-books.md)
    + [Много бесплатных книг по программированию](http://habrahabr.ru/post/191312/)

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
    + [Multilayered Abstractions for Partial Differential Equations by Graham Robert Markall: good review on Nektar++ etc.](http://www.big-grey.co.uk/g_markall_phd_thesis.pdf)
        + [Making Faster FEM Solvers, Faster MPhil Transfer Report By Graham Markall](http://www.doc.ic.ac.uk/~grm08/g_markall_mphil_transfer.pdf)
        + [Graham Markall](http://www.doc.ic.ac.uk/~grm08/)
    + Nektar++
        + [Nektar++: An efficient h to p finite element framework](http://www.nektar.info/)
        + [Nektar++: a high-order finite element framework](https://xyloid.org/assets/talks/2014-06-ices.pdf)
    + CFD + GPU
        + [Recent progress and challenges in exploiting graphics processors in computational fluid dynamics: slightly outdated but interesting](http://arxiv.org/pdf/1309.3018.pdf)
            + [Laplace solver running on GPU using CUDA, with CPU version for comparison, slightly outdated](https://github.com/kyleniemeyer/laplace_gpu)
        + PyFR
            + [PyFR is an open-source Python based framework for solving advection-diffusion type problems on streaming architectures using the Flux Reconstruction approach of Huynh](http://www.pyfr.org/)
                + [vincentlab/PyFR](https://github.com/vincentlab/PyFR)
            + [New PyFR Paper “Heterogeneous Computing on Mixed Unstructured Grids with PyFR”](http://www.techenablement.com/new-pyfr-paper-heterogeneous-computing-on-mixed-unstructured-grids-with-pyfr/)
            + [PyFR: An open source framework for solving advection–diffusion type problems on streaming architectures using the flux reconstruction approach](http://www.sciencedirect.com/science/article/pii/S0010465514002549)
            + [High Performance Parallelism Pearls Volume Two: Multicore and Many-core Programming Approaches](https://books.google.ru/books?id=MUZ0CAAAQBAJ&pg=PA261&lpg=PA261&dq=mako+python+examples+c%2B%2B&source=bl&ots=nBUXLR84mk&sig=FVLDhAaYRjzoEjDCQleT43deZv4&hl=en&sa=X&ved=0CC8Q6AEwCDgKahUKEwjCjMnGvprHAhXJjywKHQuiBnE#v=onepage&q=mako%20python%20examples%20c%2B%2B&f=false)

+ Particle simulation
    + [MercuryDPM is a code for discrete particle simulations](http://mercurydpm.org/)

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

+ CUDA and friends related surveys, papers
    + [A Survey of CPU-GPU Heterogeneous Computing Techniques](https://www.academia.edu/12355899/A_Survey_of_CPU-GPU_Heterogeneous_Computing_Techniques)
    + [Гибридная реализация алгоритма MST с использованием CPU и GPU](http://habrahabr.ru/post/253031/)
    + [Понимание конфликтов банков разделяемой (shared) памяти в NVIDIA CUDA](http://habrahabr.ru/post/100363/)

+ DSLs targeting GPU
    + [CARP: Correct and Efficient Accelerator Programming](http://carp.doc.ic.ac.uk/external/news.php)
        + [CARP dessimination](http://carp.doc.ic.ac.uk/external/dissemination.php)
            + [A taste of CARP: benchmark analysis, language design and kernel verification](http://www.cs.bris.ac.uk/Research/Micro/UKMAC2012/UKMAC12_Kravets_ARM.pdf)
        + PENCIL: a C99-based intermediate language for compute & optimization
            + [PENCIL summary in one slide: poster](http://carp.doc.ic.ac.uk/external/publications/posters/HiPEAC2013.pdf)
            + [PENCIL: A Platform-Neutral Language for Accelerator Programming](http://www.many-core.group.cam.ac.uk/ukmac2014/UKMAC2014_04_Grevendonk.pdf)
            + [PENCIL support in pet and PPCG](http://www.researchgate.net/profile/Sven_Verdoolaege/publication/273911354_PENCIL_support_in_pet_and_PPCG/links/551031d20cf27d62b913cc0b.pdf)
        + see also PPCG (below)

    + [Framework for performance-portable parallel computations on unstructured meshes](https://github.com/OP2/PyOP2)
        + [OP2: Developing an open-source framework for the execution of unstructured grid applications](http://www.oerc.ox.ac.uk/projects/op2)
        + [Optimising Unstructured Mesh Computational Fluid Dynamics Applications on Multicores via Machine Learning and Code Transformation](http://www.doc.ic.ac.uk/teaching/distinguished-projects/2012/r.rusitoru.pdf)
        + [Compiler Optimizations for Industrial Unstructured Mesh CFD Applications on GPUs](https://www.oerc.ox.ac.uk/sites/default/files/uploads/profile-pages/Gihan/op2-lcpc.pdf)
    + [Copperhead Data Parallel Python](https://copperhead.github.io/)
        + [github CU copperhead](https://github.com/copperhead)
    + [Delite](https://github.com/stanford-ppl/Delite)
    + [Scalan](https://github.com/scalan)
        + [Scalan Community Edition](https://github.com/scalan/scalan-ce)
    + [Generating Performance Portable Code using Rewrite Rules: From High-level Functional Expressions to High-Performance OpenCL Code](http://homepages.inf.ed.ac.uk/slindley/papers/array-gpu-draft-february2015.pdf)
    + [Performance Comparison of GPU, DSP and FPGA implementations of image processing and computer vision algorithms in embedded systems, Fykse, Egil](http://brage.bibsys.no/xmlui/handle/11250/256108)

    + ROSE compiler + Mint for C-to-CUDA code generation
        + [ROSE compiler github](https://github.com/rose-compiler)
        + MINT 
            + [ROSE project MINT](https://github.com/rose-compiler/rose/tree/master/projects/mint)
            + [MINT google project](https://sites.google.com/site/mintmodel/)
                + [Mint: Realizing CUDA performance in 3D Stencil Methods with Annotated C: claims 78% of handwritten CUDA performance](http://cseweb.ucsd.edu/groups/hpcl/scg/papers/2011/mint-unat-ics11.pdf)
                + [MINT PhD thesis](http://cseweb.ucsd.edu/groups/hpcl/scg/papers/2012/DidemUnat_thesis.pdf)

    + Nested Data Parallelism, Haskell, and friends
        + [Nested Data Parallelism on GPU](http://people.cs.uchicago.edu/~jhr/papers/2012/icfp-gpu.pdf)
        + [Compiling a high-level language for GPUs: (via language support for architectures and compilers)](http://hgpu.org/?p=7809)
        + [NOVA: A Functional Language for Data Parallelism](https://research.nvidia.com/sites/default/files/publications/nvr-2013-002_0.pdf)
        + [CuNesl: Compiling Nested Data-Parallel Languages for ... ](http://moss.csc.ncsu.edu/~mueller/ftp/pub/mueller/papers/icpp12.pdf)
        + [A Haskell EDSL for Nested Data-parallel Design-space ... ](http://www.cse.chalmers.se/edu/course/pfp/exploration-draft-Obsidian.pdf)
        + [Functional programming for nested data parallelism on GPUs](https://wiki.aalto.fi/download/attachments/70779066/T-106.5840_2012_Halme.pdf?version=1&modificationDate=1357205607000)
        + [Platform-Specific Optimization and Mapping of Stencil Codes through Refinement](https://graphics.cg.uni-saarland.de/2014/platform-specific-optimization-and-mapping-of-stencil-codes-through-refinement/)
        + [High-Performance Domain-Specific Languages for GPU Computing](https://anydsl.github.io/images/anydsl.pdf)

    + CUDA kernels generation using C++ expression templates technique
        + CU++ -- an interesting approach
            + [CU++, An Object Oriented Tool for CFD Applications: GTC 2012](http://on-demand.gputechconf.com/gtc/2012/presentations/S0264-CU++-An-Object-Oriented-Framework-for-CFD-CFD-Apps.pdf)
            + [CU++(ET) / UGC- CUDA With C++ Expression Templates with the Unified GPU-CPU Compiler](http://w3.uwyo.edu/~dchandar/CU++.html)
            + [A Hybrid Multi-GPU/CPU Computational Framework](http://scientific-sims.com/cfdlab/Dimitri_Mavriplis/HOME/NEW_PAPERS/Chandar.2013-2855.pdf)
        + VexCL is a C++ vector expression template library for OpenCL/CUDA
            + [VexCL is a C++ vector expression template library for OpenCL/CUDA](https://github.com/ddemidov/vexcl)
            + [Generating OpenCL/CUDA source code from C++ expressions in VexCL](https://isocpp.org/blog/2015/01/generating-opencl-cuda-source-code-from-c-expressions-in-vexcl)

    + AnyDSL - A Framework for Rapid Development of Domain-Specific Libraries; thorin (The Higher-ORder INtermediate representation) / impala (An imperative and functional programming language)
        + [A Framework for Rapid Development of Domain-Specific Libraries](http://anydsl.github.io/)
            + [AnyDSL Build Instructions](https://github.com/AnyDSL/anydsl/wiki/Build-Instructions) 
            + [Shallow Embedding of DSLs via Online Partial Evaluation.(Best Paper Award)](http://compilers.cs.uni-saarland.de/papers/gpce15.pdf)
        + [thorin - The Higher-ORder INtermediate representation](https://github.com/AnyDSL/thorin)
        + [impala - An imperative and functional programming language](https://github.com/AnyDSL/impala)
        + [A DSL for Stencil Codes](https://github.com/AnyDSL/stincilla)
        + [AnyDSL ports from http://benchmarksgame.alioth.debian.org](https://github.com/AnyDSL/benchmarks-impala)

+ Polyhedral papers intro & focused to GPU code generation
    + [Polyhedral Compilation](http://polyhedral.info/)
    + [Code Generation in the Polyhedral Model Is Easier Than You Think](https://hal.archives-ouvertes.fr/hal-00017260/document)
        + [Automatic Code Generation in the Polytope Model](http://www.infosun.fim.uni-passau.de/cl/loopo/doc/wetzel-d.ps.gz)
    + [Non-affine Extensions to Polyhedral Code Generation](http://cgo.org/cgo2014/wp-content/uploads/2013/05/Non-affine_Extensions_to_Polyhedral_Code_Generation.pdf)
    + [Putting Automatic Polyhedral Compilation for GPGPU to Work](http://www.infosun.fim.uni-passau.de/cl/publications/docs/BGC10.pdf)
    + [Polyhedral code generation for GPUs](http://www.hipeac.net/system/files/HIW5_Lesnicki.pdf)
    + [Evaluation of state-of-the-art polyhedral tools for automatic code generation on GPUs ( :-) conclusion PPCG is the most advanced tool)](http://www.researchgate.net/profile/JI_Gomez/publication/256121029_Evaluation_of_state-of-the-art_polyhedral_tools_for_automatic_code_generation_on_GPUs/links/53da568f0cf2631430c8182e.pdf)
    + Tiling:
        + [TILING OPTIMIZATIONS FOR STENCIL COMPUTATIONS](https://www.ideals.illinois.edu/bitstream/handle/2142/44340/Xing_Zhou.pdf?sequence=1)
        + [Efficient Numerical Algorithms and Software Engineering for High Performance Computing](http://www.infosun.fim.uni-passau.de/publications/docs/KoestlerHabil2013.pdf)
        + [Split Tiling for GPUs: Automatic Parallelization Using Trapezoidal Tiles to Reconcile Parallelism and Locality, avoiding Divergence and Load Imbalance](https://hal.inria.fr/hal-00786812/file/paper.pdf)
        + [Automatic Parallelization of Tiled Loop Nests with Enhanced Fine-Grained Parallelism on GPUs](http://www.cse.unsw.edu.au/~jingling/papers/icpp12.pdf)
        + [TILING OPTIMIZATIONS FOR STENCIL COMPUTATIONS : PhD thesis by Xing Zhou](https://www.ideals.illinois.edu/bitstream/handle/2142/44340/Xing_Zhou.pdf?sequence=1)
        + [The Promises of Hybrid Hexagonal/Classical Tiling for GPU](https://hal.inria.fr/hal-00848691/document)
        + [Hybrid Hexagonal/Classical Tiling for GPUs](https://lirias.kuleuven.be/bitstream/123456789/449091/1/cgo14-grosser.pdf)
        + [Alleviating memory bandwidth pressure with wavefront temporal blocking and diamond tiling](http://blogs.fau.de/hager/files/2014/02/pp14_Keyes_MCWD.pdf)
        + [The relation between diamond tiling and hexagonal tiling](http://www.exastencils.org/histencils/2014/papers/histencils2014_the_relation_between_diamond_tiling_and_hexagonal_tiling.pdf)
        + [The Pochoir Stencil Compiler](http://www.exastencils.org/histencils/2015/papers/histencils2015_pochoir.pdf)
            +[The Pochoir Project](http://groups.csail.mit.edu/sct/wiki/index.php?title=The_Pochoir_Project)
        + scala stencils use case
            +[A Scala Prototype to Generate Multigrid Solver Implementations for Different Problems and Target Multi-Core Platforms](http://arxiv.org/pdf/1406.5369v1.pdf)
    + [Polyhedral Code Generation In The Real World](http://icps.u-strasbg.fr/~bastoul/research/papers/VBC06-CC.pdf)
    + [The Polyhedral Model Is More Widely Applicable Than You Think](http://www.cs.ucla.edu/~pouchet/doc/cc-article.10.pdf)
    + [Generating Performance Portable Code using Rewrite Rules](http://homepages.inf.ed.ac.uk/slindley/papers/array-gpu-draft-february2015.pdf)
        + [PoCC: the Polyhedral Compiler Collection](http://web.cse.ohio-state.edu/~pouchet/software/pocc/)
            + [more Polyhedral Software and Lectures are here](http://web.cse.ohio-state.edu/~pouchet/)
        + [PPCG is a parallel code generator using the polyhedral model: CUDA and OpenCL backends](http://freecode.com/projects/ppcg)
            + [PPCG git repo](http://repo.or.cz/ppcg)
            + [Polyhedral Parallel Code Generation for CUDA](http://www.researchgate.net/profile/Sven_Verdoolaege/publication/256121128_Polyhedral_parallel_code_generation_for_CUDA/links/0deec52d70d531521e000000.pdf)
            + [Polyhedral Extraction Tool](http://impact.gforge.inria.fr/impact2012/workshop_IMPACT/verdoolaege.pdf)
                + [ISL:_Integer_Set_Library](https://www.cs.colostate.edu/wiki/ISL:_Integer_Set_Library)
                    + [ISL github repository](https://repo.or.cz/isl.git)
                    + [C++ bindings for the ISL (Integer Set Library)](https://github.com/jleben/isl-cpp)
                    + [islpy is a Python wrapper around Sven Verdoolaege’s isl, a library for manipulating sets and relations of integer points bounded by linear constraints](https://pypi.python.org/pypi/islpy)
                        + [from here:](http://mathema.tician.de/software/)
                        + [github repository for python wrapper for isl, an integer set library](https://github.com/inducer/islpy)
            + [see also not finished alternative to PPCG - polly](http://polly.llvm.org/documentation/gpgpucodegen.html)
        + [see also INRIA blog](http://www.irill.org/blog/homepage)

+ Heterogeneous: MPI + GPU -> MPP, good review
    + [On Simplifying and Optimizing Message Passing Programs: A Compiler and Runtime-Based Approach](http://www.dps.uibk.ac.at/~philipp/sp_thesis_final.pdf)

+ Algorithmic skeletons for automatic GPU code generation
    + [Automatic Skeleton-Based Compilation through Integration with an Algorithm Classification](http://www.cedricnugteren.nl/downloads/Nugteren2013d.pdf)
    + [Algorithmic Species Revisited: A Program Code Classification Based on Array References](http://parse.ele.tue.nl/system/attachments/55/original/MUCOCOS_Algorithmic_Species_Revisited_A_Program_Code_Classification_Based_on_Array_References.pdf)
    + [species site](http://parse.ele.tue.nl/species/)
    + [github bones site](https://github.com/gjvdbraak/bones)

+ OpenACC
    + [IPMACC is a framework for translating/executing OpenACC for C API to/over CUDA or OpenCL runtime](https://github.com/lashgar/ipmacc)
    + [IPMACC – An Open Source OpenACC to CUDA/OpenCL Translator](http://www.techenablement.com/ipmacc-open-source-openacc-cudaopencl-translator/)

+ YaCF: Yet Another Compiler Framework
    + [A programming environment for heterogeneous architectures](http://cap.pcg.ull.es/en/accULL)
    + [YaCF: Yet Another Compiler Framework: Technical Report 02/2013](http://cap.pcg.ull.es/en/system/files/private/YaCF.pdf)
    + [Frangollo: A Run-time Library for OpenACC Support](http://cap.pcg.ull.es/es/system/files/private/Frangollo.pdf)

+ [numerical linear algebra for PDE and more](https://github.com/alsam/bookmarks/blob/master/numerical.md)

+ [Scala links](https://github.com/alsam/bookmarks/blob/master/scala.md)

+ [SBV: SMT Based Verification in Haskell](http://leventerkok.github.io/sbv/)
    + [When is Cheryl's birthday?](http://www.telegraph.co.uk/education/educationnews/11534378/When-is-Cheryls-birthday-The-tricky-math-problem-that-has-everyone-stumped.html)

+ parallelforall
    + [An Efficient Matrix Transpose in CUDA C/C++](http://devblogs.nvidia.com/parallelforall/efficient-matrix-transpose-cuda-cc/)
    + [BIDMach: Machine Learning at the Limit with GPUs](http://devblogs.nvidia.com/parallelforall/bidmach-machine-learning-limit-gpus/)
    + [GPU Programming in Functional Languages](http://www.cse.chalmers.se/~joels/writing/GPUFL.pdf)

+ [(inverse) lithography links](https://github.com/alsam/bookmarks/blob/master/litho.md)

+ [Rust links](https://github.com/alsam/bookmarks/blob/master/rust.md)

+ [Julia links](https://github.com/alsam/bookmarks/blob/master/julia.md)

+ [Python links](https://github.com/alsam/bookmarks/blob/master/python.md)

+ [HPC links](https://github.com/alsam/bookmarks/blob/master/hpc.md)

+ [Tips](https://github.com/alsam/bookmarks/blob/master/tips.md)
    + [Performance optimization](https://github.com/alsam/bookmarks/blob/master/paerformance_optimization_tips.md)

+ [Machine Learning](https://github.com/alsam/bookmarks/blob/master/machine_learning.md)

+ [Math links](https://github.com/alsam/bookmarks/blob/master/math.md)

+ [Mechanics links](https://github.com/alsam/bookmarks/blob/master/mechanics.md)
