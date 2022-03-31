# Technical Typesetting links and tips

+ [Hyperpolyglot: Lightweight Markup: Markdown, reStructuredText, MediaWiki, AsciiDoc, Org-mode](http://hyperpolyglot.org/lightweight-markup)

+ [A template for textbooks in the same style as Algorithms for Optimization](https://github.com/sisl/tufte_algorithms_book.git)

+ [Accessible LaTeX](https://github.com/MatthewDaws/AccessibleLaTeX)

+ pandoc
    + [pandoc binaries](https://github.com/jgm/pandoc/releases/tag/1.15.0.6)
    + installing from `hackage`
    ```sh
    cabal install pandoc
    ```
    + [pandoc: Embedded SVG in PDF](https://github.com/jgm/pandoc/issues/265)
        + [open: Support SVG images in multiple formats](https://github.com/jgm/pandoc/issues/1793)

    + [Building pretty slides using Markdown and pandoc](https://avalz.it/2017/02/01/build-pretty-slides/)
    + [Render PDF from Markdown that is using mermaid](https://janikvonrotz.ch/2020/11/12/render-pdf-from-markdown-that-is-using-mermaid/)

+ Confluence tips
    + [How to migrate a Confluence space to a Markdown Wiki](http://blog.deveo.com/confluence-to-markdown-wiki-migration/)
    + [Confluence to Markdown converter which is actually working](https://github.com/meridius/confluence-to-markdown)

+ LaTeX tips
    + [Can people actually keep up with note-taking in Mathematics lectures with LaTeX?](https://www.quora.com/Can-people-actually-keep-up-with-note-taking-in-Mathematics-lectures-with-LaTeX/answer/Gilles-Castel-1)
        + [Как я пишу конспекты по математике на LaTeX в Vim](https://habr.com/ru/post/445066/)
    + [Modern LaTeX typesetting](https://www.olivierverdier.com/posts/2013/07/15/modern-latex/)
    + [PGFPlots?](https://ask-ubuntu.ru/questions/473263/kakoj-paket-predostavlyaet-pgfplotssty)    
    tl;dr    
    ```sh
    pacman -S texlive-pictures
    ```
    + Arch Linux Latin Modern & Latin Modern Math 
        ```sh
        yay -S otf-latin-modern
        yay -S otf-latinmodern-math
        ```
    + Arch Linux specifics for Cyrillic letters with LaTeX    
        ```sh
        pacman -S texlive-langcyrillic
        yay -S ttf-computer-modern-fonts
        yay -S ttf-cm-unicode
        yay -S ttf-pt-fonts
            to fix arch linux Invalid fontname `PT Sans'
        ```
        + [Problems with Cyrillic fonts in XeTeX](http://tex.stackexchange.com/questions/209614/problems-with-cyrillic-fonts-in-xetex)
            + Ubuntu    
                ```sh
                sudo apt install fonts-cmu
                sudo apt-get install --no-install-recommends xindy-rules po4a texlive-lang-cyrillic texlive-xetex texlive-latex-recommended texlive-latex-extra texlive-fonts-extra latex-xcolor pgf bzr texlive-fonts-recommended ttf-linux-libertine
                ```
                + [Package algorithm2e on Ubuntu](https://tex.stackexchange.com/questions/46276/package-algorithm2e-on-ubuntu)    
                ```sh    
                sudo apt-get install texlive-science
                ```

            + PT Sans, Serif, Mono    
                + [Install Google Fonts on Ubuntu](https://gist.github.com/lightonphiri/5811226a1fba0b3df3be73ff2d5b351c)    
                tl;dr    
                ```
                download from http://rus.paratype.ru/pt-sans-pt-serif and/or https://fonts.google.com/specimen/Open+Sans
                cd /usr/share/fonts
                sudo mkdir googlefonts
                sudo unzip -d . ~/Downloads/Open_Sans.zip
                sudo fc-cache -fv
                fc-match OpenSans
                ```
            + test file `test_cyrillic.tex`
            ```latex
            \documentclass{article}
            \usepackage{fontspec}
            \setmainfont{CMU Serif}  
            \begin{document}
            \section{Свои проекты и вклады}
            \emph{Докладчик}Доклад <<С++ без new и delete>>.
            \end{document}
            ```
            + test cyrillic letters
            ```sh
            xelatex test_cyrillic.tex
            pandoc --latex-engine=xelatex -V mainfont="Linux Libertine O" unsorted.md -o unsorted.pd
            pandoc --latex-engine=xelatex -V mainfont="PT Sans" unsorted.md -o unsorted1.pdf
            ```
 
            + [Problem producing PDF from Cyrillic Markdown + LaTeX](https://groups.google.com/forum/#!topic/pandoc-discuss/DOdgRfP3Z8Q)
            + [И опять шрифты](http://forum.ubuntu.ru/index.php?topic=211336.0)
            + [LaTeX support for the fonts PT Sans, PT Serif and PT Mono](https://www.ctan.org/tex-archive/fonts/paratype)
                + [Общедоступные шрифты с поддержкой национальных алфавитов России](https://www.paratype.ru/public/)
    + ['l3regex.sty' not found](https://tex.stackexchange.com/questions/479650/l3regex-sty-not-found)
    + [Show equation number only once in align environment](https://tex.stackexchange.com/questions/17528/show-equation-number-only-once-in-align-environment)
      tl;dr
      ```latex
      \begin{align}
      \begin{split}
        a &= b \\
        &=c \\
        &=d \\
        &=e
      \end{split}
      \end{align}
      ```
    + [Description list with aligned descriptions](https://tex.stackexchange.com/questions/67720/description-list-with-aligned-descriptions)
    + [Inline code and short verb with minted](https://tex.stackexchange.com/questions/45756/inline-code-and-short-verb-with-minted)
    + [Positioning of Figures](https://www.overleaf.com/learn/latex/Positioning_of_Figures)
    + [How to center a specific caption?](https://tex.stackexchange.com/questions/95207/how-to-center-a-specific-caption)
    + [Caption on the side of a figure](https://tex.stackexchange.com/questions/29143/caption-on-the-side-of-a-figure)
        + [Minted and floatrow incompatible](https://tex.stackexchange.com/questions/378563/minted-and-floatrow-incompatible)
          tl;drfloatrow conflicts with minted
    + [LaTeX forum ⇒ Graphics, Figures & Tables ⇒ Subfigures with caption on side](https://latex.org/forum/viewtopic.php?t=21220)
    + [How to put two minipages side-by-side, which use 100 % of the text width?](https://tex.stackexchange.com/questions/114520/how-to-put-two-minipages-side-by-side-which-use-100-of-the-text-width)
    + [itemize, removing natural indent](https://tex.stackexchange.com/questions/91124/itemize-removing-natural-indent/91128)
    + [No `\citation`, `\bibdata` or `\bibstyle` commands](https://tex.stackexchange.com/questions/406205/no-citation-bibdata-or-bibstyle-commands)
    + [Beamer Presentation: Figure has no number?](https://tex.stackexchange.com/questions/127145/beamer-presentation-figure-has-no-number)
        tl;dr    
        ```latex
        \setbeamertemplate{caption}[numbered]
        ```
    + [Beamer : remove the number page of the first slide](https://tex.stackexchange.com/questions/373945/beamer-remove-the-number-page-of-the-first-slide?noredirect=1&lq=1)
        tl;dr    
        ```latex
        {
        \setbeamertemplate{footline}{}
        \begin{frame}
        \titlepage
        \end{frame}
        }
        ```
    + [Customize title of beamer note pages](https://tex.stackexchange.com/questions/545199/customize-title-of-beamer-note-pages)
        tl;dr    
        ```latex
        % Space between paragraphs on notes page
        \addtobeamertemplate{note page}{\setlength{\parskip}{12pt}}{}
        %%\addtobeamertemplate{note page}{\setbeamerfont{itemize/enumerate subbody}{size=\scriptsize}}{}
        %%\addtobeamertemplate{note page}{\setbeamerfont{itemize/enumerate subsubbody}{size=\tiny}}{}
        ```
    + [What are the main differences between Texmaker and TeXstudio?](http://tex.stackexchange.com/questions/208219/what-are-the-main-differences-between-texmaker-and-texstudio)
        + [LaTeX Editors/IDEs](http://tex.stackexchange.com/questions/339/latex-editors-ides)
    + [buildtexlive](https://github.com/elkrejzi/system-management/blob/master/buildscripts/buildtexlive#L52)
    + [Introduction to TeX Live from source](http://www.linuxfromscratch.org/blfs/downloads/stable/BLFS-BOOK-7.7-nochunks.html#tl-installer)
        + [Re: [blfs-dev] Possible changes to how we do texlive](https://www.mail-archive.com/blfs-dev@lists.linuxfromscratch.org/msg02996.html)
    + [KaTeX The fastest math typesetting library for the web](http://khan.github.io/KaTeX/)
        + [KaTeX github](https://github.com/Khan/KaTeX)
    + [LaTeX Table Generator](http://www.tablesgenerator.com/)
    + [Online LaTeX Equation Editor](http://www.codecogs.com/latex/eqneditor.php)
    + [Element-wise (or pointwise) operations notation?](http://math.stackexchange.com/questions/20412/element-wise-or-pointwise-operations-notation)
        + [List of mathematical symbols](https://en.wikipedia.org/wiki/List_of_mathematical_symbols)
        + [Mathematics#List_of_Mathematical_Symbols](https://en.wikibooks.org/wiki/LaTeX/Mathematics#List_of_Mathematical_Symbols)
            + [How do I use a circle as a math accent (larger than \mathring)?](http://tex.stackexchange.com/questions/3266/how-do-i-use-a-circle-as-a-math-accent-larger-than-mathring)
            + [how to get good looking copyright and registered symbols](http://tex.stackexchange.com/questions/1676/how-to-get-good-looking-copyright-and-registered-symbols)

    + [Fonts](https://en.wikibooks.org/wiki/LaTeX/Fonts)
    + [Macros](https://en.wikibooks.org/wiki/LaTeX/Macros)
    + [LaTeX/Lengths](https://en.wikibooks.org/wiki/LaTeX/Lengths)
    + [Import graphics](https://en.wikibooks.org/wiki/LaTeX/Importing_Graphics)
    + [Aligning equations with amsmath](https://www.sharelatex.com/learn/Aligning_equations_with_amsmath)
    + [Text alignment](https://www.sharelatex.com/learn/Text_alignment)
    + [How to strike out inside LaTeX equations?](http://stackoverflow.com/questions/2663944/how-to-strike-out-inside-latex-equations)
    + [minted – highlighted source code for LaTeX](https://code.google.com/p/minted/)
        + [Code Highlighting with minted -- contains nifty colour styles to choose from](https://www.sharelatex.com/learn/Code_Highlighting_with_minted)
    + [Description list with aligned descriptions](http://tex.stackexchange.com/questions/67720/description-list-with-aligned-descriptions)
    + [texblog Lists: Enumerate, itemize, description and how to change them](http://texblog.org/2008/10/16/lists-enumerate-itemize-description-and-how-to-change-them/)
    + Unicode
        + [entering-unicode-characters-in-latex](http://tex.stackexchange.com/questions/34604/entering-unicode-characters-in-latex)
            + [insert-unicode-symbol](http://tex.stackexchange.com/questions/37445/insert-unicode-symbol)
        + Fonts (CMU aka Computer Modern Unicode especially)
            + [Adding New Fonts to Your System](http://community.linuxmint.com/tutorial/view/29)
            + [why-does-xetex-not-display-basic-unicode-characters](http://tex.stackexchange.com/questions/201622/why-does-xetex-not-display-basic-unicode-characters)
            + [Как сказать XeLaTeX, чтобы использовал шрифты Computer Modern?](http://www.linux.org.ru/forum/desktop/8254794)
            + [Using fonts installed in local texlive](http://tex.stackexchange.com/questions/202767/using-fonts-installed-in-local-texlive)

    + [PDF slides and handouts using Pandoc and Beamer](https://gist.github.com/lmullen/c3d4c7883f081ed8692a)
        + [Better-looking LaTeX/Beamer slides](https://kbroman.wordpress.com/2013/10/07/better-looking-latexbeamer-slides/)
        + [verbatim environment does not work with beamer](http://tex.stackexchange.com/questions/161202/verbatim-environment-does-not-work-with-beamer)
        + [LaTeX beamer: way to change the bullet indentation?](http://stackoverflow.com/questions/2611276/latex-beamer-way-to-change-the-bullet-indentation)

    + [The Haskell LaTeX library](https://github.com/Daniel-Diaz/HaTeX)
        + [Convenient Haskell syntax for writing in LaTeX math expressions](https://github.com/leftaroundabout/Symbolic-math-HaTeX)

    + [TeX for Gmail](http://alexeev.org/gmailtex.html)

+ MacOS X
    + [Missing fonts from LaTeX](https://forum.affinity.serif.com/index.php?/topic/2483-missing-fonts-from-latex/)
    tl;dr  
    ```latex
    \documentclass[]{article}

    \usepackage{fontspec}
    \usepackage{polyglossia}
    \usepackage{unicode-math}
    \setmainfont{CMU Serif}
    \setsansfont{CMU Sans Serif}
    \setmonofont{CMU Typewriter Text}
    \setmathfont{Latin Modern Math}

    \title{}
    \author{}
    \begin{document}
    Hello, world!
    Привет, мир!
    $ a≡b≠Ω♯$
    $$
    \int_0^\infty x^2\beta d\alpha \omega
    $$
    $$L_{{\Omega ,\nu }}^{\circ }(\nu ,T)={\frac {2{\mathrm {h}}\nu ^{3}}{c^{2}}}{\frac {1}{{\mathrm {e}}^{{{\mathrm {h}}\nu /({\mathrm {k}}T)}}-1}}$$
    \end{document}
    ```

+ Creating diagrams
    + diagrams using Rust
        + [SvgBobRus is an ascii to svg converter](https://github.com/ivanceras/svgbobrus)
        tl;dr
        ```sh
        cargo install svgbob_cli
        svgbob < examples/long.bob > long.svg
        svgbob -o long.svg < examples/long.bob
        svgbob examples/long.bob > long.svg
        ```
            + [How do I convert an SVG to a PDF on Linux](https://superuser.com/questions/381125/how-do-i-convert-an-svg-to-a-pdf-on-linux)
    + [ASCII Flow Draw](http://stable.ascii-flow.appspot.com/#Draw)

    + [Creating documents with embedded diagrams](https://byorgey.wordpress.com/2012/08/28/creating-documents-with-embedded-diagrams/)
        + [diagrams](http://projects.haskell.org/diagrams/)
            + [project haskell diagrams blog](http://projects.haskell.org/diagrams/blog/index.html)
            + [Diagrams 1.3 : what's new](http://projects.haskell.org/diagrams/blog/2015-04-24-diagrams-1.3.html)
            + blog :: Brent -> [String]
                + [About Brent Yorgey](https://byorgey.wordpress.com/about/)
                + [diagrams blog](https://byorgey.wordpress.com/tag/diagrams/)
            + [diagrams-builder](https://github.com/diagrams/diagrams-builder)
            + [Using Diagrams library in haskell (draw binary trees)](http://stackoverflow.com/questions/30667522/using-diagrams-library-in-haskell-draw-binary-trees)
            + [Haskell Diagrams wiki](https://wiki.haskell.org/Diagrams)
                + [Haskell Diagrams backends](https://wiki.haskell.org/Diagrams/Projects#PDF)
            ```sh
            cabal install gtk2hs-buildtools
            cabal install -fcairo diagrams
            cabal --reinstall install -fcairo diagrams
            ghc --make DiagramsTutorial.lhs
            ./DiagramsTutorial -o circle.svg -w 400
            ./DiagramsTutorial -o circle.pdf -w 400
            cat DiagramsTutorial.lhs
            ```
            ```lhs
            > {-# LANGUAGE NoMonomorphismRestriction #-}
            >
            > import Diagrams.Prelude
            > import Diagrams.Backend.Cairo.CmdLine
            >
            > main = mainWith (circle 1 :: Diagram B)
            ```

            The 2nd example : tree rendering
            ```lhs
            > import Diagrams.Prelude
            > import Diagrams.Backend.Cairo.CmdLine
            
            We make use of a tree layout module from the diagrams-contrib package:
            
            > import Data.Tree
            > import Diagrams.TwoD.Layout.Tree
            
            + [Diagrams.TwoD.Layout.Tree official documentation](https://hackage.haskell.org/package/diagrams-contrib-1.3.0.8/docs/Diagrams-TwoD-Layout-Tree.html)
            
            > t1 = Node 'A' [Node 'B' (map lf "CDE"), Node 'F' [Node 'G' (map lf "HIJ")]]
            >   where lf x = Node x []
            > 
            > exampleSymmTree =
            >   renderTree ((<> circle 1 # fc white) . text . (:[]))
            >              (~~)
            >              (symmLayout' (with & slHSep .~ 4 & slVSep .~ 4) t1)
            >   # centerXY # pad 1.1
            
            >
            > main = mainWith (exampleSymmTree :: Diagram B)

            ```
            as `exampleSymmTree` don't have parameters then there is no `{-# LANGUAGE NoMonomorphismRestriction #-}`
            even more with it `ghc` reports an error:
            ```haskell
            
            [1 of 1] Compiling Main             ( TimersTree.lhs, TimersTree.o )
            
            TimersTree.lhs:16:3:
                Non type-variable argument
                  in the constraint: Renderable (Path V2 n) b
                (Use FlexibleContexts to permit this)
                When checking that ‘exampleSymmTree’ has the inferred type
                  exampleSymmTree :: forall n b.
                                     (RealFloat n, Data.Typeable.Internal.Typeable n,
                                      Renderable (Path V2 n) b,
                                      Renderable (Diagrams.TwoD.Text.Text n) b) =>
                                     QDiagram b V2 n Any
            ```

            + [A pandoc filter to express diagrams inline using the haskell EDSL diagrams.](https://github.com/diagrams/diagrams-pandoc)
            + [modules not found when installed via Nix #7](https://github.com/diagrams/diagrams-pandoc/issues/7)
            ```sh
            cabal install diagrams-pandoc
            cabal install SVGFonts
            ```
            + [A PGF backend for diagrams](https://github.com/diagrams/diagrams-pgf)
            ```sh
            cabal install diagrams-pgf
            ```

            + an example of customized tree rendering
            ```lhs
            > text' (timer_name, func_name) = ((text ( timer_name ++ "\n\n")) # fc blue # fontSize (local 0.4)) === ((text ( func_name )) # fc green # italic # bold)Shared/Common/Src/CuttingLine/
            > mybox' (timer_name, func_name) = let wid = fromIntegral(length func_name)*0.3 in (text' (timer_name, func_name)) <> roundedRect wid 2 0.1 # fc gold
            > exampleSymmTree =
            >   renderTree mybox'
            >              (~~)
            >              (symmLayout' (with & slHSep .~ 8 & slVSep .~ 7) t1)
            >   # centerXY # pad 1.1 # fontSize (local 0.3)
            ```

            + [User’s Guide to the PGF Package](http://mixing.coas.oregonstate.edu/links/latex_files/pgfuserguide.pdf)

            + [The tree of function calls made by a naive Fibonacci implementation](http://projects.haskell.org/diagrams/gallery/FibCalls.html)
            + [Basic diagram with text, boxes and arrows](http://projects.haskell.org/diagrams/gallery/SymmetryCube.html)
            + [Diagrams Gallery](http://projects.haskell.org/diagrams/gallery.html)
            + [Flowchart sample](https://en.wikipedia.org/wiki/Flowchart#/media/File:Flowgorithm_Editor.png)
            + [Interactive windows for displaying Haskell-generated diagrams](https://github.com/leftaroundabout/dynamic-plot)
            + [Haskell Diagrams double lined arrows](http://www.scriptscoop.net/t/4bf84e30bd44/haskell-diagrams-double-lined-arrows.html)

            + [CSE230 Wi14 - Programming With Effects (monads)](https://cseweb.ucsd.edu/classes/wi14/cse230-a/lectures/lec-monads.html)

        + [Unordered tuples and type algebra](https://byorgey.wordpress.com/2012/08/24/unordered-tuples-and-type-algebra/)
    + [Embedded diagrams in pandoc's markdown](https://github.com/nichtich/ditaa-markdown/)
    + [PlantUML](http://plantuml.com/running.html)

+ [Support LaTeX environments in Markdown -> HTML conversion #1938](https://github.com/jgm/pandoc/issues/1938)

+ use [dillinger for markdown formatting](http://dillinger.io/)
+ [Package algorithm2e on Ubuntu: sudo apt-get install texlive-science](http://tex.stackexchange.com/questions/46276/package-algorithm2e-on-ubuntu)

+ [Syntax highlighting in markdown](https://support.codebasehq.com/articles/tips-tricks/syntax-highlighting-in-markdown)

+ [math in markdown: Survey of syntaxes for math in markdown](https://github.com/cben/mathdown/wiki/math-in-markdown)
    + [Schlolarlymarkdown: make academic writing less frustrating](http://scholarlymarkdown.com/)
    + [github repo for scholdoc](https://github.com/timtylin/scholdoc)

+ Vector Drawing Editors
    + [asymptote](http://asymptote.sf.net)
        + [Fill a triangle in space using asymptote](https://tex.stackexchange.com/questions/149480/fill-a-triangle-in-space-using-asymptote)
        + [Asymptote: Drawing](https://artofproblemsolving.com/wiki/index.php?title=Asymptote:_Drawing)
            + [dvips error unknown keyword](https://github.com/vectorgraphics/asymptote/issues/124)
            + [~Errors "File `foo_0' not found." and "Unknown keyword ("foo_0".eps)"~ resolved](https://github.com/vectorgraphics/asymptote/issues/135)
                + [grffile does not work with LuaTeX any more](https://github.com/ho-tex/grffile/issues/1)
                + tl;dr temporary workaround 
                ```sh
                sudo pacman -U https://archive.archlinux.org/packages/a/asymptote/asymptote-2.48-1-x86_64.pkg.tar.xz
                add to /etc/pacman.conf
                IgnorePkg = asymptote
                ```
                + [How To Fix “invalid or corrupted package (PGP signature)” Error In Arch Linux](https://www.ostechnix.com/fix-invalid-corrupted-package-pgp-signature-error-arch-linux/)
                ```sh
                sudo pacman -S archlinux-keyring
                ```
    + [Inkscape](https://inkscape.org)
    + [GLE - for drawing logical gates / electrical diagrams](http://glx.sourceforge.net/downloads/downloads.html)
