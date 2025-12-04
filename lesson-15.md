# What is Node.js and why use it for server-side development

**What is Node.js?**
> Node.js is a JavaScript runtime,
> its not a programming language,
> its not a framework.

Node.js is made up of - V8 JavaScript Engine + libuv

**What is a JavaScript runtime?**  
An environment that allows to run JavaScript.

**What is libuv?**  
libuv is a multi-platform C library that provides support
for asynchronous I/O operations based on event loops.

Things that are not part of the "V8 JavaScript Engine" like

- file operations (read/write etc)
- database operations
and so on...
they are handled by "libuv".
