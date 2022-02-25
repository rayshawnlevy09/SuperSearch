# SuperSearch (susearch)
A terminal program written in Python (Cython) built for both relative and system-wide searches.
*SuperSearch*, was built with simplicity and control in mind. SuperSearch has the ability to 
search for filenames and directories, and outputting the paths associated with either or. 
Though, anything containing the name, be it a filename or directory, will be found. For example, 
given the filename **test.txt**, if there are files such as: *help_test.txt* or *new_test.txt*, 
they will be shown as **Found** in the output.

To combat the number of files being found containing a given name, SuperSearch has a **--limit** 
option which will only find the specified number of paths, and limits the output based on those 
paths that are **Found**, but it **doesn't** limit the output when searching.

The help (**-h**) flag can be used to search for a specific **section** based on the usage of the 
susearch command, such as: *options*, *common*, *limits*, *output* and *limit/output*. These are 
all of the usage patterns available for the command. The *-h* flag can also be used on its own 
revealing all of the named sections.

There is much more that SuperSearch can do and more shall come.

Please create an issue if there are any bugs and I'll be happy to fix them.
