# useful tips

+ Distributed versioning systems
    + git & github
        + [Git и Github. Простые рецепты](http://habrahabr.ru/post/273897/)
        + [Моя шпаргалка по работе с Git](http://eax.me/git-commands/)
        + Mary Rose Cook on git
            + [Mary Rose Cook blog](http://maryrosecook.com/)
            + [github for maryrosecook.com](https://github.com/maryrosecook/maryrosecook.com)
        + [Revert Git repo to a previous commit](http://stackoverflow.com/questions/4114095/revert-git-repo-to-a-previous-commit)
        + [git returns http error 407 from proxy after CONNECT](http://stackoverflow.com/questions/24907140/git-returns-http-error-407-from-proxy-after-connect)
        + [Git Basics - Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
        + [Git delete a remote/local branch or tag](https://matoski.com/article/git-delete-remote-branch-tag/)
        + [How to: Delete a remote Git tag](https://nathanhoad.net/how-to-delete-a-remote-git-tag)
            + delete tag
          ```sh
          git tag -d v0.2.3
          git push origin :refs/tags/v0.2.3
          ```

            + pushing new tags to remote
          ```sh
          git push --tags
          ```

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

        + [constructive git critique](http://komar.bitcheese.net/en/git-sucks-or-why-do-I-use-darcs-instead)
        + [another point of view on darcs vs. git](http://blog.moertel.com/posts/2007-12-10-how-i-stopped-missing-darcs-and-started-loving-git.html

        + [Как оформлять коммиты, чтобы потом не было больно](https://habrahabr.ru/company/Voximplant/blog/276695/)

    + [Pijul - distributed version control system written in Rust](https://pijul.org/documentation/install/)

+ compile optimization tips (TODO reorganize)
    + [Why doesn't GCC optimize a*a*a*a*a*a to (a*a*a)*(a*a*a)?](http://stackoverflow.com/questions/6430448/why-doesnt-gcc-optimize-aaaaaa-to-aaaaaa)

+ Editors

    + [What are the best programming text editors?](http://www.slant.co/topics/12/~programming-text-editors)

    + [How to Select Columns in Editors (Kate, Vim, etc.)](http://stackoverflow.com/questions/1802616/how-to-select-columns-in-editors-notepad-kate-vim-sublime-textpad-etc-an)

    + modern ctags
        + [A maintained ctags implementation](https://github.com/universal-ctags/ctags)
        + [Universal-ctags Hacking Guide](http://docs.ctags.io/en/latest/)
            + [C++ Declarations/References?](https://github.com/universal-ctags/ctags/issues/651)
        + [Hong's Technology Blog for ctags for C++](https://www.topbug.net/blog/2012/03/17/generate-ctags-files-for-c-slash-c-plus-plus-source-files-and-all-of-their-included-header-files/)
        ```sh
        ctags -R --c++-kinds=+p --fields=+iaS --extra=+q .
        ```

    + vim tips
        :set ff=unix
        + [From Vim to Emacs+Evil chaotic migration guide](http://juanjoalvarez.net/es/)
        + [The Modern Vim Config with Pathogen](http://tammersaleh.com/posts/the-modern-vim-config-with-pathogen/)
            + [vim-pathogen](https://github.com/tpope/vim-pathogen)
        + [How to setup vim to edit both Makefile and normal code files?](http://superuser.com/questions/632657/how-to-setup-vim-to-edit-both-makefile-and-normal-code-files)
        + vim+scala
            + [Editing Scala with vim](https://leonard.io/blog/2013/04/editing-scala-with-vim/)
            + [My Vim setup for Scala](http://bleibinha.us/blog/2013/08/my-vim-setup-for-scala)
                + [vim, scala and ctags](http://andrew.stwrt.ca/posts/vim-ctags/)
            + [integration of Scala into Vim](https://github.com/derekwyatt/vim-scala)
                + [coding-scala-with-vim](http://derekwyatt.org/2013/12/31/coding-scala-with-vim.html)
        + [VIM and Python -- a Match Made in Heaven](https://realpython.com/blog/python/vim-and-python-a-match-made-in-heaven/)
        + [vim-multiple-cursors](https://github.com/terryma/vim-multiple-cursors)
        + [Provide easy code formatting in Vim by integrating existing code formatters](https://github.com/Chiel92/vim-autoformat)
        + [Vundle vs. Pathogen](http://lepture.com/en/2012/vundle-vs-pathogen)
        + [Разработка → VIM: зачем, если есть IDE, и как?](https://habrahabr.ru/post/303554/)

    + Emacs
        + [Хорошо настроенный Emacs](http://habrahabr.ru/post/274759/)

    + kate-config
        + [Kate configuration for Rust](https://github.com/rust-lang/kate-config)

    + [Textadept (Editor)](https://www.openhub.net/p/textadept)
      + [Textadept module for ctags](http://foicica.com/wiki/ctags)

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

+ Linux distros specific
    + `systemd` vs. `init`
        + [The Story Behind ‘init’ and ‘systemd’: Why ‘init’ Needed to be Replaced with ‘systemd’ in Linux](http://www.tecmint.com/systemd-replaces-init-in-linux/)
        + [ELI5: The SystemD vs. init/upstart controversy](https://www.reddit.com/r/linux/comments/132gle/eli5_the_systemd_vs_initupstart_controversy/)
        + [Systemd Essentials: Working with Services, Units, and the Journal](https://www.digitalocean.com/community/tutorials/systemd-essentials-working-with-services-units-and-the-journal)
        + [Comparison of init systems](https://wiki.gentoo.org/wiki/Comparison_of_init_systems)
        + [gentoo - systemd](https://wiki.gentoo.org/wiki/Systemd)
        + [How does systemd use /etc/init.d scripts?](http://unix.stackexchange.com/questions/233468/how-does-systemd-use-etc-init-d-scripts)
        + [`systemds for `upstart` users](https://wiki.ubuntu.com/SystemdForUpstartUsers)

    + [terse DBus introspection table - borrowed from D lang](http://www.dsource.org/projects/dbus-d/wiki/Introspection)

    + Gentoo tips
        + [Gentoo Cheat Sheet](https://wiki.gentoo.org/wiki/Gentoo_Cheat_Sheet)
    
    + Arch Linux tips
        + [Arch Linux Installation guide](https://wiki.archlinux.org/index.php/installation_guide)
            + [Installing Arch Linux on a USB key](https://wiki.archlinux.org/index.php/Installing_Arch_Linux_on_a_USB_key)
        + [Arch Linux Set timezone](https://wiki.archlinux.org/index.php?title=Time&redirect=no#Time_zone)
        + [Arch Linux SSH keys](https://wiki.archlinux.org/index.php/SSH_keys)
        + [Arch Linux AUR](https://wiki.archlinux.org/index.php/Arch_User_Repository)
        + [How to install Yaourt on Arch Linux](http://www.ostechnix.com/install-yaourt-arch-linux/)
        ```sh
        pacman -S grub
        pacman -S vim gvim
        pacman -S os-prober
        pacman -S bash-completion
        pacman -S gnome build-base base-devel scons python-pip python2-pip python-yaml qt5 wayland gdm python2 python mc gdb cgdb
        pacman -S chromium 
        pacman -S konsole
        pacman -S git
        pacman -S extra/keychain
        pacman -S openssh
        pacman -S gconf
        pacman -S hunspell-en
        pacman -S rsync
        pacman -S extra/emacs
        pacman -S texlive
        pacman -S texlive-bin
        pacman -S texlive-core
        pacman -S extra/texlive-fontsextra
        pacman -S texlive-most
        pacman -S texlive-lang
        pacman -S pandoc
        pacman -S qt extra/qt5-declarative
        pacman -S community/netactview
        pacman -S community/cairo-dock
        pacman -S community/cairo-dock-plug-ins
        pacman -S extra/clang
        pacman -S extra/kdegraphics-okular
        pacman -S the_silver_searcher

        ```
        + [Slack Desktop (Beta) for Linux](https://aur.archlinux.org/packages/slack-desktop/)
        + [The Rust toolchain installer](https://aur.archlinux.org/packages/rustup/)

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
    + Memory profiling
        + [How do VmRSS and resident set size match?](http://stackoverflow.com/questions/10400751/how-do-vmrss-and-resident-set-size-match)

+ [purescript - A small strongly typed language that compiles to Javascript](http://purescript.org)
    + [github repo for purescript](https://github.com/purescript/purescript)
    + [a bunch of purescript repos](https://github.com/freebroccolo?tab=repositories)

+ [How to extract RPM or DEB packages](http://www.g-loaded.eu/2008/01/28/how-to-extract-rpm-or-deb-packages/)

+ Linux From Scratch
    + [LFS root](http://www.linuxfromscratch.org/)
    + [Beyond Linux® From Scratch (systemd edition)](http://www.linuxfromscratch.org/blfs/view/systemd/)

+ Docker
    + [Поняв Docker](https://habrahabr.ru/post/277699/)
    + [Образы и контейнеры Docker в картинках](http://habrahabr.ru/post/272145/)

+ Haskell (see also `pandoc` and `diagrams` links above)
    + [Haskell Communities and Activities Report Twenty-Ninth Edition – November 2015](https://www.haskell.org/communities/11-2015/html/report.html)
        + [Haskell Programming _from first principles_](http://haskellbook.com/feedback.html)

+ C++
    + [C++11 FAQ rom the author of C++](http://www.stroustrup.com/C++11FAQ.html)
    + [Impossibly fast delegate in C++11](http://codereview.stackexchange.com/questions/14730/impossibly-fast-delegate-in-c11)
    + [Perfect forwarding and universal references in C++](http://eli.thegreenplace.net/2014/perfect-forwarding-and-universal-references-in-c/)
    + [Nobody Understands C++](http://blog2.emptycrate.com/tags/nobody-understands)
        + [Nobody Understands C++: Part 5: Template Code Bloat](http://blog2.emptycrate.com/content/nobody-understands-c-part-5-template-code-bloat)
    + [The C++ Core Guidelines are a set of tried-and-true guidelines, rules, and best practices about coding in C++](https://github.com/isocpp/CppCoreGuidelines)
    + [Поразрядная сортировка с человеческим лицом Radix sort in C++](http://habrahabr.ru/post/271677/)
    + [http://habrahabr.ru/company/infopulse/blog/274549/](http://habrahabr.ru/company/infopulse/blog/274549/)
    + [Советы о том, как писать на С в 2016 году](https://habrahabr.ru/company/inoventica/blog/275685/)
    + [The C++ scientist](http://jmabille.github.io/)
    + [GoF patterns in modern C++](https://accu.org/content/conf2013/Tobias_Darm_Effective_GoF_Patterns.pdf)
        + [Effective GoF Patterns with C++11 and Boost—Tobias Darm](https://isocpp.org/blog/2013/10/patterns) 
    + selected stackoverflow questions
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
        + [How do I terminate a thread in C++11?](http://stackoverflow.com/questions/12207684/how-do-i-terminate-a-thread-in-c11)
    + [What's the difference between “mutex” and “lock”?](http://stackoverflow.com/questions/9382122/whats-the-difference-between-mutex-and-lock)
    + [Потоки, блокировки и условные переменные в C++11 [Часть 2] ](https://habrahabr.ru/post/182626/)
    + [C++11 threads, affinity and hyperthreading](http://eli.thegreenplace.net/2016/c11-threads-affinity-and-hyperthreading/)
    + C++11 and semaphores
        + [C++0x has no semaphores? How to synchronize threads?](http://stackoverflow.com/questions/4792449/c0x-has-no-semaphores-how-to-synchronize-threads/19659736#19659736)
        + [Semaphores C++11 when Multithreading](http://austingwalters.com/multithreading-semaphores/)
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

        + [К тридцатилетию первого C++ компилятора: ищем ошибки в Cfront](http://www.viva64.com/ru/b/0355/)

+ Test-driven development
    + [Test-driven development and unit testing with examples in C++](http://alexott.net/en/cpp/CppTestingIntro.html)
    + Google Unit Test
        + [github repository](https://github.com/google/googletest)
        + [good intro from IBM](http://www.ibm.com/developerworks/aix/library/au-googletestingframework.html)
        + [another good introduction](https://blog.jetbrains.com/rscpp/unit-testing-google-test/)
        + [Google Test Primer](https://github.com/google/googletest/blob/master/googletest/docs/Primer.md)
        + [Google TestAdvanced](https://github.com/google/googletest/blob/master/googletest/docs/AdvancedGuide.md)
        + fast deployment in `/usr/local`
        ```sh
        git clone https://github.com/google/googletest && pushd googletest && mkdir build && cd build && cmake .. && sudo make install
        ```

+ Text search-and-replace (grep-like tools)
    + [amber (written in Rust - a good starting point)](https://github.com/dalance/amber)
        + [ag - the silver searcher](https://github.com/ggreer/the_silver_searcher)

+ config formats : CSV vs. JSON vs. XML vs. YAML
    + [XML, JSON, YAML, TOML for Configuration](http://www.client9.com/article/xml-json-yaml-toml-for-configuration/)
    + [Is CSV a good alternative to XML and JSON?](http://programmers.stackexchange.com/questions/224929/is-csv-a-good-alternative-to-xml-and-json)
    + [C/C++ JSON parser/generator benchmark](https://github.com/miloyip/nativejson-benchmark)

+ [Implementing an update/upgrade system for embedded Linux devices](http://stackoverflow.com/questions/6937592/implementing-an-update-upgrade-system-for-embedded-linux-devices)
    + [SWUpdate - Software Update for Embedded Systems](https://github.com/sbabic/swupdate)
