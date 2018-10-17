+ Code Optimization - mostly C++
    + [Intel 64 and IA-32 Architectures Optimization Reference Manual](http://www.intel.com/content/dam/www/public/us/en/documents/manuals/64-ia-32-architectures-optimization-manual.pdf)
    + [Знакомьтесь, loop fracking](http://habrahabr.ru/post/271905/)
    + [Приемы использования масочных регистров в AVX512 коде](http://habrahabr.ru/company/intel/blog/266055/)
    + [LLVM для исследователей](http://habrahabr.ru/company/abbyy/blog/265871/)
    + [Оптимизация циклов: нужны блоки](http://habrahabr.ru/company/intel/blog/265095/)
    + [«Ра-а-авняйсь, смирно!». Выравниваем данные](http://habrahabr.ru/company/intel/blog/262933/)
    + [Городские легенды о медленных вызовах виртуальных функций](http://habrahabr.ru/company/abbyy/blog/248429/)
    + [Основные проблемы влияющие на производительность вычислительного ядра и приложения и методы их решения компилятором](http://habrahabr.ru/company/intel/blog/158759/)
    + [Как правильно скопировать массив и при чем тут SFINAE](http://habrahabr.ru/post/150654/)
    + [Linux Performance](http://www.brendangregg.com/linuxperf.html)

+ g++ autovectorization tips and issues - SSE,AVX
    + [GCC auto-vectorization has no effect on runtime, even when supposedly “profitable”](http://stackoverflow.com/questions/26945981/gcc-auto-vectorization-has-no-effect-on-runtime-even-when-supposedly-profitabl) 
    + [Vectorize Source-Code](https://twiki.cern.ch/twiki/bin/view/LHCb/VectorizeSource-code)
    + [How to Write Fast Numerical Code](https://www.inf.ethz.ch/personal/markusp/teaching/263-2300-ETH-spring11/slides/class17.pdf)
    + [SSE multiplication of 4 32-bit integers](http://stackoverflow.com/questions/10500766/sse-multiplication-of-4-32-bit-integers)
    + [Vectorization in gcc](https://monoinfinito.wordpress.com/series/vectorization-in-gcc/)
    + [C++ - Getting started with SSE](http://felix.abecassis.me/2011/09/cpp-getting-started-with-sse/)
    + [FastC++: Coding Cpp Efficiently](http://fastcpp.blogspot.ru/2013/03/efficient-processing-of-arrays-using.html)

+ [Is Parallel Programming Hard, And, If So, What Can You Do About It?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
    + [Paul E. McKenney](http://www.rdrop.com/~paulmck/) 

+ Performance Monitor
    + [What are perf cache events meaning?](http://stackoverflow.com/questions/12601474/what-are-perf-cache-events-meaning)
    + [perfmon2](http://perfmon2.sourceforge.net/)
    + [perf wiki](https://perf.wiki.kernel.org/index.php/Main_Page)
        + [also](https://en.wikipedia.org/wiki/Perf_%28Linux%29)
        + [Where Do I get Source package for Perf tool](http://unix.stackexchange.com/questions/98399/where-do-i-get-source-package-for-perf-tool)
    + [Linux Performance Monitoring, any way to monitor per-thread?](http://stackoverflow.com/questions/28058710/linux-performance-monitoring-any-way-to-monitor-per-thread)
        + [An easy-to-use interface to the Linux perf_event API.](https://github.com/castl/easyperf)
    + [oprofile](http://oprofile.sourceforge.net/doc/overview.html)
        + tl;dr
        ```sh
        operf [ options ] [ --system-wide | --pid=<PID> | [ command [ args ] ] ]
        A typical usage might look like this:
        operf ./my_test_program my_arg
        ```

+ MMU - TLB - huge pages
    + [Virtual Memory](http://austingwalters.com/virtual-memory-and-you/)
    + [Which CPUs support 1GB pages?](http://superuser.com/questions/710870/which-cpus-support-1gb-pages)
    + [How to use Intel Westmere 1GB pages on Linux?](http://stackoverflow.com/questions/27951778/how-to-use-intel-westmere-1gb-pages-on-linux)
        + [Some benchmarks to evaluate NUMA remote memory overhead](https://github.com/ManuelSelva/c4fun)
    + [HugeTLB - Large Page Support in the Linux Kernel](http://linuxgazette.net/155/krishnakumar.html)
    + [Hugepages](https://wiki.debian.org/Hugepages)
    + [Huge pages part 1 (Introduction)](https://lwn.net/Articles/374424/)
        + [libhugetlbfs](https://github.com/libhugetlbfs/libhugetlbfs)
        + [Huge pages part 1 (Introduction)](http://lwn.net/Articles/374424/)
        + [Huge pages part 5: A deeper look at TLBs and costs](http://lwn.net/Articles/379748/)
        + [Memory part 7: Memory performance tools](https://lwn.net/Articles/257209/)
            + [Enabling Large Page Support](http://dev.mysql.com/doc/refman/5.1/en/large-page-support.html)
            + [Using mmap and madvise for huge pages](http://stackoverflow.com/questions/30470972/using-mmap-and-madvise-for-huge-pages)
            + [mmap failed when trying to map huge page (1GB)](http://stackoverflow.com/questions/28826470/mmap-failed-when-trying-to-map-huge-page-1gb)
            + [How do I allocate a DMA buffer backed by 1GB HugePages in a linux kernel module?](http://stackoverflow.com/questions/19460544/how-do-i-allocate-a-dma-buffer-backed-by-1gb-hugepages-in-a-linux-kernel-module)
    + [How Bad Can 1GB Pages Be?](http://www.pvk.ca/Blog/2014/02/18/how-bad-can-1gb-pages-be/#disqus_thread)
    + [Multiple Page Size Support in the Linux Kernel](https://www.researchgate.net/publication/2566253_Multiple_Page_Size_Support_in_the_Linux_Kernel)
    + mmap/munmap tips
        + [munmap()--Remove Memory Mapping](https://www.ibm.com/support/knowledgecenter/ssw_i5_54/apis/munmap.htm)
    + [Writing an OS in Rust - Page Tables](http://os.phil-opp.com/modifying-page-tables.html)

+ Cache issues
    + [Determine if cache is write-back or write-through](http://stackoverflow.com/questions/12739472/determine-if-cache-is-write-back-or-through) 
    + [What causes a L3 cache miss in CPU?](http://stackoverflow.com/questions/10414787/what-causes-a-l3-cache-miss-in-cpu?)
    + [What is “cache-friendly” code?](http://stackoverflow.com/questions/16699247/what-is-cache-friendly-code?rq=1)
    + [Cache Optimizing](http://austingwalters.com/cache-optimizing/)
    + [Caches and multithreading](http://austingwalters.com/the-cache-and-multithreading/)
    + [Optimizing `for` loops](https://docs.google.com/presentation/d/1uYhRYHBWX3J_CJ0vGi3L3bJ7lcZ2hwf4hvFA7HPxDjc/edit#slide=id.g271f1295a_048)

+ Other Memory issues
    + [stream memory benchmarks](http://www.cs.virginia.edu/stream/)
    + [Poor memcpy Performance on Linux - AVX code for `memcpy`](http://stackoverflow.com/questions/22793669/poor-memcpy-performance-on-linux)
    + [various `memcpy` tips](http://www.tek-tips.com/viewthread.cfm?qid=889739)
    + [fast memcpy](http://www.dpdk.org/browse/dpdk/tree/lib/librte_eal/common/include/arch/x86/rte_memcpy.h)

    + new technologies from Intel : Cache Monitoring Technology (CMT), Memory Bandwidth Monitoring (MBM), Cache Allocation Technology (CAT) and Code and Data Prioritization (CDP) Technology
        + [Cache Monitoring Technology (CMT), Memory Bandwidth Monitoring (MBM), Cache Allocation Technology (CAT) and Code and Data Prioritization (CDP) Technology](https://01.org/packet-processing/cache-monitoring-technology-memory-bandwidth-monitoring-cache-allocation-technology-code-and-data)
        + [User space software for Intel(R) Resource Director Technology http://www.intel.com/content/www/us/en/architecture-and-technology/resource-director-technology.html](https://github.com/01org/intel-cmt-cat/tree/master/examples/c/CAT)
        + [processors supporting CAT Cache Allocation Technology](https://communities.intel.com/thread/99160)
        + [A few experiments with the Cache Allocation Technology](https://indico.cern.ch/event/497446/attachments/1229239/1801121/A_few_experiments_with_the_Cache_Allocation_Technology.pdf)
        + [CAT white paper](http://www.intel.com/content/dam/www/public/us/en/documents/white-papers/cache-allocation-technology-white-paper.pdf)

+ Timers
    + [Precise Linux Timing - What Determines the Resolution of clock_gettime()?](http://stackoverflow.com/questions/18343188/precise-linux-timing-what-determines-the-resolution-of-clock-gettime)
    + [Measure time in Linux - time vs clock vs getrusage vs clock_gettime vs gettimeofday vs timespec_get?](http://stackoverflow.com/questions/12392278/measure-time-in-linux-time-vs-clock-vs-getrusage-vs-clock-gettime-vs-gettimeof?rq=1)

+ Videos from The 3rd annual JuliaCon 2016 (MIT)
    + [The 3rd annual JuliaCon 2016 (MIT) | Introduction to Writing High Performance Julia | Arch D. Robison](https://www.youtube.com/watch?v=szE4txAD8mk&list=PLP8iPy9hna6SQPwZUDtAM59-wPzCPyD_S&index=25)

+ Useful pieces of information
    + [Difference between Mutex, Semaphore & Spin Locks](http://stackoverflow.com/questions/23511058/difference-between-mutex-semaphore-spin-locks)
    + [Does endless While loop take up CPU resources?](http://stackoverflow.com/questions/13680512/does-endless-while-loop-take-up-cpu-resources)

+ Assembler
    + [Compiler Explorer C++](https://gcc.godbolt.org/)
    + [Whirlwind Tour of ARM Assembly](http://www.coranac.com/tonc/text/asm.htm)
