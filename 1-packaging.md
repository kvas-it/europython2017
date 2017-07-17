# Python packaging (Jakub Wasielak)

- https://packaging.python.org

- setup.py
  - version bumping: https://github.com/pypa/setuptools_scm (pep-440)
  - classifier: "Private :: Do not upload"
  - use extras\_require = {'testing': [...]} instead of test\_requires
- setup.cfg
  - default options for setup.py commands
- MANIFEST.in - what to include in the package except for the python modules: 
  - static files, license, etc
- eggs are deprecated, use wheels
  - no .pyc files inside
  - richer naming convention (includes more information)
  - can install C components without a compiler
- devpi
- pypa.io roadmap!
  - for example pipfile
- http://pypi.org/
