# bookmarks

*Looking for something else? Take a look at the [awesome collection of other awesome lists](https://github.com/sindresorhus/awesome).*
+ [Excellent list of free programming books](https://github.com/vhf/free-programming-books)
    + [The list in English](https://github.com/vhf/free-programming-books/blob/master/free-programming-books.md)
    + [Много бесплатных книг по программированию](http://habrahabr.ru/post/191312/)

+ [CFD](https://github.com/alsam/bookmarks/blob/master/hpc.md#CFD)

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
            + [Write-back vs Write-Through](https://stackoverflow.com/questions/27087912/write-back-vs-write-through)
            + [Study of Different Cache Line Replacement Algorithms in Embedded Systems](https://people.kth.se/~ingo/MasterThesis/ThesisDamienGille2007.pdf)
    + [Chisel: Constructing Hardware in a Scala Embedded Language](https://chisel.eecs.berkeley.edu/)
        + [UC Berkeley Architecture Research](https://github.com/ucb-bar)
            + [The RISC-V Instruction Set Architecture](http://riscv.org)
                + [Rocket Chip Generator](http://riscv.org/download.html#tab_rocket) 
            + [Rocket Microarchitectural Implementation of RISC-V ISA](https://github.com/ucb-bar/rocket)
            + [Rocket uncore: L2 cache, etc.](https://github.com/ucb-bar/uncore)

+ [CUDA and friends related surveys, papers](https://github.com/alsam/bookmarks/blob/master/hpc.md#cuda-and-friends-related-surveys-papers)

+ [DSLs targeting GPU](https://github.com/alsam/bookmarks/blob/master/hpc.md#dsls-targeting-gpu)

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
            + [The Pochoir Project](http://groups.csail.mit.edu/sct/wiki/index.php?title=The_Pochoir_Project)
        + scala stencils use case    
            + [A Scala Prototype to Generate Multigrid Solver Implementations for Different Problems and Target Multi-Core Platforms](http://arxiv.org/pdf/1406.5369v1.pdf)
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

+ [OpenACC](https://github.com/alsam/bookmarks/blob/master/hpc.md#OpenACC)

+ YaCF: Yet Another Compiler Framework
    + [A programming environment for heterogeneous architectures](http://cap.pcg.ull.es/en/accULL)
    + [YaCF: Yet Another Compiler Framework: Technical Report 02/2013](http://cap.pcg.ull.es/en/system/files/private/YaCF.pdf)
    + [Frangollo: A Run-time Library for OpenACC Support](http://cap.pcg.ull.es/es/system/files/private/Frangollo.pdf)

+ [numerical linear algebra for PDE and more](https://github.com/alsam/bookmarks/blob/master/numerical.md)

+ [Scala links](https://github.com/alsam/bookmarks/blob/master/scala.md)

+ [SBV: SMT Based Verification in Haskell](http://leventerkok.github.io/sbv/)
    + [When is Cheryl's birthday?](http://www.telegraph.co.uk/education/educationnews/11534378/When-is-Cheryls-birthday-The-tricky-math-problem-that-has-everyone-stumped.html)

+ [parallelforall](https://github.com/alsam/bookmarks/blob/master/hpc.md#parallelforall)

+ [(inverse) lithography links](https://github.com/alsam/bookmarks/blob/master/litho.md)

+ [C++ links](https://github.com/alsam/bookmarks/blob/master/cpp.md)
    + [CPP C++ Papyrus](https://github.com/caiorss/C-Cpp-Notes)

+ [Rust links](https://github.com/alsam/bookmarks/blob/master/rust.md)

+ [Julia links](https://github.com/alsam/bookmarks/blob/master/julia.md)

+ [Python links](https://github.com/alsam/bookmarks/blob/master/python.md)

+ [HPC links](https://github.com/alsam/bookmarks/blob/master/hpc.md)

+ [Tips](https://github.com/alsam/bookmarks/blob/master/tips.md)
    + [Technical typesetting](https://github.com/alsam/bookmarks/blob/master/technical_typesetting.md)
    + [Performance optimization](https://github.com/alsam/bookmarks/blob/master/performance_optimization_tips.md)

+ [Machine Learning](https://github.com/alsam/bookmarks/blob/master/machine_learning.md)

+ [Math links](https://github.com/alsam/bookmarks/blob/master/math.md)

+ [Mechanics links](https://github.com/alsam/bookmarks/blob/master/mechanics.md)

+ [tegra + ARM links](https://github.com/alsam/bookmarks/blob/master/tegra.md)

+ [embedded: ARM Mali; Qualcomm Snapdragon + Adreno GPU + Hexagon DSP links](https://github.com/alsam/bookmarks/blob/master/embedded_mali_snapdragon_adreno.md)

+ [3D](https://github.com/alsam/bookmarks/blob/master/3D.md)

+ [Industrial robotics: planning & locomotion & computer vision](https://github.com/alsam/bookmarks/blob/master/industrial_robotics.md)

+ [**IoT** -- **I**nternet **o**f **T**hings](https://github.com/alsam/bookmarks/blob/master/iot.md)

+ [**EE** -- **E**lectrical **E**ngineering](https://github.com/alsam/bookmarks/blob/master/ee.md)

+ [Blogs](https://github.com/alsam/bookmarks/blob/master/blogs.md)

