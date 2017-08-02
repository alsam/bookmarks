# Technical Typesetting links and tips

+ [Hyperpolyglot: Lightweight Markup: Markdown, reStructuredText, MediaWiki, AsciiDoc, Org-mode](http://hyperpolyglot.org/lightweight-markup)

+ pandoc
    + [pandoc binaries](https://github.com/jgm/pandoc/releases/tag/1.15.0.6)
    + installing from `hackage`
    ```sh
    cabal install pandoc
    ```
    + [pandoc: Embedded SVG in PDF](https://github.com/jgm/pandoc/issues/265)
        + [open: Support SVG images in multiple formats](https://github.com/jgm/pandoc/issues/1793)

+ Confluence tips
    + [How to migrate a Confluence space to a Markdown Wiki](http://blog.deveo.com/confluence-to-markdown-wiki-migration/)

+ LaTeX tips
    + [Modern LaTeX typesetting](https://www.olivierverdier.com/posts/2013/07/15/modern-latex/)
    + Arch Linux specifics for Cyrillic letters with LaTeX
        ```sh
        pacman -S texlive-langcyrillic
        yaourt -S ttf-computer-modern-fonts
        yaourt -S ttf-cm-unicode
        ```
        + [Problems with Cyrillic fonts in XeTeX](http://tex.stackexchange.com/questions/209614/problems-with-cyrillic-fonts-in-xetex)
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

+ Creating diagrams
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
            > text' (timer_name, func_name) = ((text ( timer_name ++ "\n\n")) # fc blue # fontSize (local 0.4)) === ((text ( func_name )) # fc green # italic # bold)
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
    + [Inkscape](https://inkscape.org)
    + [GLE - for drawing logical gates / electrical diagrams](http://glx.sourceforge.net/downloads/downloads.html)
