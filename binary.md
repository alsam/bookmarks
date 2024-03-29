# binary analysis frameworks

+ capstone unicorn keystone radare2
    + [unicorn + capstone + keystone](https://www.xandora.io/opensource)
    + [Unicorn Engine](https://github.com/unicorn-engine/unicorn)
        + [Unicorn Showcase](https://www.unicorn-engine.org/showcase/)
            + [CEmu : The Cheap (Assembly) Emulator](https://github.com/hugsy/cemu)
    + [Capstone is a lightweight multi-platform, multi-architecture disassembly framework](https://www.capstone-engine.org/)

+ [angr is an open-source binary analysis platform for Python](https://angr.io)
    + [angr is a platform-agnostic binary analysis framework](https://github.com/angr/angr)
    + [CLE loads binaries and their associated libraries, resolves imports and provides an abstraction of process memory the same way as if it was loader by the OS's loader](https://github.com/angr/cle)
        + [Loading a Binary - CLE and angr Projects#symbols-and-relocations](https://github.com/angr/angr-doc/blob/master/docs/loading.md#symbols-and-relocations)
    + Breaking CMU's Bomblab with Angr for Fun and Profit
        + [Breaking CMU's Bomblab with Angr for Fun and Profit - Part 1](https://fanpu.io/2020/07/30/breaking-cmu-bomblab-with-angr-for-fun-and-profit-part-1/)
        + [Breaking CMU's Bomblab with Angr for Fun and Profit - Part 2](https://fanpu.io/2020/07/31/breaking-cmu-bomblab-with-angr-for-fun-and-profit-part-2/)
        + [Breaking CMU's Bomblab with Angr for Fun and Profit - Part 3](https://fanpu.io/2020/08/01/breaking-cmu-bomblab-with-angr-for-fun-and-profit-part-3/)
        + [Breaking CMU's Bomblab with Angr for Fun and Profit - Part 4](https://fanpu.io/2020/08/02/breaking-cmu-bomblab-with-angr-for-fun-and-profit-part-4/)
        + [Breaking CMU's Bomblab with Angr for Fun and Profit - Part 5](https://fanpu.io/2020/08/02/breaking-cmu-bomblab-with-angr-for-fun-and-profit-part-5/)
        + [Breaking CMU's Bomblab with Angr for Fun and Profit - Part 6](https://fanpu.io/2020/08/02/breaking-cmu-bomblab-with-angr-for-fun-and-profit-part-6/)
        + [Breaking CMU's Bomblab with Angr for Fun and Profit - Part 7](https://fanpu.io/2020/08/02/breaking-cmu-bomblab-with-angr-for-fun-and-profit-part-7/)
    + [angr's solver engine is called Claripy](https://docs.angr.io/advanced-topics/claripy)
    + [angr ycombinator](https://news.ycombinator.com/item?id=17112998)
    + [Angr - Examples](https://book.hacktricks.xyz/reversing-and-exploiting/reversing-tools-basic-methods/angr/angr-examples)
    + [Top Level Interfaces](https://docs.angr.io/core-concepts/toplevel)
+ [Symbolic execution](https://alastairreid.github.io/RelatedWork/notes/symbolic-execution/)
    + [Enhancing symbolic execution with veritesting](https://alastairreid.github.io/RelatedWork/papers/avgerinos:icse:2014/)

+ [The purpose of LIEF project is to provide a cross platform library which can parse, modify and abstract ELF, PE and MachO formats](https://github.com/lief-project/LIEF)
    + [Profiling C++ code with Frida (2nd part)](https://lief-project.github.io/blog/2021-04-08-profiling-cpp-code-with-frida-part2/)

+ [What do the .eh_frame and .eh_frame_hdr sections store, exactly?](https://stackoverflow.com/questions/14091231/what-do-the-eh-frame-and-eh-frame-hdr-sections-store-exactly)
    + [ref code for eh_frame_header](https://github.com/mclinker/mclinker)

+ [What is PLT/GOT?](https://reverseengineering.stackexchange.com/questions/1992/what-is-plt-got)
    + [Linkers part 1](https://www.airs.com/blog/archives/38)
    + [Linkers part 6 - Relocations](https://www.airs.com/blog/archives/43)

+ gem5
    + [Creating a very simple SimObject](https://www.gem5.org/documentation/learning_gem5/part2/helloobject/)
    + [Cycle-accurate Benchmarking of JavaScript Programs](http://www2.imm.dtu.dk/pubdb/pubs/6276-full.html)
    + [gem5 TraceCPU](https://www.gem5.org/documentation/general_docs/cpu_models/TraceCPU)
    + [Memory Access Analysis and Endurance Leveling Approaches for Non-volatile Working Memory Systems](https://daes.cs.tu-dortmund.de/storages/daes-cs/r/Bilder/Beschaeftigte/Christian_Hakert/publications/2019-hakert.pdf)
    + [Minor CPU Model](https://www.gem5.org/documentation/general_docs/cpu_models/minor_cpu)
    + [O3CPU - Out-of-Order](https://www.gem5.org/documentation/general_docs/cpu_models/O3CPU)
    + [Memory controller updates for new DRAM technologies, NVM interfaces and flexible memory topologies](https://www.gem5.org/2020/05/27/memory-controller.html)
    + [gem5-gpu Developers List: question about using a different memory controller](https://groups.google.com/g/gem5-gpu-dev/c/AZFYoKzrD3I?pli=1)
    + [Using perf_event with the ARM PMU inside gem5](https://stackoverflow.com/questions/63988672/using-perf-event-with-the-arm-pmu-inside-gem5)
    + [Performance Monitoring Unit](https://trustedfirmware-a.readthedocs.io/en/latest/perf/performance-monitoring-unit.html)
    + [Investigating Black-Box Function Recognition Using Hardware Performance Counters](https://arxiv.org/pdf/2204.11639.pdf)
    + [Examining the use of ARM PMUs for DVFS and scheduling](https://teh6.host.cs.st-andrews.ac.uk/files/coursework-reports/CS5199-Report.pdf)
    + [Simulation of RISC-V based Systems in gem5](https://cfaed.tu-dresden.de/files/Images/people/chair-cc/theses/1808_Scheffel.pdf)
    + [A Tutorial on the Gem5 Minor CPU Model](https://nitish2112.github.io/post/gem5-minor-cpu/)
    TL;DR
    ```sh
    scons build/ARM/gem5.opt
    ./build/ARM/gem5.opt --debug-flags=Exec configs/example/arm/starter_se.py --cpu=minor some-elf-binary
    ```

+ ChampSim
    + [ChampSim is a trace-based simulator for a microarchitecture study](https://github.com/ChampSim/ChampSim)

+ [Building a RISC-V simulator in Rust - Part 1](https://gregchadwick.co.uk/blog/building-rrs-pt1/)

+ [trustedfirmware Performance Monitoring Unit](https://trustedfirmware-a.readthedocs.io/en/latest/perf/performance-monitoring-unit.html)

+ [Dynarmic - A dynamic recompiler for ARM](https://github.com/merryhime/dynarmic)
+ [Dust - A Nintendo DS emulator written in Rust](https://github.com/kelpsyberry/dust)
+ [ARM Guide from Michael Royal](https://github.com/mikeroyal/ARM-Guide)
+ [RISC-V Guide from Michael Royal](https://github.com/mikeroyal/RISC-V-Guide)

+ MIPT
    + [folder contains sources for the Simulation Book](https://github.com/grigory-rechistov/simbook)
    + [Presentation for "Fundamentals of Full-Platform Simulation" MIPT course](https://github.com/yulyugin/sim-lectures)
    + [Computer Architecture 2021/2022](https://mipt-ilab.github.io/mipt-mips/)
    + [MIPT-V / MIPT-MIPS is a pre-silicon simulator of MIPS and RISC-V CPU](https://github.com/MIPT-ILab/mipt-mips)
    + [Why does a processor have 32 registers?](https://cs.stackexchange.com/questions/22589/why-does-a-processor-have-32-registers)

+ RISC V
    + [8 мифов о микропроцессорах RISC-V — ответ критикам](https://habr.com/ru/companies/selectel/articles/663038/)
        + [Addressing Criticism of RISC-V Microprocessors](https://medium.com/codex/addressing-criticism-of-risc-v-microprocessors-803239b53284)
