Releasing the template
======================

1. Go to the branch with the template version to be released 

2. If you want to release the version of an older commit, use git checkout followed by the commit hash to point the current *HEAD* to it

3. Create a tag with a *name* and a *description*:
    
        git tag -a name -m "description"

4. Push the tag to your remote git repository
        
        git push origin name-of-tag

5. The release will be available [here](https://github.com/hmgaudecker/econ-project-templates/releases)


Creating a documentation for a release
--------------------------------------

1. Create a new version of the documentation in *source/version_name/language*

    - *version_name* can be something like devel, v1.0 or current
    - *language* is the language of the specific template you are writing the documentation for

2. Copy the *wscript* and *conf.py* from an older documentation and adjust the directories pointing to the new documentation in the wscript file

3. Add *ctx.recurse(relative_path_to_documentation)* to the build function in source/wscript

4. In the main index *source/index.rst* add a new link pointing to the documentation. It should have the form *version/language/index*

