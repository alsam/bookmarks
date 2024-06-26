# Rust language bookmarks
+ Rust links
    + [The Little Book of Rust Books](https://lborb.github.io/book/)
    + [Learn Rust: A Resource Guide](https://serokell.io/blog/learn-rust)
    + [Learn Rust With Entirely Too Many Linked Lists](https://rust-unofficial.github.io/too-many-lists/)
    + [Welcome to Comprehensive Rust](https://google.github.io/comprehensive-rust/)
    + [Item 3: Avoid matching Option and Result](https://lurklurk.org/effective-rust/transform.html)
    + [Rust Memory Container Cheat-sheet](https://github.com/usagi/rust-memory-container-cs)
        + [Ownership Concept Diagram](https://www.reddit.com/r/rust/comments/mgh9n9/ownership_concept_diagram/)
    + [Rust 2020 Roadmap](https://github.com/nikomatsakis/rfcs/blob/roadmap-2020/text/0000-roadmap-2020.md)
        + [Tracking issue for generic associated types (GAT)](https://github.com/rust-lang/rust/issues/44265)
            + [tracking issue for "chalkification"](https://github.com/rust-lang/rust/issues/48049)
            + [Solving the Generalized Streaming Iterator Problem without GATs](http://lukaskalbertodt.github.io/2018/08/03/solving-the-generalized-streaming-iterator-problem-without-gats.html)
            + [Generalized Autoref-Based Specialization](http://lukaskalbertodt.github.io/2019/12/05/generalized-autoref-based-specialization.html)
                + [ICE when using GATs with const generics](https://github.com/rust-lang/rust/issues/75415)
            + [Allow generic associate types in trait paths](https://github.com/rust-lang/rust/issues/67510)
                + [WIP Generic associated types in trait paths](https://github.com/rust-lang/rust/pull/78978)
                    + [Generic Associated Types in Trait Paths - Ast part](https://github.com/rust-lang/rust/pull/79266)
                    + [Method for Emulating Higher-Kinded Types in Rust](https://gist.github.com/edmundsmith/855fcf0cb35dd467c29a9350481f0ecf)
                        + [Higher Kinded Types in Rust](https://hugopeters.me/posts/14/)
            + [Monads and GATs in nightly Rust](https://www.fpcomplete.com/blog/monads-gats-nightly-rust/)
                + [GATs on Nightly!](https://www.reddit.com/r/rust/comments/k4vzvp/gats_on_nightly/)
            + [How can I avoid GATs in this code?](https://users.rust-lang.org/t/how-can-i-avoid-gats-in-this-code/48673)
                + [Trait constraints solver with GAT and recursive types](https://users.rust-lang.org/t/trait-constraints-solver-with-gat-and-recursive-types/73676)
        + [Tracking issue for const generics](https://github.com/rust-lang/rust/issues/44580)
            + [Splitting the const generics features](https://blog.rust-lang.org/inside-rust/2021/09/06/Splitting-const-generics.html)
            + [Tracking Issue for `min_const_generics`](https://github.com/rust-lang/rust/issues/74878)
                + [stabilize `#![feature(min_const_generics)]` in 1.50](https://github.com/rust-lang/rust/pull/79135)
                    + [cycle errors for unevaluated constants in the param env](https://github.com/rust-lang/rust/issues/79356)
                + [`min_const_generics` prevents references to concrete `Self` param](https://github.com/rust-lang/rust/issues/75486)
                + [Shipping Const Generics in 2020](https://without.boats/blog/shipping-const-generics/)
                    + [fix unification of const variables](https://github.com/rust-lang/rust/pull/74040)
                + [Making elementwise operations using const generics more ergonomic? (Possible new trait or FromIterator impl)](making-elementwise-operations-using-const-generics-more-ergonomic-possible-new-trait-or-fromiterator-impl)
                + [Implementing ArrayVec Using Const Generics](https://adventures.michaelfbryan.com/posts/const-arrayvec/)
                + [Add section ch19-07 on Const Generics](https://github.com/rust-lang/book/pull/2776/files)
                + [Preserving the programmers ‘Intent’ in Unsafe Rust](https://levelup.gitconnected.com/preserving-the-programmers-intent-in-unsafe-rust-beaa3266f43f)
                    + [Question on `const-generics`](https://users.rust-lang.org/t/question-on-const-generics/54381)
            + [Tracking issue for "Lazy normalization"](https://github.com/rust-lang/rust/issues/60471)
                + [check it](https://medium.com/tips-for-rust-developers/const-generics-eb46940a07e3)
                tl;dr it works!
                ```rust
                #![feature(const_generics)]
                struct MyVec<T: Sized, const LENGTH: usize> {
                    inner_data: [T; LENGTH],
                }
                
                impl<T: Copy, const L: usize> MyVec<T, L> {
                    pub fn new(value: T) -> Self {
                        MyVec {
                            inner_data: [value; L],
                        }
                    }
                }
                
                fn main() {
                    let _my_vec = MyVec::<f64, 10>::new(4.2);
                    println!("_my_vec[0] : {}", _my_vec.inner_data[0])
                } 
                ```
            + [Tracking Issue for complex generic constants (`const_evaluatable_checked`) ](https://github.com/rust-lang/rust/issues/76560)
                + [Const well-formedness and const equality](https://hackmd.io/OZG_XiLFRs2Xmw5s39jRzA?view)
                + [Addition does not commute in generic_const_exprs](https://github.com/rust-lang/rust/issues/101849)
        + [Tracking issue for specialization (RFC 1210)](https://github.com/rust-lang/rust/issues/31844)
        + [ [Analysis / Pre-RFC] Variadic generics in Rust](https://internals.rust-lang.org/t/analysis-pre-rfc-variadic-generics-in-rust/13879/39)
            + [About variadics in Rust](https://gist.github.com/PoignardAzur/aea33f28e2c58ffe1a93b8f8d3c58667)
            + [ [Brainstorming] Use cases for variadic generics](https://www.reddit.com/r/rust/comments/l8vaa6/brainstorming_use_cases_for_variadic_generics/)
    + [Rust Tutorial playlist](https://www.youtube.com/playlist?list=PLLqEtX6ql2EyPAZ1M2_C0GgVd4A-_L4_5)
        + [Rust Structs, Traits and Impl](https://www.youtube.com/watch?v=gi0AQ78diSA)
        + [Rust Generics](https://www.youtube.com/watch?v=nvur2Ast8hE&list=PLLqEtX6ql2EyPAZ1M2_C0GgVd4A-_L4_5&index=13&t=0s)
        + [Rust Ownership and Borrowing](https://www.youtube.com/watch?v=lQ7XF-6HYGc&list=PLLqEtX6ql2EyPAZ1M2_C0GgVd4A-_L4_5&index=14&t=0s)
        + [Rust Lifetimes](https://www.youtube.com/watch?v=1QoT9fmPYr8&list=PLLqEtX6ql2EyPAZ1M2_C0GgVd4A-_L4_5&index=15&t=0s)
            + [Additional examples to Rust borrowing/lifetimes topic](https://www.youtube.com/watch?v=qzp9gD6BfU4)
        + [Rust 3D Graphics in the Browser: Boilerplate Setup and WASM Introduction](https://www.youtube.com/watch?v=p7DtoeuDT5Y&list=PLLqEtX6ql2EyPAZ1M2_C0GgVd4A-_L4_5&index=21&t=0s)
        + [Rust 3D Graphics in the Browser: 2D Graphics](https://www.youtube.com/watch?v=kjYCSySObDo&list=PLLqEtX6ql2EyPAZ1M2_C0GgVd4A-_L4_5&index=22&t=0s)
        + [Rust 3D Graphics in the Browser: 3D Graphics](https://www.youtube.com/watch?v=K63uBfs1K7Y&list=PLLqEtX6ql2EyPAZ1M2_C0GgVd4A-_L4_5&index=23&t=0s)
    + Jon Gjengset's playlists
        + [Desktop and editor setup for Rust development](https://www.youtube.com/watch?v=ycMiMDHopNc)
        + [Crust of Rust: Lifetime Annotations](https://www.youtube.com/watch?v=rAl-9HwD858&t=1192s)
        + [Porting Flamegraph to Rust](https://www.youtube.com/playlist?list=PLqbS7AVVErFimAvMW-kIJUwxpPvcPBCsz)
            + [Flame Graphs](http://www.brendangregg.com/flamegraphs.html)
        + Implementing TCP in Rust
            + [Implementing TCP in Rust (part 1)](https://www.youtube.com/watch?v=bzja9fQWzdA)
            + [Implementing TCP in Rust (part 2)](https://www.youtube.com/watch?v=OCpt1I0MWXE)
            + [Implementing TCP in Rust (part 3)](https://www.youtube.com/watch?v=8GE6ltLRJA4)
        + [Advanced topics in Rust](https://www.youtube.com/playlist?list=PLqbS7AVVErFgMPqz5irpWbBInR6hxDbYi)
            + [The Why, What, and How of Pinning in Rust](https://www.youtube.com/watch?v=DkMwYxfSYNQ&list=PLqbS7AVVErFgMPqz5irpWbBInR6hxDbYi&index=2)
        + [Java's ConcurrentHashMap in Rust](https://www.youtube.com/playlist?list=PLqbS7AVVErFj824-6QgnK_Za1187rNfnl)
            + [Porting Java's ConcurrentHashMap to Rust (part 1)](https://www.youtube.com/watch?v=yQFWmGaFBjk&list=PLqbS7AVVErFj824-6QgnK_Za1187rNfnl)
            + [Porting Java's ConcurrentHashMap to Rust (part 2)](https://www.youtube.com/watch?v=018GXMjfdqg&list=PLqbS7AVVErFj824-6QgnK_Za1187rNfnl&index=2)
            + [Porting Java's ConcurrentHashMap to Rust (part 3)](https://www.youtube.com/watch?v=_z4fZkmlvrs&list=PLqbS7AVVErFj824-6QgnK_Za1187rNfnl&index=3)
            + [learning-rust-crossbeam-epoch](https://codeandbitters.com/learning-rust-crossbeam-epoch/)
        + [Rust open-source contributions stream](https://www.youtube.com/watch?v=8UzLuMiGs9s)
    + [Rust for Java Devs](https://leshow.github.io/post/rust_for_java_devs/)
    + [Rust deployment](http://blog.jfo.click/how-rust-do/)
    + [Why Rust?](http://www.oreilly.com/programming/free/files/why-rust.pdf)
    + [The Rust Book](https://doc.rust-lang.org/stable/book/)
        + [An alternative introduction to Rust](http://words.steveklabnik.com/a-new-introduction-to-rust)
        + [A Gentle Introduction To Rust](http://stevedonovan.github.io/rust-gentle-intro/readme.html)
        + [24days of rust](http://zsiciarz.github.io/24daysofrust/)
    + [rust-learning](https://github.com/ctjhoa/rust-learning)
        + [Building a runtime reflection system for Rust (Part 1: dyn Class)](https://www.osohq.com/post/rust-reflection-pt-1)
        + [Building a runtime reflection system for Rust (Part 2: dyn Attribute)](https://www.osohq.com/post/runtime-reflection-pt-2)
    + [http://rustbyexample.com/](http://rustbyexample.com/)
        + [Rust by example](https://github.com/rust-lang/rust-by-example)
    + [Implementing Rosetta Code problems in Rust](https://github.com/Hoverbear/rust-rosetta)
    + [Small but painful annoyances when writing Rust code](https://internals.rust-lang.org/t/small-but-painful-annoyances-when-writing-rust-code/5347)
    + [Rust projects]
        + [Trending Rust projects](https://github.com/trending/rust)
        + [Is Rust CI still working?](https://www.reddit.com/r/rust/comments/3blikk/is_rust_ci_still_working/)
        + [huonw/travis-cargo](https://github.com/huonw/travis-cargo)
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
            + [Neon: Node + Rust = Sparkling Heart](https://www.reddit.com/r/rust/comments/3y0vx9/neon_node_rust/)
        + FFT libraries and bindings
            + [RustFFT = "5.0.0-experimental.1"](https://crates.io/crates/rustfft/5.0.0-experimental.1)
                + [Released RustFFT 5.0.0-experimental.1: Now faster than FFTW!](https://www.reddit.com/r/rust/comments/kh2sfb/released_rustfft_500experimental1_now_faster_than/)
                + [RustFFT](https://github.com/ejmahler/RustFFT)
                    + [RustDCT](https://github.com/ejmahler/rust_dct)
            + [crate dft](https://crates.io/crates/dft)
                + [dft docs](http://stainless-steel.github.io/dft/dft/index.html)
            + [crate rustfft - 1.0 follows kiss fft](https://crates.io/crates/rustfft)
            + [crate fftw3 - not complete](https://crates.io/crates/fftw3)
            + [ndrustfft: n-dimensional real-to-complex FFT and real-to-real DCT](https://github.com/preiter93/ndrustfft)
        + [see it for FFI bindings: Rust bindings for libpcuid CPU detection and feature extraction library](https://github.com/zsiciarz/rust-cpuid)
            + [Rust Module std::ptr](https://doc.rust-lang.org/std/ptr/)
    + [Awesome documentation links for Rust](http://diveintodata.org/2015/10/11/rust-awesome-documentation-links/)
    + [Rust release milestone predictions](https://internals.rust-lang.org/t/rust-release-milestone-predictions/4591/12)

    + Are we yet?
        + [Are we (I)DE yet?](https://areweideyet.com/)
        + [Are we web yet?](http://www.arewewebyet.org/)
        + [dead link : Are we concurrent yet?](http://areweconcurrentyet.com/)
        + [Are we numeric yet?](https://www.reddit.com/r/rust/comments/4drr2c/are_we_numeric_yet/)
            + [Making Rust a perfect fit for high-performance computations](https://gist.github.com/HadrienG2/e9a875bdf98b528594f4e20f8176bb68)
        + [Are We Stdlib Yet?](https://www.reddit.com/r/rust/comments/5oqjnn/are_we_stdlib_yet/)
        + [Are we game yet?](http://arewegameyet.com/)
        + [Are we learning yet?](http://www.arewelearningyet.com/)
            + [Scientific Computing](http://www.arewelearningyet.com/scientific-computing/)
            + [Are we yet?](https://wiki.mozilla.org/Areweyet) 
                + [Taking ML to production with Rust: a 25x speedup](https://www.lpalmieri.com/posts/2019-12-01-taking-ml-to-production-with-rust-a-25x-speedup/)

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
        + [Rust Performance Pitfalls](https://llogiq.github.io/2017/06/01/perf-pitfalls.html)
        + [Profiling Rust applications on Linux](https://llogiq.github.io/2015/07/15/profiling.html)
        + [Intro to rustc's self profiler](https://blog.rust-lang.org/inside-rust/2020/02/25/intro-rustc-self-profile.html)
        + [A Better Rust Profiler](https://matklad.github.io/2021/02/10/a-better-profiler.html)
            + [Statistics-driven Microbenchmarking in Rust](https://github.com/bheisler/criterion.rs)
            + [Experimental One-shot Benchmark Framework in Rust](https://github.com/bheisler/iai)
            + [perf-event: a Rust interface to Linux performance monitoring](https://github.com/jimblandy/perf-event)
        + [Rust vs. C++: Fine-grained Performance](https://lobste.rs/s/oxuwzf/rust_vs_c_fine_grained_performance#c_0bhl8y)
        ```sh
        operf ./target/debug/add_sum_sq -k 4 -n 100
        opannotate --source --assembly > operf.listing
        ```
        + Learn Rust the Dangerous Way
            + [Why Learn Rust the Dangerous Way?](http://cliffle.com/p/dangerust/0/)
            + [You Can't Write C in Just Any Ol' Language: Learn Rust the Dangerous Way, Part 1](http://cliffle.com/p/dangerust/1/)
            + [References Available Upon Request: Learn Rust the Dangerous Way, Part 2](http://cliffle.com/p/dangerust/2/)
            + [Measure What You Optimize: Learn Rust the Dangerous Way, Part 3](http://cliffle.com/p/dangerust/3/)
            + [A More Perfect Union: Learn Rust the Dangerous Way, Part 4](http://cliffle.com/p/dangerust/4/)
            + [Making Safe Things From Unsafe Parts: Learn Rust the Dangerous Way, Part 5](http://cliffle.com/p/dangerust/5/)
            + [Let The Compiler Do The Work: Learn Rust the Dangerous Way, Part 6](http://cliffle.com/p/dangerust/6/)
        + [cargo subcommand to profile binaries](https://github.com/pegasos1/cargo-profiler)
        + [Rust support in Linux `perf` tool](https://users.rust-lang.org/t/rust-support-in-linux-perf-tool/6513)
        + [What one must understand to be productive with Rust](https://medium.com/@ericdreichert/what-one-must-understand-to-be-productive-with-rust-e9e472116728#.yc1728nv4)
        + [On pattern matching performance in rust](http://www.cjqed.com/blog/rust-pattern-matching-performance/)
            + [Mixing matching, mutation, and moves in Rust](http://blog.rust-lang.org/2015/04/17/Enums-match-mutation-and-moves.html)
            + [Idiomatic way of testing Result<T, Error>?](https://users.rust-lang.org/t/idiomatic-way-of-testing-result-t-error/2171)
                + [How to Design For Panic Resilience in Rust](https://towardsdatascience.com/how-to-design-for-panic-resilience-in-rust-55d5fd2478b9) 
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

        + [(more or less) accurate floating point algorithms](https://crates.io/crates/accurate)
        + [Benchmarking programs in Rust](http://stackoverflow.com/questions/13322479/benchmarking-programs-in-rust)
        + [How to `zip` two slices efficiently](https://users.rust-lang.org/t/how-to-zip-two-slices-efficiently/2048)
        + [How to `memcpy` bytes in stable rust](https://users.rust-lang.org/t/how-to-memcpy-bytes-in-stable-rust/2740)
            + [Stabilizing basic functions on arrays and slices: `clone_from_slice`](https://internals.rust-lang.org/t/stabilizing-basic-functions-on-arrays-and-slices/2868)
        + [`Builder` pattern without cloning](https://users.rust-lang.org/t/builder-pattern-without-cloning/2044)
        + [Fearless Concurrency with Rust](http://blog.rust-lang.org/2015/04/10/Fearless-Concurrency.html)
        + [Rust vs. C++: Fine-grained Performance](https://users.rust-lang.org/t/rust-vs-c-fine-grained-performance/4407)
        + [cargo benchcmp](https://github.com/BurntSushi/cargo-benchcmp)
            + [Porting cargo benchcmp](https://apanatshka.github.io/compsci/2016/09/04/porting-cargo-benchcmp/)

        + [Macros in Rust: A tutorial with examples](https://blog.logrocket.com/macros-in-rust-a-tutorial-with-examples/)
            + [How do I create a Rust macro with optional parameters using repetitions?](https://stackoverflow.com/questions/34373169/how-do-i-create-a-rust-macro-with-optional-parameters-using-repetitions)
            + [macro expand](https://github.com/dtolnay/cargo-expand)
            + Loop unrolling
                + [Can I create a macro that unrolls loops?](http://stackoverflow.com/questions/30887356/can-i-create-a-macro-that-unrolls-loops)
                    + [How do I see the expanded macro code that's causing my compile error?](http://stackoverflow.com/questions/28580386/how-do-i-see-the-expanded-macro-code-thats-causing-my-compile-error)
            + [Loop unrolling on request](https://internals.rust-lang.org/t/loop-unrolling-on-request/3091/3)

    + Linear Algebra + Numerics
        + [faer is a collection of crates that implement low level linear algebra routines in pure Rust](https://github.com/sarah-ek/faer-rs)
            + [faer announcement on reddit](https://www.reddit.com/r/rust/comments/z17l0g/introducing_faer_a_linear_algebra_library_in_rust/)
        + [Rust Science crates](https://lib.rs/science)
            + [Russell - Rust Scientific Library](https://github.com/cpmech/russell)
            + [aegir is an experimental autodifferentiation framework designed to leverage the powerful type-system in Rust and avoid runtime as much as humanly possible](https://github.com/tspooner/aegir)
            + [argmin is a numerical optimization library written entirely in Rust](https://github.com/argmin-rs/argmin)
            + [Arbitrary-Precision Floating-Point Library](https://github.com/nadavrot/arpfloat)
        + [Mathru crate](https://crates.io/crates/mathru)
            + [Mathru Getting started](https://matthiaseiholzer.gitlab.io/mathru/getting-started/)
            + [mathru](https://gitlab.com/matthiaseiholzer/mathru)
        + [Scientific computing: a Rust adventure [Part 0 - Vectors] ](https://www.lpalmieri.com/posts/2019-02-23-scientific-computing-a-rust-adventure-part-0-vectors/)
        + [Scientific computing: a Rust adventure [Part 1 - Zero-cost abstractions] ](https://www.lpalmieri.com/posts/2019-03-12-scientific-computing-a-rust-adventure-part-1-zero-cost-abstractions/)
        + [Eigenvalue Decomposition](https://github.com/felipeZ/eigenvalues)
        + [Scientific computing: a Rust adventure [Part 2 - Array1] ](https://www.lpalmieri.com/posts/2019-04-07-scientific-computing-a-rust-adventure-part-2-array1/)
        + [Ventifact’s Linear Algebra. A place for learning about and sharing linear algebra.](https://medium.com/ventifacts-linear-algebra)
            + [Writing A Linear Algebra Library in Rust, Part I](https://medium.com/ventifacts-linear-algebra/1-a-linear-algebra-library-in-rust-237d3f465675)
            + [Ventifact's Linear Algebra](https://github.com/ventifact/ventifacts-linear-algebra)
        + [diffeq](https://github.com/mattsse/diffeq)
            + [diffeq | Lorenz Attractor](https://mattsse.github.io/diffeq/)
            + [diffeq - Basic Ordinary Differential Equation solvers](https://www.reddit.com/r/rust/comments/euq5xg/diffeq_basic_ordinary_differential_equation/)
        + [Surface reconstruction library and CLI for particle data from SPH simulations](https://github.com/w1th0utnam3/splashsurf)
            + [numeric_literals](https://github.com/Andlon/numeric_literals)
        + [FENRIS: A Rust library for building advanced applications with the Finite Element Method (FEM)](https://github.com/InteractiveComputerGraphics/fenris)
        + [Scientific Computing in Rust: bacon-sci](https://github.com/aftix/bacon)
            + [Scientific Computing in Rust: bacon-sci](https://aftix.xyz/home/bacon/)
        + [Rust 2020: Scientific Rust](https://github.com/willi-kappler/rust_2020)
            + [Staggered-Grid Fluid Solver in Rust](https://github.com/seanlth/Fluid-Solver)
            + [Weak Galerkin Finite Element Method -- looks promising but very outdated](https://github.com/scharris/WGFEM-Rust)
                + for translation to modern Rust:
                    + [The Periodic Table of Rust Types: ycombinator](https://news.ycombinator.com/item?id=7060951)    
                        tl;dr **sigil ~** -> `Box`
                    + [The Periodic Table of Rust Types](https://cosmic.mearie.org/2014/01/periodic-table-of-rust-types/0.11)
                    + [A quick reference of the sigils and their meaning](https://github.com/rust-lang/rust-wiki-backup/blob/master/Sigil-reference.md)
            + [A curated list of Rust code and resources that do NOT exist yet, but would be beneficial to the Rust community.](https://github.com/not-yet-awesome-rust/not-yet-awesome-rust)
        + [Rust 2019: Beat C++ ?](https://www.reddit.com/r/rust/comments/acjcbp/rust_2019_beat_c/)
            + [Rust numeric-array](https://crates.io/crates/numeric-array)
            + [Embedded Rust arithmetic, 2D/3D vector, and statistics library](https://github.com/neobirth/micromath)
        + [Special functions for Rust by binding to the Cephes library](https://crates.io/crates/special-fun/)
        + [Library of well known algorithms for numerical root finding](https://crates.io/crates/roots/)
        + [rcpr - Rust Chebyshev Proxy Rootfinder: A robust global rootfinder using adaptive Chebyshev interpolation with automatic subdivision that accurately finds all roots of a smooth function F(x) on [a, b] using the Chebyshev-Frobenius companion matrix](https://github.com/drobnyjt/rcpr)
        + [funspace - chebyshev](https://github.com/preiter93/funspace)
        + [Polsim - a case study for small-scale scientific computing in Rust](https://tinkering.xyz/polsim/)
            + [Simulate the polarization of a laser beam](https://github.com/zmitchell/polarization)
            + [A command line utility for doing polarization simulations](https://github.com/zmitchell/polsim)
        + [a collection of Summation By Parts operators which can be used for solving partial differential equations](https://github.com/mulimoen/SummationByParts)
            + [Solving the compressible Euler equations by using the SBP-SAT method](https://gitlab.com/mulimoen/EulerSolver)
        + [FEM_2D: A Rust Package for 2D Finite Element Method Computations with Extensive Support for hp-refinement](https://www.techrxiv.org/articles/preprint/FEM_2D_A_Rust_Package_for_2D_Finite_Element_Method_Computations_with_Extensive_Support_for_hp-refinement/19166339)
            + [fem_2d](https://github.com/jeremiah-corrado/fem_2d) 
        + [Fast Fluid Dynamics Built with Rust+WASM and WebGL](https://github.com/sanjayyepuri/fluids)
        + [ponyo - A 2D, semi-Lagrangian fluid solver](https://github.com/mwalczyk/ponyo)

        + [delaunator-rs A very fast static 2D Delaunay triangulation library for Rust. A port of Delaunator](https://github.com/mourner/delaunator-rs)
        + [Implementation of a 2-dimensional MAC (marker and cell) fluid solver in Rust](https://github.com/jackyarndley/rust-fluid)
        + [Delaunay mesh](https://github.com/d-dorazio/delaunay-mesh)
            + [Rust Delaunay Triangulation](https://github.com/nelsonatgithub/nlsn-delaunay-refine)
            + [Rust Discontinuous Galerkin](https://github.com/nelsonatgithub/discontinuous_galerkin)
            + [Rust Symbolic Algebraic](https://github.com/nelsonatgithub/ncas)
                + [Computer Algebra System in Rust](https://users.rust-lang.org/t/computer-algebra-system-in-rust/49016/27)
            + [Open Rust CFD: A 3D, unstructured computational fluid dynamics (CFD) solver](https://github.com/reidprichard/ORC

        + [a list of linear algebra libraries for Rust](https://libraries.io/search?keywords=matrix&languages=Rust)
        + [Numerics & math foundation](https://users.rust-lang.org/t/numerics-math-foundation/7247)
        + [Solving Sparse Matrix Systems in Rust](https://medium.com/software-makes-hardware/solving-sparse-matrix-systems-in-rust-5e978ed07bc3)
            + [Sparse multidimensional structures written in Rust](https://c410-f3r.github.io/posts/sparse-multidimensional-structures-written-in-rust/)
                + [ndsparse](https://github.com/c410-f3r/ndsparse)
        + [An extensible HPC-Framework for CUDA, OpenCL and native CPU](https://github.com/lychee-eng/parenchyma)
        + [Extremely generic linear algebra libary for Rust](https://github.com/maplant/aljabar)
        + [A Linear Algebra library that uses const generics to be no_std and specialization to enable SIMD](https://github.com/djugei/optimath/)
        + [A Rust linear algebra library based on const generics](https://github.com/27factorial/const-linear)
        + [al-jabr - n-dimensional linear algebra and mathematics library for computer graphics and other applications](https://crates.io/crates/al-jabr)
        + [The all-in-one maths library for Rust : A general purpose mathematics library for Rust, not usable now](https://github.com/jordanosborn/RustyPandas)
        + [Request for some numerics related features](https://users.rust-lang.org/t/request-for-some-numerics-related-features/3530/6)
            + [(former Unum)Create RUST posit arithmetic library based on 21 February 2017 Posit Arithmetic by John L. Gustafson - Beating Floating Point at its Own Game](https://users.rust-lang.org/t/create-rust-posit-arithmetic-library-based-on-21-february-2017-posit-arithmetic-by-john-l-gustafson-beating-floating-point-at-its-own-game/10077/3)
                + [A Rust implementation of the posit number system](https://github.com/japaric/posit#posit)
            + [Pre-RFC: Dealing with broken floating point](https://internals.rust-lang.org/t/pre-rfc-dealing-with-broken-floating-point/2673/22)
            + [John Gustafson presents: Beyond Floating Point – Next Generation Computer Arithmetic](http://insidehpc.com/2017/02/john-gustafson-presents-beyond-floating-point-next-generation-computer-arithmetic/)
        + [Multithreaded matrix multiplication in Rust - Part I](http://athemathmo.github.io/2016/04/16/multithreading-multiplication-1.html)
        + [Multithreaded matrix multiplication in Rust - Part II](http://athemathmo.github.io/2016/04/25/multithreading-multiplication-2.html)
            + [Anatomy of High-Performance Many-Threaded Matrix Multiplication](http://www.cs.utexas.edu/users/flame/pubs/blis3_ipdps14.pdf)
        + [A gemmed rabbit hole](http://bluss.github.io/rust/2016/03/28/a-gemmed-rabbit-hole/)
            + [GEMM in Rust implementation](https://github.com/bluss/matrixmultiply)
        + [Matrix Multiplication in Rust (Part 1)](http://www.suchin.co/2016/04/25/Matrix-Multiplication-In-Rust-Pt-1/)
        + [ndarray: an N-dimensional array with array views, multidimensional slicing, and efficient operations](https://github.com/bluss/rust-ndarray)
            + [ndarray presentation by the author](http://bluss.github.io/rust-ndarray/talk1/)
            + [ndarray_for_numpy_users](https://docs.rs/ndarray/0.14.0/ndarray/doc/ndarray_for_numpy_users/)
        + [sparse linear algebra library for rust](https://github.com/vbarrielle/sprs)
        + [Linear algebra library for the Rust programming language](https://nalgebra.org/)
            + [Linear algebra library for Rust](https://github.com/rustsim/nalgebra)
        + [Peroxide - Rust numeric library contains linear algebra, numerical analysis, statistics and machine learning tools with R, MATLAB, Python like macros](https://crates.io/crates/peroxide)
            + [Peroxide github repo](https://github.com/Axect/Peroxide)
        + [A Rust linear algebra library based on expression templates](https://github.com/SiegeLord/RustAlgebloat)
            + [Rust’s operator overloading doesn’t scale](https://internals.rust-lang.org/t/rusts-operator-overloading-doesnt-scale/408)
        + [Convolutions in Rust for Deep Learning](https://athemathmo.github.io/2016/04/29/convolutions-deep-learning.html)
            + [Understanding Convolution in Deep Learning](http://timdettmers.com/2015/03/26/convolution-deep-learning/)
            + [Convolutional Neural Networks](http://andrew.gibiansky.com/blog/machine-learning/convolutional-neural-networks/)
        + [UKF written in Rust based on the C++ UKF from the Udacity SD Car Nanodegree](https://github.com/hortovanyi/Unscented-Kalman-Filter-Rust)
        + [Neuronika is a machine learning framework written in pure Rust, built with a focus on ease of use, fast prototyping and performance](https://github.com/neuronika/neuronika)

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
                # used to be for ArrayFire
                #export AF_PATH=$HOME/work/arrayfire-3
                #export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$AF_PATH/lib
                # now

                # for openblas-provider
                # see [OpenBLAS: Detecting CPU failed during build](https://github.com/JuliaLang/julia/issues/394)
                # symptome: error: ‘SGEMM_DEFAULT_UNROLL_M’ undeclared
                export CARGO_FEATURE_SYSTEM_OPENBLAS=1
                
                # for arrayfire-rust
                export AF_PATH=/usr
                ```
                
                * use *ArrayFire*
                ```sh
                mkdir build
                pushd build
                cmake -DArrayFire_DIR=$AF_PATH/share/ArrayFire/cmake ..
                make VERBOSE=1
                ```
                + [arrayfire-project-templates/CMake/CMakeModules/FindOpenCL.cmake](https://github.com/arrayfire/arrayfire-project-templates/blob/master/CMake/CMakeModules/FindOpenCL.cmake)

    + async
        + [Are we async yet?](https://areweasyncyet.rs/)
        + [The What and How of Futures and async/await in Rust](https://www.youtube.com/watch?v=9_3krAQtD2k&list=PLqbS7AVVErFgMPqz5irpWbBInR6hxDbYi&index=2&t=130s)
        + [Comparison of Rust async and Linux thread context switch time and memory use](https://github.com/jimblandy/context-switch)
        + [A practical guide to async in Rust](https://blog.logrocket.com/a-practical-guide-to-async-in-rust/)
        + [Different levels of async in Rust](https://www.fpcomplete.com/blog/different-levels-async-rust/)
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

    + [Setting vision for 2017 cycle](https://internals.rust-lang.org/t/setting-our-vision-for-the-2017-cycle/3958/156)
        + [Rust's 2017 roadmap](https://blog.rust-lang.org/2017/02/06/roadmap.html)
        + [Associated type constructors (a form of higher-kinded polymorphism)](https://github.com/rust-lang/rfcs/pull/1598)
        + [[Roadmap 2017] Productivity: learning curve and expressiveness](https://internals.rust-lang.org/t/roadmap-2017-productivity-learning-curve-and-expressiveness/4097)
        + [Roadmap 2017 request - needs of HPC](https://internals.rust-lang.org/t/roadmap-2017-request-needs-of-hpc/4276)
        + [Language ergonomic/learnability improvements](https://github.com/rust-lang/rust-roadmap/issues/17)
        + [Rust Objectives Observation](https://users.rust-lang.org/t/rust-objectives-observation/10348/40)

    + [On Rust goals in 2018 and beyond](https://users.rust-lang.org/t/on-rust-goals-in-2018-and-beyond/12336/27)
        tl;dr
        rust sucks for numerics

    + [IDE для Rust](http://rustycrate.ru/%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%B0/2015/12/04/ide-for-rust.html)
        + [Are we (I)DE yet?](http://areweideyet.com/)

    + [rusty-tags : Create ctags/etags for a cargo project and all of its dependencies](https://github.com/dan-t/rusty-tags)

    + [New Rustacean : http://www.newrustacean.com/show_notes/e008/ : http://www.newrustacean.com/show_notes/e008/](http://www.newrustacean.com/show_notes/e008/)
    + [Getting into the nitty-gritty with Rust's traits](http://www.newrustacean.com/show_notes/e009/)
        + [“Subclassing” traits in Rust](https://stackoverflow.com/questions/47965967/subclassing-traits-in-rust)

    + ['The Rust Programming Language' E-Books'](http://killercup.github.io/trpl-ebook/)
      + [Rust iterators](https://doc.rust-lang.org/book/iterators.html)
        + [Reddit Rust iterator cheet sheet](https://www.reddit.com/r/rust/comments/38dl0o/rust_iterator_cheat_sheet/)
    + [The Advanced Rust Programming Language](https://doc.rust-lang.org/nightly/adv-book/)
    + [Rust For C++ Programmers](https://github.com/nrc/r4cppp)
        + [C++ to Rust - or how to render your mindset](https://jduchniewicz.com/posts/2021/02/c-to-rust-or-how-to-render-your-mindset/#introduction)
        + [blogs: Rust for C++ programmers](http://featherweightmusings.blogspot.co.nz/search/label/rust-for-c)
        + [Arrays and Vectors in Rust](https://github.com/nrc/r4cppp/blob/master/arrays.md)
        + [On rust's memory management: Mainly for C/C++ programmers](http://blog.zgtm.de/)
        + [Why not just add classes?](https://users.rust-lang.org/t/why-not-just-add-classes/4618)
            + [Composition over inheritance](https://en.wikipedia.org/wiki/Composition_over_inheritance)
        + [Today I learned — episode 3 (strong typing in C++ vs. Rust)](https://andidog.de/blog/2016-11-04-today-i-learned-3-strong-typing-in-cpp-vs-rust)

    + Rust patterns
        + [Common data structures and algorithms in Rust](https://github.com/EbTech/rust-algorithms)
        + [A catalogue of Rust design patterns](https://github.com/rust-unofficial/patterns)
        + [Rust Patterns: Using traits for function overloading](https://medium.com/@jreem/advanced-rust-using-traits-for-argument-overloading-c6a6c8ba2e17)
            + [rust-modifier: emulates overloading](https://github.com/reem/rust-modifier)
        + [Dependency Injection in Rust](https://medium.com/geekculture/dependency-injection-in-rust-3822bf689888)
        + [Dependency injection container - Learning the ropes in Rust](http://nercury.github.io/rust/di/2015/01/02/dependency-injection-learning-rust.html)
        + [Rust's flawed dynamic type](https://www.reddit.com/r/rust/comments/3mtim0/rusts_flawed_dynamic_type/)
            + [chris-morgan/mopa](https://github.com/chris-morgan/mopa)
        + [Mixing matching, mutation, and moves in Rust](http://blog.rust-lang.org/2015/04/17/Enums-match-mutation-and-moves.html)
        + [Polymorphism in Rust: Enum vs Trait + Struct](http://keepcalmandlearnrust.com/2017/03/polymorphism-in-rust-enum-vs-trait-struct/)
            + [Recursive Enum Types](https://users.rust-lang.org/t/recursive-enum-types/2938)
            + [How to use C++ polymorphism in Rust](https://medium.com/swlh/how-to-use-c-polymorphism-in-rust-76e1d1a88ed1)
        + [Implementing an object factory pattern in Rust using closures](http://keepcalmandlearnrust.com/2016/08/implementing-an-object-factory-pattern-in-rust-using-closures/)
        + [Typestates in Rust](https://yoric.github.io/post/rust-typestate/)
            + [CS 242: Programming Languages, Fall 2019](https://stanford-cs242.github.io/f19/)
                + [Graphs: All Foundational Methods](https://github.com/jlikhuva/blog/blob/main/posts/mathematical-sciences/graphs.md)
                + [Word Level Parallelism](https://github.com/jlikhuva/blog/blob/main/posts/mathematical-sciences/wlp.md)

    + Rust concurrency
        + [Rust Atomics and Locks](https://marabos.nl/atomics/)
            + [This repository contains the code examples, data structures, and links from Rust Atomics and Locks](https://github.com/m-ou-se/rust-atomics-and-locks)
            + [Mara's Blog](https://blog.m-ou.se/)
                + [Comparing Rust's and C++'s Concurrency Library](https://blog.m-ou.se/rust-cpp-concurrency/)
        + [Gregory Terzian](https://medium.com/@polyglot_factotum)
            + [Rust concurrency: the archetype of a message-passing bug.](https://medium.com/@polyglot_factotum/rust-concurrency-the-archetype-of-a-message-passing-bug-817b60efd8f8)
            + [Rust concurrency: five easy pieces.](https://medium.com/@polyglot_factotum/rust-concurrency-five-easy-pieces-871f1c62906a)
            + [Further thoughts on async/await.](https://medium.com/@polyglot_factotum/further-thoughts-on-async-await-7767f924cb7e)
            + [Rust concurrency patterns: condvars and locks](https://medium.com/@polyglot_factotum/rust-concurrency-patterns-condvars-and-locks-e278f18db74f)
        + [Comparing parallel Rust and C++](https://parallel-rust-cpp.github.io/)
            + [Performance comparison of parallel Rust and C++](https://github.com/parallel-rust-cpp/shortcut-comparison)
        + [Concurrent Programming in Rust course EECS 3/495](http://users.eecs.northwestern.edu/~jesse/course/eecs395rust-wi16/)
        + [An Adventure in API Design and Concurrency in Rust](http://damienradtke.com/adventures-in-concurrency-1/)
            + [Concurrency in Rust: vimeo video](https://vimeo.com/144809407)
        + [Lock free stack](https://crates.io/crates/concurrent-stack)
            + [Lock free stack on github](https://github.com/lucklove/concurrent-stack)
            + [AtomicPtr with stamp to avoid ABA problem](https://github.com/lucklove/atomic-stamped-ptr)
            + [AtomicU128 for x86_64](https://github.com/lucklove/atomic128)
        + [Learn Rust: Dining Philosophers runs not concurrent](https://users.rust-lang.org/t/learn-rust-dining-philosophers-runs-not-concurrent/4458)
        + [parry - Parallel array processing: deflect performance problems](https://github.com/huonw/parry)
        + [crossbeam - Support for parallelism and low-level concurrency in Rust](https://github.com/aturon/crossbeam)

    + [Pros and cons: Rust vs. C++](https://plus.google.com/+nialldouglas/posts/AXFJRSM8u2t)
        + [Rust: A Scala Engineer's Perspective](https://beachape.com/blog/2017/05/24/rust-from-scala/)
        + [Rust and the Blub Paradox](http://www.jonathanturner.org/2016/01/rust-and-blub-paradox.html)
             + [You can't spell trust without Rust](https://cdn.rawgit.com/Gankro/thesis/master/thesis.pdf)
             + [*twitter* You can't spell trust without Rust](https://twitter.com/rustlang/status/689823725219377152)
        + [cpp_to_rust](https://github.com/rust-qt/cpp_to_rust)
        + [What are the problems that Rust solves for you?](https://www.reddit.com/r/rust/comments/5o3yet/what_are_the_problems_that_rust_solves_for_you/)
            + [Simple N-Body with LeapFrog integrator](https://github.com/marblestation/benchmark-leapfrog)

    + Books, Docs: generation, in Russian, vs. C++
        + [*mpankov* ООП на Rust](https://github.com/mkpankov/rust-polymorphism-talk/blob/master/talk.org)
        + [*mpankov* rust-crash-course](https://github.com/mkpankov/rust-crash-course)
        + [Rust Books List](https://github.com/sger/RustBooks)
        + [Rust for C++ Programmers](https://www.gitbook.com/book/aminb/rust-for-c/details)
        + [Rust Programming Step-by-Step](https://www.gitbook.com/book/carlomilanesi/rust-programming-step-by-step/details)
        + [Convert The Rust Programming Language to Epub](https://gist.github.com/killercup/a793e09638379dbc74e4#file-trpl-epub-rb)
        + [The Rust Programming Language (на русском)](https://www.gitbook.com/book/kgv/rust_book_ru/details)
        + [Rust for clojurists](https://gist.github.com/oakes/4af1023b6c5162c6f8f0)
        + [Язык программирования Rust и первые впечатления от него (17 ноября 2014)](http://eax.me/rust/)
            + [Десять веских причин не тащить в продакшн новые игрушки](http://eax.me/avoid-new-toys/)
            + [Criticizing the Rust Language, and Why C/C++ Will Never Die](http://www.viva64.com/en/b/0324/)

    + [epsilonz - Functional Programming in Rust](https://github.com/epsilonz)

    + [Abstracted Algebra in Rust, or, Why Rust is better than C++, part I](http://maniagnosis.crsr.net/2015/07/abstracted-algebra-in-rust.html)
        + [More Abstracted Algebra in Rust, or Does 'Group' distribute over 'Ring'?](http://maniagnosis.crsr.net/2015/07/more-abstracted-algebra-in-rust.html)
    + [Graphs in Rust](http://featherweightmusings.blogspot.co.nz/2015/04/graphs-in-rust.html)
        + [Graphs and arena allocation](https://github.com/nrc/r4cppp/tree/master/graphs)

    + [A library of mesh generation utilities](https://github.com/gfx-rs/genmesh)

    + [rust on habrahabr](http://habrahabr.ru/hub/rust/)
        + [Многопоточность в Rust](http://habrahabr.ru/post/256211/)
        + [Создание функции на Rust, которая возвращает String или &str](http://habrahabr.ru/post/274565/)
        + [Куча способов переиспользовать код в Rust](https://habrahabr.ru/post/307616/)

    + [Adam Leventhal's blog: First Rust Program Pain (So you can avoid it...)](http://dtrace.org/blogs/ahl/2015/06/22/first-rust-program-pain/)

    + [LLVM изнутри: как это работает](http://habrahabr.ru/post/101838/)

    + [Thorin/Impala paper: A Graph-Based Higher-Order Intermediate Representation](http://compilers.cs.uni-saarland.de/papers/lkh15_cgo.pdf)

    + [unicode chars for idents](http://www.reddit.com/r/rust/comments/2pvksp/filename_with_dots_or_unicode_chars_not_working/)

    + Misc
        + [Why does serde_json::to_writer not require its argument to be `mut`?](https://stackoverflow.com/questions/57232515/why-does-serde-jsonto-writer-not-require-its-argument-to-be-mut)
        + [Implementing Finite Automata (Part 1)](https://apanatshka.github.io/compsci/2016/10/03/implementing-finite-automata-part-1/)
        + [Contributing to Rust](http://www.ncameron.org/rust.html)
        + [Interview with Mozilla’s Aaron Turon](http://www.pl-enthusiast.net/2015/06/09/interview-with-mozillas-aaron-turon/)
        + [julia vs. rust](http://vschart.com/compare/julia/vs/rust)
        + [Rust library for opening and working with dynamic link libraries](https://github.com/szymonwieloch/rust-dlopen)
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

        + [Good Practices for Writing Rust Libraries](https://pascalhertleif.de/artikel/good-practices-for-writing-rust-libraries/)

        + Porting to Rust
            + [C to Rust transpiler, based on cparser](https://github.com/PeterReid/cparser-to-rust)
            + [Type-Safe Unions in C++ and Rust](http://genbattle.bitbucket.org/blog/2016/10/07/Type-Safe-Unions-in-C-and-Rust/)
                + [Beyond Memory Safety With Types](https://insanitybit.github.io/2016/05/30/beyond-memory-safety-with-types)
            + [The Arduous Journey of Porting C to Rust](https://bawk.space/2016/10/06/c-to-rust.html)
            + [Baby Steps: Slowly Porting musl to Rust](http://blog.adamperry.me/rust/2016/06/11/baby-steps-porting-musl-to-rust/)
            + [That's so Rusty!: Smart pointers](https://dev.to/imaculate3/that-s-so-rusty-smart-pointers-245l)
            + [That's so Rusty! Fearless concurrency](https://dev.to/imaculate3/fearless-concurrency-5fk8)
            + [Dancing Links In Rust](https://ferrous-systems.com/blog/dlx-in-rust/)

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

        + [Generics, Arrays and Cloning](https://users.rust-lang.org/t/generics-arrays-and-cloning/694/3)
        + [Tricks with ownership in Rust](http://xion.io/post/code/rust-borrowchk-tricks.html)
        + [Effectively Using Iterators In Rust](http://hermanradtke.com/2015/06/22/effectively-using-iterators-in-rust.html)
            + [What is the difference between iter and into_iter?](http://stackoverflow.com/questions/34733811/what-is-the-difference-between-iter-and-into-iter)
            tl;dr
            ```rust
            let vec1 = vec![1, 2, 3];
            let vec2 = vec![4, 5, 6];
            
            // `iter()` for vecs yields `&i32`. Destructure to `i32`.
            println!("2 in vec1: {}", vec1.iter()     .any(|&x| x == 2));
            // `into_iter()` for vecs yields `i32`. No destructuring required.
            println!("2 in vec2: {}", vec2.into_iter().any(| x| x == 2));
            ```
        + [Initialize an array with a closure](http://stackoverflow.com/questions/29682881/initialize-an-array-with-a-closure)
        + [Inheritance, why is bad?](https://users.rust-lang.org/t/inheritance-why-is-bad/35705/49)
        + [*deprecated* OOP inheritance adapted to Rust](https://internals.rust-lang.org/t/oop-inheritance-adapted-to-rust/586)
            + [Usecases for inheritance](https://users.rust-lang.org/t/usecases-for-inheritance/348)
                + [Rust type system and the Circle-ellipse problem](https://internals.rust-lang.org/t/rust-type-system-and-the-circle-ellipse-problem/3057)
            + [Abstraction without overhead: traits in Rust](http://blog.rust-lang.org/2015/05/11/traits.html)
                + [Most coveted Rust features](https://users.rust-lang.org/t/most-coveted-rust-features/324/15)
        + [confusing error "ambiguous associated type" on missing enum variants](https://github.com/rust-lang/rust/issues/41003)
            + [How do I disambiguate associated types?](http://stackoverflow.com/questions/31251170/how-do-i-disambiguate-associated-types)

        + [Announcing Alacritty, a GPU-accelerated terminal emulator](http://blog.jwilm.io/announcing-alacritty/)

    + Useful tips
        + [Rust after the honeymoon](http://dtrace.org/blogs/bmc/2020/10/11/rust-after-the-honeymoon/)

        + [Use VIM as your RUST IDE](https://github.com/ivanceras/rust-vim-setup)

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

        + [How do you import macros in submodules in Rust?](http://stackoverflow.com/questions/39175953/how-do-you-import-macros-in-submodules-in-rust)
        tl;dr
        ```sh
        an `extern crate` loading macros must be at the crate root
        ```
        put the `#[macro_use] extern crate serde_derive;` in the crate root, which is `main.rs` and/or `lib.rs`

        + [Lifetime error when creating a function that returns a value implementing serde::Deserialize](http://stackoverflow.com/questions/43554679/lifetime-error-when-creating-a-function-that-returns-a-value-implementing-serde)
        + [Using serde's deserialize_with to handle custom strings](https://brokenco.de/2020/08/03/serde-deserialize-with-string.html)
        + [How to unit-test a deserialization function used in serde(deserialize_with)?](https://stackoverflow.com/questions/56985101/how-to-unit-test-a-deserialization-function-used-in-serdedeserialize-with)

        + [Closures don’t move Copy types by default?](https://internals.rust-lang.org/t/closures-dont-move-copy-types-by-default/5179/6)

    + Misc.
        + [Converting from Option<String> to Option<&str>](https://stackoverflow.com/questions/31233938/converting-from-optionstring-to-optionstr)
        + [Rust and Default Parameters](https://www.thecodedmessage.com/posts/default-params/)
        + [Dual numbers in Rust](https://github.com/potan/dual.rs)

        + [libfloat](https://github.com/peterhj/libfloat)

        + [A vantage-point tree implementation backed by vectors for good performance with no unsafe code](https://crates.io/crates/vec-vp-tree)

        + [[Announcement] ArrayDeque: Deque (ring buffer) on stack!](https://users.rust-lang.org/t/announcement-arraydeque-deque-ring-buffer-on-stack/11122)

        + [Grouping structs with enums](http://stackoverflow.com/questions/29088633/grouping-structs-with-enums)
            + [Proc macro crate for working with newtype enums: FromVariants](https://users.rust-lang.org/t/proc-macro-crate-for-working-with-newtype-enums-fromvariants/10546)
            tl;dr
            ```rust
            //! Example
            #![warn(missing_docs)]
            
            #[macro_use]
            extern crate from_variants;
            
            /// A sample struct.
            #[derive(Debug, Clone, FromVariants)]
            pub enum Lorem {
                /// Hello world
                #[from_variants(skip)]
                Str(String),
                
                /// Hello world
                Num(u16),
            }
            
            fn main() {
                println!("{:?}", Lorem::from(10));
            }
            ```
            generated
            ```rust
            #[doc = "Convert into a `Num` variant."]
            impl ::std::convert::From<u16> for Lorem {
                fn from(v: u16) -> Self {
                    Lorem::Num(v)
                }
            }
            ```

        + [Rustdoc: reStructuredText vs Markdown: On The Potential Inadequacy of Markdown](https://internals.rust-lang.org/t/rustdoc-restructuredtext-vs-markdown/356/71)

        + [How to implement a C union in Rust](https://users.rust-lang.org/t/how-to-implement-a-c-union-in-rust/3291/4)

        + [Implementation of Software transactional memory](https://crates.io/crates/stm/)

        + [Basic wrapper around libVEX from Valgrind](https://crates.io/crates/libvex-sys/)

        + [Rust implementation of the Quine-McCluskey](https://github.com/oli-obk/quine-mc_cluskey)

        + [cargo-tree](https://github.com/sfackler/cargo-tree)
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

        + [Rust task runner and build tool](https://github.com/sagiegurari/cargo-make)

        + [Parse command line argument by defining a struct](https://github.com/TeXitoi/structopt)
            + [How to Build CLIs in Rust with StructOpt](https://www.thorsten-hans.com/how-to-build-clis-in-rust-with-structopt/)
            + [Manual for structopt library](https://www.sobyte.net/post/2021-07/rust-lib-structopt/)

        + [Rust and Rest](http://lucumr.pocoo.org/2016/7/10/rust-rest/)
            + [Rust bindings to libcurl](https://github.com/alexcrichton/curl-rust)

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
        + [Why the [u8] inside Box<[u8]> does not implement AsRef<[u8]> + AsMut<[u8]>?](https://stackoverflow.com/questions/69921658/why-the-u8-inside-boxu8-does-not-implement-asrefu8-asmutu8)
                + [Why does T implement A+B but not trait C: A+B?](https://stackoverflow.com/questions/69916809/why-does-t-implement-ab-but-not-trait-c-ab)

        + [Working around the lack of associated method on parametric traits?](http://stackoverflow.com/questions/27888069/working-around-the-lack-of-associated-method-on-parametric-traits)
        + [cpp-templates-vs-rust-generics](https://gist.github.com/bjz/9220415)
        + [Rust, Generics, and Collections](http://cglab.ca/~abeinges/blah/rust-generics-and-collections/)
            + [Generics and Compile-Time in Rust](https://pingcap.com/blog/generics-and-compile-time-in-rust#monomorphized-generics)

        + [Matching, saving and replacing text with the regex crate](https://elliotekj.com/2017/03/10/matching-saving-and-replacing-text-with-the-regex-crate/)

    + Ideas, RFCs, that are not in the language yet
        + HKT
            + [What Are Sum, Product, and Pi Types?](https://www.reddit.com/r/rust/comments/5xkmnh/what_are_sum_product_and_pi_types/)
            + [Rust/Haskell: Higher-Kinded Types (HKT)](https://gist.github.com/CMCDragonkai/a5638f50c87d49f815b8)
                + [Higher-kinded type trait](https://gist.github.com/14427/af90a21b917d2892eace)
                + [Does/Will Rust support functional programming idioms?](https://stackoverflow.com/questions/18374612/does-will-rust-support-functional-programming-idioms)
            + [Blog post series: Alternative type constructors and HKT](https://internals.rust-lang.org/t/blog-post-series-alternative-type-constructors-and-hkt/4300/89)
                + [Associated type constructors, part 1: basic concepts and introduction](http://smallcultfollowing.com/babysteps/blog/2016/11/02/associated-type-constructors-part-1-basic-concepts-and-introduction/)
                + [Associated type constructors, part 2: family traits](http://smallcultfollowing.com/babysteps/blog/2016/11/03/associated-type-constructors-part-2-family-traits/)
                + [Associated type constructors, part 3: What higher-kinded types might look like](http://smallcultfollowing.com/babysteps/blog/2016/11/04/associated-type-constructors-part-3-what-higher-kinded-types-might-look-like/)
                + [Associated type constructors, part 4: Unifying ATC and HKT](http://smallcultfollowing.com/babysteps/blog/2016/11/09/associated-type-constructors-part-4-unifying-atc-and-hkt/)
            + [Pi types v2 (const generics)](https://internals.rust-lang.org/t/pi-types-v2/4860)
                + [[lang-team-minutes] Const generics](https://internals.rust-lang.org/t/lang-team-minutes-const-generics/5090)
                    + [*new* Const generics RFC](https://github.com/rust-lang/rfcs/pull/2000)
                + [with-bounds-in-pi-types](https://github.com/ticki/rfcs/blob/pi-types-ext-1/text/0000-with-bounds-in-pi-types.md)
                + [RFC: Constant generics (restricted Π types) for Rust, core RFC (v2)](https://github.com/rust-lang/rfcs/pull/1931)
                    + [Generics over the size of an array type (in anticipation of const generics)](https://internals.rust-lang.org/t/generics-over-the-size-of-an-array-type/2845)
                        + [generic-array](http://fizyk20.github.io/generic-array/generic_array/)
                    + [Associated Consts](https://github.com/rust-lang/rust/issues/29646)
                        + [Associated constant doesn’t exist?](https://users.rust-lang.org/t/associated-constant-doesnt-exist/12070/2)
                            + [associated-constants can not be used in constant expressions](https://github.com/rust-lang/rust/issues/34344)
                        + [Generic associated consts can't currently be used to parameterize fixed array lengths](https://github.com/rust-lang/rust/issues/42863)
                        tl;dr *it works!*
                        ```rust
                        #![feature(associated_consts)]

                        trait Const {
                            const VALUE: usize;
                        }

                        struct Foo;

                        impl Const for Foo {
                            const VALUE: usize = 4;
                        }

                        fn test(x: [u8; Foo::VALUE]) {
                            for _ in x.iter() {
                                println!("hello");
                            }
                        }

                        fn main() {
                            let x = [1,2,3,4];
                            test(x);
                        }
                        ```
            + [Dissertation on Algebraic Subtyping](https://internals.rust-lang.org/t/dissertation-on-algebraic-subtyping/4906)
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

    + [Unable to create a polymorphic type because the trait cannot be made into an object](https://stackoverflow.com/questions/39412626/unable-to-create-a-polymorphic-type-because-the-trait-cannot-be-made-into-an-obj)

    + [Add LaTeX support to Rustdoc](https://github.com/rust-lang/rust/issues/34261)
        + [Crate katex_doc](https://docs.rs/katex-doc/0.1.0/katex_doc/)
            + [katex_doc](https://crates.io/crates/katex-doc)
        + [horrible-katex-hack](https://lib.rs/crates/horrible-katex-hack)
        + [rustdoc-katex-demo](https://crates.io/crates/rustdoc-katex-demo)
            + [KaTeX for documentation](https://github.com/rust-ndarray/ndarray/issues/598)
                + [Struct hmmm::HMM](https://docs.rs/hmmm/0.1.1/hmmm/struct.HMM.html)
        + [Add Mathjax (KaTeX?) Support to Rustdoc #16300 ](https://github.com/rust-lang/rust/issues/16300)
        + [Add mathematics support to rustdoc #17390](https://github.com/rust-lang/rust/pull/17390#issuecomment-61195381)
        + [Rustdoc: reStructuredText vs Markdown](https://internals.rust-lang.org/t/rustdoc-restructuredtext-vs-markdown/356/63)
        + [*Embedding LaTeX in Rust documentation?*](https://users.rust-lang.org/t/embedding-latex-in-rust-documentation/11234)
            + [Snekdown - More than just Markdown](https://crates.io/crates/snekdown)
                + [Snekdown - More than just Markdown](https://github.com/trivernis/snekdown)
                    + [Snekdown docs](https://github.com/Trivernis/snekdown-docs)
                    + [AsciiMath](http://asciimath.org/)
            + [Minimal Rust project example for using Latex in docs](https://github.com/victe/rust-latex-doc-minimal-example)
            + [The Tectonic Typesetting System](https://tectonic-typesetting.github.io/en-US/)
                + [Rewriting LaTeX in Pure Rust](https://news.ycombinator.com/item?id=25328874)
                + [Porting all of Tectonic (modern TeX/LaTeX engine) from C to Rust](https://www.reddit.com/r/rust/comments/d1ql5s/porting_all_of_tectonic_modern_texlatex_engine/)
                    + [Rust port of Tectonic](https://github.com/crlf0710/tectonic/tree/oxidize)
            + [ReX - typesetting mathematics](https://github.com/ReTeX/ReX)
                + [ReTeX - Typesetting mathematics](https://www.reddit.com/r/rust/comments/hrd8hx/retex_typesetting_mathematics/)
                + [modern up-to-date fork of ReX - typesetting mathematics](https://github.com/grafeia/ReX)
            + Extending the Literate Programming Tool Tango
                + [Markdown-based Literate programming in Rust, integrated with Cargo](https://github.com/pnkfelix/tango)
                    + [Demonstration crate for the tango literate programming tool](https://github.com/pnkfelix/tango-demo/)
                + [md sample for literate programming in Rust with tango](https://github.com/pnkfelix/mon-artist/blob/a3388c11e8b1910cc4eb4c31bd1540a46851618b/src/lit/src/format.md)
                    + [Increasing Rust’s Reach](https://blog.rust-lang.org/2017/06/27/Increasing-Rusts-Reach.html)
        + [mdBook](https://github.com/rust-lang/mdBook)
            + [Scientific mdbook plugin](https://github.com/bytesnake/mdbook-scientific)
                + [The Rust Machine Learning Book](https://github.com/rust-ml/book)

    + *GC in Rust*
        + [GC and Rust Part 0: Garbage Collection Background](http://blog.pnkfx.org/blog/2015/10/27/gc-and-rust-part-0-how-does-gc-work/)
        + [GC and Rust Part 1: Specifying the Problem](http://blog.pnkfx.org/blog/2015/11/10/gc-and-rust-part-1-specing-the-problem/)
        + [GC and Rust Part 2: The Roots of the Problem](http://blog.pnkfx.org/blog/2016/01/01/gc-and-rust-part-2-roots-of-the-problem/)

    + [Machine Learning in Rust](https://github.com/alsam/bookmarks/blob/master/machine_learning.md)
        + [linfa aims to provide a comprehensive toolkit to build Machine Learning applications with Rust](https://github.com/rust-ml/linfa)
        + [A linear algebra library in Rust designed for machine learning](https://github.com/AtheMathmo/rulinalg)
        + [Linear Algebra in Rust](http://athemathmo.github.io/2016/03/23/linear-algebra-in-rust.html)
        + [rustlearn - A machine learning package for Rust](https://github.com/maciejkula/rustlearn)
        + [autograph - Machine Learning Library for Rust](https://github.com/charles-r-earp/autograph/tree/rocm)
            + [AMD / ROCm support for autograph](https://www.reddit.com/r/rust/comments/i7fwba/amd_rocm_support_for_autograph/)
        + [Nengo RS is an experimental Nengo backend written in Rust](https://github.com/jgosmann/nengo-rs)
            + [The Nengo Brain Maker is a Python package for building, testing, and deploying neural networks](https://www.nengo.ai/)
        + [tch-rs : Rust bindings for the C++ api of PyTorch](https://github.com/LaurentMazare/tch-rs)

    + [The Kolmogorov-Smirnov Test](http://daithiocrualaoich.github.io/kolmogorov_smirnov/)
        + [Implementation of the Kolmogorov-Smirnov statistical test as a Rust library](https://github.com/daithiocrualaoich/kolmogorov_smirnov)

    + [rand : A Rust library for random number generators and other randomness functionality.](https://github.com/rust-lang-nursery/rand)

    + [A library for differential-geometric calculations](https://crates.io/crates/differential-geometry/)
        + [A Rust crate for differential-geometric calculations](https://github.com/fizyk20/differential-geometry)
        + [Differential geometry in Rust](https://ebvalaim.pl/en/2015/12/18/differential-geometry-in-rust/)
            + [Possible bug in trait bounds evaluation #30262](https://github.com/rust-lang/rust/issues/30262)

    + [A native-rust implementation of an Effect monad, inspired by PureScript's EFF Monad](https://crates.io/crates/effect-monad/)

    + [pijul - distributed version control system written in Rust](https://pijul.org)
        + [Commutation and scalability in pijul, the new version control system written in Rust](https://www.reddit.com/r/rust/comments/kh706i/commutation_and_scalability_in_pijul_the_new/)
        + [Add Pijul support to Cargo](https://github.com/rust-lang/cargo/pull/3842)
        + [Pijul: Sane Version Control (Pierre Étienne Meunier)](https://vk.com/video-75161087_456239088)
        + [Announcing Pijul 1.0 beta, a Version Control System written in rust](https://www.reddit.com/r/rust/comments/s7v0hp/announcing_pijul_10_beta_a_version_control_system/)    
        tl;dr    
        ```sh
        cargo install pijul --version "~1.0.0-beta" --features git
        ```

        + [How to convert git to pijul repositories?](https://discourse.pijul.org/t/how-to-convert-git-to-pijul-repositories/728)

    + [`Recycle` - ergonomic allocated memory reusing.](https://www.reddit.com/r/rust/comments/521vxl/recyle_ergonomic_allocated_memory_reusing/)

    + Hardware (bare metal) - OSes, ISA simulators,etc.
        + DBus
            + [DBus projects in Rust](https://crates.io/search?q=dbus)
            + [A D-Bus binding for Rust](https://github.com/diwic/dbus-rs)
                + [dbus-rs: Serde support for msgarg](https://github.com/diwic/dbus-rs/issues/56)
            + [dbus-rs/src/message.rs](https://github.com/diwic/dbus-rs/blob/564e5af97a536d1a8cf93abdd2ad8550852a7b69/src/message.rs)
            + [argument_guide](https://github.com/diwic/dbus-rs/blob/master/examples/argument_guide.md)
            + [Struct dbus::arg::Iter](https://docs.rs/dbus/0.5.2/dbus/arg/struct.Iter.html)
            tl;dr
            ```rust
            struct ServiceBrowserItemNew {
                interface: i32,
                protocol: i32,
                name: String,
                item_type: String,
                domain: String,
                flags: u32,
            }
            
            fn service_browser_item_new_msg(m: &Message) -> Result<ServiceBrowserItemNew, TypeMismatchError> {
                let mut iter = m.iter_init();
                Ok(ServiceBrowserItemNew {
                    interface: try!(iter.read()),
                    protocol: try!(iter.read()),
                    name: try!(iter.read()),
                    item_type: try!(iter.read()),
                    domain: try!(iter.read()),
                    flags: try!(iter.read()),
                })
            }
            ```

            + [D-Bus Desktop Notification using dbus-rs](http://stackoverflow.com/questions/29800616/d-bus-desktop-notification-using-dbus-rs)
                + [Send Desktop Notifications on linux and bsd](https://github.com/hoodie/notify-rust)
                    + [Handpicked Rusty Crates](http://blog.hoodie.de/2016/04/30/handpicked-rusty-crates/)
 
        + [Writing an OS in Rust](http://os.phil-opp.com/)
            + [Introduction to Paging](https://os.phil-opp.com/paging-introduction/)
            + [Paging Implementation](https://os.phil-opp.com/paging-implementation/)
            + [Async/Await](https://os.phil-opp.com/async-await/)
        + [A comparison of operating systems written in Rust](https://github.com/flosse/rust-os-comparison)
            + [Writing a Linux-compatible kernel in Rust](https://seiya.me/writing-linux-clone-in-rust)
                + [Kerla is a monolithic operating system kernel from scratch in Rust which aims to be compatible with the Linux ABI](https://github.com/nuta/kerla)
                + [Resea [ríːseə] is a microkernel-based operating system written from scratch](https://github.com/nuta/resea)
                + [Kazari - A no_std GUI software stack](https://github.com/nuta/kazari)
                + [nsh](https://github.com/nuta/nsh)
            + Redox: A Rust Operating System
                + [github redox os](https://github.com/redox-os/redox)
                    + [This Week in Redox 5](http://www.redox-os.org/news/this-week-in-redox-5/)
                    + [Sodium: Vim 2.0](https://github.com/redox-os/sodium)
                        + [the Redox editor now is here](https://github.com/redox-os/editor)
                    + [Redox is Serious](http://dictator.redox-os.org/index.php?controller=post&action=view&id_post=17)
                    + [ion-shell](https://crates.io/crates/ion-shell/)
                        + [redox-os/ion](https://github.com/redox-os/ion)
                    + [The Orbital Widget Toolkit](https://crates.io/crates/orbtk/)
            + [Theseus: an Experiment in Operating System Structure and State Management](https://www.usenix.org/conference/osdi20/presentation/boos)
                    + [Theseus: an Experiment in Operating System Structure and State Management: slides](https://www.usenix.org/system/files/osdi20-boos.pdf)
                    + [OSDI '20 - Theseus: an experiment in operating system structure and state management](https://www.youtube.com/watch?v=i1pLDZKtlBI)
                    + [Theseus OS: OSDI 2020 Long Talk](https://www.youtube.com/watch?v=j4ZPZoPNjkw)
                + [Theseus: Rethinking Operating Systems Structure and State Management](https://scholarship.rice.edu/handle/1911/109201)
                    + [PhD Defense -- Theseus: Rethinking OS Structure and State Management](https://www.youtube.com/watch?v=JWGPLVYXZlU)
                + [	Theseus: A modern experimental OS written from scratch in Rust](https://news.ycombinator.com/item?id=25741729)
                + [Theseus is Hiring!](https://www.theseus-os.com/2022/04/29/Theseus-Is-Hiring.html)
                    + [Introduction to Theseus](https://www.theseus-os.com/Theseus/book/index.html
                    + [Theseus OS](https://github.com/theseus-os/Theseus)
            + [MOROS: Obscure Rust Operating System](https://github.com/vinc/moros)
                + [Writing a file system from scratch in Rust](https://news.ycombinator.com/item?id=23967016)
                + [Writing a file system from scratch in Rust](https://lobste.rs/s/8ipzof/writing_file_system_from_scratch_rust)
        + [rustv - A minimal, intentionally inaccurate RISC-V ISA simulator](https://crates.io/crates/rustv/)
            + [about RISC-V and Rocket processor see The RISC-V Instruction Set Architecture](http://riscv.org/)
            + [see also Chisel - Constructing Hardware in a Scala Embedded Language](https://chisel.eecs.berkeley.edu/)
            + [Building a RISC-V simulator in Rust - Part 1](https://gregchadwick.co.uk/blog/building-rrs-pt1/)
            + [R2VM is the Rust for RISC-V Virtual Machine.](https://github.com/nbdd0121/r2vm)
                + [Accelerate Cycle-Level Full-System Simulation of Multi-Core RISC-V Systems with Binary Translation](https://arxiv.org/pdf/2005.11357.pdf)
                + [Muntjac is a minimal 64-bit RISC-V multicore processor that's easy to understand, verify, and extend.](https://github.com/lowRISC/muntjac)
                + [Spike RISC-V ISA Simulator](https://github.com/lowRISC/riscv-isa-sim)
                + [Parallax Static Timing Analyzer](https://github.com/The-OpenROAD-Project/OpenSTA)

        + [Grover: Why Rust for Low-level Linux programming?](https://lwn.net/Articles/690821/)

        + [CLOCK-Pro: An Effective Improvement of the CLOCK Replacement](http://static.usenix.org/event/usenix05/tech/general/full_papers/jiang/jiang_html/html.html)

        + [Writing Bare-metal Rust Applications with no_std](https://morioh.com/p/d5368f55c2fb)

    + Formal Verification
        + [rsmt2](https://crates.io/crates/rsmt2)
            + [rsmt2 github](https://github.com/kino-mc/rsmt2)
        + [Synthesizing Loop-Free Programs with Rust and Z3](https://fitzgeraldnick.com/2020/01/13/synthesizing-loop-free-programs.html)
            + [Synthesis of Loop-free Programs in Rust](https://github.com/fitzgen/synth-loop-free-prog)
        + [Simple verification of Rust programs via functional purification](https://github.com/Kha/electrolysis)
            + [LEAN](https://github.com/leanprover/lean)
            + [Theorem Proving in Lean](https://leanprover.github.io/tutorial/index.html)
        + [A Formal Verification of Rust's Binary Search Implementation](https://kha.github.io/2016/07/22/formally-verifying-rusts-binary-search.html)
        + [GitHub - Kha/electrolysis: Simple verification of Rust programs via functional purification](https://www.reddit.com/r/rust/comments/4ty6z8/github_khaelectrolysis_simple_verification_of/)
        + [Electrolysis Reference](http://kha.github.io/electrolysis/)
        + [Status of Rust Code Analyzers](https://users.rust-lang.org/t/status-of-rust-code-analyzers/10106)
            + [Thesis: Simple Verification of Rust Programs via Functional Purification](https://users.rust-lang.org/t/thesis-simple-verification-of-rust-programs-via-functional-purification/9704)
        + [Pre-RFC: Extending where clauses with limited formal verification](https://internals.rust-lang.org/t/pre-rfc-extending-where-clauses-with-limited-formal-verification/13791/12)

    + C & C++ projects being converted to Rust
        + Physically Based Rendering
            + [Rust crate to implement at least parts of the PBRT book's C++ code](https://github.com/wahn/rs_pbrt)
            + [Release Notes for rs PBRT](https://github.com/wahn/rs_pbrt/wiki/Release-Notes)
                + [from here](https://users.rust-lang.org/t/whats-everyone-working-on-this-week-21-2017/10941/2)
        + Think Bayes
            + [a unofficial rewrite of Allen B. Downey's ThinkBayes in to Rust](https://github.com/Eh2406/ThinkBayes-rs)
        + Algorithms and Concepts from Stepanov's "Elements of Programming"
            + [Algorithms and Concepts from Stepanov's "Elements of Programming" implemented in Rust](https://github.com/keean/elements_in_rust)
        + Editors
            + [Build Your Text Editor With Rust!](https://medium.com/@otukof/build-your-text-editor-with-rust-678a463f968b)
            + [Helix](https://github.com/helix-editor/helix)
                + [Helix - A post-modern text editor](https://helix-editor.com/)
                + [Helix docs](https://docs.helix-editor.com/)
                + [Lapce - Lightning-fast And Powerful Code Editor](https://github.com/lapce/lapce)
                    + [Plugin: C/C++ (clangd) No such file or directory (os error 44)](https://github.com/lapce/lapce/issues/1792)
            + [A community-driven port of Emacs to Rust](https://github.com/Wilfred/remacs)
            + [Aspiring vim-like text editor](https://github.com/mathall/rim)
            + [**No Nonsense Neovim Client in Rust**](https://github.com/Kethku/neovide)
            + [A complete text editor for your terminal.](https://amp.rs/)
                + [The Bram Moole-Laaw: There Will be Attempts to Rewrite Vim in Nearly Every New Language](http://joshldavis.com/2015/11/29/the-bram-moole-laaw-vim-re-write/)

        + [How I Wrote a Modern C++ Library in Rust](https://hsivonen.fi/modern-cpp-in-rust)
        + [Rewritten in Rust: Modern Alternatives of Command-Line Tools](https://www.reddit.com/r/rust/comments/i1abpg/rewritten_in_rust_modern_alternatives_of/)
            + Text search-and-replace & Find (grep-like tools)
                + [amber (written in Rust - a good starting point)](https://github.com/dalance/amber)
                + [ripgrep is faster than {grep, ag, git grep, ucg, pt, sift}](https://blog.burntsushi.net/ripgrep/)
                + [A simple, fast and user-friendly alternative to 'find'](https://github.com/sharkdp/fd)
        + [[Share] Rust 14 CLI tools](https://www.reddit.com/r/rust/comments/10kip2s/share_rust_14_cli_tools/) 
            + [14 Rust Tools for Linux Terminal Dwellers](https://itsfoss.com/rust-cli-tools/)
        + [Awesome Rewrite It In Rust - A curated list of replacements for existing software written in Rust](https://www.reddit.com/r/rust/comments/nm96n1/awesome_rewrite_it_in_rust_a_curated_list_of/)
            + [uutils coreutils rewrite in Rust](https://github.com/uutils/coreutils)
            + [SAD! -Space Age seD](https://github.com/ms-jpq/sad)
            + [broot - get an overview of a directory, even a big one](https://github.com/Canop/broot)
            + [FClones — Efficient Duplicate File Finder and Remover](https://github.com/pkolaczk/fclones)

    + Video
        + [warming up: Even more general pixels](https://users.rust-lang.org/t/even-more-general-pixels/12068)
        + [imgref: A trivial Rust struct for interchange of pixel buffers with width, height & stride](https://github.com/pornel/imgref)
        + [resize: Simple resampling library in pure Rust](https://github.com/PistonDevelopers/resize)

    + Linux distros Rust support
        + [Fedora to support Rust Compiler](https://fedoraproject.org/wiki/Changes/RustCompiler)
        + Rust crates for packaging systems
            + [A cargo subcommand that generates Debian packages from information in Cargo.toml](https://github.com/mmstick/cargo-deb)
                + [Announcing Cargo Deb](https://www.reddit.com/r/rust/comments/4ofiyr/announcing_cargo_deb/)
            + [cargo-arch - generate Arch Linux packages from information in Cargo.toml](https://github.com/wdv4758h/cargo-arch/)

    + Run Rust code on your NVIDIA GPU
        + [Rust nvptx](https://github.com/japaric/nvptx)
        + [NVPTX backend metabug](https://github.com/rust-lang/rust/issues/38789)
        + [Utilize GPU computational capabilities](https://github.com/lychee-eng/miro/issues/5)
        + [PTX support, take 2](https://github.com/rust-lang/rust/pull/38559)
        + [Tracking issue for the "ptx-kernel" ABI](https://github.com/rust-lang/rust/issues/38788)

    + Rust & CUDA OpenCL
        + [State of GPGPU in 2022](https://www.reddit.com/r/rust/comments/ud88pj/state_of_gpgpu_in_2022/)
            + [rust-gpu](https://github.com/EmbarkStudios/rust-gpu)
            + [Announcing The Rust CUDA Project; An ecosystem of crates and tools for writing and executing extremely fast GPU code fully in Rust](https://www.reddit.com/r/rust/comments/qzv428/announcing_the_rust_cuda_project_an_ecosystem_of/)
            + [The Rust CUDA Project](https://github.com/Rust-GPU/Rust-CUDA)
                + [Getting Started](https://github.com/Rust-GPU/Rust-CUDA/blob/master/guide/src/guide/getting_started.md)
            + [opencl3](https://github.com/kenba/opencl3)
        + [rust-gpu](https://github.com/EmbarkStudios/rust-gpu)
        + [Пишем на Rust + CUDA C](https://habr.com/ru/post/447968/)
        + [Accel: GPGPU Framework for Rust](https://crates.io/crates/accel)
        + [My Rust 2021 roadmap](https://www.reddit.com/r/rust/comments/imd8b8/my_rust_2021_roadmap/)
        + [RustiCL](https://gitlab.freedesktop.org/karolherbst/mesa/-/tree/rusticl/src/gallium/frontends/rusticl)
        + [Rust opencl3](https://github.com/kenba/opencl3)
            + [Crate opencl3](https://docs.rs/opencl3/0.5.2/opencl3/)

    + diagrams using Rust
        + [SvgBobRus is an ascii to svg converter](https://github.com/ivanceras/svgbobrus)
        tl;dr
        ```sh
        cargo install svgbob_cli
        svgbob < examples/long.bob > long.svg
        svgbob -o long.svg < examples/long.bob
        svgbob examples/long.bob > long.svg
        ```
        + [Drawing SVG Graphs with Rust](https://cetra3.github.io/blog/drawing-svg-graphs-rust/)
        + [resvg is an SVG rendering library](https://github.com/RazrFalcon/resvg)

    + Graphics in Rust
        + [Rust Graphics Crates](https://github.com/ocboogie/rust-graphics-crates)
        + [librsvg - A small library to render Scalable Vector Graphics (SVG), associated with the GNOME Project](https://gitlab.gnome.org/GNOME/librsvg)
            + [libRSVG bindings for Rust](https://github.com/selaux/rsvg-rs)
            + [Federico's Blog on librsvg](https://people.gnome.org/~federico/blog/index.html)
        + [Rust Graphics Mages](https://github.com/gfx-rs)
            + [Awesome wgpu](https://github.com/rofrol/awesome-wgpu)
            + [Native WebGPU implementation based on gfx-hal](https://github.com/gfx-rs/wgpu)
            + [Rust bindings to wgpu native library](https://github.com/gfx-rs/wgpu-rs)
            + [Universal shader translation in Rust](https://github.com/gfx-rs/naga)
            + [Graham scan from Algorithms in a Nutshell in Rust](https://codereview.stackexchange.com/questions/141809/graham-scan-from-algorithms-in-a-nutshell-in-rust)
            + [Plexus is a Rust library for 2D and 3D mesh processing](https://crates.io/crates/plexus)
                + [entry point for quad-edge implementation in Rust](https://github.com/computemachines/quad-edge)
                + [The quad-edge data structure (Delaunay/Voronoi)](https://cstheory.stackexchange.com/questions/4746/the-quad-edge-data-structure-delaunay-voronoi)
            + Vulkan bindings in Rust
                + [Ash - A very lightweight wrapper around Vulkan](https://github.com/MaikKlein/ash)
                + [erupt - Vulkan API bindings](https://gitlab.com/Friz64/erupt)
                + [Vulkano is a Rust wrapper around the Vulkan graphics API](https://github.com/vulkano-rs/vulkano)
                + [Work-in-progress software-rendering Vulkan implementation](https://salsa.debian.org/Kazan-team/kazan)
            + [A low-overhead Vulkan-like GPU API for Rust](https://github.com/gfx-rs/gfx)
                + [N-Body-Simulation](https://github.com/timokoesters/nbodysim)
                    + [Rust Galaxy Simulator with GPU acceleration powered by wgpu](https://www.reddit.com/r/rust/comments/fdxdhb/i_released_my_rust_galaxy_simulator_with_gpu/)
                    + [LBM fluid simulation based on wgpu-rs](https://github.com/grenlight/fluid-webgpu)
                + [Nannou Update - WebGPU, capturing frames and more!](https://nannou.cc/posts/nannou_v0.13)
                + [Announcing salva2d and salva3d: fluid simulation in Rust](https://users.rust-lang.org/t/announcing-salva2d-and-salva3d-fluid-simulation-in-rust/34083)
                    + [2D and 3D fluid simulation engine](https://salva.rs/)
                        + [2D WASM version](https://www.salva.rs/all_examples2/)
                        + [3D WASM version](https://www.salva.rs/all_examples3/)
                        + [This month in rustsim #8 (August − September - October 2019)](https://www.rustsim.org/blog/2019/11/01/this-month-in-rustsim/)
                            + [2 and 3-dimensional fluid simulation library in Rust.](https://github.com/rustsim/salva)

        + [Relm the idiomatic GUI library for Rust](https://relm.antoyo.xyz/getting-started/)

        + [A Guide to Rust Graphics Libraries](https://wiki.alopex.li/AGuideToRustGraphicsLibraries2019)
            + [winit - Cross-platform window creation and management in Rust](https://crates.io/crates/winit)
            + [KAS, the toolKit Abstraction System, is a general-purpose GUI toolkit](https://github.com/dhardy/kas)
        + Rust and OpenGL from scratch
            + [Rust and OpenGL from scratch - Setup](http://nercury.github.io/rust/opengl/tutorial/2018/02/08/opengl-in-rust-from-scratch-00-setup.html)
            + [Rust and OpenGL from scratch - Window](http://nercury.github.io/rust/opengl/tutorial/2018/02/08/opengl-in-rust-from-scratch-01-window.html)
            + [Rust and OpenGL from scratch - OpenGL Context](http://nercury.github.io/rust/opengl/tutorial/2018/02/09/opengl-in-rust-from-scratch-02-opengl-context.html)
            + [Rust and OpenGL from scratch - Compiling Shaders](http://nercury.github.io/rust/opengl/tutorial/2018/02/10/opengl-in-rust-from-scratch-03-compiling-shaders.html)
            + [Rust and OpenGL from scratch - Triangle](http://nercury.github.io/rust/opengl/tutorial/2018/02/11/opengl-in-rust-from-scratch-04-triangle.html)
            + [Rust and OpenGL from scratch - Colored Triangle](http://nercury.github.io/rust/opengl/tutorial/2018/02/11/opengl-in-rust-from-scratch-05-triangle-colors.html)
            + [Rust and OpenGL from scratch - GL Generator](http://nercury.github.io/rust/opengl/tutorial/2018/02/12/opengl-in-rust-from-scratch-06-gl-generator.html)
            + [Rust and OpenGL from scratch - Basic Resources](http://nercury.github.io/rust/opengl/tutorial/2018/02/14/opengl-in-rust-from-scratch-07-basic-resources.html)
            + [Rust and OpenGL from scratch - Failure](http://nercury.github.io/rust/opengl/tutorial/2018/02/15/opengl-in-rust-from-scratch-08-failure.html)
            + [Пишем свой упрощенный OpenGL на Rust — часть 1 (рисуем линию)](http://habrahabr.ru/post/261629/)
            + [Пишем свой упрощенный OpenGL на Rust — часть 2 (проволочный рендер)](http://habrahabr.ru/post/261739/)
            + [Пишем свой упрощенный OpenGL на Rust — часть 3 (растеризатор)](http://habrahabr.ru/post/262235/)

            + [Simple ray tracer written in Rust from scratch](https://github.com/dranikpg/simple-rays)
            + [rpt - a physically based, CPU-only rendering engine written in Rust](https://github.com/ekzhang/rpt)
                + [a compound of five cubes, one of the five regular polyhedral compounds](https://www.reddit.com/r/rust/comments/ltazux/compound_of_five_cubes_rendered_using_rust_rpt_v02/)

            + [A Rust guide to Raytracing in One Weekend by Peter Shirley](https://github.com/JDuchniewicz/rustracing)
                + [C++ to Rust - or how to render your mindset](https://jduchniewicz.com/posts/2021/02/c-to-rust-or-how-to-render-your-mindset/)
                + [C++ to Rust introduction with practical "Raytracing in One Weekend" project](https://www.reddit.com/r/rust/comments/lukgyi/c_to_rust_introduction_with_practical_raytracing/)
                + [Ray Tracing in One Weekend](https://raytracing.github.io/books/RayTracingInOneWeekend.html)
                    + [Ray tracing in one weekend : several languages](https://github.com/nsauzede/realist/tree/master/rtiow)

        + [Vision Cortex - Semantic Computer Vision](https://github.com/visioncortex/visioncortex)
            + [visioncortex VTracer](https://github.com/visioncortex/vtracer)

    + Rust Computer Vision CV
        + [Dedicated to making photogrammetry and computer vision easier than OpenCV and faster than C++ (one day)](https://github.com/rust-cv)
            + [Rust computer vision core crate](https://github.com/rust-cv/cv-core)
            + [Implements the eight-point algorithm for estimating the essential matrix](https://github.com/rust-cv/eight-point)
            + [Essential matrix estimation from 5 normalized image coordinate correspondences from the paper "Recent developments on direct relative orientation"](https://github.com/rust-cv/nister-stewenius)
 
    + Rust robotics
        + [rust-robotics-libraries](https://gist.github.com/ClintLiddick/2966203a425ac5fb70a3d6eb0022f675)
        + [Rusty robots Programming a self-balancing robot in Rust](https://www.youtube.com/watch?v=kCTp8jzIzaQ)
        + [adventures-in-motion-control](http://adventures.michaelfbryan.com/tags/adventures-in-motion-control/)
            + [Geometric Constraint Solvers Part 1: Algebraic Expressions](http://adventures.michaelfbryan.com/posts/constraints-part-1-expressions/)

        + ROS stands for **R**obot **O**perating **S**ystem
            + [Awesome Rust for Robotics](http://robotics.rs/)
            + [Urdf-viz: URDF file viewer](http://ros-users.122217.n3.nabble.com/Discourse-ros-org-ROS-Projects-Urdf-viz-URDF-file-viewer-td4025049.html)
                tl;dr links to
                    + [kinematics](https://github.com/OTL/k)
                    + [urdf loader](https://github.com/OTL/urdf-rs)
                    + [visualizer](https://github.com/OTL/urdf-viz)
                    + [rrt](https://github.com/OTL/rrt)
                    + [OTL repositories](https://github.com/OTL?tab=repositories)
                in Rust
            + [adnanademovic repositories](https://github.com/adnanademovic?tab=repositories)
                + [Pure Rust implementation of a ROS client library](https://github.com/adnanademovic/rosrust)
                + [A pure Rust implementation of xml-rpc](https://github.com/adnanademovic/xml-rpc-rs)
                + [Serde ROSMSG](https://github.com/adnanademovic/serde_rosmsg)
        + [Learning embedded Rust by building RISC-V-powered robot](https://k155la3.blog/categories/allbot-rust/)
            + [Part 1](https://k155la3.blog/2020/03/21/learning-embedded-rust-by-building-riscv-powered-robot-part-1/)
            + [Part 2](https://k155la3.blog/2020/03/28/learning-embedded-rust-by-building-riscv-powered-robot-part-2/)
            + [Part 3](https://k155la3.blog/2020/04/04/learning-embedded-rust-by-building-riscv-powered-robot-part-3/)
            + [Part 4](https://k155la3.blog/2020/04/19/learning-embedded-rust-by-building-riscv-powered-robot-part-4/)

    + WIP : Selected RFCs
        + [RFC 1598: generic associated types](https://github.com/rust-lang/rfcs/blob/master/text/1598-generic_associated_types.md)
            + [Tracking issue for generic associated types (GAT)](https://github.com/rust-lang/rust/issues/44265)
                + [Coherence in Chalk By Sunjay Varma](http://slides.com/sunjay/coherence-in-chalk/fullscreen#/)
                    + [Coherence in Chalk by Sunjay Varma](https://www.youtube.com/watch?v=rZqS4bLPL24)
                        + [Ignore overflow when finding auto-trait impls in Rustdoc](https://github.com/rust-lang/rust/pull/73335)
                            + [Upgrade Chalk](https://github.com/rust-lang/rust/pull/72936)
                                + [Unify region variables when projecting associated types](https://github.com/rust-lang/rust/pull/73452)
                                    + [convert higher ranked `Predicate`s to `PredicateKind::ForAll`](https://github.com/rust-lang/rust/pull/73503)
            + [Generic associated types RFC was merged!](https://www.reddit.com/r/rust/comments/6xkqdl/generic_associated_types_rfc_was_merged/)
            + [Generic associated types (AKA ACT, AKA HKT) RFC merged!](https://www.reddit.com/r/rust/comments/6yt9vd/generic_associated_types_aka_act_aka_hkt_rfc/)
        + [RFC 2000: const generics](https://github.com/rust-lang/rfcs/blob/master/text/2000-const-generics.md)
            + [Tracking issue for const generics (RFC 2000)](https://github.com/rust-lang/rust/issues/44580)
                + [WIP The Genesis of Generic Germination](https://github.com/rust-lang/rust/pull/53645)
                    + To summarise, this PR is being split out into smaller ones:
                        + [Add const generics to the AST](https://github.com/rust-lang/rust/pull/58191)
                        + [Add const generics to the HIR](https://github.com/rust-lang/rust/pull/58503)
                        + [Refactor generic parameter encoder functions](https://github.com/rust-lang/rust/pull/58581)
                        + [Add const generics to ty (and transitive dependencies)](https://github.com/rust-lang/rust/pull/58583)
                            + [Add const generics to infer (and transitive dependencies)](https://github.com/rust-lang/rust/pull/59008)
                            + [typeck: Fix const generic in repeat param ICE](https://github.com/rust-lang/rust/pull/61698)
                            + [rustc/rustc_mir: Implement RFC 2203.](https://github.com/rust-lang/rust/pull/61749)
                                + [Add `IntoIterator` impl for arrays by value (`for [T; N]`)](https://github.com/rust-lang/rust/pull/65819)
                                + [Canonicalize inputs to const eval where needed](https://github.com/rust-lang/rust/pull/68505)
                                + [Lazy normalization of constants](https://github.com/rust-lang/rust/pull/67890)
            + [generic-array : in anticipation of **const generics**](https://crates.io/crates/generic-array/)
            tl;dr
            generic-array defines a new trait `ArrayLength<T>` and a `struct GenericArray<T, N: ArrayLength<T>>`,
            which let the above be implemented as:
            ```rust
            struct Foo<N: ArrayLength<i32>> {
            	data: GenericArray<i32, N>
            }
            ```
        + [RFC 1210: impl specialization](https://github.com/rust-lang/rfcs/blob/master/text/1210-impl-specialization.md)
            + [Implement RFC 1210: impl specialization #30652](https://github.com/rust-lang/rust/pull/30652)
            + [Specialize to reuse](https://aturon.github.io/blog/2015/09/18/reuse/)
            + [Shipping specialization: a story of soundness](https://internals.rust-lang.org/t/shipping-specialization-a-story-of-soundness/5507/13)
                + [Shipping specialization: a story of soundness](http://aturon.github.io/blog/2017/07/08/lifetime-dispatch/)

            + [Specialization/Inheritance](https://internals.rust-lang.org/t/specialization-inheritance/3030)
            + [Specialization Tree](https://users.rust-lang.org/t/specialization-tree/11863)
            + [Conditional Trait Implementations](https://users.rust-lang.org/t/conditional-trait-implementations/11850/4)
                + [Rust: Conditional Trait Implementation](https://stackoverflow.com/questions/45113763/rust-conditional-trait-implementation)
        + [RFC 1422: pub_restricted](https://github.com/rust-lang/rfcs/blob/master/text/1422-pub-restricted.md)

        + [Upcoming Rust syntax changes #234](https://github.com/dtolnay/syn/issues/234)
            + [Generic Associated Types Parsing #45904](https://github.com/rust-lang/rust/pull/45904)
            + [Update AST to hold const generics #227](https://github.com/dtolnay/syn/issues/227)
                + [Generics refactoring (groundwork for const generics)](https://github.com/rust-lang/rust/pull/45930)

    + [Secure and fast microVMs for serverless computing](https://github.com/firecracker-microvm/firecracker)

    + [Writing BPF code in Rust](https://blog.redsift.com/labs/writing-bpf-code-in-rust/)
        + [Writing eBPF tracing tools in Rust](https://jvns.ca/blog/2018/02/05/rust-bcc/)
        + [PoC: compiling to eBPF from Rust](http://unhandledexpression.com/general/rust/2018/02/02/poc-compiling-to-ebpf-from-rust.html)
        + [Rust virtual machine and JIT compiler for eBPF programs](https://github.com/qmonnet/rbpf)

    + embedded Rust
        + Cross compile for ARM
            + [Everything you need to know about cross compiling Rust programs!](https://github.com/japaric/rust-cross)
            + [Cross compiling Rust for ARM (e.g. Raspberry Pi) using any OS!](https://medium.com/@wizofe/cross-compiling-rust-for-arm-e-g-raspberry-pi-using-any-os-11711ebfc52b)
            + [“Zero setup” cross compilation and “cross testing” of Rust crates](https://github.com/rust-embedded/cross/)
            + [Operating System development tutorials in Rust on the Raspberry Pi](https://github.com/rust-embedded/rust-raspberrypi-OS-tutorials/)
        + [Real Time For the Masses](https://rtfm.rs/0.5/book/en/)
            + [Real Time For the Masses: Organization for the RTFM scheduler and ecosystem](https://github.com/rtfm-rs)
        + [Rust Embedded. Разработка под процессоры Cortex-M3 на примере отладочной платы STM32F103C8T6 (Black Pill)](https://habr.com/ru/post/495948/)
        + [(unofficial) Embedded Rust HAL Guidelines](https://github.com/jonas-schievink/hal-guidelines)
        + [Tock is an embedded operating system designed for running multiple concurrent, mutually distrustful applications on Cortex-M and RISC-V based embedded platforms](https://github.com/tock/tock)
        + [Bobbin is an open-source, cross-platform, vendor-independent development system for embedded programming in the Rust programming language](http://www.bobbin.io/)

    + misc
        + [Awesome Space](https://github.com/AeroRust/awesome-space)
        + [Object-Orientation in Rust](https://stevedonovan.github.io/rust-gentle-intro/object-orientation.html)
            + [Object-Oriented Programming in Rust](https://medium.com/dev-genius/object-oriented-programming-in-rust-691baf4d2996)
        + [This is a collection of implementations of algorithms and data structures in Rust language](https://tmaehara.gitlab.io/spaghetti-source/spaghetti_source/)
        + [How do I convert a Vec<String> to Vec<&str>?](https://stackoverflow.com/questions/33216514/how-do-i-convert-a-vecstring-to-vecstr)
        + [Is there any way to get the address of a `struct` in Rust?](https://stackoverflow.com/questions/35882994/is-there-any-way-to-get-the-address-of-a-struct-in-rust)
            + [A sampling CPU profiler for Linux similar to perf](https://github.com/koute/not-perf)
            + [gimli](https://github.com/gimli-rs/gimli)
                + [Switching the backtrace crate to using object](https://github.com/gimli-rs/object/issues/215#issue-604046969)
                    + [WIP: Switch from goblin to object](https://github.com/rust-lang/backtrace-rs/pull/315/files)
                    + [How do I use goblin's Elf::parse with a temporary variable?](https://stackoverflow.com/questions/70439842/how-do-i-use-goblins-elfparse-with-a-temporary-variable)
                + [cpp_demangle: a C++ linker symbol demangler](https://github.com/gimli-rs/cpp_demangle)
                + [A DWARF unwinder based on gimli](https://github.com/gimli-rs/unwind-rs/blob/master/unwind/src/find_cfi/baremetal.rs)
                tl;dr    
                ```rs
                let text = AddrRange {
                    start: &__text_start as *const _ as u64,
                    end: &__text_end as *const _ as u64,
                };
                let eh_frame_hdr = AddrRange {
                    start: &__ehframehdr_start as *const _ as u64,
                    end: &__ehframehdr_end as *const _ as u64,
                };
                let eh_frame_end = &__ehframe_end as *const _ as u64;
                ```
        + Logic in Rust
            + [SAT solver written in Rust](https://github.com/jix/varisat)
                + [Varisat](https://jix.one/project/varisat/)
            + [Stevia - Satisfiability Modulo Theories (SMT) Solver](https://github.com/Robbepop/stevia)
                + [A Satisfiability Modulo Theories (SMT) solver for the theories of fixed-size bit-vectors, arrays and uninterpreted functions](https://github.com/Boolector/boolector)
                    + [Boolector](https://boolector.github.io/)
            + [A modern Prolog implementation written mostly in Rust](https://github.com/mthom/scryer-prolog)
        + [Rust and WebAssembly](https://rustwasm.github.io/book/)
            + [Rust, WebAssembly, and the future of Serverless](https://morioh.com/p/f20294691bac)
            + [BxJS - Building wasm markdown renderer with Rust](https://www.youtube.com/watch?v=ihybuCp9pnc)
            + [sunglasses Curated list of awesome things regarding WebAssembly (wasm) ecosystem](https://github.com/mbasso/awesome-wasm)
            + [PGA Axioms](https://github.com/mwalczyk/pga-axioms)
            + [FPS Counter](http://adventures.michaelfbryan.com/posts/fps-counter/)
        + [The best Rust frameworks to check out in 2019](https://blog.logrocket.com/the-best-rust-frameworks-to-check-out-in-2019/)
            + [Actix-rs - rust's powerful actor system and most fun web framework](https://actix.rs/)
            + [Azul - A free, functional, immediate-mode GUI framework for rapid development of desktop applications written in Rust, supported by the Mozilla WebRender rendering engine. ](https://azul.rs/)
        + [Rust Tutorial on YouTube](https://www.youtube.com/playlist?list=PLLqEtX6ql2EyPAZ1M2_C0GgVd4A-_L4_5)
        + [The If Works](https://blog.jcoglan.com/)
            + [A little polymorphism, part 2: channels, combinators and const generics](https://blog.jcoglan.com/2020/01/06/a-little-polymorphism-part-2/)
        + [Rust high performance xml reader and writer](https://github.com/tafia/quick-xml)
        + [Prior work on Krylov subspace methods?](https://users.rust-lang.org/t/prior-work-on-krylov-subspace-methods/13261/3)
        + [Herb Sutter: “Metaclasses: Thoughts on generative C++”](https://internals.rust-lang.org/t/herb-sutter-metaclasses-thoughts-on-generative-c/5647)
        + [ x-post How do I integrate Rust into other projects?](https://users.rust-lang.org/t/x-post-how-do-i-integrate-rust-into-other-projects/13507)
        + [Sometimes you just want to count something globally, and you really dont want to worry to much about data races, other race conditions, all the fun stuff.](https://github.com/LukiRe/global_counter)
        + [Rust новости #5 (январь 2019)](https://m.habr.com/ru/post/439354/)

        + [triangle mesh data structure including basic operations](https://github.com/asny/tri-mesh)
        + [The fastest and safest AV1 encoder. in Rust](https://github.com/xiph/rav1e)
        + [Is there a time I should use C++ instead of Rust?](https://www.quora.com/Is-there-a-time-I-should-use-C-instead-of-Rust)
        + [Speedy Desktop Apps With GTK and Rust](https://nora.codes/tutorial/speedy-desktop-apps-with-gtk-and-rust/)
            + [nora codes](https://nora.codes/)
        + [Nannou Update - Vulkan, LASERs and more!](https://nannou.cc/posts/nannou_v0.9)
        + [Rust with Visual Studio Code: A simple how-to](https://levelup.gitconnected.com/rust-with-visual-studio-code-46404befed8)
        + [Visual Embedded Rust Programming with Visual Studio Code](https://medium.com/@ly.lee/visual-embedded-rust-programming-with-visual-studio-code-1bc1262e398c)
        + [Return-type based dispatch](https://deterministic.space/return-type-based-dispatch.html)
        + [Configure neovim for rust development](https://dev.to/drmason13/configure-neovim-for-rust-development-1fjn)
        + [cargo ssl download error behind proxy on windows](https://stackoverflow.com/questions/47221811/cargo-ssl-download-error-behind-proxy-on-windows)    
        tl;dr    
        ```sh
        git clone --bare https://github.com/rust-lang/crates.io-index.git
        ```
        + [Языковое замещение, или Почему Rust сменяет C](https://vc.ru/evrone/70821-yazykovoe-zameshchenie-ili-pochemu-rust-smenyaet-c)
            + [Operating System development tutorials in Rust on the Raspberry Pi](https://github.com/rust-embedded/rust-raspberrypi-OS-tutorials/)
        + [Zero To Production #1: Setup - Toolchain, IDEs, CI](https://www.lpalmieri.com/posts/2020-06-06-zero-to-production-1-setup-toolchain-ides-ci/)
        + [Zero To Production #2: Learn By Building An Email Newsletter](https://www.lpalmieri.com/posts/2020-06-21-zero-to-production-2-learn-by-building-an-email-newsletter/)
            + [3K, 60fps, 130ms: achieving it with Rust](https://blog.tonari.no/why-we-love-rust?ref=twtr)
        + [The Rust Compilation Model Calamity](https://pingcap.com/blog/rust-compilation-model-calamity/)
        + [Generics and Compile-Time in Rust](https://pingcap.com/blog/generics-and-compile-time-in-rust/)
        + [Automatic Differentiation/Differential Programming Support](https://internals.rust-lang.org/t/automatic-differentiation-differential-programming-support/12510)
            + [Reverse-mode automatic differentiation: a tutorial](https://rufflewind.com/2016-12-30/reverse-mode-automatic-differentiation)
        + [Do the compilers really create more optimal code for Rust than for C/C++?](https://www.reddit.com/r/rust/comments/k7pssg/do_the_compilers_really_create_more_optimal_code/)
        + [Get next `n` items from an iterator with const generics](https://internals.rust-lang.org/t/get-next-n-items-from-an-iterator-with-const-generics/13526/3)
        + FFI
            + [How to expose a Rust `Vec<T>` to FFI?](https://stackoverflow.com/questions/39224904/how-to-expose-a-rust-vect-to-ffi)
            + [Introducting Safer FFI](https://www.ditto.live/blog/introducing-safer-ffi)
            + [Deriving ReprC for custom enums](https://getditto.github.io/safer_ffi/derive-reprc/enum.html)
            + [Complex data types and the Rust FFI](http://kmdouglass.github.io/posts/complex-data-types-and-the-rust-ffi)
            + [CXX — safe FFI between Rust and C++](https://github.com/dtolnay/cxx)
        + clap
            + [clap::_derive::_tutorial](https://docs.rs/clap/latest/clap/_derive/_tutorial/)
            + [Clap: is it possible to have options with multiple values rather than multiple repeats?](https://users.rust-lang.org/t/clap-is-it-possible-to-have-options-with-multiple-values-rather-than-multiple-repeats/82755/3)
            tl;dr    
            ```rust
            /// Dissassemble given sections
            #[arg(short, long, num_args(1..))] // at least one section, such as .text
            disasm: Option<Vec<String>>,
            ```
            + [clap_derive: Vec/Option<Vec> behavior is inconsistent with other types](https://github.com/clap-rs/clap/issues/1772/)

+ [Rust for Data-Intensive Computation](https://materialize.io/rust-for-data-intensive-computation/)
    + [Timely Dataflow](https://github.com/TimelyDataflow/timely-dataflow)
    + [Differential Dataflow](https://github.com/TimelyDataflow/differential-dataflow)

+ [An introduction to Data Oriented Design with Rust](https://jamesmcm.github.io/blog/2020/07/25/intro-dod/)
+ [Rust serialization: What’s ready for production today?](https://blog.logrocket.com/rust-serialization-whats-ready-for-production-today/)

+ [Rust Persistent Data Structures](https://github.com/orium/rpds)

+ [Attempt at quad tree](https://users.rust-lang.org/t/attempt-at-quad-tree/49994)

+ [I want to implement add trait for a struct which imlpements Fn trait](https://users.rust-lang.org/t/i-want-to-implement-add-trait-for-a-struct-which-imlpements-fn-trait/103479)
    + [Structure and Interpretation of Classical Mechanics](https://tgvaughan.github.io/sicm/toc.html)
    + [Structure and Interpretation of Classical Mechanics: org mode](https://github.com/mentat-collective/sicm-book)
    + [Structure and Interpretation of Classical Mechanics: pdf](https://library.oapen.org/handle/20.500.12657/26048)
    + [SICM: Executable books](https://notes.andymatuschak.org/zJTBSJF2GwVvca1SdFb3JTE?stackedNotes=zLNcy2JiH3AGNaZjYkHzK9P)

+ [An HDL embedded in Rust](https://github.com/yupferris/kaze)
    + [Q: Rust as a hardware description language to be synthesized on an FPGA?](https://www.reddit.com/r/rust/comments/fyd57q/q_rust_as_a_hardware_description_language_to_be/)
    + [LLHD](https://github.com/fabianschuiki/llhd)
        + [Fabian Schuiki](https://fabian.schuiki.ch/)
        + [LLHD: A Multi-level Intermediate Representation for Hardware Description Languages](https://pldi20.sigplan.org/details/pldi-2020-papers/64/LLHD-A-Multi-level-Intermediate-Representation-for-Hardware-Description-Languages)
        + [LLHD: A Multi-level Intermediate Representation for
Hardware Description Languages](https://arxiv.org/pdf/2004.03494.pdf)
        + [Moore is a compiler for hardware description languages that outputs llhd assembly](https://github.com/fabianschuiki/moore)
        + [MLIR for Hardware Accelerators](https://github.com/circt/MLIRAccelerators)

+ [A dependency-free chess engine library built to run anywhere](https://github.com/adam-mcdaniel/chess-engine)
+ [crdts: family of thoroughly tested hybrid crdt's](https://crates.io/crates/crdts)
    + [Conflict-free replicated data type](https://en.wikipedia.org/wiki/Conflict-free_replicated_data_type)

+ [Neovim and Rust](https://sharksforarms.dev/posts/neovim-rust/)
+ [Is this the right way to read lines from file and split them into words in Rust?](https://stackoverflow.com/questions/25581463/is-this-the-right-way-to-read-lines-from-file-and-split-them-into-words-in-rust)
+ [How to Design For Panic Resilience in Rust](https://towardsdatascience.com/how-to-design-for-panic-resilience-in-rust-55d5fd2478b9)
+ [Rust modules easy explanation](https://logicai.io/blog/rust-modules-easy-explanation/)
+ [Rusts Module System Explained](https://aloso.github.io/2021/03/28/module-system.html)
+ [Rust Design Patterns](https://rust-unofficial.github.io/patterns/)
+ [Why I Scatter Use Statements Throughout My Rust](https://tarquin-the-brave.github.io/blog/posts/rust_use_statements/)
+ [Alignment of floating point numbers printed in scientific notation](https://stackoverflow.com/questions/65264069/alignment-of-floating-point-numbers-printed-in-scientific-notation)
+ [Fuchsia OS partially written in Rust has shipped](https://www.reddit.com/r/rust/comments/nldg5c/fuchsia_os_partially_written_in_rust_has_shipped/)
+ [zig - A general-purpose programming language and toolchain for maintaining robust, optimal, and reusable software](https://github.com/ziglang/zig)

+ HVM: a next-gen massively parallel, beta-optimal functional runtime is 50x faster than its predecessors
    + [HVM: a next-gen massively parallel, beta-optimal functional runtime is 50x faster than its predecessors](https://www.reddit.com/r/rust/comments/sh947t/hvm_a_nextgen_massively_parallel_betaoptimal/)
        + [High-order Virtual Machine (HVM)](https://github.com/Kindelia/HVM)

+ [Deep learning superresolution in pure rust](https://rustrepo.com/repo/millardjn-rusty_sr)

+ Sunrise
    + [heliocron](https://crates.io/crates/heliocron)
    + [Solar Position Algorithm (SPA)](https://crates.io/crates/spa)
    + [sunrise](https://github.com/nathan-osman/rust-sunrise)
