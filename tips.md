# useful tips
+ git & github
    + [Git и Github. Простые рецепты](http://habrahabr.ru/post/273897/)
    + [Моя шпаргалка по работе с Git](http://eax.me/git-commands/)
    + Mary Rose Cook on git
        + [Mary Rose Cook blog](http://maryrosecook.com/)
        + [github for maryrosecook.com](https://github.com/maryrosecook/maryrosecook.com)
    + [git returns http error 407 from proxy after CONNECT](http://stackoverflow.com/questions/24907140/git-returns-http-error-407-from-proxy-after-connect)
    + [19 советов по повседневной работе с Git](http://habrahabr.ru/company/mailru/blog/267595/)
    + [Достаточно Git-а, чтобы быть (менее) опасным](http://habrahabr.ru/post/268951/)
    + [git checkout tag, git pull fails in branch](http://stackoverflow.com/questions/10147475/git-checkout-tag-git-pull-fails-in-branch)
      ```sh
      git push -u origin master
      git pull origin master
      git pull
      git branch --set-upstream-to=origin/master master
      git pull
      git branch -u origin/master
      git branch --set-upstream-to=origin/master master
      git branch -u origin/master
      ```
    + [A Git Horror Story: Repository Integrity With Signed Commits](https://mikegerwitz.com/papers/git-horror-story)

+ compile optimization tips (TODO reorganize)
    + [Why doesn't GCC optimize a*a*a*a*a*a to (a*a*a)*(a*a*a)?](http://stackoverflow.com/questions/6430448/why-doesnt-gcc-optimize-aaaaaa-to-aaaaaa)

+ Editors

    + [What are the best programming text editors?](http://www.slant.co/topics/12/~programming-text-editors)

    + [How to Select Columns in Editors (Kate, Vim, etc.)](http://stackoverflow.com/questions/1802616/how-to-select-columns-in-editors-notepad-kate-vim-sublime-textpad-etc-an)

    + vim tips
        :set ff=unix
        + [From Vim to Emacs+Evil chaotic migration guide](http://juanjoalvarez.net/es/)
        + [The Modern Vim Config with Pathogen](http://tammersaleh.com/posts/the-modern-vim-config-with-pathogen/)
            + [vim-pathogen](https://github.com/tpope/vim-pathogen)
        + vim+scala
            + [Editing Scala with vim](https://leonard.io/blog/2013/04/editing-scala-with-vim/)
            + [My Vim setup for Scala](http://bleibinha.us/blog/2013/08/my-vim-setup-for-scala)
                + [vim, scala and ctags](http://andrew.stwrt.ca/posts/vim-ctags/)
            + [integration of Scala into Vim](https://github.com/derekwyatt/vim-scala)
                + [coding-scala-with-vim](http://derekwyatt.org/2013/12/31/coding-scala-with-vim.html)
        + [VIM and Python -- a Match Made in Heaven](https://realpython.com/blog/python/vim-and-python-a-match-made-in-heaven/)
        + [vim-multiple-cursors](https://github.com/terryma/vim-multiple-cursors)

    + kate-config
        + [Kate configuration for Rust](https://github.com/rust-lang/kate-config)

    + [Atom - The hackable text editor](https://atom.io)
        + [atom github](https://github.com/atom/atom)
        + [Atom Flight Manual](https://atom.io/docs/latest/getting-started-atom-basics)
        + [The Atom text editor and Rust](http://www.perfectchipperman.com/2015/10/the-atom-text-editor-and-rust.html)
            + [Software development and other things](http://markusjais.com/)
            + [atom/markdown-preview](https://github.com/atom/markdown-preview/pull/298)
            + [atom/multi-cursor-plus](https://atom.io/packages/multi-cursor-plus)
            + [[Solved] disable alt+mouse "move window"?](https://forum.xfce.org/viewtopic.php?id=2989)
              + [How can I disable 'Alt' + mouse default behavior in KDE?](http://superuser.com/questions/584730/how-can-i-disable-alt-mouse-default-behavior-in-kde)
              + [use 'Shift-MiddleMouse' for column selection](https://github.com/bigfive/atom-sublime-select/issues/26)
              + [Automatically use hard tabs for Makefile buffers #3](https://github.com/atom/language-make/issues/3)
        + performance issues
            + [atom performance issues](https://github.com/atom/atom/labels/performance)
                + [Atom hangs on large directories/files and when window switching #9325](https://github.com/atom/atom/issues/9325)
                + [ Render lines via tiles #6733 ](https://github.com/atom/atom/pull/6733#issuecomment-108407945)
                + [Find remaining performance bottlenecks for large files #6692](https://github.com/atom/atom/issues/6692)

+ [Technical typesetting](https://github.com/alsam/bookmarks/blob/master/technical_typesetting.md)

+ [ZeroMQ \zero-em-queue\, \ØMQ\:](http://zeromq.org/)
    + [source git](http://zeromq.org/docs:source-git)
    + [ØMQ Language Bindings](http://zeromq.org/bindings:_start)
    + [Scala binding for ZeroMQ http://www.zeromq.org/bindings:scala-binding](https://github.com/valotrading/zeromq-scala-binding)

+ MIT online courses
    + [physics](http://ocw.mit.edu/courses/physics/)
    + [special courses](http://ocw.mit.edu/courses/special-programs/)

+ Gentoo tips
    + [Gentoo Cheat Sheet](https://wiki.gentoo.org/wiki/Gentoo_Cheat_Sheet)

+ RHEL
    + [Software Collections for Scientific Linux CERN 6](http://linux.web.cern.ch/linux/scl/)
    + [Software Collections for Scientific Linux CERN 6 : RPMS](http://linuxsoft.cern.ch/cern/scl/slc6X/x86_64/RPMS/)

+ profilers
    + [gperftools: Fast, multi-threaded malloc() and nifty performance analysis tools](https://code.google.com/p/gperftools/?redir=1)
        + [cpuprofile doc](http://google-perftools.googlecode.com/svn/trunk/doc/cpuprofile.html)
        + [Issue 278 in google-perftools: CPU profiler shows function addresses instead of function names](https://groups.google.com/forum/#!topic/google-perftools/BQqP6ectdoQ)
        + [Instructing configure where libunwind lives: an answer to `#error Cannot calculate stack trace: will need to write for your environment`](https://groups.google.com/forum/#!topic/google-perftools/30OlGHFNKZw)
    + [IgProf, The Ignominous Profiler](http://igprof.org/index.html)
    + [OProfile](http://oprofile.sourceforge.net/news/)
    + [Heaptrack - A Heap Memory Profiler for Linux](http://milianw.de/blog/heaptrack-a-heap-memory-profiler-for-linux)

    + [http://milianw.de/blog/heaptrack-a-heap-memory-profiler-for-linux](http://milianw.de/blog/heaptrack-a-heap-memory-profiler-for-linux)

    + [Ubuntu Linux C++ error: undefined reference to 'clock_gettime' and 'clock_settime' : add `-lrt`](http://stackoverflow.com/questions/2418157/ubuntu-linux-c-error-undefined-reference-to-clock-gettime-and-clock-settim)

+ [purescript - A small strongly typed language that compiles to Javascript](http://purescript.org)
    + [github repo for purescript](https://github.com/purescript/purescript)
    + [a bunch of purescript repos](https://github.com/freebroccolo?tab=repositories)

+ [How to extract RPM or DEB packages](http://www.g-loaded.eu/2008/01/28/how-to-extract-rpm-or-deb-packages/)

+ Linux From Scratch
    + [LFS root](http://www.linuxfromscratch.org/)
    + [Beyond Linux® From Scratch (systemd edition)](http://www.linuxfromscratch.org/blfs/view/systemd/)

+ Docker
    + [Образы и контейнеры Docker в картинках](http://habrahabr.ru/post/272145/)

+ Haskell (see also `pandoc` and `diagrams` links above)
    + [Haskell Communities and Activities Report Twenty-Ninth Edition – November 2015](https://www.haskell.org/communities/11-2015/html/report.html)
        + [Haskell Programming _from first principles_](http://haskellbook.com/feedback.html)

+ C++
    + [The C++ Core Guidelines are a set of tried-and-true guidelines, rules, and best practices about coding in C++](https://github.com/isocpp/CppCoreGuidelines)
    + [Поразрядная сортировка с человеческим лицом Radix sort in C++](http://habrahabr.ru/post/271677/)


