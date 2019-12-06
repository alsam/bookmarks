# python language bookmarks

+ [Hybrid Python/C++ packages, revisited](https://www.benjack.io/2018/02/02/python-cpp-revisited.html)
    + [An example of a hybrid python/C++ package with unit tests](https://github.com/benjaminjack/python_cpp_example)

+ virtual environments
    + [Python Virtual Environments](http://docs.python-guide.org/en/latest/dev/virtualenvs/#virtualenvwrapper-ref)
    + [Linux: Install pip Client To Install Python Packages](http://www.cyberciti.biz/faq/debian-ubuntu-centos-rhel-linux-install-pipclient/)
    + [ Virtual Python Environment builder http://virtualenv.pypa.io ](https://github.com/pypa/virtualenv)
    + [ The PyPA recommended tool for installing Python packages https://pip.pypa.io/ ](https://github.com/pypa/pip)

+ anaconda links
    + [Installation of Python, Spyder, Numpy, Sympy, Scipy, Pytest, Matplotlib via Anaconda (2014)](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html)
    + [Anaconda Package Documentation](http://docs.continuum.io/anaconda/pkg-docs.html)
    + [anaconda ska inux-x86_64 Repodata](https://conda.binstar.org/ska/linux-64)
    + [Peter Williams pkgw: `conda install --channel https://conda.anaconda.org/pkgw gdk-pixbuf`](https://anaconda.org/pkgw)
        + [ImportError: libpng15.so.15: cannot open shared object file: No such file or directory](https://groups.google.com/a/continuum.io/forum/#!topic/anaconda/FuTqRu96fbo)
        + [Meld crashes Unrecognized image file format #33138](https://github.com/Homebrew/homebrew/issues/33136)
        + [symbol loopkup error: libgobject-2.0.so.0:undefined symbol: g_bytes_unref](http://stackoverflow.com/questions/14911046/symbol-loopkup-error-libgobject-2-0-so-0undefined-symbol-g-bytes-unref)
    + [Anaconda Accelerate Fast Python for GPUs and multi-core with NumbaPro and MKL Optimizations](https://store.continuum.io/cshop/accelerate/)
        + [Thread: Non-standard python](http://ubuntuforums.org/showthread.php?t=2263955)
    + miniconda
        tl;dr    
        ```sh
        wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
        bash ~/miniconda.sh -b -p ~/miniconda 
        rm ~/miniconda.sh
        echo "PATH=$PATH:$HOME/miniconda/bin" >> .bashrc
        echo ". ~/miniconda/etc/profile.d/conda.sh" >> ~/.bash_profile
        ```
        + [Conda activate not working?](https://stackoverflow.com/questions/47246350/conda-activate-not-working/47249905#47249905)
        + [Install Python dependency packages from requirements.txt using conda](https://gist.github.com/luiscape/19d2d73a8c7b59411a2fb73a697f5ed4)


+ cython links
    + [Cython code for the Computer Language Benchmark Game](https://github.com/cython/cython-shootout)

+ numpy issues
    + [Unable to import numpy: Error: /usr/lib/liblapack.so.3: undefined symbol: gotoblas](http://www.codeotel.com/CHVjqeqkUX/unable-to-import-numpy-error-usrlibliblapackso3-undefined-symbol-gotoblas.html)
    + [the cure `pip install --upgrade numpy` from here](http://stackoverflow.com/questions/23612728/error-by-import-numpy-lapack-lite-so-undefined-symbol)

+ [pychebfun - Python Chebyshev Functions](https://github.com/cswiercz/pychebfun)
    + [AN EXTENSION OF MATLAB TO CONTINUOUS FUNCTIONS AND OPERATORS](http://people.maths.ox.ac.uk/trefethen/publication/PDF/2004_107.pdf)

+ [Bessel functions in SciPy](http://www.johndcook.com/blog/bessel_python/)

+ [PyInterval](https://pypi.python.org/pypi/PyIntervalTree)

+ Numba
    + [Numba: Tell those C++ bullies to get lost](http://lorenabarba.com/blog/numba-tell-those-c-bullies-to-get-lost/)
        + [Numba tutorial materials for Scipy 2016](https://github.com/barbagroup/numba_tutorial_scipy2016)

+ StackOverflow questions
    + [Python sort dict by key](http://stackoverflow.com/questions/9001509/python-dictionary-sort-by-key)
    + [Python item freq count](http://stackoverflow.com/questions/893417/item-frequency-count-in-python)

+ Quantum Mechanics in Python
    + [Symbolic Quantum Mechanics using SymPy](https://github.com/sympsi/sympsi)
        + [Test and demo notebooks for the sympy.physics.quantum](https://github.com/jrjohansson/sympsi-notebooks)
    + [QuTiP: Quantum Toolbox in Python](https://github.com/qutip/qutip)
    + [Quantum Python: Animating the Schrodinger Equation](https://jakevdp.github.io/blog/2012/09/05/quantum-python/)

+ [Asynchronous Programming in Python](https://engineering.quora.com/Asynchronous-Programming-in-Python)

+ HTTP Server and Client in Python
    + [Let’s Build A Web Server. Part 1.](https://ruslanspivak.com/lsbaws-part1/)
    + [Simple HTTP Server and Client in Python](https://www.junian.net/2014/07/simple-http-server-and-client-in-python.html)

+ Python daemon
    + [python-daemon 2.1.1](https://pypi.python.org/pypi/python-daemon/)
    + [Python daemonizer class - outdated](https://github.com/serverdensity/python-daemon)
    + [How to make a Python script run like a service or daemon in Linux](http://stackoverflow.com/questions/1603109/how-to-make-a-python-script-run-like-a-service-or-daemon-in-linux)
    + [Немного фактов о python asyncio](https://habrahabr.ru/post/314606/)

+ Selected StackOverflow Python questions
    + [Invalid Token when using Octal numbers](http://stackoverflow.com/questions/1837874/invalid-token-when-using-octal-numbers)
    use `0o22` instead of `022`.
    + [How to unzip a list of tuples into individual lists?](https://stackoverflow.com/questions/12974474/how-to-unzip-a-list-of-tuples-into-individual-lists/12974504)
    + [Transpose/Unzip Function (inverse of zip)](https://stackoverflow.com/questions/19339/transpose-unzip-function-inverse-of-zip)
    + [How do I use Python's itertools.groupby()?](https://stackoverflow.com/questions/773/how-do-i-use-pythons-itertools-groupby)
    + [The order of nested list comprehension and nested generator expression in python](https://stackoverflow.com/questions/26759339/the-order-of-nested-list-comprehension-and-nested-generator-expression-in-python)
    + [list comprehension vs. lambda + filter](https://stackoverflow.com/questions/3013449/list-comprehension-vs-lambda-filter)
    + [How to split a sequence according to a predicate?](https://stackoverflow.com/questions/8793772/how-to-split-a-sequence-according-to-a-predicate)
    + numpy linear algebra stack overflow questions and other numpy questions
        + [How can I project a 3D point onto a 3D line?](https://gamedev.stackexchange.com/questions/72528/how-can-i-project-a-3d-point-onto-a-3d-line)
        + [Shortest distance between a point and a line in 3 d space](https://stackoverflow.com/questions/50727961/shortest-distance-between-a-point-and-a-line-in-3-d-space)
        + [Distance between point and a line (from two points)](https://stackoverflow.com/questions/39840030/distance-between-point-and-a-line-from-two-points)
        + [How to compute angle using NumPy?](https://stackoverflow.com/questions/52080614/how-to-compute-angle-using-numpy)
        + [Finding the closest point to a list of points](https://codereview.stackexchange.com/questions/28207/finding-the-closest-point-to-a-list-of-points)
        + [Convert numpy array to tuple](https://stackoverflow.com/questions/10016352/convert-numpy-array-to-tuple)
        + [ValueError: setting an array element with a sequence](https://stackoverflow.com/questions/4674473/valueerror-setting-an-array-element-with-a-sequence)
        + [How to zip two 1d numpy array to 2d numpy array](https://stackoverflow.com/questions/44409084/how-to-zip-two-1d-numpy-array-to-2d-numpy-array)
        + [numpy max vs amax vs maximum](https://stackoverflow.com/questions/33569668/numpy-max-vs-amax-vs-maximum)

    + [Python3: Invalid Syntax](http://stackoverflow.com/questions/12519554/python3-invalid-syntax)
    + [In practice, what are the main uses for the new “yield from” syntax in Python 3.3?](https://stackoverflow.com/questions/9708902/in-practice-what-are-the-main-uses-for-the-new-yield-from-syntax-in-python-3)
    + [What does the “yield” keyword do?](https://stackoverflow.com/questions/231767/what-does-the-yield-keyword-do)
    + [attrs by Example](http://www.attrs.org/en/stable/examples.html)
    + [Why should you use namedtuple instead of a tuple?](https://pythontips.com/2015/06/06/why-should-you-use-namedtuple-instead-of-a-tuple/)
    + [Try out walrus operator in Python 3.8](https://medium.com/hultner/try-out-walrus-operator-in-python-3-8-d030ce0ce601)

+ [Seamless operability between C++11 and Python](https://github.com/pybind/pybind11)
    + [pybind11 : First steps](http://pybind11.readthedocs.io/en/stable/basics.html)

+ [improve-your-python-understanding-unit-testing](https://jeffknupp.com/blog/2013/12/09/improve-your-python-understanding-unit-testing/)
    + [What is the best way to compare floats for almost-equality in Python](https://stackoverflow.com/questions/5595425/what-is-the-best-way-to-compare-floats-for-almost-equality-in-python)

+ [Object Oriented Programming(OOP) in Python Full Tutorial - 2019](https://youtu.be/6vV190q9vxA)

+ [Python Image Processing Tutorial (Using OpenCV)](https://likegeeks.com/python-image-processing/)

+ [An A-Z of useful Python tricks](https://morioh.com/p/9ef4ff8ac752/an-a-z-of-useful-python-tricks)
