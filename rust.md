# rust language bookmarks
+ Rust links
    + [Why Rust?](http://www.oreilly.com/programming/free/files/why-rust.pdf)
    + [The Rust Book](https://doc.rust-lang.org/stable/book/)
        + [An alternative introduction to Rust](http://words.steveklabnik.com/a-new-introduction-to-rust)
        + [24day sof rust](http://zsiciarz.github.io/24daysofrust/)
    + [rust-learning](https://github.com/ctjhoa/rust-learning)
    + [this-week-in-rust](https://github.com/cmr/this-week-in-rust)
        + [Data for http://this-week-in-rust.org/ in case it is down](http://this-week-in-rust.org/)
    + [Rust homepage](http://www.rust-ang.org/)
    + [Rust learning](https://github.com/ctjhoa/rust-learning)
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
        + [An N-dimensional array for elements of arbitrary type. Lightweight array views and slicing. Supports both uniquely owned and shared copy-on-write arrays similar to numpy’s ndarray](https://crates.io/crates/rendarray/)
            + [rendarray: N-dimensional array like numpy's ndarray](https://github.com/bluss/rust-ndarray)
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

    + *Performance Tips*
        + [What one must understand to be productive with Rust](https://medium.com/@ericdreichert/what-one-must-understand-to-be-productive-with-rust-e9e472116728#.yc1728nv4)
        + [On pattern matching performance in rust](http://www.cjqed.com/blog/rust-pattern-matching-performance/)
        + [Rust Faster!](https://llogiq.github.io/2015/10/03/fast.html)
            + [The Computer Language Benchmarks Game: Rust implementations](https://github.com/TeXitoi/benchmarksgame-rs)
            + [Compile-time type checking for arbitrary unit systems](https://github.com/llogiq/dimensioned)
        + [Сравниваем Swift и Rust](http://habrahabr.ru/post/272681/)
        + [Which language has the brightest future in replacement of C between D, Go and Rust? And Why? Andrei Alexandrescu, D Language Architect](https://www.quora.com/Which-language-has-the-brightest-future-in-replacement-of-C-between-D-Go-and-Rust-And-Why/answer/Andrei-Alexandrescu)
        + [I wrote my Bachelor's thesis about Go and Rust in high-performance computing](https://www.reddit.com/r/rust/comments/34m7gw/i_wrote_my_bachelors_thesis_about_go_and_rust_in/)
            + [bachelor's thesis titled "Evaluation of performance and productivity metrics of potential programming languages in the HPC environment"](https://github.com/mrfloya/thesis-ba)
            + [Evaluation of C, Go, and Rust in the HPC environment](https://news.ycombinator.com/item?id=9477014)
            + [Evaluation of performance and productivity metrics of potential programming languages in the HPC environment - A comparison of Rust, Go and C -- University of Hamburg](https://www.reddit.com/r/programming/comments/34ml5f/evaluation_of_performance_and_productivity/)
            + [Rust programs versus Go by benchmark task performance](http://benchmarksgame.alioth.debian.org/u64q/compare.php?lang=rust&lang2=go

    + [Announcing Rust 1.0](http://blog.rust-lang.org/2015/05/15/Rust-1.0.html)

    + [Announcing Rust 1.2](http://blog.rust-lang.org/2015/08/06/Rust-1.2.html)
        + [Implement associated items](https://github.com/rust-lang/rust/issues/17307)

    + [Announcing Rust 1.5 stable](http://blog.rust-lang.org/2015/12/10/Rust-1.5.html)
        + [Version 1.5.0 (2015-12-10)](https://github.com/rust-lang/rust/blob/stable/RELEASES.md#version-150-2015-12-10)

    + ['The Rust Programming Language' E-Books'](http://killercup.github.io/trpl-ebook/)
      + [Rust iterators](https://doc.rust-lang.org/book/iterators.html)
        + [Reddit Rust iterator cheet sheet](https://www.reddit.com/r/rust/comments/38dl0o/rust_iterator_cheat_sheet/)
    + [The Advanced Rust Programming Language](https://doc.rust-lang.org/nightly/adv-book/)
    + [Rust For C++ Programmers](https://github.com/nrc/r4cppp)
        + [blogs: Rust for C++ programmers](http://featherweightmusings.blogspot.co.nz/search/label/rust-for-c)
        + [Arrays and Vectors in Rust](https://github.com/nrc/r4cppp/blob/master/arrays.md)

    + [Priorities after 1.0](http://internals.rust-lang.org/t/priorities-after-1-0/1901)
    + [Rust Patterns: Using traits for function overloading](https://medium.com/@jreem/advanced-rust-using-traits-for-argument-overloading-c6a6c8ba2e17)
        + [rust-modifier: emulates overloading](https://github.com/reem/rust-modifier)
    + [An Adventure in API Design and Concurrency in Rust](http://damienradtke.com/adventures-in-concurrency-1/)
        + [Concurrency in Rust: vimeo video](https://vimeo.com/144809407)
    + [Pros and cons: Rust vs. C++](https://plus.google.com/+nialldouglas/posts/AXFJRSM8u2t)
    + Docs: generation, in Russian, vs. C++
        + [Convert The Rust Programming Language to Epub](https://gist.github.com/killercup/a793e09638379dbc74e4#file-trpl-epub-rb)
        + [The Rust Programming Language (на русском)](https://www.gitbook.com/book/kgv/rust_book_ru/details)
        + [Rust for C++ Programmers](https://www.gitbook.com/book/aminb/rust-for-c/details)
        + [Rust for clojurists](https://gist.github.com/oakes/4af1023b6c5162c6f8f0)
        + [Язык программирования Rust и первые впечатления от него (17 ноября 2014)](http://eax.me/rust/)
            + [Десять веских причин не тащить в продакшн новые игрушки](http://eax.me/avoid-new-toys/)
            + [Criticizing the Rust Language, and Why C/C++ Will Never Die](http://www.viva64.com/en/b/0324/)
    + [A Rust linear algebra library based on expression templates](https://github.com/SiegeLord/RustAlgebloat)
        + [Rust’s operator overloading doesn’t scale](https://internals.rust-lang.org/t/rusts-operator-overloading-doesnt-scale/408)
    + [epsilonz - Functional Programming in Rust](https://github.com/epsilonz)

    + [Abstracted Algebra in Rust, or, Why Rust is better than C++, part I](http://maniagnosis.crsr.net/2015/07/abstracted-algebra-in-rust.html)
        + [More Abstracted Algebra in Rust, or Does 'Group' distribute over 'Ring'?](http://maniagnosis.crsr.net/2015/07/more-abstracted-algebra-in-rust.html)
    + [Graphs in Rust](http://featherweightmusings.blogspot.co.nz/2015/04/graphs-in-rust.html)
        + [Graphs and arena allocation](https://github.com/nrc/r4cppp/tree/master/graphs)

    + [A library of mesh generation utilities](https://github.com/gfx-rs/genmesh)

    + [rust on habrahabr](http://habrahabr.ru/hub/rust/)
        + [Многопоточность в Rust](http://habrahabr.ru/post/256211/)

    + [Adam Leventhal's blog: First Rust Program Pain (So you can avoid it...)](http://dtrace.org/blogs/ahl/2015/06/22/first-rust-program-pain/)

    + [LLVM изнутри: как это работает](http://habrahabr.ru/post/101838/)

    + [Thorin/Impala paper: A Graph-Based Higher-Order Intermediate Representation](http://compilers.cs.uni-saarland.de/papers/lkh15_cgo.pdf)

    + [unicode chars for idents](http://www.reddit.com/r/rust/comments/2pvksp/filename_with_dots_or_unicode_chars_not_working/)

    + Rust parser generators
        + [nom 1.0 Write Really Fast Parsers](https://www.clever-cloud.com/blog/engineering/2015/11/16/nom-1-0/)
            + [nom on github](https://github.com/Geal/nom)
        + [LALRPOP](http://smallcultfollowing.com/babysteps/blog/2015/09/14/lalrpop/)
            + [LALRPOP tutorial](https://github.com/nikomatsakis/lalrpop/blob/master/doc/tutorial.md)
        + [rusty-peg crate](https://crates.io/crates/rusty-peg)
            + [rusty-peg github](https://github.com/nikomatsakis/rusty-peg)

    + Misc
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

        + [A comparison of operating systems written in Rust](https://github.com/flosse/rust-os-comparison)
            + Redox: A Rust Operating System
                + [github redox os](https://github.com/redox-os/redox)
                    + [This Week in Redox 5](http://www.redox-os.org/news/this-week-in-redox-5/)
                    + [sodium editor TODO](https://github.com/redox-os/redox/blob/master/filesystem/apps/sodium/TODO.md)
                        + [the Redox editor now is here](https://github.com/redox-os/editor)
                    + [Redox is Serious](http://dictator.redox-os.org/index.php?controller=post&action=view&id_post=17)
                    + [ion-shell](https://crates.io/crates/ion-shell/)
                        + [redox-os/ion](https://github.com/redox-os/ion)
                    + [The Orbital Widget Toolkit](https://crates.io/crates/orbtk/)

        + [Rust Lifetimes](http://www.charlesetc.com/rust/2015/10/29/)
        + [Lifetime Reference](http://www.charlesetc.com/rust/2015/10/31/)
            + [official lifetimes doc](https://doc.rust-lang.org/book/lifetimes.html)

        + [Iterator trait](https://doc.rust-lang.org/nightly/std/iter/trait.Iterator.html)
            + [iota editor written in Rust; use case for idiomatic iterator usage](https://github.com/gchp/iota/blob/master/src/iota/iterators.rs)

        + [Can't find crate for `num`](http://stackoverflow.com/questions/29189615/cant-find-crate-for-num)

        + [Multiple binaries in Cargo](https://users.rust-lang.org/t/multiple-binaries-in-cargo/3049/2)

        + [Rosetta code for complex in Rust](http://rosettacode.org/wiki/Arithmetic/Complex#Rust)

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
            + [Abstraction without overhead: traits in Rust](http://blog.rust-lang.org/2015/05/11/traits.html)
                + [Most coveted Rust features](https://users.rust-lang.org/t/most-coveted-rust-features/324/15)

    + Useful tips
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

        + [A bunch of lints to catch common mistakes and improve your Rust code](https://github.com/Manishearth/rust-clippy)

        + [Convert string slice to int in rust](http://stackoverflow.com/questions/26919609/convert-string-slice-to-int-in-rust)
        + [Learning to 'try!' things in Rust](http://www.jonathanturner.org/2015/11/learning-to-try-things-in-rust.html)
            + [try!](http://rustbyexample.com/std/result/try.html)

    + *Performance tips*
        + [Benchmarking programs in Rust](http://stackoverflow.com/questions/13322479/benchmarking-programs-in-rust)
        + [How to `zip` two slices efficiently](https://users.rust-lang.org/t/how-to-zip-two-slices-efficiently/2048)
        + [How to `memcpy` bytes in stable rust](https://users.rust-lang.org/t/how-to-memcpy-bytes-in-stable-rust/2740)
            + [Stabilizing basic functions on arrays and slices: `clone_from_slice`](https://internals.rust-lang.org/t/stabilizing-basic-functions-on-arrays-and-slices/2868)
        + [`Builder` pattern without cloning](https://users.rust-lang.org/t/builder-pattern-without-cloning/2044)
        + [Profiling Rust applications on Linux](https://llogiq.github.io/2015/07/15/profiling.html)

    + Misc.
        + [Dual numbers in Rust](https://github.com/potan/dual.rs)

        + [libfloat](https://github.com/peterhj/libfloat)

        + [Rustdoc: reStructuredText vs Markdown: On The Potential Inadequacy of Markdown](https://internals.rust-lang.org/t/rustdoc-restructuredtext-vs-markdown/356/71)

        + [How to implement a C union in Rust](https://users.rust-lang.org/t/how-to-implement-a-c-union-in-rust/3291/4)

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
            + [Accumulator factory](http://rosettacode.org/wiki/Accumulator_Factory)
                + [Accumulator factory C++, see esp. C++11 ](http://rosettacode.org/wiki/Accumulator_Factory#C.2B.2B)

        + [Working around the lack of associated method on parametric traits?](http://stackoverflow.com/questions/27888069/working-around-the-lack-of-associated-method-on-parametric-traits)
        + [cpp-templates-vs-rust-generics](https://gist.github.com/bjz/9220415)
        + [Rust, Generics, and Collections](http://cglab.ca/~abeinges/blah/rust-generics-and-collections/)
        + [Rust, Lifetimes, and Collections](http://cglab.ca/~abeinges/blah/rust-lifetimes-and-collections/)

    + Ideas, RFCs, that are not in the language yet
        + [`step_by` on negative numbers](https://internals.rust-lang.org/t/step-by-on-negative-numbers/2231)
        + [GPU support](https://internals.rust-lang.org/t/single-source-gpu-support/898/13)
        + [Higher-kinded type trait](https://www.reddit.com/r/rust/comments/31g0qd/higherkinded_type_trait/)
            + [GitHub Gist for HKT](https://gist.github.com/14427)
            + [Rust and the Monad trait - Not just higher kinded types](https://m4rw3r.github.io/rust-and-monad-trait/)
            + [Reddit: Rust and the Monad trait - Not just higher kinded types](https://www.reddit.com/r/rust/comments/3li3by/rust_and_the_monad_trait_not_just_higher_kinded/)
        + [ Add Mathjax (KaTeX?) Support to Rustdoc #16300 ](https://github.com/rust-lang/rust/issues/16300)
            + [ Add mathematics support to rustdoc #17390 ](https://github.com/rust-lang/rust/pull/17390#issuecomment-61195381)
            + [Rustdoc: reStructuredText vs Markdown](https://internals.rust-lang.org/t/rustdoc-restructuredtext-vs-markdown/356/63)
        + GC in Rust
            + [GC and Rust Part 0: Garbage Collection Background](http://blog.pnkfx.org/blog/2015/10/27/gc-and-rust-part-0-how-does-gc-work/)
            + [(GC and Rust Part 1: Specifying the Problem](http://blog.pnkfx.org/blog/2015/11/10/gc-and-rust-part-1-specing-the-problem/)

    + [Machine Learning in Rust](https://github.com/alsam/bookmarks/blob/master/machine_learning.md#Rust based projects)
        + [rustlearn - A machine learning package for Rust](https://github.com/maciejkula/rustlearn)

    + [The Kolmogorov-Smirnov Test](http://daithiocrualaoich.github.io/kolmogorov_smirnov/)
        + [Implementation of the Kolmogorov-Smirnov statistical test as a Rust library](https://github.com/daithiocrualaoich/kolmogorov_smirnov)

    + [A library for differential-geometric calculations](https://crates.io/crates/differential-geometry/)
        + [A Rust crate for differential-geometric calculations](https://github.com/fizyk20/differential-geometry)
        + [Differential geometry in Rust](http://ebvalaim.mydevil.net/en/2015/12/18/differential-geometry-in-rust/)

    + [A native-rust implementation of an Effect monad, inspired by PureScript's EFF Monad](https://crates.io/crates/effect-monad/)
