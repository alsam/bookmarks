# C++ language bookmarks
+ C++ links
    + [ C++ Ecosystem: Compilers, IDEs, Tools, Testing and More ](https://www.bfilipek.com/2019/10/cppecosystem.html?m=1)
        + [and meson, missed from the above review](https://mesonbuild.com/)
            + [The Meson Build System](https://github.com/mesonbuild/meson)
            + [List of projects using Meson](https://mesonbuild.com/Users.html)
                + [HelenOS is a portable microkernel-based multiserver operating system designed and implemented from scratch](http://www.helenos.org/)
            + [Let's build Chuck Norris!](https://dmerej.info/blog/post/introducing-the-chuck-norris-project/)
                + [Part 1: CMake and Ninja](https://dmerej.info/blog/post/chuck-norris-part-1-cmake-ninja/)
                + [Part 2: SQLite and conan](https://dmerej.info/blog/post/chuck-norris-part-2-sqlite-conan/)
                + [Part 3: A C wrapper](https://dmerej.info/blog/post/chuck-norris-part-3-a-c-wrapper/)
                + [Part 4: Python and ctypes](https://dmerej.info/blog/post/chuck-norris-part-4-python-ctypes/)
                + [Part 5: Python and cffi](https://dmerej.info/blog/post/chuck-norris-part-5-python-cffi/)
                + [Part 6: Cross-compilation for Android](https://dmerej.info/blog/post/chuck-norris-part-6-android-cross-compilation/)
                + [Part 7: Android and JNA](https://dmerej.info/blog/post/chuck-norris-part-7-android-jna/)
                + [Part 8: Using C++ in an iOS application](https://dmerej.info/blog/post/chuck-norris-part-8-ios/)

            + [How to use "--allow-multiple-definition"](https://groups.google.com/forum/#!topic/harbour-users/_2CsENxyp7g)
            tl;dr the correct syntax is   
            ```sh
            -ldflag=-Wl,--allow-multiple-definition

            ...
            mylib = shared_library(..., dependencies: [liblog,], ... link_args: '-Wl,--allow-multiple-definition')
            ```
    + CMake
        + [An Introduction to Modern CMake](https://cliutils.gitlab.io/modern-cmake/)
        + [CGold: The Hitchhiker’s Guide to the CMake](https://cgold.readthedocs.io/en/latest/)
        + [CMake cheat sheet](https://ps-group.github.io/cxx/cmake_cheatsheet)
        + [CMake cannot find GoogleTest required library in Ubuntu](https://stackoverflow.com/questions/24295876/cmake-cannot-find-googletest-required-library-in-ubuntu)
        + [CMake by Example](https://mirkokiefer.com/cmake-by-example-f95eb47d45b1)
            + [How to copy contents of a directory into build directory after make with CMake?](https://stackoverflow.com/questions/13429656/how-to-copy-contents-of-a-directory-into-build-directory-after-make-with-cmake)    
            ```cmake
            add_custom_command(TARGET ${PROJECT_NAME} POST_BUILD
                               COMMAND ${CMAKE_COMMAND} -E copy_directory
                                   ${CMAKE_SOURCE_DIR}/config $<TARGET_FILE_DIR:${PROJECT_NAME}>/config)
            ```
            + [Executing multiple post build commands in CMake depending on condition](https://stackoverflow.com/questions/33769077/executing-multiple-post-build-commands-in-cmake-depending-on-condition)
            + [Problems with directory delimiters turning into backslashes when running cmake](https://stackoverflow.com/questions/48717138/problems-with-directory-delimiters-turning-into-backslashes-when-running-cmake)    
            tl;dr    
            ```sh
             cmake -DCMAKE_CXX_COMPILER:FILEPATH=C:\Game Dev\Tools\MingW-
            ```

    + [CppCon 2017: Rong Lu "C++ Development with Visual Studio Code"](https://www.youtube.com/watch?v=rFdJ68WbkdQ)
    + [Thoughts about Software Development with an eye on the world of modern C++ Programming](https://thoughts-on-cpp.com/)
        + [My God, It’s Full Of Stars: The N-Body-Problem Series](https://thoughts-on-cpp.com/2019/02/08/the-n-body-problem-series/)
        + [My God, It’s Full Of Stars: And then there was CMake](https://thoughts-on-cpp.com/2019/02/14/and-then-there-was-cmake/)
        + [My God, It’s Full Of Stars: Testing Point Mass Attraction with Catch2](https://thoughts-on-cpp.com/2019/02/28/testing-point-mass-attraction-with-catch2/)
        + [My God, It’s Full of Stars: Implementing the implicit Euler-Method with STL](https://thoughts-on-cpp.com/2019/03/07/implementing-the-implicit-euler-method-with-stl/)
        + [Introduction into Logging with Loguru](https://thoughts-on-cpp.com/2019/03/12/introduction-into-logging-with-loguru/)
        + [Using Pointer to Members on STL Algorithms](https://thoughts-on-cpp.com/2019/02/22/cpp-using-pointer-to-members/)
        + [Introduction into Logging with Loguru](https://thoughts-on-cpp.com/2019/03/27/introduction-into-build-automation-setup-with-jenkins-and-cmake/)
        + [Introduction into C++ Builds with Gradle](https://thoughts-on-cpp.com/2019/04/10/introduction-into-c-builds-with-gradle/)
        + [A short Introduction into IEEE 754 Floating-Point Model](https://thoughts-on-cpp.com/2019/04/03/a-short-introduction-into-ieee-754-floating-point-model/)
        + [Numerical Methods with C++ Part 1: Newton-Cotes Integration](https://thoughts-on-cpp.com/2019/04/17/numerical-methods-in-c-part-1-newton-cotes-integration/)
        + [Numerical Methods with C++ Part 2: Gauss-Legendre Integration](https://thoughts-on-cpp.com/2019/04/25/numerical-methods-in-c-part-2-gauss-legendre-integration/)
        + [Numerical Methods with C++ Part 3: Root Approximation Algorithms](https://thoughts-on-cpp.com/2019/06/06/numerical-methods-with-cpp-part-3-root-approximation-algorithms/)
        + [Numerical Methods with C++ Part 4: Introduction Into Decomposition Methods of Linear Equation Systems](https://thoughts-on-cpp.com/2019/06/12/numerical-methods-with-c-part-4-introduction-into-decomposition-methods-of-linear-equation-systems/)

    + [Is C++ fast?](https://zeux.io/2019/01/17/is-c-fast/)
        + [Flavors of SIMD](https://zeux.io/2019/02/17/flavors-of-simd/)
+ C
    + [9 интересных трюков на Си, с которыми вы раньше не сталкивались](https://tproger.ru/translations/9-clang-tricks/)
    + [How do I create a custom file system in C?](https://www.quora.com/How-do-I-create-a-custom-file-system-in-C)

+ C++
    + [Feature freeze C++20. Coroutines, Modules и прочее](https://habr.com/ru/company/yandex/blog/438864/)

    + C++ Best Practices
        + [C++ Best Practices](https://lefticus.gitbooks.io/cpp-best-practices/content/02-Use_the_Tools_Available.html)
        + [C++ Russia 2017: Антон Полухин, Как делать не надо: C++ велосипедостроение для профессионалов](https://www.youtube.com/watch?v=rJWSSWYL83U)
        + [Зачем избегать друзей, или как я растерял все свои плюсы](https://habr.com/ru/post/472780/)
        + [How to split a string in C++](https://www.fluentcpp.com/2017/04/21/how-to-split-a-string-in-c/)

+ [free modern C++ book: Discovering Modern C++](https://github.com/stoneyang-cs/cpp_book/blob/master/Discovering%20Modern%20C%2B%2B%20-%20Peter%20Gottschling.pdf)

    + CppCon
        + [C++ Atomics, From Basic to Advanced by Fedor Pikus](https://github.com/CppCon/CppCon2017/tree/master/Presentations/C%2B%2B%20Atomics%2C%20From%20Basic%20to%20Advanced)
        + [Building C++ Modules by Boris Kolpackov](https://github.com/CppCon/CppCon2017/tree/master/Presentations/Building%20C%2B%2B%20Modules)
        + [Concurrency, Parallelism and Coroutines - Anthony Williams](https://github.com/CppCon/CppCon2017/blob/master/Presentations/Concurrency%2C%20Parallelism%20and%20Coroutines/Concurrency%2C%20Parallelism%20and%20Coroutines%20-%20Anthony%20Williams%20-%20CppCon%202017.pdf)
        + [CUDA Kernels with C++ by Michael Gopshtein](https://github.com/CppCon/CppCon2018/blob/master/Presentations/cuda_kernels_with_cpp/cuda_kernels_with_cpp__michael_gopshtein__cppcon_2018.pdf)

    + [C++ TUTORIAL - TEMPLATES - 2018](https://www.bogotobogo.com/cplusplus/templates.php)

    + [C++11 async tutorial](https://solarianprogrammer.com/2012/10/17/cpp-11-async-tutorial/)

    + [C++ Lifetime safety, inspired by Rust](https://github.com/isocpp/CppCoreGuidelines/blob/master/docs/Lifetime.pdf)

    + [C++17 features list](http://www.bfilipek.com/2017/01/cpp17features.html)
        + [C++17 in details: Standard Library Utilities](http://www.bfilipek.com/2017/09/cpp17-details-utils.html)
        + [C++17 in details: Parallel Algorithms](http://www.bfilipek.com/2017/08/cpp17-details-parallel.html)
        + [Value Categories in C++17](https://medium.com/@barryrevzin/value-categories-in-c-17-f56ae54bccbe)
            + [Категории выражений в C++](https://m.habr.com/ru/post/441742/)
            + [C++17 **Guaranteed** Copy Elision](https://jonasdevlieghere.com/guaranteed-copy-elision/)
        + [Simplify code with 'if constexpr' in C++17](https://www.bfilipek.com/2018/03/ifconstexpr.html)
            + [Constexpr if alternative](https://stackoverflow.com/questions/43587405/constexpr-if-alternative)
        + [C++17 Fold expressions](http://filipjaniszewski.com/2016/11/24/c17-folding-expression/)
            + [Reduce: From functional programming to C++17 Fold expressions - Nikos Athanasiou - Meeting C++ 2016](https://www.youtube.com/watch?v=ymNdAkS7Ljc)
        + [simplify C++](https://arne-mertz.de/category/cpp/modern-cpp/)
            + [`std::make_shared` vs. the Normal `std::shared_ptr` Constructor](https://arne-mertz.de/2018/09/make_shared-vs-the-normal-shared_ptr-constructor/)
            + [Как устроен shared_ptr](http://artemy-kolesnikov.blogspot.com/2014/11/sharedptr.html?m=1)
            + [Как устроен weak_ptr](http://artemy-kolesnikov.blogspot.com/2014/11/weakptr.html?m=1)
        + [Top 10 dumb mistakes to avoid with C++ 11 smart pointers](https://www.acodersjourney.com/top-10-dumb-mistakes-avoid-c-11-smart-pointers/)

        + [Stanford C++ Style Guide](http://stanford.edu/class/archive/cs/cs106b/cs106b.1158/styleguide.shtml)
            + [Stanford C++ Style Guide](https://tproger.ru/translations/stanford-cpp-style-guide/amp/)

    + [Trending C++ github repositories](https://github.com/trending/c++)

    + [Optimized C++ book](http://www.guntheroth.com/)

    + [C++17 High Performance](https://github.com/PacktPublishing/Cpp-High-Performance)

    + Valery Lesin. C++ In-Depth, 2014
        + [Лекция 3. Move семантика и Rvalue reference](https://compscicenter.ru/media/slides/cpp_2_2014_spring/2014_02_25_cpp_2_2014_spring.pdf)

    + [The C++ Standards Library for Concurrency and Parallelism http://stellar-group.org/libraries/hpx](https://github.com/STEllAR-GROUP/hpx)
        + [HPX (High Performance ParalleX) is a general purpose C++ runtime system for parallel and distributed applications of any scale](http://stellar-group.org/libraries/hpx)
        + [HPX — рантайм-система для параллельных и распределенных вычислений](https://corehard.by/2016/02/15/conf2016-hpx/)

    + [Modern C++ for fun and profit](https://chariotsolutions.com/wp-content/uploads/2016/04/Modern-C-for-Fun-and-Profit-ETE.pdf)
        + [free C++ books](http://freecomputerbooks.com/langCppBooks.html)
        + [MODERN C++ FOR C PROGRAMMERS: PART 4](https://ds9a.nl/articles/posts/cpp-4/)

    + [using extern template (C++11)](https://stackoverflow.com/questions/8130602/using-extern-template-c11)
        + tl;dr
            + use case in [Flexible Collision Library](https://github.com/flexible-collision-library/fcl)
            + don't confuse with [export templates](https://stackoverflow.com/questions/5416872/using-export-keyword-with-templates)

    + [Is pass-by-value a reasonable default in C++11?](https://stackoverflow.com/questions/7592630/is-pass-by-value-a-reasonable-default-in-c11/7592741#7592741)

    + SFINAE
        + [SFINAE](https://en.cppreference.com/w/cpp/language/sfinae)
        + [C++ SFINAE examples?](https://stackoverflow.com/questions/982808/c-sfinae-examples)

    + [C++ samples](http://www.cppsamples.com/)
        + [Introduction To valarray](http://cppisland.com/?p=518)
            + [C++ valarray vs. vector](https://stackoverflow.com/questions/1602451/c-valarray-vs-vector)
        + [Atomic Basics](http://cppisland.com/?p=436)
        + [Подборка ресурсов с примерами кода на разных языках](https://tproger.ru/digest/learn-everything-by-examples/)

    + enum to string in modern C++11 / C++14 and future C++17 / C++20
        + [enum to string in modern C++11 / C++14 and future C++17 / C++20](https://stackoverflow.com/questions/28828957/enum-to-string-in-modern-c11-c14-and-future-c17-c20)
        + [Enum to string в современном C ++ и будущем C ++ 17 / C ++ 20](http://qaru.site/questions/9861/enum-to-string-in-modern-c-and-future-c17-c20)
        + [How to perform tuple arithmetic in C++ (c++11/c++17)?](https://stackoverflow.com/questions/47209672/how-to-perform-tuple-arithmetic-in-c-c11-c17)

    + [CRTP demystifyed](http://scrutator.me/post/2014/06/26/crtp_demystified.aspx)
        + [The Curiously Recurring Template Pattern (CRTP)](https://www.fluentcpp.com/2017/05/12/curiously-recurring-template-pattern/)
        + [What the Curiously Recurring Template Pattern can bring to your code](https://www.fluentcpp.com/2017/05/16/what-the-crtp-brings-to-code/)
        + [An Implementation Helper For The Curiously Recurring Template Pattern](https://www.fluentcpp.com/2017/05/19/crtp-helper/)
        + [The “Extract Interface” refactoring, at compile time](https://www.fluentcpp.com/2017/04/28/extract-interface-cpp/)

    + C++ and multithreading
        + Memory Model
            + [C++11 introduced a standardized memory model. What does it mean? And how is it going to affect C++ programming?](https://stackoverflow.com/questions/6319146/c11-introduced-a-standardized-memory-model-what-does-it-mean-and-how-is-it-g?rq=1)
        + [Top 20 C++ multithreading mistakes and how to avoid them](http://www.acodersjourney.com/2017/08/top-20-cplusplus-multithreading-mistakes/)    
        tl;dr
            1. Not using `join()` to wait for background threads before terminating an application.
            2. Trying to `join()` a thread that has been previously detached.
            3. Not realizing that `std::thread::join()` blocks the calling thread.
            4. Thinking that thread function arguments are pass by reference by default.    
                tl;dr use `std::ref()` for passing by reference.
            5. Not protecting shared data or shared resources with a critical section (eg. mutex).
            6. Forgetting to release locks after a critical section.
            7. Not keeping critical sections as compact and small as possible.
            8. Not acquiring multiple locks in the same order.
            9. Trying to acquire a `std::mutex` twice.
            10. Using mutexes when `std::atomic` types will suffice.
            11. Creating and Destroying a lot of threads directly when using a thread pool is available.
            12. Not handling exceptions in background threads.
            13. Using threads to simulate Asyn jobs when `std::async` will do.
            14. Not using `std::launch::async` if asynchronicity is desired.
            15. Calling `.get()` on a `std::future` in a time sensitive code path.
            16. Not realizing that an exception thrown inside an async task is propagated when `std::future::get()` is invoked.
            17. Using `std::async` when you need granular control over thread execution.
            18. Creating many more "Runnable" threads than available cores.
            19. Using `volatile` keyword for synchronization.
            20. Using a Lock Free architecture unless absolutely needed

        + [lucid and terse multithread intro](http://www.bogotobogo.com/cplusplus/multithreaded.php)
        + [Multithreading in C++11/14 – Part 1](http://www.loic-yvonnet.com/articles/multithreading-in-cpp14-part-1/)
        + [Multithreading in C++11/14 – Part 2](http://www.loic-yvonnet.com/articles/multithreading-in-cpp14-part-2/)
        + [Multithreading in C++11/14 – Part 12](http://www.loic-yvonnet.com/articles/multithreading-in-cpp14-part-12/)
        + Locking and Conditional Variables
            + [C++11 Multithreading  Part 7: Condition Variables Explained](https://thispointer.com/c11-multithreading-part-7-condition-variables-explained/)
            + [C++11-concurrency-tutorial-advanced-locking-and-condition-variables](http://baptiste-wicht.com/posts/2012/04/c11-concurrency-tutorial-advanced-locking-and-condition-variables.html)
            + [C++11 concurrency: condition variables](http://codexpert.ro/blog/2013/03/01/cpp11-concurrency-condition-variables/)
                + [Потоки, блокировки и условные переменные в C++11 [Часть 2]](https://habrahabr.ru/post/182626/)
            + [std::unique_lock<std::mutex> or std::lock_guard<std::mutex>?](https://stackoverflow.com/questions/20516773/stdunique-lockstdmutex-or-stdlock-guardstdmutex)
            + [std::unique_lock vs. от std::lock_guard?](https://ru.stackoverflow.com/questions/843495/%D0%A7%D0%B5%D0%BC-stdunique-lock-%D0%BE%D1%82%D0%BB%D0%B8%D1%87%D0%B0%D0%B5%D1%82%D1%81%D1%8F-%D0%BE%D1%82-stdlock-guard)
                + tl;dr
                almost the same, but `lock_guard` has less functionality, locks only once and more preferrable;
                use `lock_guard` unless you need unlocling, for `condition_variable`s that `wait()`ing from sleep.
        + [http://preshing.com/20130618/atomic-vs-non-atomic-operations/](http://preshing.com/20130618/atomic-vs-non-atomic-operations/)
        + [Comparison: Lockless programming with atomics in C++ 11 vs. mutex and RW-locks](https://www.arangodb.com/2015/02/comparing-atomic-mutex-rwlocks/)
        + [THE INFINITE LOOP: The ticket spinlock](https://geidav.wordpress.com/tag/spinlock/)
        + [Разработка → Конкурентность: Параллелизм](https://m.habrahabr.ru/post/318374/)
        + [What is the equivalent of boost::upgrade_to_unique_lock in STL?](http://stackoverflow.com/questions/30300212/what-is-the-equivalent-of-boostupgrade-to-unique-lock-in-stl)
        + [Охранные классы в boost::thread](http://htrd.su/wiki/zhurnal/2012/12/10/oxrannye_klassy_v_boost_thread)
        + [code review: Yet another event dispatcher in c++11](http://codereview.stackexchange.com/questions/123296/yet-another-event-dispatcher-in-c11)
        + [A simple proof-of-concept for C++11 event dispatching](https://github.com/Submanifold/Events)
    + [C++11 FAQ rom the author of C++](http://www.stroustrup.com/C++11FAQ.html)
    + [C++11 Tidbits: Template Aliases](https://blogs.oracle.com/pcarlini/entry/template_aliases)
        + [Why is `allocator::rebind` necessary when we have template template parameters?](http://stackoverflow.com/questions/12362363/why-is-allocatorrebind-necessary-when-we-have-template-template-parameters)
        + tl;dr
        instead of
        ```c++
        template<typename T>
        class allocator {
            //...
 
            template<typename U>
                struct rebind { typedef allocator<U> other; };
        };

        allocator<T>::rebind<U>::other x;  // sample usage
        ```
        can be rewritten
        ```c++
        template<typename T>
        class allocator {
            //...

            template<typename U>
                using rebind = allocator<U>;
        };

        allocator<T>::rebind<U> x;         // sample usage
        ```
        + why `rebind`
        ```c++
        template <typename T, typename A = std::allocator<T>>
        class list {
            struct node {
                T value;
                node* next;
                node* prev;
            };
            using allocator = typename A::template rebind<node>::other;
        };
        ```
    + [Variable template](http://en.cppreference.com/w/cpp/language/variable_template)
        + tl;dr
        ```
        template<class T>
        constexpr T pi = T(3.1415926535897932385);  // variable template
         
        template<class T>
        T circular_area(T r) // function template
        {
            return pi<T> * r * r; // pi<T> is a variable template instantiation
        }
        ```
    + [What Every C++ Developer Should Know to (Correctly) Define Global Constants](https://www.fluentcpp.com/2019/07/23/how-to-define-a-global-constant-in-cpp/)
    + [Why const Doesn't Make C Code Faster](https://theartofmachinery.com/2019/08/12/c_const_isnt_for_performance.html)
    + [Impossibly fast delegate in C++11](http://codereview.stackexchange.com/questions/14730/impossibly-fast-delegate-in-c11)
    + [Разработка → RAII + С++ variadic templates = win](https://habrahabr.ru/post/172817/)
    + [C++ convert integer to string at compile time](https://stackoverflow.com/questions/6713420/c-convert-integer-to-string-at-compile-time)
    + [Is there any RAII file handle already implemented?](https://stackoverflow.com/questions/22775500/is-there-any-raii-file-handle-already-implemented)
    + [Perfect forwarding and universal references in C++](http://eli.thegreenplace.net/2014/perfect-forwarding-and-universal-references-in-c/)
    + [Nobody Understands C++](http://blog2.emptycrate.com/tags/nobody-understands)
        + [Nobody Understands C++: Part 5: Template Code Bloat](http://blog2.emptycrate.com/content/nobody-understands-c-part-5-template-code-bloat)
    + [The C++ Core Guidelines are a set of tried-and-true guidelines, rules, and best practices about coding in C++](https://github.com/isocpp/CppCoreGuidelines)
    + [Поразрядная сортировка с человеческим лицом Radix sort in C++](http://habrahabr.ru/post/271677/)
    + [http://habrahabr.ru/company/infopulse/blog/274549/](http://habrahabr.ru/company/infopulse/blog/274549/)
    + [Советы о том, как писать на С в 2016 году](https://habrahabr.ru/company/inoventica/blog/275685/)
    + [The C++ scientist](http://jmabille.github.io/)
    + [Algorithms in C++](https://towardsdatascience.com/algorithms-in-c-62b607a6131d)
    + [Fast function to parse strings into double floating-point values](https://github.com/lemire/fast_double_parser)
    + [C++20: Python's map Function](https://www.modernescpp.com/index.php/c-20-pythons-map-function)
    + [HowardHinnant.github.io World-class C++ expert](http://howardhinnant.github.io/)
        + [Everything You Ever Wanted To Know About Move Semantics](https://github.com/HowardHinnant/presentations/blob/master/accu_2014/accu_2014.pdf)
        + [A date and time library based on the C++11 (and beyond) <chrono> header](https://github.com/HowardHinnant/date)
            + [This paper fully documents a date and time library for use with C++11 and C++14.](https://howardhinnant.github.io/date/date.html)
            + [How to get current time and date in C++?](http://stackoverflow.com/questions/997946/how-to-get-current-time-and-date-in-c)
            + [Convert std::duration to human readable time](https://stackoverflow.com/questions/22590821/convert-stdduration-to-human-readable-time)
    + [GoF patterns in modern C++](https://accu.org/content/conf2013/Tobias_Darm_Effective_GoF_Patterns.pdf)
        + [Effective GoF Patterns with C++11 and Boost—Tobias Darm](https://isocpp.org/blog/2013/10/patterns) 
    + selected stackoverflow questions
        + [What is the usefulness of `enable_shared_from_this`?](https://stackoverflow.com/questions/712279/what-is-the-usefulness-of-enable-shared-from-this)
            + [std::enable_shared_from_this](http://ru.cppreference.com/w/cpp/memory/enable_shared_from_this)
        + [How and why one would use Boost signals2?](http://stackoverflow.com/questions/18663490/how-and-why-one-would-use-boost-signals2)
            + [Is boost::signals2 overkill for simple applications?](http://stackoverflow.com/questions/22416860/is-boostsignals2-overkill-for-simple-applications?noredirect=1&lq=1)    
            tl;dr almost 100x performance penalty over plain function call
            + [Conversion of Qt Signals to Boost Signals2](http://stackoverflow.com/questions/20562430/conversion-of-qt-signals-to-boost-signals2)
                + [Messaging and Signaling in C++](https://meetingcpp.com/index.php/br/items/messaging-and-signaling-in-cplusplus.html)
            + [Making Boost.Signals2 More OOP‐Friendly](https://thehermeticvault.com/software-development/making-boost-signals2-more-oop-friendly)
                + [Protected вызов сигналов в Boost.Signals2](http://www.prog.org.ru/topic_29431_0.html)
        + [Should I use std::function or a function pointer in C++?](http://stackoverflow.com/questions/25848690/should-i-use-stdfunction-or-a-function-pointer-in-c)
            + [C++11 variadic std::function parameter](http://stackoverflow.com/questions/9242234/c11-variadic-stdfunction-parameter)
        + [Difference in make_shared and normal shared_ptr in C++](http://stackoverflow.com/questions/20895648/difference-in-make-shared-and-normal-shared-ptr-in-c)
        + [Usage of std::forward vs std::move](http://stackoverflow.com/questions/28828159/usage-of-stdforward-vs-stdmove)
        + [Advantages of using forward](http://stackoverflow.com/questions/3582001/advantages-of-using)
        + [How does std::forward work?](http://stackoverflow.com/questions/8526598/how-does-stdforward-work)
        + [Why is std::forward useless in this context](http://stackoverflow.com/questions/33999565/why-is-stdforward-useless-in-this-context)
        + [throwing exceptions out of a destructor](http://stackoverflow.com/questions/130117/throwing-exceptions-out-of-a-destructor)
            + summary: `Throwing an exception out of a destructor is dangerous. If another exception is already propagating the application will terminate.` 
            + ["More Effective C++" Item 11: Prevent exceptions from leaving destructors](http://bin-login.name/ftp/pub/docs/programming_languages/cpp/cffective_cpp/MEC/MI11_FR.HTM)
        + [What does the explicit keyword in C++ mean?](http://stackoverflow.com/questions/121162/what-does-the-explicit-keyword-in-c-mean)
            + dubbed from above link
            ```c++
            // Suppose you have a class String:

            class String {
            public:
                String(int n); // allocate n bytes to the String object
                String(const char *p); // initializes object with char *p
            };
            // Now if you try
            
            String mystring = 'x';
            // the char 'x' will be implicitly converted to int and then will call the String(int) constructor.
            // But this is not what the user might have intended. So to prevent such conditions, we shall define the constructor as explicit:
            
            class String {
            public:
                explicit String (int n); //allocate n bytes
                String(const char *p); // initialize sobject with string p
            };
            ```
        + [C++ convert from 1 char to string?](https://stackoverflow.com/questions/17201590/c-convert-from-1-char-to-string)
            + tl;dr
            ```c++
            char c = 42; std::cout << string(1, c) << std::endl;
            ```
        + [How to automatically convert strongly typed enum into int?](http://stackoverflow.com/questions/8357240/how-to-automatically-convert-strongly-typed-enum-into-int)

        + [Can a C++ lambda constructor argument capture the constructed variable?](http://stackoverflow.com/questions/29738655/can-a-c-lambda-constructor-argument-capture-the-constructed-variable)

        + generic variadic lambdas
            + TL;DR
            ```c++
            auto get_item = [&ifs](auto& item) {
                std::string line;
                std::getline(ifs, line);
                std::istringstream iss(line);
                iss >> item;
            };
            ...
            get_items(std::ref(params.thorus_params.xfirst), std::ref(params.thorus_params.yfirst));
            ```
            + [Fun with Lambdas: C++14 Style (part 3)](http://cpptruths.blogspot.ru/2014/08/fun-with-lambdas-c14-style-part-3.html)
            + [What is the easiest way to print a variadic parameter pack using std::ostream?](http://stackoverflow.com/questions/27375089/what-is-the-easiest-way-to-print-a-variadic-parameter-pack-using-stdostream)
            + [Composing Continuations](https://functionalcpp.wordpress.com/)
            + [Unpacking Tuples in C++14](http://aherrmann.github.io/programming/2016/02/28/unpacking-tuples-in-cpp14/)

        + [how to get only keys of values from map](https://stackoverflow.com/questions/39555726/stdmapstring-string-to-string-first-values)
            + [boost::adaptors::map_keys](https://greek0.net/boost-range/boost-adaptors-map_keys.html)

        ```c++
        #include <boost/range/adaptor/map.hpp>
        #include <boost/range/algorithm/copy.hpp>
        #include <boost/assign.hpp>
        #include <boost/algorithm/string/join.hpp>
        #include <algorithm>
        #include <iostream>
        #include <map>
        #include <vector>
        
        int main()
        {
            std::map<std::string, std::string> m;
            m["hello"] = "world";
            m["goodbye"] = "now";
        
            std::vector<std::string> o;
        //    boost::copy(m | boost::adaptors::map_keys, std::back_inserter(o));
            boost::copy(m | boost::adaptors::map_values, std::back_inserter(o));
            std::cout << boost::algorithm::join(o, ", ") << std::endl;
        }
        ```

        + boost.histogram **bare-bone** installation    
        ```sh
        https://github.com/boostorg/histogram.git
        https://github.com/boostorg/mp11.git
        https://github.com/boostorg/callable_traits.git
        https://github.com/boostorg/assert.git
        https://github.com/boostorg/throw_exception.git
        https://github.com/boostorg/core.git
        https://github.com/boostorg/config.git
        https://github.com/boostorg/variant2.git
        ```

        + [Python bindings for the C++14 Boost::Histogram library](https://github.com/scikit-hep/boost-histogram)
            + [Boost-histogram is a Python package providing Python bindings for Boost.Histogram ](https://boost-histogram.readthedocs.io/en/latest/)
            + [issues to Boost-histogram](https://github.com/scikit-hep/boost-histogram/issues)
        + [Boosting the Accuracy of Differentially Private Histograms Through Consistency](https://www.vldb.org/pvldb/vldb2010/pvldb_vol3/R91.pdf)
        + [Improving Accuracy and Robustness of Self-Tuning Histograms by Subspace Clustering](https://dbis.ipd.kit.edu/download/MineClusSTHoles_-_Minor_Revision.pdf)
            + [Improving Accuracy and Robustness of Self-Tuning Histograms by Subspace Clustering](https://www.youtube.com/watch?v=ZXb0ETrzhrs)

        + cheat-sheet for callbacks in C++
            + [Callback functions in c++](http://stackoverflow.com/questions/2298242/callback-functions-in-c)
        + [Using std::make_unique with custom deleter on a derived class?](http://stackoverflow.com/questions/37514101/using-stdmake-unique-with-custom-deleter-on-a-derived-class)
            + tl;dr you cannot indicate a custom deleter with the `make_*` helper functions for smart pointers (neither with `make_unique`, nor with `make_shared`). use
              to explicitly construct your pointer as it follows:
              ```c++
              std::unique_ptr<T, D> ptr{new T{)};
              ```
              If the deleter is not default constructible, you can do this:
              ```c++
              std::unique_ptr<T, D> ptr{new T{}, d};
              ```

        + [std::unique_ptr for class data member ABI (Pimpl idiom)](https://stackoverflow.com/questions/30072094/stdunique-ptr-for-class-data-member-abi-pimpl-idiom)
            + [Move constructor involving const unique_ptr](https://stackoverflow.com/questions/29194304/move-constructor-involving-const-unique-ptr)
            + [Why am I getting compile error “use of deleted function 'std::unique_ptr …”](https://stackoverflow.com/questions/39703954/why-am-i-getting-compile-error-use-of-deleted-function-stdunique-ptr/39705668)    
            tl;dr 
            The chief feature of std::unqiue_ptr is that it cannot be copied. That's by design, and the name tells you as much.
            take `std::unique_ptr<..> const&` -- no copy is needed.

        + `std::call_once()`
            + [std::call_once, std::once_flag](https://riptutorial.com/cplusplus/example/30171/std--call-once--std--once-flag)
            + [std::call_once vs std::mutex for thread-safe initialization](https://stackoverflow.com/questions/26985370/stdcall-once-vs-stdmutex-for-thread-safe-initialization)
            + [Why is this pointer needed when calling std::call_once()?](https://stackoverflow.com/questions/23197333/why-is-this-pointer-needed-when-calling-stdcall-once)
            + [std::call_once safe for non atomic variables?](https://stackoverflow.com/questions/48221492/stdcall-once-safe-for-non-atomic-variables)
            + [Is std::call_once a blocking call?](https://stackoverflow.com/questions/43054677/is-stdcall-once-a-blocking-call)

        + Some tips on iterators
            + [Common Knowledge: Output Iterator Adapters](http://www.drdobbs.com/common-knowledge-output-iterator-adapter/184401483)
            + [A smart iterator for inserting into a sorted container in C++](https://www.fluentcpp.com/2017/03/17/smart-iterators-for-inserting-into-sorted-container/)
        + C++ specialization
            + [Function Templates Partial Specialization in C++](https://www.fluentcpp.com/2017/08/15/function-templates-partial-specialization-cpp/)
            + [C++ Template specialization for subclasses with abstract base class](https://stackoverflow.com/questions/24936862/c-template-specialization-for-subclasses-with-abstract-base-class)
                + [c++ template specialization for base class](https://stackoverflow.com/questions/21437730/c-template-specialization-for-base-class)    
                tl;dr look [partial_specialization.cpp](https://github.com/alsam/cpp-samples/blob/master/c%2B%2Bnew-features/partial_specialization.cpp)
                ```c++
                template <typename M>
                struct SetTarget
                {
                  SetTarget(M* t): target(t) {}
                  M* target;
                };
                
                template <typename M, typename T, bool = std::is_base_of<OperationMessage, T>::value>
                struct SetId : public SetTarget<M>
                {
                  SetId(M* t) : SetTarget<M>(t) {}
                  void operator()(T)
                  {
                    std::cout << "SetId with -1\n";
                    SetTarget<M>::target->setId(-1);
                  }
                };
                
                // partial specialization
                template <typename M, typename T>
                struct SetId<M, T, true> : SetTarget<M>
                {
                  SetId(M* t) : SetTarget<M>(t) {}
                  void operator()(T msg)
                  {
                    std::cout << "SetId with msg.getSequence()\n";
                    SetTarget<M>::target->setId(msg.getSequence());
                  }
                };
                ```

        + selected boost tips
            + boost property tree
                + [boost property tree 5 minutes tutorial](http://www.boost.org/doc/libs/1_61_0/doc/html/property_tree/tutorial.html)
                + [3 ways of getting data from propert tree](http://www.boost.org/doc/libs/1_61_0/doc/html/property_tree/accessing.html)    
                tl;dr
                ```
                auto dump_vector = [](std::string const& name, auto const& v)
                {
                    std::cout << name << " : { ";
                    for (auto val : v)
                    {
                        std::cout << val << ", ";
                    }
                    std::cout << "}\n";
                };
                auto vec = xml_data.get("A.E.S.coeffs", std::vector<float>());
                dump_vector("coeffs", vec);
                ```
            + [Christian Aichinger's thoughts : boost::make_iterator_range](https://greek0.net/boost-range/boost-make_iterator_range.html)
                + [Overview of C++ Variable Initialization](https://greek0.net/cpp/initialization.html)

            + [A method to list all files in directory and sub-directories using boost and c++](https://stackoverflow.com/questions/37618229/a-method-to-list-all-files-in-directory-and-sub-directories-using-boost-and-c)
                + [GitGist : vivithemage/boost_list_directory.cpp](https://gist.github.com/vivithemage/9517678)
                ```c++
                #include <iostream>
                #include <string>
                #include <vector>
                #include <boost/filesystem.hpp>
                #include <boost/range.hpp>
                
                std::vector<std::string>
                get_file_list(std::string const& path)
                {
                    std::vector<std::string> files;
                    if (!path.empty()) {
                        boost::filesystem::path dir = ".";
                        boost::filesystem::recursive_directory_iterator it(dir), end;
                
                        for (auto& entry : boost::make_iterator_range(it, end))
                            if (boost::filesystem::is_regular(entry))
                                files.push_back(entry.path().native());
                    }
                    return files;
                }
                
                int main(int argc, char** argv)
                {
                    if (argc > 1) {
                        auto file_list = get_file_list(argv[1]);
                        for (auto const& f : file_list) {
                            std::cout << "- " << f << std::endl;
                        }
                    }
                }
                ```

        + [non-trivial designated initializers not supported](https://stackoverflow.com/questions/31215971/non-trivial-designated-initializers-not-supported)
        + [No matching function std::forward with lambdas](https://stackoverflow.com/questions/42044116/no-matching-function-stdforward-with-lambdas)
        + [Lambda expressions as class template parameters](https://stackoverflow.com/questions/5849059/lambda-expressions-as-class-template-parameters)
        + [Passing capturing lambda as function pointer](https://stackoverflow.com/questions/28746744/passing-capturing-lambda-as-function-pointer)
        + [Can I use std::vector as a template parameter or does it need to be std::vector<T>?](https://stackoverflow.com/questions/16925041/can-i-use-stdvector-as-a-template-parameter-or-does-it-need-to-be-stdvector)
        + [Clang refuses to compile libstdc++'s <filesystem> header](https://stackoverflow.com/questions/57963460/clang-refuses-to-compile-libstdcs-filesystem-header)
            + [How can I create directory tree in C++/Linux?](https://stackoverflow.com/questions/675039/how-can-i-create-directory-tree-in-c-linux)
            + [C++ Copy directory recursive under unix](https://stackoverflow.com/questions/36428121/c-copy-directory-recursive-under-unix)

        + [Hash Functions for C++ Unordered Containers](https://marknelson.us/posts/2011/09/03/hash-functions-for-c-unordered-containers.html)
            + [About size_t and ptrdiff_t](https://www.viva64.com/en/a/0050/)

    + REST API
        + [REST APIs in C++](http://lordjeb.com/category/c-2/)
        + [What is a good open source C++11 web/HTTP server library for building an application server ?](https://www.reddit.com/r/cpp/comments/2rjbrd/what_is_a_good_open_source_c11_webhttp_server/)
    + XML, HTML and network libraries in C++
        + [A Cheat Sheet for HTTP Libraries in C++](http://kukuruku.co/hub/cpp/a-cheat-sheet-for-http-libraries-in-c)
            + [Boost asio docs](http://theboostcpplibraries.com/boost.asio-network-programming)
        + [Benchmark. Analyzing and Testing Current HTML Parsers TL;DR HTML5Ever is written in Rust:) MyHTML is the fastest; Gumbo is produced by Google](https://lexborisov.github.io/benchmark-html-persers/)
        + [Parsing HTML with C++: Revisited](http://blog.laplante.io/2014/11/parsing-html-c-revisited/)
        + [Getting directory listing over http](http://stackoverflow.com/questions/4496182/getting-directory-listing-over-http)
        + [Downloading flv from youtube using curlpp on top of curl - video not playing](http://stackoverflow.com/questions/3850934/downloading-flv-from-youtube-using-curlpp-on-top-of-curl-video-not-playing)

    + [How do I terminate a thread in C++11?](http://stackoverflow.com/questions/12207684/how-do-i-terminate-a-thread-in-c11)
        + [How to terminate a C++ std::thread?](http://www.bo-yang.net/2017/11/19/cpp-kill-detached-thread)
            + [terminate_cpp_thread : kill thread](https://github.com/bo-yang/terminate_cpp_thread/blob/master/kill_cpp_thread.cc)
    + [What's the difference between “mutex” and “lock”?](http://stackoverflow.com/questions/9382122/whats-the-difference-between-mutex-and-lock)
    + [Потоки, блокировки и условные переменные в C++11 [Часть 2] ](https://habrahabr.ru/post/182626/)
    + [C++11 threads, affinity and hyperthreading](http://eli.thegreenplace.net/2016/c11-threads-affinity-and-hyperthreading/)
    + C++11 and semaphores
        + [C++0x has no semaphores? How to synchronize threads?](http://stackoverflow.com/questions/4792449/c0x-has-no-semaphores-how-to-synchronize-threads/19659736#19659736)
        + [Semaphores C++11 when Multithreading](http://austingwalters.com/multithreading-semaphores/)
        + [why do I need std::condition_variable?](http://stackoverflow.com/questions/16350473/why-do-i-need-stdcondition-variable)
    + intrusive prt vs. `std::shared_ptr`
        + [Boost intrusive_ptr and its usage in C++ programming](http://baptiste-wicht.com/posts/2011/11/boost-intrusive_ptr.html)
        + [Archives for posts with tag: intrusive_ptr](https://kinestheticcoding.wordpress.com/tag/intrusive_ptr/)
        + [intrusive_ptr против shared_ptr. Что лучше.](http://www.gamedev.ru/code/forum/?id=34739)
    + [Double-Checked Locking is Fixed In C++11](http://preshing.com/20130930/double-checked-locking-is-fixed-in-cpp11/)
        + [Several C++ singleton implementations](http://silviuardelean.ro/2012/06/05/few-singleton-approaches/) 
        ```c++
        class smartSingleton
        {
          private:
            static std::mutex _mutex;
         
            smartSingleton();
            smartSingleton(const smartSingleton& rs);
            smartSingleton& operator = (const smartSingleton& rs);
         
          public:
            ~smartSingleton();
         
          static std::shared_ptr& getInstance() {
            static std::shared_ptr instance = nullptr;

            if (!instance) {
              std::lock_guard lock(_mutex);

              if (!instance) {
                instance.reset(new smartSingleton());
              }
            }
         
            return instance;
          }
         
          void demo() { std::cout << "smart pointers # next - your code ..." << std::endl; }
        };
        ```
        + [How to implement multithread safe singleton in C++11 without using <mutex>](http://stackoverflow.com/questions/11711920/how-to-implement-multithread-safe-singleton-in-c11-without-using-mutex) 
        ```c++
        class Singleton
        {
        public:
        static Singleton & Instance()
        {
            // Since it's a static variable, if the class has already been created,
            // It won't be created again.
            // And it **is** thread-safe in C++11.
        
            static Singleton myInstance;
        
            // Return a reference to our instance.
            return myInstance;
        }
        
        // delete copy and move constructors and assign operators
        Singleton(Singleton const&) = delete;             // Copy construct
        Singleton(Singleton&&) = delete;                  // Move construct
        Singleton& operator=(Singleton const&) = delete;  // Copy assign
        Singleton& operator=(Singleton &&) = delete;      // Move assign
        
        // Any other public methods
        
        protected:
        Singleton()
        {
             // Constructor code goes here.
        }
        
        ~Singleton()
        {
             // Destructor code goes here.
        }
        
         // And any other protected methods.
        }
        ```

        + Progress Bar
            + [How to display a progress indicator in pure C/C++ (cout/printf)?](https://stackoverflow.com/questions/14539867/how-to-display-a-progress-indicator-in-pure-c-c-cout-printf)
            tl;dr more neat and nice solution    
            ```c++
            void printProgressNice (float percentage, int wid = 60)
            {
                const char PBFILLER[] = "█";
                int val = (int) (percentage * 100);
                int lpad = (int) (percentage * wid);
                int rpad = wid - lpad;
                printf("\r%3d%%[", val);
                while (lpad--)
                    printf("%s", PBFILLER);
                while (rpad--)
                    putchar(' ');
                printf("]");
                fflush(stdout);
            }
            ```
            + [Make better CLI progress bars with Unicode block characters](https://mike42.me/blog/2018-06-make-better-cli-progress-bars-with-unicode-block-characters)
            + [How to repeat a string a variable number of times in C++?](https://stackoverflow.com/questions/166630/how-to-repeat-a-string-a-variable-number-of-times-in-c)

        + [К тридцатилетию первого C++ компилятора: ищем ошибки в Cfront](http://www.viva64.com/ru/b/0355/)

        + [Is C++21 the Next Standard?](https://stackoverflow.com/questions/38789652/is-c21-the-next-standard/38789876)
            + [juCi++: a lightweight, platform independent C++-IDE with support for C++11, C++14 and C++17 features depending on libclang version.](https://gitlab.com/cppit/jucipp)
            + [Pure Virtual C++ 2020](https://www.youtube.com/playlist?list=PLReL099Y5nRdHYz4JwB0bq1kaVw2yGDag)
                + [Dynamic Polymorphism with Metaclasses and Code Injection with Sy Brand](https://www.youtube.com/watch?v=drt3yXI-fqk&list=PLReL099Y5nRdHYz4JwB0bq1kaVw2yGDag&index=2&t=0s)
                + [Practical C++20 Modules and the future of tooling around C++ Modules with Cameron DaCamara](https://www.youtube.com/watch?v=ow2zV0Udd9M&list=PLReL099Y5nRdHYz4JwB0bq1kaVw2yGDag&index=8&t=0s)
                + [C++ Development with Visual Studio Code with Julia Reid](https://www.youtube.com/watch?v=WqXrYfSKJXk&list=PLReL099Y5nRdHYz4JwB0bq1kaVw2yGDag&index=6&t=0s)
                + [Peeking Safely at a Table with Concepts with Gabriel Dos Reis](https://www.youtube.com/watch?v=xO7JG0GarG4&list=PLReL099Y5nRdHYz4JwB0bq1kaVw2yGDag&index=7&t=0s)
            + [C++20: The Big Four](https://www.modernescpp.com/index.php/thebigfour)
                + [C++20: Coroutines - A First Overview](https://www.modernescpp.com/index.php/c-20-coroutines-the-first-overview)
                + [C++20: More Details to Coroutines](https://www.modernescpp.com/index.php/c-20-coroutines-more-details)
                + [C++20: Coroutines with cppcoro](https://www.modernescpp.com/index.php/c-20-coroutines-with-cppcoro)
                + [C++20: An Infinite Data Stream with Coroutines](https://www.modernescpp.com/index.php/c-20-an-infinite-data-stream-with-coroutines)
                + [C++20: Thread Synchronization with Coroutines](https://www.modernescpp.com/index.php/c-20-thread-synchronization-with-coroutines)
                + [C++20: Thread Pools with cppcoro](https://www.modernescpp.com/index.php/c-20-thread-pools-with-cppcoro)


        + selected C++ projects
            + [Modern C++ Parallel Task Programming](https://github.com/cpp-taskflow/cpp-taskflow)
                + [docs for Modern C++ Parallel Task Programming](https://cpp-taskflow.github.io/cpp-taskflow/index.html)
            + [Filament is a physically based rendering engine for Android, Windows, Linux and macOS](https://github.com/google/filament)
