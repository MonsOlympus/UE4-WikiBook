# Modules
Projects and plugins within Unreal Engine are composed of components called modules, C++ code is compiled to modules using C# target and build files. These files tell the compiler when a module has a depedency on another, what plugins a module might require and which type of build a module is targeting. The plugin manager will notify you when loading/unloading a module which has a dependency on another or if a project requires a plugin to start.

Projects / Plugins can be compiled from a number of modules, you may have modules which are only editor or developer related which arnt required for shipping builds.

Client, Editor, Game, Server

### Basic Procedure
[Adding Modules](Lessons/BasicProcedures/AddingModules.md)
[Creating Plugins](Lessons/BasicProcedures/CreatingPlugins.md)

## UProjects && UPlugins
These files contain JSON which describes which modules a Project or Plugin include, and the circumstances for when they are loaded.

Content only plugins

### With Git
I have found the best method for sharing parts of a project is to seperate them into a plugin and using Gits Submodules on those sub directories within the project.
This can be a challenge because Git only allows for one repository per directory, this is why splitting projects into modules can be useful especially in the case you have multiple different access levels, public vs private repositories.

# Categories / Tags
* API
* C++

Back to [Main Page](../README.md)