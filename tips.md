# useful tips

+ Software Architecture
    + [Michael-F-Bryan Tag: Architecture](https://adventures.michaelfbryan.com/tags/architecture/)
        + [How I Translate Feature Requests into Code](https://adventures.michaelfbryan.com/posts/turning-feature-requests-into-code/)

+ [OOP cheatsheet](https://tproger.ru/translations/oop-principles-cheatsheet/)
    + tl;dr
        + use with inheritance
            + delegation
            + composition
            + aggregation
        + DRY - don't repeat yourself
        + [How I Declare My class And Why](http://howardhinnant.github.io/classdecl.html)

    + [Inheritance, why is bad?](https://users.rust-lang.org/t/inheritance-why-is-bad/35705)

    + [How to Learn Software Design and Architecture - a Roadmap](https://www.freecodecamp.org/news/software-design/)

    + SOLID OOP
        + [S.O.L.I.D: The First 5 Principles of Object Oriented Design](https://scotch.io/bar-talk/s-o-l-i-d-the-first-five-principles-of-object-oriented-design)
            + [Простое объяснение принципов SOLID](https://habr.com/en/company/mailru/blog/412699/)
            + [Как с помощью принципа единственной ответственности писать гибкий и модульный код](https://tproger.ru/translations/solid-srp-explained/?fbclid=IwAR3DdqAxAO55xtU-Rq8VWQDoh_FufzB1pPoXcxc60eWlrOj3ieAHy5IrKKY)
            + [Covariance and contravariance in subtyping](https://eli.thegreenplace.net/2018/covariance-and-contravariance-in-subtyping/)
                + [Why can't I pass std::vector<Child*> as std::vector<Parent*>?](https://mcla.ug/blog/cpp-templates-with-subtype-type-args.html)

+ Backup + Restore of the system
    + [Howto: Backup and restore your system!](https://ubuntuforums.org/showthread.php?t=35087)
        + Backup:
        ```
        sudo su
        cd /
        tar cvpjf backup.tar.bz2 --exclude=/proc --exclude=/lost+found --exclude=/backup.tar.bz2 --exclude=/mnt --exclude=/sys /
        ```
        + Restore:
        ```sh
        tar xvpfj backup.tar.bz2 -C /
        mkdir proc
        mkdir lost+found
        mkdir mnt
        mkdir sys
        etc...
        ```
+ [Fstab doesn't mount with exec](http://askubuntu.com/questions/678857/fstab-doesnt-mount-with-exec)

+ Distributed versioning systems
    + git & github & gitlab
        + [git LFS](https://git-lfs.github.com/)
        + [Tig: text-mode interface for Git](https://jonas.github.io/tig/)
        + [Lazygit — псевдографический консольный клиент для Git](https://www.linux.org.ru/news/opensource/15584752)
        + Git remote access
            + [s there a way to skip password typing when using https:// on GitHub?](Is there a way to skip password typing when using https:// on GitHub?)
            + [How to use git with gnome-keyring integration](https://stackoverflow.com/questions/13385690/how-to-use-git-with-gnome-keyring-integration)
                + tl;dr
                ```sh
                $ sudo pacman -S libgnome-keyring
                $ pushd /usr/share/git/credential/gnome-keyring
                $ sudo make
                $ popd
                $ git config --global credential.helper /usr/share/git/credential/gnome-keyring/git-credential-gnome-keyring
                ```
            + [Git на сервере - Создание открытого SSH-ключа](https://git-scm.com/book/ru/v1/Git-%D0%BD%D0%B0-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B5-%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BE%D1%82%D0%BA%D1%80%D1%8B%D1%82%D0%BE%D0%B3%D0%BE-SSH-%D0%BA%D0%BB%D1%8E%D1%87%D0%B0)
            + [Как настроить подключение к удаленному Git репозиторию](https://ru.stackoverflow.com/questions/468812/%D0%9A%D0%B0%D0%BA-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B8%D1%82%D1%8C-%D0%BF%D0%BE%D0%B4%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BA-%D1%83%D0%B4%D0%B0%D0%BB%D0%B5%D0%BD%D0%BD%D0%BE%D0%BC%D1%83-git-%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D1%8E)
        + [Git и Github. Простые рецепты](http://habrahabr.ru/post/273897/)
        + [Моя шпаргалка по работе с Git](http://eax.me/git-commands/)
        + Mary Rose Cook on git
            + [Mary Rose Cook blog](http://maryrosecook.com/)
            + [github for maryrosecook.com](https://github.com/maryrosecook/maryrosecook.com)
        + [Revert Git repo to a previous commit](http://stackoverflow.com/questions/4114095/revert-git-repo-to-a-previous-commit)
            + [How to revert to origin's master branch's version of file](https://stackoverflow.com/questions/1817766/how-to-revert-to-origins-master-branchs-version-of-file)
        + [git returns http error 407 from proxy after CONNECT](http://stackoverflow.com/questions/24907140/git-returns-http-error-407-from-proxy-after-connect)
        + [Git Basics - Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
        + [Git delete a remote/local branch or tag](https://matoski.com/article/git-delete-remote-branch-tag/)

        + [How to change your commit messages in Git?](https://gist.github.com/nepsilon/156387acf9e1e72d48fa35c4fabef0b4)

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
        + [GitLab rename branch and start over on another](https://stackoverflow.com/questions/35119034/gitlab-rename-branch-and-start-over-on-another)
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
        + [Reset Demystified](https://git-scm.com/blog/2011/07/11/reset.html)
        + [A Git Horror Story: Repository Integrity With Signed Commits](https://mikegerwitz.com/papers/git-horror-story)

        + [constructive git critique](http://komar.bitcheese.net/en/git-sucks-or-why-do-I-use-darcs-instead)
        + [another point of view on darcs vs. git](http://blog.moertel.com/posts/2007-12-10-how-i-stopped-missing-darcs-and-started-loving-git.html)

        + [Как оформлять коммиты, чтобы потом не было больно](https://habrahabr.ru/company/Voximplant/blog/276695/)

        + [Git: Squash your latests commits into one](https://www.devroom.io/2011/07/05/git-squash-your-latests-commits-into-one/)
            + [How to Squash Multiple Commits Into One with Git](https://forum.freecodecamp.org/t/how-to-squash-multiple-commits-into-one-with-git-squash/13231)
            + [Squash my last X commits together using Git](https://stackoverflow.com/questions/5189560/squash-my-last-x-commits-together-using-git)

        + [git rebase vs. merge](https://tyvik.ru/blog/49)

        + git rebase memo
        ```sh
        git rebase origin/master
        git status
        <fix conflicts>
        git add <changed>
        git rebase --continue
        git push origin my-branch --force
        <repeat>
        ```
        + aborting & syncing with origin/master
            ```sh
            git rebase --abort
            git merge --abort
            git checkout -B master origin/master
            ...
            git push origin master:master
            ...
            ```

        + [Syncing a fork](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/syncing-a-fork)
        + [Как удалить сабмодуль в git?](https://jeka.by/ask/111/delete-submodule-git/)

        + [Merging a subdirectory from another repo via git-subtree](https://jrsmith3.github.io/merging-a-subdirectory-from-another-repo-via-git-subtree.html)
        + [How to import existing Git repository into another?](http://stackoverflow.com/questions/1683531/how-to-import-existing-git-repository-into-another)
        ```sh
        git subtree add -P u-boot /scratch/tegra-sources/u-boot_nvidia_distribution/u-boot master
        ```

        + subtree import of the subfolder
            + [Add subdirectory of remote repo with git-subtree](http://stackoverflow.com/questions/23937436/add-subdirectory-of-remote-repo-with-git-subtree)    
            tl;dr
            ```sh
            git subtree split -P modules/my_module -b temporary-split-branch
            git subtree add -P prefix-name/  /path-to-repo temporary-split-branch
            ```

        + [Git - Find when a method is removed](http://stackoverflow.com/questions/21110272/git-find-when-a-method-is-removed)    
            tl;dr
            ```sh
            git log -c -S'methodName' /path/to/file.cpp
            ```

        + [Support .ssh/config for specifying keys if ssh-agent fails](https://github.com/rust-lang/cargo/issues/2078)

        + [Adding an existing project to GitHub using the command line](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/)

        + [Малоизвестные Git-команды](https://habrahabr.ru/company/mailru/blog/318508/)

        + [two-factor authentication in your Github account leads to inability to push via HTTPS](https://stackoverflow.com/questions/17659206/git-push-results-in-authentication-failed)    
        tl;dr  
        ```sh
        git remote -v
        git remote remove origin
        git remote add origin git@github.com:user/repo.git
        git push --set-upstream origin master
        ```

        + [git - remote add origin vs remote set-url origin](https://stackoverflow.com/questions/42830557/git-remote-add-origin-vs-remote-set-url-origin/42830632)    
        tl;dr    
        below is used to a add a new remote:
        ```sh
        git remote add origin git@github.com:User/UserRepo.git
        ```
        below is used to change the url of an existing remote repository:    
        ```sh
        git remote set-url origin git@github.com:User/UserRepo.git
        ```
        below will push your code to the master branch of the remote repository defined with origin and -u let you point your current local branch to the remote master branch:    
        ```sh
        git push -u origin master
        ```

        + [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)

    + gitlab
        + [Gitlab : Managing Issues](https://docs.gitlab.com/ee/user/project/issues/managing_issues.html)
        + [GitLab Quick Actions](https://docs.gitlab.com/ee/user/project/quick_actions.html)

    + [Pijul - distributed version control system written in Rust](https://pijul.org/manual/)

+ **gcc** unsorted question (TODO reorganize)
    + list gcc's pre-defined macros    
        ```sh
        gcc -x c /dev/null -dM -E
        ```
    + [Why doesn't GCC optimize a*a*a*a*a*a to (a*a*a)*(a*a*a)?](http://stackoverflow.com/questions/6430448/why-doesnt-gcc-optimize-aaaaaa-to-aaaaaa)

+ Terminal emulators
    + [A look at terminal emulators, part 1](https://anarc.at/blog/2018-04-12-terminal-emulators-1/)
    + [A look at terminal emulators, part 2](https://anarc.at/blog/2018-05-04-terminal-emulators-2/)
    + [20 Useful Terminal Emulators for Linux](https://www.tecmint.com/linux-terminal-emulators/)
    + [A tiling terminal emulator for Linux using GTK+ 3](https://github.com/gnunn1/tilix)
        + [Tilix is an advanced GTK3 tiling terminal emulator that follows the Gnome Human Interface Guidelines.](https://gnunn1.github.io/tilix-web/)    
        ```sh
        Source vte.sh in bashrc

        Update ~/.bashrc (or ~/.zshrc if you are using zsh) to execute vte.sh directly, this involves adding the following line at the end of the file.

        if [ $TILIX_ID ] || [ $VTE_VERSION ]; then
            source /etc/profile.d/vte.sh
        fi
        ```

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
        + [Vim: Squeezing the Text Editor’s Juice with More Features](http://www.datastuff.tech/programming/vim-squeezing-text-editors-juice-with-more-features/)
        + [How I revamped my Vim setup](https://alex.dzyoba.com/blog/vim-revamp)
        + [Minimalist Vim Plugin Manager](https://github.com/junegunn/vim-plug)
        + [A guide to setting up Vim for JavaScript development](https://freshman.tech/vim-javascript/)
        + [You Should Be Using Tags In Vim](https://vimways.org/2018/you-should-be-using-tags-in-vim)
        + [Browsing programs with tags](https://vim.fandom.com/wiki/Browsing_programs_with_tags)
        + [Find and replace using regular expressions](https://vi.stackexchange.com/questions/3115/find-and-replace-using-regular-expressions)
        + [Understanding Vim’s Jump List](https://medium.com/breathe-publication/understanding-vims-jump-list-7e1bfc72cdf0)
        + [Что вам стоит знать, если вы начали изучение Vim](https://proglib.io/p/vim-what-i-wish-i-knew/)
        + [Configure coc.nvim for C/C++ Development](https://ianding.io/2019/07/29/configure-coc-nvim-for-c-c++-development/)
            + [CCLS (C/C++) extension for coc.nvim](https://github.com/Maxattax97/coc-ccls)
                + [Is this extension in a usable state?](https://github.com/Maxattax97/coc-ccls/issues/1)    
        ```sh
        pacman -S nodejs yarn
        yay -S ccls
        ```
        + [A guide to modern Web Development with (Neo)vim](https://www.freecodecamp.org/news/a-guide-to-modern-web-development-with-neo-vim-333f7efbf8e2/)
        + [Vim’s absolute, relative and hybrid line numbers](https://jeffkreeftmeijer.com/vim-number/)
            + [How to turn off Vim relativenumber setting?](https://stackoverflow.com/questions/32306604/how-to-turn-off-vim-relativenumber-setting)
        + [Об удобной навигации и отладке C++ кода в Vim](https://habr.com/en/post/245681/)
        + [Vim - open new tab in buffer](https://stackoverflow.com/questions/26073226/vim-open-new-tab-in-buffer)
          + tl;dr
          ```sh
          :Te
          ```
        + [From Vim to Emacs+Evil chaotic migration guide](http://juanjoalvarez.net/es/)
        + [The Modern Vim Config with Pathogen](http://tammersaleh.com/posts/the-modern-vim-config-with-pathogen/)
            + [vim-pathogen](https://github.com/tpope/vim-pathogen)
        + [How to setup vim to edit both Makefile and normal code files?](http://superuser.com/questions/632657/how-to-setup-vim-to-edit-both-makefile-and-normal-code-files)
        + [How to Configure Vim like VSCode](https://www.youtube.com/watch?v=gnupOrSEikQ)
            + [init.vim](https://gist.github.com/benawad/b768f5a5bbd92c8baabd363b7e79786f)
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
        + [Vim vs. Neovim](https://www.slant.co/versus/42/62/~vim_vs_neovim)
            + [How to setup Neovim](https://g14n.info/2021/04/neovim-setup/)
            + [Setting up Neovim for C++ Development with LSP](https://jdhao.github.io/2020/11/29/neovim_cpp_dev_setup/)
            + [Configure coc.nvim for C/C++ Development](https://ianding.io/2019/07/29/configure-coc-nvim-for-c-c++-development/)
            + [How to Install and Set Up Neovim for Code Editing](https://mattermost.com/blog/how-to-install-and-set-up-neovim-for-code-editing/)
            + [Turning Neovim into a Full-Fledged Code Editor with Lua](https://mattermost.com/blog/turning-neovim-into-a-full-fledged-code-editor-with-lua/)
        + [Find in files within Vim](http://vim.wikia.com/wiki/Find_in_files_within_Vim)
        + [Vim: Substitute pattern between braces](https://vi.stackexchange.com/questions/2751/substitute-pattern-between-braces)
        + Neovim 0.5+
            + Modern neovim
                + [Taking Neovim to the Moon](https://dev.to/elvessousa/taking-neovim-to-the-moon-274g)
                + [Rust and Neovim - A Thorough Guide and Walkthrough](https://rsdlt.github.io/posts/rust-nvim-ide-guide-walkthrough-development-debug/)
                + [Neovim configuration for c++ and rust. Requires a nerd-font, vim-plug, fzf, ripgrep, rust-analyzer, and clangd](https://gist.github.com/matthewjberger/707a6813d65bd5bc7505e1d849bd4726)
            + [Awesome Neovim](https://github.com/rockerBOO/awesome-neovim)
            + [Neovim with LSP and tree-sitter](https://github.com/nikvdp/nvim-lsp-config)
            + [nvim tree-sitter config](https://github.com/craftzdog/dotfiles-public/tree/master/.config/nvim)
            + [LunarVim](https://github.com/ChristianChiarulli/LunarVim)
                + [Neovim 0.5 and LunarVim Q&A Livestream](https://www.youtube.com/watch?v=V-6GkfeIi3w)
            + [How to set up Neovim 0.5 (LSP, Treesitter, fuzzy finder, etc)](https://www.youtube.com/watch?v=FW2X1CXrU1w)
            + [How to migrate from init.vim to init.lua?](https://www.reddit.com/r/neovim/comments/kfxqcr/how_to_migrate_from_initvim_to_initlua/)
                + [Getting started using Lua in Neovim](https://github.com/nanotee/nvim-lua-guide/)
                + [dot dot dot](https://github.com/elianiva/dotfiles/)
                + [Neovim 0.5 features and the switch to `init.lua`](https://oroques.dev/notes/neovim-init/)
                + [Configuring Neovim using Lua](https://icyphox.sh/blog/nvim-lua/)
                + [Converting neovim config to lua](https://www.imaginaryrobots.net/2021/04/17/converting-vimrc-to-lua)
                + [Neovim (0.5) Is Overpowering](https://crispgm.com/page/neovim-is-overpowering.html)
                + [How to set up Neovim 0.5 + Modern plugins (LSP, Treesitter, Fuzzy finder, etc)](https://blog.inkdrop.info/how-to-set-up-neovim-0-5-modern-plugins-lsp-treesitter-etc-542c3d9c9887)    
                + [Neovim Navigator](https://github.com/ray-x/navigator.lua)
            tl;dr
            ```sh
            viB:s/word/replacement/gc
            ```
            or
            ```sh
            vi{:s...
        + [The Ultimate Vim Distribution](http://vim.spf13.com/)
        + [Ultimate auto-completion system for Vim](https://github.com/Shougo/neocomplcache.vim)
        ```sh
        Plugin 'Shougo/neocomplcache'
        Plugin 'Shougo/neosnippet'
        Plugin 'Shougo/neosnippet-snippets'
        Open up Vim and start installation with :PluginInstall
        ```
        + YouComplete    
            tl;dr
            ```sh
            ~/.vim/bundle/YouCompleteMe$ ./install.sh --clang-completer --racer-completer
            ```
            + [libtinfo.so.* missing in Arch Linux](https://github.com/Valloric/YouCompleteMe/issues/778)
            + [supercede: Package Details: ncurses5-compat-libs 6.1-1 ](https://aur.archlinux.org/packages/ncurses5-compat-libs/?comments=all)    
            tl;dr  
            ```sh
            gpg --keyserver keys.gnupg.net --recv-keys 702353E0F7E48EDB
            yay -S ncurses5-compat-libs
            ```
            + ["ycmd server SHUTDOWN" error on Arch Linux](https://github.com/Valloric/YouCompleteMe/issues/2579#issuecomment-288315182)
                + tl;dr
                ```sh
                yay -S libtinfo
                yay -S libtinfo5
                :YcmGenerateConfig
                :YcmRestartServer
                ```
            + [Ubuntu : fatal error: pyconfig.h: No such file or directory # include <pyconfig.h>](https://github.com/Valloric/YouCompleteMe/issues/2219)
              + tl;dr
              ```sh
              sudo apt install python3-dev
              python3 install.py --clang-completer --racer-completer
              ```

        + [TabNine uses deep learning to help you write code faster.](https://tabnine.com/)
        + CoC - **C**onquer **o**f **C**ompletion
            + [Install coc.nvim](https://github.com/neoclide/coc.nvim/wiki/Install-coc.nvim)
                + Ubuntu install issues
                    + [Ubuntu 17 apt-get installs cmdtest instead of yarn](https://github.com/yarnpkg/yarn/issues/3189)
                    + [How to Install Yarn on Ubuntu 18.04](https://linuxize.com/post/how-to-install-yarn-on-ubuntu-18-04/)    
                    tl;dr    
                    ```sh
                    sudo apt install npm
                    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
                    echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
                    sudo apt update
                    sudo apt install yarn
                    yarn --version
                    1.17.3
                    ```
                + Fast check after install    
                tl;dr    
                ```
                :CocInfo
                :CocList diagnostics
                :CocInstall coc-json
                :CocInstall coc-rls
                :CocConfig
                :CocCommand
                ```    
                tl;dr look into `~/.config/coc`    
                `rustup component add rls rust-analysis rust-src`
            + [Intellisense engine for vim8 & neovim, full language server protocol support as VSCode](https://github.com/neoclide/coc.nvim)
                + [coc.nvim : read it first](https://www.npmjs.com/package/coc.nvim)
                    + [Floating windows](https://github.com/neoclide/coc.nvim/wiki/F.A.Q#how-to-make-preview-window-shown-aside-with-pum)
            + [CoC Language servers : C++](https://github.com/neoclide/coc.nvim/wiki/Language-servers#ccobjective-c)
                + [C/C++/ObjC language server supporting cross references, hierarchies, completion and semantic highlighting](https://github.com/MaskRay/ccls)
                    + [ccls : Build](https://github.com/MaskRay/ccls/wiki/Build#system-specific-notes)
                    + [Extend .ccls](https://github.com/MaskRay/ccls/pull/171)
                + [[Guide] How to setup ctags with gutentags properly for almost every language](https://www.reddit.com/r/vim/comments/d77t6j/guide_how_to_setup_ctags_with_gutentags_properly/)
                + [Rust support for coc.nvim](https://github.com/neoclide/coc-rls/)
                + [Guide To Turn Neovim Into A Rust IDE?](https://www.reddit.com/r/rust/comments/adepau/guide_to_turn_neovim_into_a_rust_ide/)
                    + [useful init for nvim](https://github.com/realcr/my_init_vim/blob/master/init.vim)
                    + [Why You Should Still Use Neovim](https://codekoalas.com/blog/why-you-should-still-use-neovim)
                        + [ [RFC] Built-in LSP Support](https://github.com/neovim/neovim/pull/10222)

                    + [~~Amp: "a complete text editor for your terminal"~~](https://www.reddit.com/r/rust/comments/7t6rsq/amp_a_complete_text_editor_for_your_terminal/)

        + [Demystifying multi file searches in `vim` and the command line](https://seesparkbox.com/foundry/demystifying_multi_file_searches_in_vim_and_the_command_line)
        + [Use VIM as your RUST IDE](https://github.com/ivanceras/rust-vim-setup)
        + [How to install NERDTree with Vundle?](https://vi.stackexchange.com/questions/5335/how-to-install-nerdtree-with-vundle)

        + NeoVim specific
            + [Neovim ArchLinux notes](https://wiki.archlinux.org/index.php/Neovim)    
            *tl;dr*
            ```sh
            mkdir -p ~/.config/nvim/
            ln -s ~/.vimrc ~/.config/nvim/init.vim
            ```
            + [rxrc/nvimrc](https://libraries.io/github/rxrc/nvimrc)
                + [from nvimrc](https://devhub.io/repos/makenew-nvimrc)
            + [NeoVim config files](https://github.com/bigeagle/neovim-config)
            + [GTK ui for neovim written in rust using gtk-rs bindings](https://github.com/daa84/neovim-gtk)
        + [Can't enter a tab character when previous character is not a tab or space in insert mode](https://vi.stackexchange.com/questions/32983/cant-enter-a-tab-character-when-previous-character-is-not-a-tab-or-space-in-ins)
        + [7 Vim Editors for Better Productivity in 2022](https://geekflare.com/best-vim-editors/)

    + Emacs
        + [Хорошо настроенный Emacs](http://habrahabr.ru/post/274759/)
        + [Prelude is an enhanced Emacs 24 or 25 distribution that should make your experience with Emacs both more pleasant and more powerful](https://github.com/bbatsov/prelude)

    + kate-config
        + [Kate configuration for Rust](https://github.com/rust-lang/kate-config)

    + [Textadept (Editor)](https://www.openhub.net/p/textadept)
        + [Textadept module for ctags](http://foicica.com/wiki/ctags)
        + [Git mirror of Mitchell's Textadept editor](https://github.com/rgieseke/textadept)

    + [Atom - The hackable text editor](https://atom.io)
        + [atom github](https://github.com/atom/atom)
        + [Atom Flight Manual](https://atom.io/docs/latest/getting-started-atom-basics)
        + [Atom Keymaps In-Depth](http://flight-manual.atom.io/behind-atom/sections/keymaps-in-depth/)
            + [Atom How to replace a keymap binding](https://discuss.atom.io/t/how-to-replace-a-keymap-binding/16834/6)
        + [Atom Editor Keyboard Shortcut Cheat Sheet](https://blog.bugsnag.com/atom-editor-cheat-sheet/)
            + *Line Manipulation*
                1. ⌘ + ] / [ Indent/outdent current line.
                2. ⌘ + enter. Insert new line after current line.
                3. ⌘ + shift + enter. Insert new line before current line.
                4. ctrl + shift + k. Delete current line.
                5. ctrl + ⌘ + up/down. Move current line up/down.
                6. shift + ⌘ + d. Duplicate current line.
                7. ⌘ + j. Join current and next lines.
            + [Auto indent code in Atom editor](http://stackoverflow.com/questions/22611377/auto-indent-code-in-atom-editor)
                + *TL;DR*
                    Package auto-indent exists to apply auto-indent to entire file with this shortcuts :
                    `ctrl+shift+i`
                    Package url : [auto-indent](atom.io/packages/auto-indent)


        + [The Atom text editor and Rust](http://www.perfectchipperman.com/2015/10/the-atom-text-editor-and-rust.html)
            + [Software development and other things](http://markusjais.com/)
            + [atom Force file reload](https://discuss.atom.io/t/force-file-reload/11508)
            + [atom/markdown-preview](https://github.com/atom/markdown-preview/pull/298)
            + [atom/multi-cursor-plus](https://atom.io/packages/multi-cursor-plus)
            + [atom/Sublime Style Column Selection](https://atom.io/packages/Sublime-Style-Column-Selection)
                + *TL;DR*
                ```
                Platform    Modifier Key    Mouse Button
                Linux       Shift           Left
                ```

            + [[Solved] disable alt+mouse "move window"?](https://forum.xfce.org/viewtopic.php?id=2989)
              + [How can I disable 'Alt' + mouse default behavior in KDE?](http://superuser.com/questions/584730/how-can-i-disable-alt-mouse-default-behavior-in-kde)
              + [use 'Shift-MiddleMouse' for column selection](https://github.com/bigfive/atom-sublime-select/issues/26)
              + [Automatically use hard tabs for Makefile buffers #3](https://github.com/atom/language-make/issues/3)
              + [Atom - The Arch Linux Development Package](https://atom.io/packages/language-archlinux)
        + performance issues
            + [atom performance issues](https://github.com/atom/atom/labels/performance)
                + [Atom hangs on large directories/files and when window switching #9325](https://github.com/atom/atom/issues/9325)
                + [ Render lines via tiles #6733 ](https://github.com/atom/atom/pull/6733#issuecomment-108407945)
                + [Find remaining performance bottlenecks for large files #6692](https://github.com/atom/atom/issues/6692)

    + [Slap is a sublime-like text editor which works inside the terminal.](https://www.slant.co/options/53/~slap-review)
        + [Slap - sublime-like terminal-based text editor](https://github.com/slap-editor/slap)

    + [Xi-editor - a modern editor with a backend written in Rust.](https://github.com/google/xi-editor)
        + [GTK frontend for the Xi text editor, written in Rust](https://gitlab.gnome.org/World/Tau)    
        tl;dr    
        `yay -S tau-editor-git`    
        ```sh
        sudo pacman -S flatpak
        ...
        flatpak install flathub org.gnome.Tau
            Required runtime for org.gnome.Tau/x86_64/stable (runtime/org.freedesktop.Platform/x86_64/19.08) found in remote flathub
            Do you want to install it? [Y/n]: 
            
            org.gnome.Tau permissions:
                ipc wayland x11
            
            
            
                    ID                                                       Branch               Remote                Download
             1. [✓] org.freedesktop.Platform                                 19.08                flathub               223.6 MB / 237.7 MB
             2. [✓] org.freedesktop.Platform.GL.default                      19.08                flathub                90.8 MB / 90.8 MB
             3. [✓] org.freedesktop.Platform.GL.nvidia-435-21                1.4                  flathub               103.3 MB / 103.3 MB
             4. [✓] org.freedesktop.Platform.Locale                          19.08                flathub               163.7 MB / 318.9 MB
             5. [✓] org.freedesktop.Platform.openh264                        19.08                flathub               594.2 kB / 593.4 kB
             6. [✓] org.gnome.Tau                                            stable               flathub                 4.6 MB / 4.6 MB
             7. [✓] org.gnome.Tau.Locale                                     stable               flathub                45.3 kB / 41.0 kB
            
                    Installation complete.
        
        flatpak run org.gnome.Tau
        
            Note that the directories 
            
            '/var/lib/flatpak/exports/share'
            '$HOME/.local/share/flatpak/exports/share'
            
            are not in the search path set by the XDG_DATA_DIRS environment variable, so
            applications installed by Flatpak may not appear on your desktop until the
            session is restarted.
            
            Gtk-Message: 23:05:39.139: Failed to load module "canberra-gtk-module"
            Gtk-Message: 23:05:39.140: Failed to load module "canberra-gtk-module"
        ```

    + [Monaco Editor](https://microsoft.github.io/monaco-editor/)
        + [Monaco Editor repo](https://github.com/Microsoft/monaco-editor)

    + [Collection of miscellaneous portable C snippets.](https://github.com/nemequ/portable-snippets)
        + [Debug trap portable](https://github.com/nemequ/portable-snippets/blob/master/debug-trap/debug-trap.h)
            + [Is there a portable equivalent to DebugBreak()/__debugbreak?](https://stackoverflow.com/questions/173618/is-there-a-portable-equivalent-to-debugbreak-debugbreak)

+ [Technical typesetting](https://github.com/alsam/bookmarks/blob/master/technical_typesetting.md)

+ [ZeroMQ \zero-em-queue\, \ØMQ\:](http://zeromq.org/)
    + [source git](http://zeromq.org/docs:source-git)
    + [ØMQ Language Bindings](http://zeromq.org/bindings:_start)
    + [Scala binding for ZeroMQ http://www.zeromq.org/bindings:scala-binding](https://github.com/valotrading/zeromq-scala-binding)

+ MIT online courses
    + [physics](http://ocw.mit.edu/courses/physics/)
    + [special courses](http://ocw.mit.edu/courses/special-programs/)

+ Linux distros specific
    + [How to Keep ‘sudo’ Password Timeout Session Longer in Linux](http://www.tecmint.com/set-sudo-password-timeout-session-longer-linux/)
    + `systemd` vs. `init`
        + [RHEL7: How to get started with Systemd](https://www.certdepot.net/rhel7-get-started-systemd/)
        + [The Story Behind ‘init’ and ‘systemd’: Why ‘init’ Needed to be Replaced with ‘systemd’ in Linux](http://www.tecmint.com/systemd-replaces-init-in-linux/)
        + [ELI5: The SystemD vs. init/upstart controversy](https://www.reddit.com/r/linux/comments/132gle/eli5_the_systemd_vs_initupstart_controversy/)
        + [Systemd Essentials: Working with Services, Units, and the Journal](https://www.digitalocean.com/community/tutorials/systemd-essentials-working-with-services-units-and-the-journal)
        + [Comparison of init systems](https://wiki.gentoo.org/wiki/Comparison_of_init_systems)
        + [gentoo - systemd](https://wiki.gentoo.org/wiki/Systemd)
        + [How does systemd use /etc/init.d scripts?](http://unix.stackexchange.com/questions/233468/how-does-systemd-use-etc-init-d-scripts)
        + [`systemds for `upstart` users](https://wiki.ubuntu.com/SystemdForUpstartUsers)
        + `journald`
            + [Logging message workflow with journald](http://www.gabriel.urdhr.fr/2015/04/29/journald-workflow/)
            + [systemd for Developers III : Logging to the Journal](http://0pointer.de/blog/projects/journal-submit.html)    
            tl;dr
            ```c
            #include <systemd/sd-journal.h>
            #include <unistd.h>
            #include <stdlib.h>
             
            int main(int argc, char *argv[]) {
                    sd_journal_send("MESSAGE=Hello World!",
                                    "MESSAGE_ID=52fb62f99e2c49d89cfbf9d6de5e3555",
                                    "PRIORITY=5",
                                    "HOME=%s", getenv("HOME"),
                                    "TERM=%s", getenv("TERM"),
                                    "PAGE_SIZE=%li", sysconf(_SC_PAGESIZE),
                                    "N_CPUS=%li", sysconf(_SC_NPROCESSORS_ONLN),
                                    NULL);
                    return 0;
            }
            ```
            ```sh
            journalctl -o json-pretty MESSAGE="Hello World!"
            ```
            ```sh
            printf "hola\n\rbro\n\r" | systemd-cat -t HOLA-BRO-SLASH-R
            journalctl --sync
            journalctl -b -t HOLA-BRO-SLASH-R --no-pager --no-hostname
            ```
            + [How can I send a message to the systemd journal from the command line?](https://serverfault.com/questions/573946/how-can-i-send-a-message-to-the-systemd-journal-from-the-command-line)
            + [How to configure systemd journal-remote?](https://serverfault.com/questions/758244/how-to-configure-systemd-journal-remote)
            + [LOGGING DONE RIGHT systemd-journal-upload & systemd-journal-remote setup](https://www.youtube.com/watch?v=45CQ0tgXQmY)
            + [log4cplus](https://github.com/wilx/log4cplus)
            + polltest
            ```c
            #include <stdio.h>
            #include <stdlib.h>
            #include <string.h>
            #include <systemd/sd-journal.h>
            
            int main(int argc, char *argv[]) {
                    int r;
                    sd_journal *j;
                    r = sd_journal_open(&j, SD_JOURNAL_LOCAL_ONLY);
                    if (r < 0) {
                            fprintf(stderr, "Failed to open journal: %s\n", strerror(-r));
                            return 1;
                    }
            
                    /* Opening the fd now means the first sd_journal_wait() will actually wait */
                    r = sd_journal_get_fd(j);
                    if (r < 0) {
                            fprintf(stderr, "Failed to get fd: %s\n", strerror(-r));
                            return 1;
                    }
            
                    r = sd_journal_seek_tail(j);
                    if (r < 0) {
                            fprintf(stderr, "Failed to seek tail: %s\n", strerror(-r));
                            return 1;
                    }
            
                    if (getenv("seek"))
                            r = sd_journal_previous_skip(j, 0);
                    else
                            r = sd_journal_next_skip(j, 0);
                    if (r < 0) {
                            fprintf(stderr, "Failed to skip: %s\n", strerror(-r));
                            return 1;
                    }
            
                    r = sd_journal_wait(j, (uint64_t) -1);
                    if (r < 0) {
                            fprintf(stderr, "Failed to wait for changes: %s\n", strerror(-r));
                            return 1;
                    }
            
                    for (;;)  {
                            const void *d;
                            size_t l;
                            r = sd_journal_next(j);
                            if (r < 0) {
                                    fprintf(stderr, "Failed to iterate to next entry: %s\n", strerror(-r));
                                    break;
                            }
                            if (r == 0) {
                                    /* Reached the end, let's wait for changes, and try again */
                                    r = sd_journal_wait(j, (uint64_t) -1);
                                    if (r < 0) {
                                            fprintf(stderr, "Failed to wait for changes: %s\n", strerror(-r));
                                            break;
                                    }
                                    continue;
                            }
                            r = sd_journal_get_data(j, "MESSAGE", &d, &l);
                            if (r < 0) {
                                    fprintf(stderr, "Failed to read message field: %s\n", strerror(-r));
                                    continue;
                            }
                            printf("%.*s\n", (int) l, (const char*) d);
                    }
                    sd_journal_close(j);
                    return 0;
            }

    + D-Bus
        + [Understanding D-Bus](http://free-electrons.com/pub/conferences/2016/meetup/dbus/josserand-dbus-meetup.pdf)
        + [terse DBus introspection table - borrowed from D lang](http://www.dsource.org/projects/dbus-d/wiki/Introspection)
        + [Building object-oriented software with the D-Bus messaging system](https://www.doria.fi/bitstream/handle/10024/78669/gradu2012Salli.pdf?sequence=1)
        + [Profiling and Optimizing D-Bus APIs](https://willthompson.co.uk/talks/profiling-and-optimizing-d-bus-apis.pdf)
        + [DBus: How to use variant](https://lists.freedesktop.org/archives/dbus/2007-July/008119.html)
        + [The Extended Introspection XML Format](https://wiki.allseenalliance.org/irb/extended_introspection_xml)
        + [CommonAPI C++ D-Bus in 10 minutes (from scratch)](https://at.projects.genivi.org/wiki/pages/viewpage.action?pageId=5472316)
            + [CommonAPI C++ Tutorial](https://at.projects.genivi.org/wiki/pages/viewpage.action?pageId=5472311)
            + [A framework for defining and transforming interfaces](https://github.com/franca/franca)
        + Telepathy
            + [Telepathy is a modular framework for real-time communications](http://www.aosabook.org/en/telepathy.html)
            + [Telepathy docs](https://telepathy.freedesktop.org/wiki/Documentation/)
            + [Telepathy DbusSpec](https://telepathy.freedesktop.org/wiki/DbusSpec/)
        + [QDBus : Send an array of objects (C++)](http://www.qtcentre.org/threads/47018-QDBus-Send-an-array-of-objects-(C-))
        + [[dbus-cplusplus-devel] Variant type handling](https://sourceforge.net/p/dbus-cplusplus/mailman/message/25874526/)
        + [Passing structure over d-bus - glib - example](https://lists.freedesktop.org/archives/dbus/2008-January/009171.html)
        + [[dbus-cplusplus-devel] Proposal: Give objects through dbus-c++](https://sourceforge.net/p/dbus-cplusplus/mailman/message/20200933/)
        + [DBus speed presentation](https://willthompson.co.uk/talks/the-slothful-ways-of-d-bus.pdf)
        + dbus-c++ and g++-7.1
            + [#18 Invalid template code in Threading class](https://sourceforge.net/p/dbus-cplusplus/patches/18/)    
            + tl;dr
              patch '/usr/include/dbus-c++-1/dbus-c++/dispatcher.h'
        + sdbus - and shutdown
            + [The new sd-bus API of systemd](http://0pointer.net/blog/the-new-sd-bus-api-of-systemd.html)
                + [Patrick Williams' gists for sdbus](https://gist.github.com/williamspatrick)
            + [systemd-233/src/libsystemd/sd-bus/test-bus-objects.c](https://fossies.org/linux/systemd/src/libsystemd/sd-bus/test-bus-objects.c)
            + [C++ bindings for systemd dbus APIs](https://github.com/openbmc/sdbusplus)    

            tl;dr poweroff
            ```
            gdbus introspect --system --dest org.freedesktop.systemd1 --object-path /org/freedesktop/systemd1
            ...
              interface org.freedesktop.systemd1.Manager {
                methods:
            ...
                 PowerOff();
            ...
            ```
            ```sh
            sudo busctl call org.freedesktop.systemd1 /org/freedesktop/systemd1 org.freedesktop.systemd1.Manager PowerOff
            reboot: Power down
            ```
            ```c++
            #include <stdio.h>
            #include <stdlib.h>
            #include <systemd/sd-bus.h>
             
            int main(int argc, char *argv[])
            {
                sd_bus_error error = SD_BUS_ERROR_NULL;
                sd_bus_message *m = NULL;
                sd_bus *bus = NULL;
                const char *path;
                int r;
             
                // Connect to the system bus
                r = sd_bus_open_system(&bus);
                if (r < 0) {
                    fprintf(stderr, "Failed to connect to system bus: %s\n", strerror(-r));
                    goto finish;
                }
             
                // Issue the method call and store the respons message in m
                r = sd_bus_call_method(bus,
                                       "org.freedesktop.systemd1",           // service to contact
                                       "/org/freedesktop/systemd1",          // object path
                                       "org.freedesktop.systemd1.Manager",   // interface name
                                       "PowerOff",                           // method name
                                       &error,                               // object to return error in
                                       nullptr,                              // input signature
                                       nullptr);                             // 1st arg
                if (r < 0) {
                    fprintf(stderr, "Failed to issue method call: %s\n", error.message);
                    goto finish;
                }
             
                /* Parse the response message */
                r = sd_bus_message_read(m, "o", &path);
                if (r < 0) {
                    fprintf(stderr, "Failed to parse response message: %s\n", strerror(-r));
                    goto finish;
                }
             
                printf("Queued service job as %s.\n", path);
             
            finish:
                sd_bus_error_free(&error);
                sd_bus_message_unref(m);
                sd_bus_unref(bus);
             
                return r < 0 ? EXIT_FAILURE : EXIT_SUCCESS;
            }
            ```
            ```sh
            g++ systemd-service-client.cc -o systemd-service-client `pkg-config --cflags --libs libsystemd`
            ``` 

    + WebSockets
        + [ws: a Node.js WebSocket library](https://github.com/websockets/ws#sending-and-receiving-text-data)
            + [Autobahn test suite reports](http://websockets.github.io/ws/)    
            tl;dr
            ```sh
            npm install -g ws
            ...
            ```

    + [How to shutdown Linux using C++ or Qt without call to “system()”?](http://stackoverflow.com/questions/28812514/how-to-shutdown-linux-using-c-or-qt-without-call-to-system/28812629)
        + [Core utility library for all LXQt components http://lxqt.org](https://github.com/lxde/liblxqt/blob/master/lxqtpower/lxqtpowerproviders.cpp)


+ profilers
    + [gperftools: Fast, multi-threaded malloc() and nifty performance analysis tools](https://code.google.com/p/gperftools/?redir=1)
        + [cpuprofile doc](http://google-perftools.googlecode.com/svn/trunk/doc/cpuprofile.html)
        + [pmu tools is a collection of tools and libraries for profile collection and performance analysis on Intel CPUs on top of Linux perf](https://github.com/andikleen/pmu-tools)
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

+ Docker+Kubernetes+FireCracker
    + [Основы Kubernetes](https://habr.com/ru/post/258443/)
        + [How to install Kubernetes on Ubuntu 18.04 Bionic Beaver Linux](https://linuxconfig.org/how-to-install-kubernetes-on-ubuntu-18-04-bionic-beaver-linux)
            + [Install and Set Up kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

    + [Поняв Docker](https://habrahabr.ru/post/277699/)
    + [Post-installation steps for Linux](https://docs.docker.com/engine/install/linux-postinstall/)    
        ```sh
        sudo usermod -aG docker $USER
        ```
    + [Образы и контейнеры Docker в картинках](http://habrahabr.ru/post/272145/)
    + [Configure and troubleshoot the Docker daemon](https://docs.docker.com/engine/admin/)
        + [Why docker container exits immediately](https://stackoverflow.com/questions/28212380/why-docker-container-exits-immediately)
            + tl;dr `run -it --entrypoint=/bin/bash custom-ubuntu-image`
    + [Docker - a way to give access to a host USB or serial device?](https://stackoverflow.com/questions/24225647/docker-a-way-to-give-access-to-a-host-usb-or-serial-device)
    + [Starting Docker as Daemon on Ubuntu](https://stackoverflow.com/questions/26137834/starting-docker-as-daemon-on-ubuntu)
        + tl;dr
        ```sh
        sudo service docker restart
        ```
    + [add-apt-repository: command not found in Docker installation on Ubuntu](https://github.com/threatstream/mhn/issues/284)
        + tl;dr docker command to add g++-7 to ubuntu16.04 docker image
        ```sh
        apt-get install -y software-properties-common python-software-properties && \
        add-apt-repository ppa:ubuntu-toolchain-r/test && \
        apt-get -qq update && \
        apt-get install -y -qq gcc-7 g++-7 gfortran-7 && \
        ```
    + [docker run -> name is already in use by container](https://stackoverflow.com/questions/31697828/docker-run-name-is-already-in-use-by-container)
        + tl;dr `docker rm $(docker ps -aq --filter name=CONTAINER_NAME)`

    + [Nvidia-docker - cant find libnvcuvid.so on building process](https://stackoverflow.com/questions/44131890/nvidia-docker-cant-find-libnvcuvid-so-on-building-process)

    + [How to force Docker for a clean build of an image](https://stackoverflow.com/questions/35594987/how-to-force-docker-for-a-clean-build-of-an-image)
        + tl;dr `docker build --no-cache -t u12_core -f u12_core .` `docker system prune`

    + [Secure and fast microVMs for serverless computing](https://github.com/firecracker-microvm/firecracker)

+ CLion
    + [Debugging in CLion](https://blog.jetbrains.com/clion/2015/05/debug-clion/)
    + [How to enable debugging for CLion](https://stackoverflow.com/questions/42509757/how-to-enable-debugging-for-clion)
    + [Commands available during CGDB mode](http://cgdb.sourceforge.net/docs/cgdb-no-split.html)

+ Jenkins
    + [Jenkins - Running a single job in master as well as slave](https://stackoverflow.com/questions/9214501/jenkins-running-a-single-job-in-master-as-well-as-slave)
    + [Hudson: Copy artifact from master to slave fails](https://stackoverflow.com/questions/5830334/hudson-copy-artifact-from-master-to-slave-fails)
    + [A VERY QUICK GUIDE TO DEPLOYING ARTIFACTS WITH JENKINS](https://codurance.com/training/2014/10/03/guide-to-deploying-artifacts-with-jenkins/)

+ Haskell (see also `pandoc` and `diagrams` links above)
    + [Haskell Communities and Activities Report Twenty-Ninth Edition – November 2015](https://www.haskell.org/communities/11-2015/html/report.html)
        + [Haskell Programming _from first principles_](http://haskellbook.com/feedback.html)

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
+ Scriptics selected tips
    + [Is double square brackets [[ ]] preferable over single square brackets [ ] in Bash?](https://stackoverflow.com/questions/669452/is-double-square-brackets-preferable-over-single-square-brackets-in-ba)
    + The most recently changed file.
        + [from here #5: 20 SHELL SCRIPTING QUESTIONS FOR PRACTICE](http://www.techbeamers.com/20-shell-scripting-questions-answers/)
    ```sh
    ls -lrt | grep ^- | awk 'END{print $NF}'
    ```

    + [What are the best open-source build systems for C/C++?](https://www.slant.co/topics/4263/~open-source-build-systems-for-c-c)
        + [Meson](https://www.slant.co/topics/4263/viewpoints/14/~open-source-build-systems-for-c-c~meson)
            + [Investigate using Meson build system alongside CMake](https://musescore.org/en/node/120116)
            + [Can you glob source code with meson?](https://stackoverflow.com/questions/34441673/can-you-glob-source-code-with-meson)

+ [Getting started with Google Test (GTest) on Ubuntu](https://www.eriksmistad.no/getting-started-with-google-test-on-ubuntu/)

+ Text search-and-replace (grep-like tools)
    + [Grep все, что можно](https://habrahabr.ru/post/316414/)
    + [amber (written in Rust - a good starting point)](https://github.com/dalance/amber)
        + [ag - the silver searcher](https://github.com/ggreer/the_silver_searcher)
    + [ripgrep is faster than {grep, ag, git grep, ucg, pt, sift}](https://blog.burntsushi.net/ripgrep/)
    + [A simple, fast and user-friendly alternative to 'find'](https://github.com/sharkdp/fd)

+ config formats : CSV vs. JSON vs. XML vs. YAML
    + [XML, JSON, YAML, TOML for Configuration](http://www.client9.com/article/xml-json-yaml-toml-for-configuration/)
    + [Is CSV a good alternative to XML and JSON?](http://programmers.stackexchange.com/questions/224929/is-csv-a-good-alternative-to-xml-and-json)
    + [C/C++ JSON parser/generator benchmark](https://github.com/miloyip/nativejson-benchmark)
        + [Tutorial for yaml-cpp](https://github.com/jbeder/yaml-cpp/wiki/Tutorial)

+ [Implementing an update/upgrade system for embedded Linux devices](http://stackoverflow.com/questions/6937592/implementing-an-update-upgrade-system-for-embedded-linux-devices)
    + [SWUpdate - Software Update for Embedded Systems](https://github.com/sbabic/swupdate)
        + [Creating Linux based Embedded System Images with Yocto](https://github.com/Nuand/bladeRF/wiki/Creating-Linux-based-Embedded-System-Images-with-Yocto)

+ VirtualBox
    + [VirtualBox on ArchLinux](https://wiki.archlinux.org/index.php/VirtualBox)
        + [GNU Parted](https://wiki.archlinux.org/index.php/GNU_Parted)
        ```sh
        parted /dev/sda
        (parted) mklabel gpt
        (parted) mkpart primary ext4 0% 100%
        mkfs.ext4 /dev/sda1
        tune2fs -L "/scratch" /dev/sda1
        ```
        + [ [Solved]Vboxdrv kernel module is not loaded](https://bbs.archlinux.org/viewtopic.php?id=117795)
    + [How To Install Ubuntu 14.04.3 LTS On VirtualBox](https://www.unixmen.com/install-ubuntu-14-04-3-lts-virtualbox/)
        ```sh
        sudo gpasswd -a <username> vboxusers
        VBoxManage list usbhost
        ```
+ [Checkpoint/Restore tool http://criu.org](https://github.com/xemul/criu)
    + [CRIU, a project to implement checkpoint/restore functionality for Linux.](http://criu.org/Main_Page)

+ Ext4
    + [Ext4 Disk Layout](https://ext4.wiki.kernel.org/index.php/Ext4_Disk_Layout)
    + [How to extract raw ext3 inode data from disk?](http://unix.stackexchange.com/questions/167222/how-to-extract-raw-ext3-inode-data-from-disk)
    + `debugfs` sample session:
    ```sh
    debugfs:  imap <262328>
    Inode 262328 is part of block group 32
            located at block 1048619, offset 0x0700
    debugfs:  show_inode_info <262328>
    Inode: 262328   Type: regular    Mode:  0644   Flags: 0x80000
    Generation: 933973137    Version: 0x00000000:00000001
    User:  1000   Group:  1000   Project:     0   Size: 948
    File ACL: 0    Directory ACL: 0
    Links: 1   Blockcount: 8
    Fragment:  Address: 0    Number: 0    Size: 0
     ctime: 0x5809deb8:1af1cef0 -- Fri Oct 21 12:24:08 2016
     atime: 0x5809deb8:1af1cef0 -- Fri Oct 21 12:24:08 2016
     mtime: 0x5809deb6:00000000 -- Fri Oct 21 12:24:06 2016
    crtime: 0x5809deb8:1af1cef0 -- Fri Oct 21 12:24:08 2016
    Size of extra inode fields: 32
    EXTENTS:
    (0):1082813
    ```

    + [Determine the size of a block device](http://unix.stackexchange.com/questions/52215/determine-the-size-of-a-block-device)
        + tl;dr with `sudo`
        ```sh
        #include <linux/fs.h>
        ...
        ioctl(file, BLKGETSIZE64, &file_size_in_bytes);
        ```
+ bash
    + [comparison operators](http://www.tldp.org/LDP/abs/html/comparison-ops.html)
    ```sh
    if [ "${target_partname}" = "" -o "${target_partname}" = "APP" ]; then
	build_fsimg "$localsysfile" "$fillpat" \
		    "$rootfssize" "$rootfs_type" "$rootfs_dir";
    fi;
    ```
    is equivalent to more readable
    ```sh
    if [[ "${target_partname}" == "" || "${target_partname}" == "APP" ]]; then
    ...
    ```

    + [Check if string is neither empty nor space in shell script](https://stackoverflow.com/questions/13509508/check-if-string-is-neither-empty-nor-space-in-shell-script)
    + [How best to include other scripts?](https://stackoverflow.com/questions/192292/how-best-to-include-other-scripts)
    + [Subtract time using date and bash](https://unix.stackexchange.com/questions/497639/subtract-time-using-date-and-bash)
    + [Bash script template (incl. logging functions)](https://gist.github.com/PhilipSchmid/df69017fc15877997d3528633abd802d)

+ tmux
    + [Краткая шпаргалка по tmux](https://habrahabr.ru/post/126996/)

+ TCP backup
    + [Chapter 2. The Transport Layer: TCP, UDP, and SCTP](https://notes.shichao.io/unp/ch2/)
        + [Chapter 4. Elementary TCP Sockets](https://notes.shichao.io/unp/ch4/)
    + [«Boost.Asio C++ Network Programming». Глава 4: Клиент и Сервер](https://habrahabr.ru/post/195794/)
    + [Boost.Asio C++ Network Programming examples](http://www.boost.org/doc/libs/1_65_1/doc/html/boost_asio/examples/cpp11_examples.html)
    + [SOCKETS - SERVER & CLIENT C++ - 2017](http://www.bogotobogo.com/cplusplus/sockets_server_client.php#block_vs_non_blocking)
    + [Error : “Transport endpoint is already connected”](https://stackoverflow.com/questions/7140438/error-transport-endpoint-is-already-connected)
        + [Socket program gives “Transport endpoint is already connected” error](https://stackoverflow.com/questions/9873650/socket-program-gives-transport-endpoint-is-already-connected-error)
        + [Reconnecting with connect() on restarted server returns -Transport endpoint is already connected](https://stackoverflow.com/questions/16910973/reconnecting-with-connect-on-restarted-server-returns-transport-endpoint-is-a)
        + [Starter UDP Server And Client in C++](https://prglb.ru/4evp2)
        + [Creating a TCP Server in C++ [Linux / Code Blocks]](https://www.youtube.com/watch?v=cNdlrbZSkyQ)
        + [How to Watch TCP and UDP Ports in Real-time](https://www.tecmint.com/watch-tcp-and-udp-ports-in-linux/)

+ [The Illustrated TLS Connection Every byte of a TLS connection explained and reproduced](https://tls.ulfheim.net/)
    + [The Illustrated TLS Connection: Every byte explained](https://github.com/syncsynchalt/illustrated-tls)

+ [VPP](https://wiki.fd.io/view/VPP)
    + [VPP/What is VPP? The VPP platform is an extensible framework that provides out-of-the-box production quality switch/router functionality](https://wiki.fd.io/view/VPP/What_is_VPP%3F)
    + [VPP/Pulling, Building, Running, Hacking and Pushing VPP Code](_Hacking_and_Pushing_VPP_Code)    
    tl;dr
    ```
    git clone https://USERNAME@gerrit.fd.io/r/a/vpp
    ```
    + [Building FD.io VPP 18.10 on Ubuntu 18.04 LTS with Mellanox DPDK PMD without OFED](http://www.jimmdenton.com/vpp-1810-mellanox/)
    + [VPP/Installing VPP binaries from packages](https://wiki.fd.io/view/VPP/Installing_VPP_binaries_from_packages)
    + [Arch Linux in the Arch User Repository (AUR)](https://aur.archlinux.org/packages/vpp/)

+ [WHY MILLISECONDS MATTER : REST vs. gRPC](https://www.yonego.com/nl/why-milliseconds-matter/#gref)

+ Data transfer
    + [So you want to write to a file real fast…](https://blog.plenz.com/2014-04/so-you-want-to-write-to-a-file-real-fast.html)
        + tl;dr
        ```c++
        ssize_t do_sendfile(int in, int out)
        {
            ssize_t t = filesize(in);
            off_t ofs = 0;

            while(ofs < t) {
                if(sendfile(out, in, &ofs, t - ofs) == -1) {
                    assert(errno == EINTR);
                    continue;
                }
            }

            return t;
        }
        ```
        + [Use sendfile() to speed up transfers](https://github.com/giampaolo/pyftpdlib/issues/152)
    + [high CPU load by 'mmcqd' in Ubuntu](https://community.nxp.com/thread/318739)
    + [Copy a file in a sane, safe and efficient way](http://stackoverflow.com/questions/10195343/copy-a-file-in-a-sane-safe-and-efficient-way)
    + [Linux function to get mount points](http://stackoverflow.com/questions/9280759/linux-function-to-get-mount-points)
        + tl;dr    
        ```c
        #include <stdio.h>
        #include <stdlib.h>
        #include <mntent.h>
        
        int main(void)
        {
          struct mntent *ent;
          FILE *aFile;
        
          aFile = setmntent("/proc/mounts", "r");
          if (aFile == NULL) {
            perror("setmntent");
            exit(1);
          }
          while (NULL != (ent = getmntent(aFile))) {
            printf("%s %s\n", ent->mnt_fsname, ent->mnt_dir);
          }
          endmntent(aFile);
        }
    + [How to Get Available Filesystem Space on Linux: a C Function with a C++ Example](https://www.systutorials.com/136585/how-to-get-available-filesystem-space-on-linux-a-c-function-and-a-cpp-example/)    ```

+ [Linking](http://www.cs.utexas.edu/~witchel/429/lectures/11-linking.pdf)
    + [Controlling the Exported Symbols of Shared Libraries](https://www.gnu.org/software/gnulib/manual/html_node/Exported-Symbols-of-Shared-Libraries.html)
    + [Control over symbol exports in GCC](http://anadoxin.org/blog/control-over-symbol-exports-in-gcc.html)

+ packaging
    + [Hosting a Private Apt Repository on S3](https://zcox.wordpress.com/2012/08/13/hosting-a-private-apt-repository-on-s3/)
    + [Managing Apt Repos in S3 Using Lambda](http://webscale.plumbing/managing-apt-repos-in-s3-using-lambda)
        + [apt-s3](https://github.com/castlabs/apt-s3)

+ lock files
    + [Linux: What is the difference between advisory lock and mandatory lock?](https://www.quora.com/Linux-What-is-the-difference-between-advisory-lock-and-mandatory-lock)
    + [`flock` use case](http://stackoverflow.com/questions/1599459/optimal-lock-file-method)
    + [lock files: 2.9 Synchronizing Resource Access Across Processes on Unix](http://etutorials.org/Programming/secure+programming/Chapter+2.+Access+Control/2.9+Synchronizing+Resource+Access+Across+Processes+on+Unix/)

+ misc
    + [nm vs “readelf -s”](https://stackoverflow.com/questions/9961473/nm-vs-readelf-s)    
    tl;dr    
    ```sh
    nm -o -D *.so
    ```
    + [fdupes – A Comamndline Tool to Find and Delete Duplicate Files in Linux](http://www.tecmint.com/fdupes-find-and-delete-duplicate-files-in-linux/)
    + [Is there a difference between using pmount and mount?](https://superuser.com/questions/273956/is-there-a-difference-between-using-pmount-and-mount)
    + [How To Quickly Generate A Large File On The Command Line (With Linux)](http://www.skorks.com/2010/03/how-to-quickly-generate-a-large-file-on-the-command-line-with-linux/)
    + [How to check programatically if the Ethernet cable is plugged in?](https://unix.stackexchange.com/questions/163503/how-to-check-programatically-if-the-ethernet-cable-is-plugged-in)    

    tl;dr
    ```sh
    for i in $( ls /sys/class/net ); do echo $i; done
    dummy0
    enx00044b5acf64
    ip6tnl0
    lo
    rmnetctl
    sit0
    tunl0
    wlan0

    for i in $( ls /sys/class/net ); do echo -n $i: ; cat /sys/class/net/$i/carrier; done
    dummy0:cat: /sys/class/net/dummy0/carrier: Invalid argument
    enx00044b5acf64:1
    ip6tnl0:cat: /sys/class/net/ip6tnl0/carrier: Invalid argument
    lo:1
    rmnetctl:cat: /sys/class/net/rmnetctl/carrier: Invalid argument
    sit0:cat: /sys/class/net/sit0/carrier: Invalid argument
    tunl0:cat: /sys/class/net/tunl0/carrier: Invalid argument
    wlan0:1

    for i in $( ls /sys/class/net ); do echo -n $i: ; cat /sys/class/net/$i/operstate; done
    dummy0:down
    enx00044b5acf64:up
    ip6tnl0:down
    lo:unknown
    rmnetctl:down
    sit0:down
    tunl0:down
    wlan0:unknown
    ```
+ [Maximum length of the textual representation of an IPv6 address?](https://stackoverflow.com/questions/166132/maximum-length-of-the-textual-representation-of-an-ipv6-address)

+ [Apache Thrift vs Protocol Buffers detailed comparison as of 2019](https://www.slant.co/versus/9125/9127/~apache-thrift_vs_protocol-buffers)
    + [Apache Thrift Language Support](https://thrift.apache.org/docs/Languages)

+ [Slimjet Browser Review – speed and utility](https://malwarecomplaints.info/slimjet-browser-review-speed-utility/)

+ [Video Downloader](https://www.duplicate-finder.com/video-dl.html)

+ [Where does YouTube's offline feature store video files?](https://android.stackexchange.com/questions/97399/where-does-youtubes-offline-feature-store-video-files)
    + [An extensible media player for Android](https://github.com/google/ExoPlayer)

+ [Предметно-ориентированное проектирование на самом деле](https://habr.com/ru/post/490270/)

+ youtube-dl
    + [youtube-dl, или как скачать видео с YouTube в качестве 1080p и выше](https://habr.com/ru/post/369853/)
    + [youtube-dl github repo](https://github.com/ytdl-org/youtube-dl)
    + [Скачиваем видео на Андроид с помощью youtube-dl](http://wpilot.blogspot.com/2018/06/download-video-youtube-dl-to-android.html)

+ [Why you should use named pipes on Linux](https://www.networkworld.com/article/3251853/why-use-named-pipes-on-linux.html)

+ [Can I share a file descriptor to another process on linux or are they local to the process?](https://stackoverflow.com/questions/2358684/can-i-share-a-file-descriptor-to-another-process-on-linux-or-are-they-local-to-t?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa)

+ [Take a screenshot of a area in xfce?](https://askubuntu.com/questions/525988/take-a-screenshot-of-a-area-in-xfce)    
    ```sh
    xfce4-screenshooter -f
    ```

+ Linux refresh
    + [Примеры программ для операционной системы Linux](https://github.com/devtype-blogspot-com/Linux-Sample-Code/blob/master/README.md)
    + [Основы программирования для Linux - terse Linux basics](https://devtype.blogspot.com/2016/05/Osnovy-programmirovanija-dlja-Linux.html)
    + [Difference between r+ and w+ in fopen()](https://stackoverflow.com/questions/21113919/difference-between-r-and-w-in-fopen)
    + [Duplicating file pointers?](https://stackoverflow.com/questions/6099315/duplicating-file-pointers)
    + [Linux terminals, tty, pty and shell](https://dev.to/napicella/linux-terminals-tty-pty-and-shell-192e)
    + [Linux terminals, tty, pty and shell - part 2](https://dev.to/napicella/linux-terminals-tty-pty-and-shell-part-2-2cb2)

+ AWS
    + [Configuration file cannot be used with CMake 3.22.0](https://github.com/aws/aws-sdk-cpp/issues/1820)
        + [Fix building AWS SDK for C++ with CMake 3.22.0](https://github.com/microsoft/vcpkg/pull/21668)
            + [Fix AWS SDK for C++ configuration](https://github.com/microsoft/vcpkg/pull/21668/commits/adfafc73e1993e351388561bde2c2852b58935ef)
