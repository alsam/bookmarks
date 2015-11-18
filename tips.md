# useful tips
+ git & github
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

+ compile optimization tips (TODO reorganize)
    + [Why doesn't GCC optimize a*a*a*a*a*a to (a*a*a)*(a*a*a)?](http://stackoverflow.com/questions/6430448/why-doesnt-gcc-optimize-aaaaaa-to-aaaaaa)
+ scala
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

+ LaTeX tips
    + [Modern LaTeX typesetting](https://www.olivierverdier.com/posts/2013/07/15/modern-latex/)
    + [buildtexlive](https://github.com/elkrejzi/system-management/blob/master/buildscripts/buildtexlive#L52)
    + [Introduction to TeX Live from source](http://www.linuxfromscratch.org/blfs/downloads/stable/BLFS-BOOK-7.7-nochunks.html#tl-installer
        + [Re: [blfs-dev] Possible changes to how we do texlive](https://www.mail-archive.com/blfs-dev@lists.linuxfromscratch.org/msg02996.html)
    + [LaTeX Table Generator](http://www.tablesgenerator.com/)
    + [Online LaTeX Equation Editor](http://www.codecogs.com/latex/eqneditor.php)
    + [Fonts](https://en.wikibooks.org/wiki/LaTeX/Fonts)
    + [Import graphics](https://en.wikibooks.org/wiki/LaTeX/Importing_Graphics)
    + [Aligning equations with amsmath](https://www.sharelatex.com/learn/Aligning_equations_with_amsmath)
    + [Text alignment](https://www.sharelatex.com/learn/Text_alignment)
    + [minted – highlighted source code for LaTeX](https://code.google.com/p/minted/)
        + [Code Highlighting with minted -- contains nifty colour styles to choose from](https://www.sharelatex.com/learn/Code_Highlighting_with_minted)
    + [Description list with aligned descriptions](http://tex.stackexchange.com/questions/67720/description-list-with-aligned-descriptions)
    + Unicode
        + [entering-unicode-characters-in-latex](http://tex.stackexchange.com/questions/34604/entering-unicode-characters-in-latex)
            + [insert-unicode-symbol](http://tex.stackexchange.com/questions/37445/insert-unicode-symbol)
        + Fonts (CMU aka Computer Modern Unicode especially)
            + [Adding New Fonts to Your System](http://community.linuxmint.com/tutorial/view/29)
            + [why-does-xetex-not-display-basic-unicode-characters](http://tex.stackexchange.com/questions/201622/why-does-xetex-not-display-basic-unicode-characters)
            + [Как сказать XeLaTeX, чтобы использовал шрифты Computer Modern?](http://www.linux.org.ru/forum/desktop/8254794)
            + [Using fonts installed in local texlive](http://tex.stackexchange.com/questions/202767/using-fonts-installed-in-local-texlive)

            + [Mathematics#List_of_Mathematical_Symbols](https://en.wikibooks.org/wiki/LaTeX/Mathematics#List_of_Mathematical_Symbols)
                + [How do I use a circle as a math accent (larger than \mathring)?](http://tex.stackexchange.com/questions/3266/how-do-i-use-a-circle-as-a-math-accent-larger-than-mathring)
                + [how to get good looking copyright and registered symbols](http://tex.stackexchange.com/questions/1676/how-to-get-good-looking-copyright-and-registered-symbols)

+ Creating diagrams
    + [Creating documents with embedded diagrams](https://byorgey.wordpress.com/2012/08/28/creating-documents-with-embedded-diagrams/)
        + [diagrams](http://projects.haskell.org/diagrams/)
            + [diagrams-builder](https://github.com/diagrams/diagrams-builder)
                + [Flowchart sample](https://en.wikipedia.org/wiki/Flowchart#/media/File:Flowgorithm_Editor.png)
        + [Unordered tuples and type algebra](https://byorgey.wordpress.com/2012/08/24/unordered-tuples-and-type-algebra/)
    + [Embedded diagrams in pandoc's markdown](https://github.com/nichtich/ditaa-markdown/)
    + [PlantUML](http://plantuml.com/running.html)

+ [Support LaTeX environments in Markdown -> HTML conversion #1938](https://github.com/jgm/pandoc/issues/1938)

+ use [dillinger for markdown formatting](http://dillinger.io/)
+ [Package algorithm2e on Ubuntu: sudo apt-get install texlive-science](http://tex.stackexchange.com/questions/46276/package-algorithm2e-on-ubuntu)

+ [ZeroMQ \zero-em-queue\, \ØMQ\:](http://zeromq.org/)
    + [source git](http://zeromq.org/docs:source-git)
    + [ØMQ Language Bindings](http://zeromq.org/bindings:_start)
    + [Scala binding for ZeroMQ http://www.zeromq.org/bindings:scala-binding](https://github.com/valotrading/zeromq-scala-binding)

+ [math in markdown: Survey of syntaxes for math in markdown](https://github.com/cben/mathdown/wiki/math-in-markdown)
    + [Schlolarlymarkdown: make academic writing less frustrating](http://scholarlymarkdown.com/)
    + [github repo for scholdoc](https://github.com/timtylin/scholdoc)

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

+ [pandoc binaries](https://github.com/jgm/pandoc/releases/tag/1.15.0.6)

+ Linux From Scratch
    + [LFS root](http://www.linuxfromscratch.org/)
    + [Beyond Linux® From Scratch (systemd edition)](http://www.linuxfromscratch.org/blfs/view/systemd/)

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
            + [](https://github.com/atom/atom/pull/6733#issuecomment-108407945)
            + [Find remaining performance bottlenecks for large files #6692](https://github.com/atom/atom/issues/6692)

+ C++
    + [The C++ Core Guidelines are a set of tried-and-true guidelines, rules, and best practices about coding in C++](https://github.com/isocpp/CppCoreGuidelines)
