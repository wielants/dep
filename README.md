# dep

This is a collection of programs that support a dependency analyzing workflow.
It depends on the Java jdeps tool to find the dependencies between classes therefore it is for the moment limited to the analysis of Java class files.
It also depends on bash (as this is a collection of bash scripts) and on awk.

The intended workflow is something like this:
- dep_init (create a dependency analyzing session with some classes)
- dep_list_cp (list all classes in the DEP_CLASSPATH)
- dep_ls (list all classes in the session)
- dep_add (add some classes to the session)
- dep_rm (remove some classes from the session)
- dep_search (search for a dependency by providing a regex)
- dep_search_class (search for a specific class)
- dep_stats (show some statistics about the classes currently in the session)
- dep_stats_uniq (show the number of dependent classes which were added the the session because a class was added to the session)
- dep_dot (stdout the contents of a graphviz dot file from the dependencies of some classes in the session)
- dep_gml (stdout the contents of a graph modelling language (gml) file from the dependencies of some classes in the session)
- dep_clear (close and delete the current analyzing session, BE ABSOLUTELY SURE that you want to delete your work! The tool does not ask!)

Before you can call dep_init, you have to set some environment variables.
You can configure make-env.sh and source it like this "source make-env.sh".

First you have to add the scripts from the bin directory to your PATH.
Then you must define, where your classpath is (DEP_CLASSPATH; at the moment only one class file directory is supported!) and 
the name of the base directory of your current dependency analyzing session (DEP_ROOTDIR).

After that you are free to run the scripts!
