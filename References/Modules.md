# Modules
When programming for Unreal Engine code is compiled to modules using C# target and build files. These files tell the compiler when a modules has a depedency on another, what plugins a module might require and which type of build a module is targeting.

Client, Editor, Game, Server


The main difference between a module and a plugin is organizational.
A plugin is an optional module compiled outside of the game/engine modules and is added via the plugin browser in your project file.

Modules can have any number of dependencies on other modules, in the plugin browser you will be notified when loading/unloading a module which requires another.

Projects / Plugins can be compiled from a number of modules, you may have modules which are only editor or developer related which arnt required for shipping builds.

### With Git
I have found the best method for sharing parts of a project is to seperate them into a plugin and using Gits Submodules on those sub directories within the project.
This can be a challenge because Git only allows for one repository per directory, this is why splitting projects into modules can be useful especially in the case you have multiple different access levels, public vs private repositories.

# Categories / Tags
* API
* C++

Back to [Main Page](../README.md)