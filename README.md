# fog-documentation

Documentation for FOG 1.X

This gets built by readthedocs via this readthedocs project https://readthedocs.org/projects/fogproject/

The latest version will be available at https://docs.fogproject.org/

See also for more discussion - https://forums.fogproject.org/topic/14794/improve-documentation?_=1602258264683

The documentation is written in restructured text and built with sphinx

## Resources from writing in rst

These links are some good references for how to write in rst and how to configure and customize the readthedocs site

- https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html
- https://www.ericholscher.com/blog/2016/jul/1/sphinx-and-rtd-for-writers/
- https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html
- https://docs.readthedocs.io/en/stable/guides/adding-custom-css.html?highlight=css
- https://docs.readthedocs.io/en/stable/custom_domains.html?highlight=domain

## Building locally

see also (https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html)

To test and build documemtation locally you need the following

- Python 3.7+ (can install from python.org, windows store, apt-get, yum, chocolatey, etc.)
- sphinx (`pip install sphinx`)
- sphinx_rtd_theme (`pip install sphinx_rtd_theme`)

Once you have those pre-reqs installed follow these steps

- Clone the repo
- Add additional .rst documentation following the existing structure
- run `make.ps1` from the root of the repo
  - This will create your `.\_build` directory and run `make html` with the project's settings
  - This is just a powershell version of the autogenerated make.bat file. It has some built-in error handling to help find the sphinx-build.exe if it isn't added to your path

You will now have the files for the html site in you `_build` directory (the `_build` directory is excluded via .gitignore)
You can then open the `index.html` file from `.\_build\html` to browse the site locally.
