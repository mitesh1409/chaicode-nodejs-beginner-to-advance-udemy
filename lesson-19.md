# Understanding Node.js modules and their role in structuring code

Module and wrapper functions

There are 3 types of modules:  

1. Built-in modules
2. 3rd party modules
3. Custom modules (built by developer for the application)

When we import a module, it searches in the following order:  

1. Built-in Modules (e.g., 'path')

2. Custom Modules/Files (if the path starts with ./, ../, or /)

3. 3rd Party Modules (searching through node_modules folders for bare names)

This order ensures that built-in functionality is prioritized and that relative paths to your own custom code are found before the more extensive search through node_modules.

> Once the module is imported, it is cached.
