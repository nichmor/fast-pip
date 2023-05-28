pip. just faster.

Under construction.

This is my vision of how a front-end ( pip-like tool) should work. It is not a replacement of pip, but a new tool. My aim is to provide a faster and more strict tool for installing python packages.

Current roadmap is in  unstable phase, but represent my current mind map for it.

I plan to support 3.7+ python versions.

Suggestions are welcome.


Roadmap:
* [] parallel async downloads of candidates
* [] parallel build of wheels
* [] do not install a requirement if it is conflicting with another installed requirement. Have an option to override this behavior. Rationale for this is that very often during CI preparation step, pip install -r requirements.txt doc_requirements.txt is green. Later, on testing phase we can discover that during installing some of the requirements were overidden and we have a different set of packages installed. This is a very common problem, which for debug you need to go back on installing phase and look what conflictings requirements you have. This tool will prevent this from happening.
* [] fast-pip uninstall --with-childs <package> which will uninstall package with all installed dependencies of it.
* [] caching of already installed packages, so next time we do not download them again. An option to control this behavior.