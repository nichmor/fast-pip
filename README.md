pip. just faster.

Under construction.

This is my vision of how a front-end ( pip-like tool) should work. It is not a replacement of pip, but a new tool. My aim is to provide a faster and more strict tool for installing python packages.

Current roadmap is in  unstable phase, but represent my current mind map for it.

Suggestions are welcome.


Roadmap:
* [x] parallel async downloads of candidates
* [x] parallel build of wheels
* [x] do not install a requirement if it is conflicting with another installed requirement. Have an option to override this behavior.
* [x] fast-pip uninstall --with-childs <package> which will uninstall package with all installed dependencies of it.
* [x] caching of already installed packages, so next time we do not download them again. An option to control this behavior.