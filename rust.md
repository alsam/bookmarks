# rust language bookmarks
+ Rust links
    + [Rust deployment](http://blog.jfo.click/how-rust-do/)
    + [Why Rust?](http://www.oreilly.com/programming/free/files/why-rust.pdf)
    + [The Rust Book](https://doc.rust-lang.org/stable/book/)
        + [An alternative introduction to Rust](http://words.steveklabnik.com/a-new-introduction-to-rust)
        + [24days of rust](http://zsiciarz.github.io/24daysofrust/)
    + [rust-learning](https://github.com/ctjhoa/rust-learning)
    + [http://rustbyexample.com/](http://rustbyexample.com/)
        + [Rust by example](https://github.com/rust-lang/rust-by-example)
    + [Implementing Rosetta Code problems in Rust](https://github.com/Hoverbear/rust-rosetta)
    + [Rust projects](http://www.rust-ci.org/projects/)
        + [Is Rust CI still working?](https://www.reddit.com/r/rust/comments/3blikk/is_rust_ci_still_working/)
    + [Awesome Rust: A curated list of awesome Rust code and resources](https://github.com/kud1ing/awesome-rust)
        + [gmp bindings for rust: status: build failing, ranges syntax changed](https://github.com/thestinger/rust-gmp)
            + [rust-gmp crate](https://crates.io/crates/rust-gmp)
            + [fixed repoworking with up-to-date rust](https://crates.io/crates/rust-gmp)
            + [ramp - A high-performance multiple-precision arithmetic library](https://crates.io/crates/ramp)
                + [ramp github repo](https://github.com/Aatch/ramp)
        + [BLAS bindings](https://github.com/stainless-steel/blas)
        + [LAPACK bindings](https://github.com/stainless-steel/lapack)
            + [Ivan Ukhov](https://github.com/IvanUkhov?tab=repositories)
            + [OpenBLAS Provider](https://github.com/cmr/openblas-provider)
        + [Rayon: A data parallelism library for Rust](https://github.com/huonw/rayon)
            + [Neon: Node + Rust = ������](https://www.reddit.com/r/rust/comments/3y0vx9/neon_node_rust/)
        + [parry - Parallel array processing: deflect performance problems](https://github.com/huonw/parry)
        + [crossbeam - Support for parallelism and low-level concurrency in Rust](https://github.com/aturon/crossbeam)
        + FFT libraries and bindings
            + [crate dft](https://crates.io/crates/dft)
                + [dft docs](http://stainless-steel.github.io/dft/dft/index.html)
            + [crate rustfft - 1.0 follows kiss fft](https://crates.io/crates/rustfft)
            + [crate fftw3 - not complete](https://crates.io/crates/fftw3)
        + [see it for FFI bindings: Rust bindings for libpcuid CPU detection and feature extraction library](https://github.com/zsiciarz/rust-cpuid)
            + [Rust Module std::ptr](https://doc.rust-lang.org/std/ptr/)
    + [Awesome documentation links for Rust](http://diveintodata.org/2015/10/11/rust-awesome-documentation-links/)

    + Are we yet?
        + [Are we (I)DE yet?](https://areweideyet.com/)
        + [Are we web yet?](http://www.arewewebyet.org/)
        + [Are we concurrent yet?](http://areweconcurrentyet.com/)
        + [Are we numeric yet?](https://www.reddit.com/r/rust/comments/4drr2c/are_we_numeric_yet/)
        + [Are we game yet?](http://arewegameyet.com/)
        + [Are we learning yet?](http://www.arewelearningyet.com/)
            + [Are we yet?](https://wiki.mozilla.org/Areweyet) 

    + Rust ownership, lifetimes and borrowing
        + [Why Rust's ownership/borrowing is hard](http://softwaremaniacs.org/blog/2016/02/12/ownership-borrowing-hard/en/)
        + [Explore the ownership system in Rust](http://nercury.github.io/rust/guide/2015/01/19/ownership.html)
        + [Rust ownership, the hard way](http://chrismorgan.info/blog/rust-ownership-the-hard-way.html)
        + [Rust Lifetimes](http://www.charlesetc.com/rust/2015/10/29/)
        + [Lifetime Reference](http://www.charlesetc.com/rust/2015/10/31/)
            + [official lifetimes doc](https://doc.rust-lang.org/book/lifetimes.html)
            + [Aha! Understanding lifetimes in Rust](http://codrspace.com/buntine/aha-understanding-lifetimes-in-rust/)
            + [Lifetime elision in struct impl](https://users.rust-lang.org/t/lifetime-elision-in-struct-impl/4255/6)
        + [Rust, Lifetimes, and Collections](http://cglab.ca/~abeinges/blah/rust-lifetimes-and-collections/)
            + [Problem about borrowing: My timer implementation requires a mutable reference to the timer queue](https://users.rust-lang.org/t/problem-about-borrowing-my-timer-implementation-requires-a-mutable-reference-to-the-timer-queue/4118/1)
            + [Problems with a recursive parser](https://users.rust-lang.org/t/problems-with-a-recursive-parser/7721/8)

    + *Performance Tips*
        + [Profiling Rust applications on Linux](https://llogiq.github.io/2015/07/15/profiling.html)
        ```sh
        operf ./target/debug/add_sum_sq -k 4 -n 100
        opannotate --source --assembly > operf.listing
        ```
        + [cargo subcommand to profile binaries](https://github.com/pegasos1/cargo-profiler)
        + [Rust support in Linux `perf` tool](https://users.rust-lang.org/t/rust-support-in-linux-perf-tool/6513)
        + [What one must understand to be productive with Rust](https://medium.com/@ericdreichert/what-one-must-understand-to-be-productive-with-rust-e9e472116728#.yc1728nv4)
        + [On pattern matching performance in rust](http://www.cjqed.com/blog/rust-pattern-matching-performance/)
            + [Mixing matching, mutation, and moves in Rust](http://blog.rust-lang.org/2015/04/17/Enums-match-mutation-and-moves.html)
            + [Idiomatic way of testing Result<T, Error>?](https://users.rust-lang.org/t/idiomatic-way-of-testing-result-t-error/2171)
        + [Rust Faster!](https://llogiq.github.io/2015/10/03/fast.html)
            + [The Computer Language Benchmarks Game: Rust implementations](https://github.com/TeXitoi/benchmarksgame-rs)
            + [Compile-time type checking for arbitrary unit systems](https://github.com/llogiq/dimensioned)
        + [Сравниваем Swift и Rust](http://habrahabr.ru/post/272681/)
        + [Which language has the brightest future in replacement of C between D, Go and Rust? And Why? Andrei Alexandrescu, D Language Architect](https://www.quora.com/Which-language-has-the-brightest-future-in-replacement-of-C-between-D-Go-and-Rust-And-Why/answer/Andrei-Alexandrescu)
        + [I wrote my Bachelor's thesis about Go and Rust in high-performance computing](https://www.reddit.com/r/rust/comments/34m7gw/i_wrote_my_bachelors_thesis_about_go_and_rust_in/)
            + [bachelor's thesis titled "Evaluation of performance and productivity metrics of potential programming languages in the HPC environment"](https://github.com/mrfloya/thesis-ba)
            + [Evaluation of C, Go, and Rust in the HPC environment](https://news.ycombinator.com/item?id=9477014)
            + [Evaluation of performance and productivity metrics of potential programming languages in the HPC environment - A comparison of Rust, Go and C -- University of Hamburg](https://www.reddit.com/r/programming/comments/34ml5f/evaluation_of_performance_and_productivity/)
            + [Rust programs versus Go by benchmark task performance](http://benchmarksgame.alioth.debian.org/u64q/compare.php?lang=rust&lang2=go)
        + [How to explain slowdown with Sieve of Eratosthenes versus Nim and C?](https://users.rust-lang.org/t/how-to-explain-slowdown-with-sieve-of-eratosthenes-versus-nim-and-c/4394)
        + [Learn Rust: Dining Philosophers runs not concurrent](https://users.rust-lang.org/t/learn-rust-dining-philosophers-runs-not-concurrent/4458)

        + [(more or less) accurate floating point algorithms](https://crates.io/crates/accurate)
        + [Benchmarking programs in Rust](http://stackoverflow.com/questions/13322479/benchmarking-programs-in-rust)
        + [How to `zip` two slices efficiently](https://users.rust-lang.org/t/how-to-zip-two-slices-efficiently/2048)
        + [How to `memcpy` bytes in stable rust](https://users.rust-lang.org/t/how-to-memcpy-bytes-in-stable-rust/2740)
            + [Stabilizing basic functions on arrays and slices: `clone_from_slice`](https://internals.rust-lang.org/t/stabilizing-basic-functions-on-arrays-and-slices/2868)
        + [`Builder` pattern without cloning](https://users.rust-lang.org/t/builder-pattern-without-cloning/2044)
        + [Fearless Concurrency with Rust](http://blog.rust-lang.org/2015/04/10/Fearless-Concurrency.html)
        + [Rust vs. C++: Fine-grained Performance](https://users.rust-lang.org/t/rust-vs-c-fine-grained-performance/4407)
        + [Are we concurrent yet](http://areweconcurrentyet.com/)
        + [cargo benchcmp](https://github.com/BurntSushi/cargo-benchcmp)
            + [Porting cargo benchcmp](https://apanatshka.github.io/compsci/2016/09/04/porting-cargo-benchcmp/)

        + Loop unrolling
            + [Can I create a macro that unrolls loops?](http://stackoverflow.com/questions/30887356/can-i-create-a-macro-that-unrolls-loops)
                + [How do I see the expanded macro code that's causing my compile error?](http://stackoverflow.com/questions/28580386/how-do-i-see-the-expanded-macro-code-thats-causing-my-compile-error)
                    + [macro expand](https://github.com/dtolnay/cargo-expand)
            + [Loop unrolling on request](https://internals.rust-lang.org/t/loop-unrolling-on-request/3091/3)

    + Linear Algebra
        + [Numerics & math foundation](https://users.rust-lang.org/t/numerics-math-foundation/7247
        + [A linear algebra library in Rust designed for machine learning](https://github.com/AtheMathmo/rulinalg)
        + [Linear Algebra in Rust](http://athemathmo.github.io/2016/03/23/linear-algebra-in-rust.html)
        + [Multithreaded matrix multiplication in Rust - Part I](http://athemathmo.github.io/2016/04/16/multithreading-multiplication-1.html)
        + [Multithreaded matrix multiplication in Rust - Part II](http://athemathmo.github.io/2016/04/25/multithreading-multiplication-2.html)
            + [Anatomy of High-Performance Many-Threaded Matrix Multiplication](http://www.cs.utexas.edu/users/flame/pubs/blis3_ipdps14.pdf)
        + [A gemmed rabbit hole](http://bluss.github.io/rust/2016/03/28/a-gemmed-rabbit-hole/)
            + [GEMM in Rust implementation](https://github.com/bluss/matrixmultiply)
        + [Matrix Multiplication in Rust (Part 1)](http://www.suchin.co/2016/04/25/Matrix-Multiplication-In-Rust-Pt-1/)
        + [ndarray: an N-dimensional array with array views, multidimensional slicing, and efficient operations](https://github.com/bluss/rust-ndarray)
            + [ndarray presentation by the author](http://bluss.github.io/rust-ndarray/talk1/)
        + [A Rust linear algebra library based on expression templates](https://github.com/SiegeLord/RustAlgebloat)
            + [Rust’s operator overloading doesn’t scale](https://internals.rust-lang.org/t/rusts-operator-overloading-doesnt-scale/408)
        + [Convolutions in Rust for Deep Learning](https://athemathmo.github.io/2016/04/29/convolutions-deep-learning.html)
            + [Understanding Convolution in Deep Learning](http://timdettmers.com/2015/03/26/convolution-deep-learning/)
            + [Convolutional Neural Networks](http://andrew.gibiansky.com/blog/machine-learning/convolutional-neural-networks/)

        + *Arrayfire*
            + [ArrayFire: a general purpose GPU library. http://arrayfire.com](https://github.com/arrayfire/arrayfire)
                + [ArrayFire install on Ubuntu](http://www.arrayfire.com/docs/installing.htm#Ubuntu) 
                + [ArrayFire convolve1](http://www.arrayfire.com/docs/group__signal__func__convolve1.htm)
            + [Arrayfire Rust Bindings - is a high performance library for parallel computing with an easy-to-use API ](https://github.com/arrayfire/arrayfire-rust)
                + [Function arrayfire::fft_convolve1](http://arrayfire.github.io/arrayfire-rust/arrayfire/fn.fft_convolve1.html)
                    + [a composition of forward fft and inverse ifft operations is not identical to the original vector #51](https://github.com/arrayfire/arrayfire-rust/issues/51)
                    + [Add code examples to documentation #52](https://github.com/arrayfire/arrayfire-rust/issues/52)
    
                requisites
    
                + GLFW
    
                    ```sh
                    ldd ./lu_cpu
                    ...
                    libglfw.so.3 => not found
                    ```
    
                    + [GLFW build apps](http://www.glfw.org/docs/latest/build.html)
    
                    + [GLFW github](https://github.com/glfw/glfw)
                    ```sh
                    git diff -u CMakeLists.txt
                    diff --git a/CMakeLists.txt b/CMakeLists.txt
                    index aa22cc3..0fb3c0e 100644
                    --- a/CMakeLists.txt
                    +++ b/CMakeLists.txt
                    @@ -18,7 +18,7 @@ set(LIB_SUFFIX "" CACHE STRING "Takes an empty string or 64. Directory where lib
                    
                     set_property(GLOBAL PROPERTY USE_FOLDERS ON)
                    
                    -option(BUILD_SHARED_LIBS "Build shared libraries" OFF)
                    +option(BUILD_SHARED_LIBS "Build shared libraries" ON)
                     option(GLFW_BUILD_EXAMPLES "Build the GLFW example programs" ON)
                     option(GLFW_BUILD_TESTS "Build the GLFW test programs" ON)
                     option(GLFW_BUILD_DOCS "Build the GLFW documentation" ON)
                    ```
    
    
                * add to `.bashrc`
                ```sh
                # for ArrayFire
                export AF_PATH=$HOME/work/arrayfire-3
                export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$AF_PATH/lib
                ```
                
                * use *ArrayFire*
                ```sh
                mkdir build
                pushd build
                cmake -DArrayFire_DIR=$AF_PATH/share/ArrayFire/cmake ..
                make VERBOSE=1
                ```
                + [arrayfire-project-templates/CMake/CMakeModules/FindOpenCL.cmake](https://github.com/arrayfire/arrayfire-project-templates/blob/master/CMake/CMakeModules/FindOpenCL.cmake)

    + Asynchronous IO
        + [History and status quo of async/non-blocking I/O in Rust?](https://users.rust-lang.org/t/history-and-status-quo-of-async-non-blocking-i-o-in-rust/6441)
            + [Add a Client Guide](https://github.com/hyperium/hyper/issues/805)
        + [Stateful: A Rust Experimental Syntax Extension for Generators and More](http://erickt.github.io/blog/2016/01/27/stateful-in-progress-generators/)
        + [Pretty State Machine Patterns in Rust](https://hoverbear.org/2016/10/12/rust-state-machine-pattern/)
        + [Async IO for Rust (part II)](https://medium.com/@paulcolomiets/async-io-for-rust-part-ii-33b9a7274e67#.7d7vsjfni)
        + [Condition variable not playing well with `thread::sleep`](http://stackoverflow.com/questions/42353366/condition-variable-not-playing-well-with-threadsleep)

    + Rust parser generators
        + [nom 1.0 Write Really Fast Parsers](https://www.clever-cloud.com/blog/engineering/2015/11/16/nom-1-0/)
            + [nom on github](https://github.com/Geal/nom)
        + [LALRPOP](http://smallcultfollowing.com/babysteps/blog/2015/09/14/lalrpop/)
            + [LALRPOP tutorial](https://github.com/nikomatsakis/lalrpop/blob/master/doc/tutorial.md)
        + [rusty-peg crate](https://crates.io/crates/rusty-peg)
            + [rusty-peg github](https://github.com/nikomatsakis/rusty-peg)
        + [Parser Combinators: The road to Chomp 0.1](https://m4rw3r.github.io/)
            + [A fast monadic-style parser combinator designed to work on stable Rust](https://github.com/m4rw3r/chomp)

    + [Announcing Rust 1.0](http://blog.rust-lang.org/2015/05/15/Rust-1.0.html)
        + [Priorities after 1.0](http://internals.rust-lang.org/t/priorities-after-1-0/1901)

    + [Announcing Rust 1.12](https://blog.rust-lang.org/2016/09/29/Rust-1.12.html)
        + [Announcing Rust 1.12.1](https://blog.rust-lang.org/2016/10/20/Rust-1.12.1.html)

    + [Rust в 2016 году](http://habrahabr.ru/post/274757/)
        + [My thoughts on Rust in 2016](http://www.ncameron.org/blog/my-thoughts-on-rust-in-2016/)

    + [Setting vision for 2017 cycle](https://internals.rust-lang.org/t/setting-our-vision-for-the-2017-cycle/3958/156)
        + [Associated type constructors (a form of higher-kinded polymorphism)](https://github.com/rust-lang/rfcs/pull/1598)
        + [[Roadmap 2017] Productivity: learning curve and expressiveness](https://internals.rust-lang.org/t/roadmap-2017-productivity-learning-curve-and-expressiveness/4097)
        + [Roadmap 2017 request - needs of HPC](https://internals.rust-lang.org/t/roadmap-2017-request-needs-of-hpc/4276)

    + [IDE для Rust](http://rustycrate.ru/%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%B0/2015/12/04/ide-for-rust.html)
        + [Are we (I)DE yet?](http://areweideyet.com/)

    + [rusty-tags : Create ctags/etags for a cargo project and all of its dependencies](https://github.com/dan-t/rusty-tags)

    + [New Rustacean : http://www.newrustacean.com/show_notes/e008/ : http://www.newrustacean.com/show_notes/e008/](http://www.newrustacean.com/show_notes/e008/)
    + [Getting into the nitty-gritty with Rust's traits](http://www.newrustacean.com/show_notes/e009/)

    + ['The Rust Programming Language' E-Books'](http://killercup.github.io/trpl-ebook/)
      + [Rust iterators](https://doc.rust-lang.org/book/iterators.html)
        + [Reddit Rust iterator cheet sheet](https://www.reddit.com/r/rust/comments/38dl0o/rust_iterator_cheat_sheet/)
    + [The Advanced Rust Programming Language](https://doc.rust-lang.org/nightly/adv-book/)
    + [Rust For C++ Programmers](https://github.com/nrc/r4cppp)
        + [blogs: Rust for C++ programmers](http://featherweightmusings.blogspot.co.nz/search/label/rust-for-c)
        + [Arrays and Vectors in Rust](https://github.com/nrc/r4cppp/blob/master/arrays.md)
        + [On rust's memory management: Mainly for C/C++ programmers](http://blog.zgtm.de/)
        + [Why not just add classes?](https://users.rust-lang.org/t/why-not-just-add-classes/4618)
            + [Composition over inheritance](https://en.wikipedia.org/wiki/Composition_over_inheritance)

    + Rust patterns
        + [A catalogue of Rust design patterns](https://github.com/rust-unofficial/patterns)
        + [Rust Patterns: Using traits for function overloading](https://medium.com/@jreem/advanced-rust-using-traits-for-argument-overloading-c6a6c8ba2e17)
            + [rust-modifier: emulates overloading](https://github.com/reem/rust-modifier)
        + [Dependency injection container - Learning the ropes in Rust](http://nercury.github.io/rust/di/2015/01/02/dependency-injection-learning-rust.html)
        + [Rust's flawed dynamic type](https://www.reddit.com/r/rust/comments/3mtim0/rusts_flawed_dynamic_type/)
            + [chris-morgan/mopa](https://github.com/chris-morgan/mopa)
        + [Mixing matching, mutation, and moves in Rust](http://blog.rust-lang.org/2015/04/17/Enums-match-mutation-and-moves.html)

    + [An Adventure in API Design and Concurrency in Rust](http://damienradtke.com/adventures-in-concurrency-1/)
        + [Concurrency in Rust: vimeo video](https://vimeo.com/144809407)
    + [Pros and cons: Rust vs. C++](https://plus.google.com/+nialldouglas/posts/AXFJRSM8u2t)
        + [Rust and the Blub Paradox](http://www.jonathanturner.org/2016/01/rust-and-blub-paradox.html)
             + [You can't spell trust without Rust](https://cdn.rawgit.com/Gankro/thesis/master/thesis.pdf)
             + [You can't spell trust without Rust](https://twitter.com/rustlang/status/689823725219377152)
    + Docs: generation, in Russian, vs. C++
        + [Convert The Rust Programming Language to Epub](https://gist.github.com/killercup/a793e09638379dbc74e4#file-trpl-epub-rb)
        + [The Rust Programming Language (на русском)](https://www.gitbook.com/book/kgv/rust_book_ru/details)
        + [Rust for C++ Programmers](https://www.gitbook.com/book/aminb/rust-for-c/details)
        + [Rust for clojurists](https://gist.github.com/oakes/4af1023b6c5162c6f8f0)
        + [Язык программирования Rust и первые впечатления от него (17 ноября 2014)](http://eax.me/rust/)
            + [Десять веских причин не тащить в продакшн новые игрушки](http://eax.me/avoid-new-toys/)
            + [Criticizing the Rust Language, and Why C/C++ Will Never Die](http://www.viva64.com/en/b/0324/)
    + [epsilonz - Functional Programming in Rust](https://github.com/epsilonz)

    + [Abstracted Algebra in Rust, or, Why Rust is better than C++, part I](http://maniagnosis.crsr.net/2015/07/abstracted-algebra-in-rust.html)
        + [More Abstracted Algebra in Rust, or Does 'Group' distribute over 'Ring'?](http://maniagnosis.crsr.net/2015/07/more-abstracted-algebra-in-rust.html)
    + [Graphs in Rust](http://featherweightmusings.blogspot.co.nz/2015/04/graphs-in-rust.html)
        + [Graphs and arena allocation](https://github.com/nrc/r4cppp/tree/master/graphs)

    + [A library of mesh generation utilities](https://github.com/gfx-rs/genmesh)a

    + [rust on habrahabr](http://habrahabr.ru/hub/rust/)
        + [Многопоточность в Rust](http://habrahabr.ru/post/256211/)
        + [Создание функции на Rust, которая возвращает String или &str](http://habrahabr.ru/post/274565/)
        + [Куча способов переиспользовать код в Rust](https://habrahabr.ru/post/307616/)

    + [Adam Leventhal's blog: First Rust Program Pain (So you can avoid it...)](http://dtrace.org/blogs/ahl/2015/06/22/first-rust-program-pain/)

    + [LLVM изнутри: как это работает](http://habrahabr.ru/post/101838/)

    + [Thorin/Impala paper: A Graph-Based Higher-Order Intermediate Representation](http://compilers.cs.uni-saarland.de/papers/lkh15_cgo.pdf)

    + [unicode chars for idents](http://www.reddit.com/r/rust/comments/2pvksp/filename_with_dots_or_unicode_chars_not_working/)

    + Misc
        + [Implementing Finite Automata (Part 1)](https://apanatshka.github.io/compsci/2016/10/03/implementing-finite-automata-part-1/)
        + [Contributing to Rust]([http://www.ncameron.org/rust.html)
        + [Interview with Mozilla’s Aaron Turon](http://www.pl-enthusiast.net/2015/06/09/interview-with-mozillas-aaron-turon/)
        + [julia vs. rust](http://vschart.com/compare/julia/vs/rust)
        + [Higher kinded polymorphism #324](https://github.com/rust-lang/rfcs/issues/324)
            + [Higher-kinded types #1185 ](https://github.com/rust-lang/rfcs/issues/1185#issuecomment-117812357)
                + [implement higher-order unification for type constructor inference](https://issues.scala-lang.org/browse/SI-2712)
            + [What languages other than Haskell support higher kinded types?](https://www.reddit.com/r/haskell/comments/35ay8f/what_languages_other_than_haskell_support_higher/)

        + [Rust, дисциплинирующий язык программирования](http://habrahabr.ru/company/piter/blog/267203/)
            + [Основы Rust – Глава 2. Использование переменных и типов](http://habrahabr.ru/post/260759/)
            + [Обработка ошибок в Rust](http://habrahabr.ru/post/270371/)
            + [Сопоставление с образцом, изменения и перемещения в Rust](http://habrahabr.ru/post/256941/)
            + [Сравнение производительности языков на примере простейшего классификатора](http://habrahabr.ru/post/261201/)
            + [Заимствование и время существования в Rust](http://habrahabr.ru/post/266715/)
            + [Создаём REST-сервис на PostgreSQL и Rust. Часть 1: прототип](http://habrahabr.ru/post/267477/)
            + [Создаём REST-сервис на Rust. Часть 2: читаем INI; multirust](http://habrahabr.ru/post/267661/)
            + [Создаём REST-сервис на Rust. Часть 3: обновляем базу из консоли](http://habrahabr.ru/post/267779/)
            + [Создаём REST-сервис на Rust. Часть 4: переходим к REST API](http://habrahabr.ru/post/268617/)
            + [Создаём REST-сервис на Rust. Часть 5: обработчики, рефакторинг, и макросы](http://habrahabr.ru/post/269903/)
            + [Rust в деталях: пишем масштабируемый чат с нуля, часть 1](http://habrahabr.ru/post/268609/)
            + [Пишем свой упрощенный OpenGL на Rust — часть 1 (рисуем линию)](http://habrahabr.ru/post/261629/)
            + [Пишем свой упрощенный OpenGL на Rust — часть 2 (проволочный рендер)](http://habrahabr.ru/post/261739/)
            + [Пишем свой упрощенный OpenGL на Rust — часть 3 (растеризатор)](http://habrahabr.ru/post/262235/)

        + [Good Practices for Writing Rust Libraries](https://pascalhertleif.de/artikel/good-practices-for-writing-rust-libraries/)

        + Porting to Rust
            + [C to Rust transpiler, based on cparser](https://github.com/PeterReid/cparser-to-rust)
            + [Type-Safe Unions in C++ and Rust](http://genbattle.bitbucket.org/blog/2016/10/07/Type-Safe-Unions-in-C-and-Rust/)
                + [Beyond Memory Safety With Types](https://insanitybit.github.io/2016/05/30/beyond-memory-safety-with-types)
            + [The Arduous Journey of Porting C to Rust](https://bawk.space/2016/10/06/c-to-rust.html)
            + [Baby Steps: Slowly Porting musl to Rust](http://blog.adamperry.me/rust/2016/06/11/baby-steps-porting-musl-to-rust/)

        + [Iterator trait](https://doc.rust-lang.org/nightly/std/iter/trait.Iterator.html)
            + [iota editor written in Rust; use case for idiomatic iterator usage](https://github.com/gchp/iota/blob/master/src/iota/iterators.rs)

        + [Can't find crate for `num`](http://stackoverflow.com/questions/29189615/cant-find-crate-for-num)

        + [Multiple binaries in Cargo](https://users.rust-lang.org/t/multiple-binaries-in-cargo/3049/2)

        + [Rosetta code for complex in Rust](http://rosettacode.org/wiki/Arithmetic/Complex#Rust)

        + [RustType is a pure Rust alternative to libraries like FreeType](https://github.com/dylanede/rusttype)

        + [Raw Pointers](https://doc.rust-lang.org/nightly/book/raw-pointers.html)
             + [Primitive Type pointer](https://doc.rust-lang.org/nightly/std/primitive.pointer.html)
             + [Dereferencing untyped raw pointer](https://users.rust-lang.org/t/dereferencing-untyped-raw-pointer/896)
             + [Rust FFI and Opaque pointer idiom](https://www.reddit.com/r/rust/comments/2fmvcy/rust_ffi_and_opaque_pointer_idiom/)

        + [Reading binary file](https://users.rust-lang.org/t/reading-binary-files/2132)
        ```rust
        use std::fs::File;
        use std::io::Read;
        
        fn main()
        {
            let mut file=File::open("Cargo.toml").unwrap();
            let mut buf=[0u8;12];
            file.read(&mut buf).unwrap();
            println!("{:?}",buf);
            // use file
        }
        ```

        + [Generics over the size of an array type](https://internals.rust-lang.org/t/generics-over-the-size-of-an-array-type/2845)
        + [Generics, Arrays and Cloning](https://users.rust-lang.org/t/generics-arrays-and-cloning/694/3)
        + [Initialize an array with a closure](http://stackoverflow.com/questions/29682881/initialize-an-array-with-a-closure)
        + [OOP inheritance adapted to Rust](https://internals.rust-lang.org/t/oop-inheritance-adapted-to-rust/586)
            + [Usecases for inheritance](https://users.rust-lang.org/t/usecases-for-inheritance/348)
                + [Rust type system and the Circle-ellipse problem](https://internals.rust-lang.org/t/rust-type-system-and-the-circle-ellipse-problem/3057)
            + [Specialization/Inheritance](https://internals.rust-lang.org/t/specialization-inheritance/3030)
            + [Abstraction without overhead: traits in Rust](http://blog.rust-lang.org/2015/05/11/traits.html)
                + [Most coveted Rust features](https://users.rust-lang.org/t/most-coveted-rust-features/324/15)

    + Useful tips
        + [Read a file line by line](https://users.rust-lang.org/t/read-a-file-line-by-line/1585)

        + [Rust Tips and Tricks](https://thesquareplanet.com/blog/rust-tips-and-tricks/)

        + [Using rustfmt in Vim](http://johannh.me/blog/rustfmt-vim.html)
        ```sh
        # for cargo
        export CARGO_HOME=$HOME/.cargo
        export RUST_SRC_PATH=$HOME/work/github/rust/src
        export PATH=$CARGO_HOME/bin:$PATH
        ```
        ```sh
        cargo install --git 'https://github.com/phildawes/racer.git'
        cargo install --git https://github.com/nrc/rustfmt
        echo 'pub fn main(){println!("hello");}' | rustfmt
        ```
        ```rust
        pub fn main() {
            println!("hello");
        }
        ```

        + [Vim Racer Plugin](https://github.com/racer-rust/vim-racer)
        + [Racer progress update Dec 29, 2015](http://phildawes.net/blog/2015/12/29/racer-update-6/) 

        + [A bunch of lints to catch common mistakes and improve your Rust code](https://github.com/Manishearth/rust-clippy)

        + [Convert string slice to int in rust](http://stackoverflow.com/questions/26919609/convert-string-slice-to-int-in-rust)
        + [Learning to 'try!' things in Rust](http://www.jonathanturner.org/2015/11/learning-to-try-things-in-rust.html)
            + [try!](http://rustbyexample.com/std/result/try.html)

        + [How do I sum a vector using fold?](http://stackoverflow.com/questions/29548819/how-do-i-sum-a-vector-using-fold)


    + Selected RFCs
        + [RFC 1210: impl specialization](https://github.com/rust-lang/rfcs/blob/master/text/1210-impl-specialization.md)
            + [Implement RFC 1210: impl specialization #30652](https://github.com/rust-lang/rust/pull/30652)
            + [Specialize to reuse](https://aturon.github.io/blog/2015/09/18/reuse/)
        + [RFC 1422: pub_restricted](https://github.com/rust-lang/rfcs/blob/master/text/1422-pub-restricted.md)

    + Misc.
        + [Dual numbers in Rust](https://github.com/potan/dual.rs)

        + [libfloat](https://github.com/peterhj/libfloat)

        + [A vantage-point tree implementation backed by vectors for good performance with no unsafe code](https://crates.io/crates/vec-vp-tree)

        + [Special functions for Rust by binding to the Cephes library](https://crates.io/crates/special-fun/)

        + [Library of well known algorithms for numerical root finding](https://crates.io/crates/roots/)

        + [Rust docopt](Library of well known algorithms for numerical root finding)

        + [Rustdoc: reStructuredText vs Markdown: On The Potential Inadequacy of Markdown](https://internals.rust-lang.org/t/rustdoc-restructuredtext-vs-markdown/356/71)

        + [How to implement a C union in Rust](https://users.rust-lang.org/t/how-to-implement-a-c-union-in-rust/3291/4)

        + [Implementation of Software transactional memory](https://crates.io/crates/stm/)

        + [Basic wrapper around libVEX from Valgrind](https://crates.io/crates/libvex-sys/)

        + [Rust implementation of the Quine-McCluskey](https://github.com/oli-obk/quine-mc_cluskey)

        + [cargo-tree](https://github.com/sfackler/cargo-tree)

        + [Rust and Rest](http://lucumr.pocoo.org/2016/7/10/rust-rest/)
            + [Rust bindings to libcurl](https://github.com/alexcrichton/curl-rust)

        produces
        ```sh
        $ cargo tree
        chrono v0.2.17 (file:///Volumes/git/rust/rust-chrono)
        ├── num v0.1.29
        │  ├── rand v0.3.12
        │  │  ├── advapi32-sys v0.1.2
        │  │  │  ├── winapi v0.2.5
        │  │  │  └── winapi-build v0.1.1
        │  │  ├── libc v0.2.4
        │  │  └── winapi v0.2.5 (*)
        │  └── rustc-serialize v0.3.16
        ├── rustc-serialize v0.3.16 (*)
        ├── serde v0.6.6
        │  └── num v0.1.29 (*)
        ├── serde_json v0.6.0
        │  ├── num v0.1.29 (*)
        │  └── serde v0.6.6 (*)
        └── time v0.1.34
           ├── kernel32-sys v0.2.1
           │  ├── winapi v0.2.5 (*)
           │  └── winapi-build v0.1.1 (*)
           ├── libc v0.2.4 (*)
           └── winapi v0.2.5 (*)
        ```

        + [Accumulator factory Rust](http://rosettacode.org/wiki/Accumulator_Factory#Rust)
        ```rust
        use std::ops::Add;
         
        fn foo<Num>(n: Num) -> Box<FnMut(Num) -> Num>
                where Num: Add<Output=Num> + Copy + 'static {
            let mut acc = n;
            Box::new(move |i: Num| {
                acc = acc + i;
                acc
            })
        }
         
        fn main() {
            let mut x = foo(1.);
            x(5.);
            foo(3.);
            println!("{}", x(2.3));
        }
        ```

        + [Accumulator factory C++, see esp. C++11 ](http://rosettacode.org/wiki/Accumulator_Factory#C.2B.2B)

        + [Working around the lack of associated method on parametric traits?](http://stackoverflow.com/questions/27888069/working-around-the-lack-of-associated-method-on-parametric-traits)
        + [cpp-templates-vs-rust-generics](https://gist.github.com/bjz/9220415)
        + [Rust, Generics, and Collections](http://cglab.ca/~abeinges/blah/rust-generics-and-collections/)

    + Ideas, RFCs, that are not in the language yet
        + HKT
            + [Blog post series: Alternative type constructors and HKT](https://internals.rust-lang.org/t/blog-post-series-alternative-type-constructors-and-hkt/4300/89)
                + [Associated type constructors, part 1: basic concepts and introduction](http://smallcultfollowing.com/babysteps/blog/2016/11/02/associated-type-constructors-part-1-basic-concepts-and-introduction/)
                + [Associated type constructors, part 2: family traits](http://smallcultfollowing.com/babysteps/blog/2016/11/03/associated-type-constructors-part-2-family-traits/)
                + [Associated type constructors, part 3: What higher-kinded types might look like](http://smallcultfollowing.com/babysteps/blog/2016/11/04/associated-type-constructors-part-3-what-higher-kinded-types-might-look-like/)
                + [Associated type constructors, part 4: Unifying ATC and HKT](http://smallcultfollowing.com/babysteps/blog/2016/11/09/associated-type-constructors-part-4-unifying-atc-and-hkt/)
            + [Higher-kinded type trait](https://www.reddit.com/r/rust/comments/31g0qd/higherkinded_type_trait/)
            + [GitHub Gist for HKT](https://gist.github.com/14427)
            + [Rust and the Monad trait - Not just higher kinded types](https://m4rw3r.github.io/rust-and-monad-trait/)
            + [Reddit: Rust and the Monad trait - Not just higher kinded types](https://www.reddit.com/r/rust/comments/3li3by/rust_and_the_monad_trait_not_just_higher_kinded/)
            + [Higher Kinded Types](http://cglab.ca/~abeinges/blah/rust-reuse-and-recycle/#higher-kinded-types)
            + [Does rust really need higher kinded types?](https://users.rust-lang.org/t/does-rust-really-need-higher-kinded-types/5531/28)
                + [High Order Function with Type Parameter](https://users.rust-lang.org/t/high-order-function-with-type-parameter/3112)
                + [Design patterns for composability with traits (i.e. typeclasses)?](https://users.rust-lang.org/t/design-patterns-for-composability-with-traits-i-e-typeclasses/5569/)
        + [`step_by` on negative numbers](https://internals.rust-lang.org/t/step-by-on-negative-numbers/2231)
        + [GPU support](https://internals.rust-lang.org/t/single-source-gpu-support/898/13)
49)
        + [Add LaTeX support to Rustdoc](https://github.com/rust-lang/rust/issues/34261)
            + [ Add Mathjax (KaTeX?) Support to Rustdoc #16300 ](https://github.com/rust-lang/rust/issues/16300)
            + [ Add mathematics support to rustdoc #17390 ](https://github.com/rust-lang/rust/pull/17390#issuecomment-61195381)
            + [Rustdoc: reStructuredText vs Markdown](https://internals.rust-lang.org/t/rustdoc-restructuredtext-vs-markdown/356/63)
        + GC in Rust
            + [GC and Rust Part 0: Garbage Collection Background](http://blog.pnkfx.org/blog/2015/10/27/gc-and-rust-part-0-how-does-gc-work/)
            + [GC and Rust Part 1: Specifying the Problem](http://blog.pnkfx.org/blog/2015/11/10/gc-and-rust-part-1-specing-the-problem/)
            + [GC and Rust Part 2: The Roots of the Problem](http://blog.pnkfx.org/blog/2016/01/01/gc-and-rust-part-2-roots-of-the-problem/)

    + [Algorithms and Concepts from Stepanov's "Elements of Programming" implemented in Rust](https://github.com/keean/elements_in_rust)

    + [Machine Learning in Rust](https://github.com/alsam/bookmarks/blob/master/machine_learning.md#Rust based projects)
        + [rustlearn - A machine learning package for Rust](https://github.com/maciejkula/rustlearn)

    + [The Kolmogorov-Smirnov Test](http://daithiocrualaoich.github.io/kolmogorov_smirnov/)
        + [Implementation of the Kolmogorov-Smirnov statistical test as a Rust library](https://github.com/daithiocrualaoich/kolmogorov_smirnov)

    + [rand : A Rust library for random number generators and other randomness functionality.](https://github.com/rust-lang-nursery/rand)
        + [Fails to compile on newest Rust 1.7.0 (2016-01-04) #91](https://github.com/rust-lang-nursery/rand/issues/91)
            + [Type inference(?) regression, rand fails to build on nightly 2016-01-04 #30713](https://github.com/rust-lang/rust/issues/30713) 

    + [A library for differential-geometric calculations](https://crates.io/crates/differential-geometry/)
        + [A Rust crate for differential-geometric calculations](https://github.com/fizyk20/differential-geometry)
        + [Differential geometry in Rust](http://ebvalaim.mydevil.net/en/2015/12/18/differential-geometry-in-rust/)
            + [Possible bug in trait bounds evaluation #30262](https://github.com/rust-lang/rust/issues/30262)

    + [A native-rust implementation of an Effect monad, inspired by PureScript's EFF Monad](https://crates.io/crates/effect-monad/)

    + [pijul - distributed version control system written in Rust](https://pijul.org)

    + [`Recycle` - ergonomic allocated memory reusing.](https://www.reddit.com/r/rust/comments/521vxl/recyle_ergonomic_allocated_memory_reusing/)

    + [Lock free stack](https://crates.io/crates/concurrent-stack)
        + [Lock free stack on github](https://github.com/lucklove/concurrent-stack)
        + [AtomicPtr with stamp to avoid ABA problem](https://github.com/lucklove/atomic-stamped-ptr)
        + [AtomicU128 for x86_64](https://github.com/lucklove/atomic128)

    + Hardware (bare metal) - OSes, ISA simulators,etc.
        + DBus
            + [DBus projects in Rust](https://crates.io/search?q=dbus)

            + [D-Bus Desktop Notification using dbus-rs](http://stackoverflow.com/questions/29800616/d-bus-desktop-notification-using-dbus-rs)
                + [Send Desktop Notifications on linux and bsd](https://github.com/hoodie/notify-rust)
                    + [Handpicked Rusty Crates](http://blog.hoodie.de/2016/04/30/handpicked-rusty-crates/)
 
        + [Writing an OS in Rust](http://os.phil-opp.com/)
            + [Page Tables](http://os.phil-opp.com/modifying-page-tables.html)
        + [A comparison of operating systems written in Rust](https://github.com/flosse/rust-os-comparison)
            + Redox: A Rust Operating System
                + [github redox os](https://github.com/redox-os/redox)
                    + [This Week in Redox 5](http://www.redox-os.org/news/this-week-in-redox-5/)
                    + [Sodium: Vim 2.0](https://github.com/redox-os/sodium)
                        + [the Redox editor now is here](https://github.com/redox-os/editor)
                    + [Redox is Serious](http://dictator.redox-os.org/index.php?controller=post&action=view&id_post=17)
                    + [ion-shell](https://crates.io/crates/ion-shell/)
                        + [redox-os/ion](https://github.com/redox-os/ion)
                    + [The Orbital Widget Toolkit](https://crates.io/crates/orbtk/)
        + [rustv - A minimal, intentionally inaccurate RISC-V ISA simulator](https://crates.io/crates/rustv/)
            + [about RISC-V and Rocket processor see The RISC-V Instruction Set Architecture](http://riscv.org/)
            + [see also Chisel - Constructing Hardware in a Scala Embedded Language](https://chisel.eecs.berkeley.edu/)

        + [Grover: Why Rust for Low-level Linux programming?](https://lwn.net/Articles/690821/)

        + [CLOCK-Pro: An Effective Improvement of the CLOCK Replacement](http://static.usenix.org/event/usenix05/tech/general/full_papers/jiang/jiang_html/html.html)

        + [rust-cross](https://github.com/japaric/rust-cross)

    + Formal Verification
        + [Simple verification of Rust programs via functional purification](https://github.com/Kha/electrolysis)
            + [LEAN](https://github.com/leanprover/lean)
            + [Theorem Proving in Lean](https://leanprover.github.io/tutorial/index.html)
        + [A Formal Verification of Rust's Binary Search Implementation](https://kha.github.io/2016/07/22/formally-verifying-rusts-binary-search.html)
        + [GitHub - Kha/electrolysis: Simple verification of Rust programs via functional purification](https://www.reddit.com/r/rust/comments/4ty6z8/github_khaelectrolysis_simple_verification_of/)
        + [Electrolysis Reference](http://kha.github.io/electrolysis/)

    + Linux distros Rust support
        + [Fedora to support Rust Compiler](https://fedoraproject.org/wiki/Changes/RustCompiler) 
