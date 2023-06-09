pip. just faster.

Under construction.

This is my vision of how a front-end ( pip-like tool) should work. It is not a replacement of pip, but a new tool. My aim is to provide a faster and more strict tool for installing python packages.

Current roadmap is in  unstable phase, but represent my current mind map for it.

I plan to support 3.7+ python versions.

Suggestions are welcome.


Roadmap:
* [] parallel async downloads of candidates
* [] parallel build of wheels
* [] do not install a requirement if it is conflicting with another installed requirement. Have an option to override this behavior. 
* [] fast-pip uninstall --with-childs <package> which will uninstall package with all installed dependencies of it.
* [] caching ( .whl ) of already installed packages, so next time we do not download them again. An option to control this behavior.
* [] move critical parts to rust, using pyo3
