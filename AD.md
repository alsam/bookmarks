# Automatic Differentiation: mostly Julia, C++, Haskell. Scala as well
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
