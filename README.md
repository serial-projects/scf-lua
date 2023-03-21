# What is SCF?
SCF means _Sectionized Configuration File_ it is a simple configuration language that organizes into
sections values. This is the LUA API for it.

# Why?
SCF is planned to be used in the Solar Engine for maps, saves, user configuration and etc. SCF
was created for simplicity in order to be lightweight for LOVE2D or Lua in common.

# Features
- It supports lists!
- Simple syntax, just three keywords: _section_, _end-section_ and _define_!
- Everything must be inside a section, So your data is always organized.

# Demo
_some_file.conf_:
``` 
section main
  define my_var, 10
end-section
``` 

_read.lua_:
```lua
local scf = require("scf")
tree = scf.LoadFile("some_file.conf")
local my_value = tree["main"]["my_var"]
...
```
