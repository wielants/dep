# dep

This is a collection of programs that support a dependency analyzing workflow.
It depends on the Java jdeps tool to find the dependencies between classes therefore it is for the moment limited to the analysis of Java class files.

The intended workflow is like this:
- dep_init (create a dependency analyzing session with some classes)
- dep_list_cp (list all classes in the DEP_CLASSPATH)
- dep_ls (list all classes in the session)
- dep_add (add some classes to the session)
- dep_rm (remove some classes from the session)
- dep_search (search for dependency by providing a regex)
- dep_search_class (search for a specific class)
- dep_stats (show some statistics about the classes currenty in the session)
- dep_dot (create a graphviz dot file from the dependencies of some classes in the session)
- dep_gml (creaze a graph modelling language (gml) file from the dependencies of some classes in the session)
- dep_clear (close and delete the current analyzing session)

