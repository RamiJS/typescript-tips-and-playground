  # What's Typescript?
  it's a language that is built on top of JavaScript.

  ## Benefits of Typescript?
  - Static typing 
  - Code completion
  - Refactoring
  - Shorthand notations

  ## Drawbacks of Typescript ?
  - Compilation Time (it will be converted to Javascript first)

  ## Types of Typescript ?
  - any
  - unknown
  - never
  - tuples : used for fixed length array of different types of data
  - enums : used for fixed constant values

  ## How do we compile a Typescript file ?
  We use tsc filename.any

  ## How do we configure Typescript ?
  We use tsc --init to create a config file

  How do we debug Typescript files ?
  In vscode, we could click on the debugging option to create a launch.json file
  and then click on the line we want to debug so the compilor knows which line
  needs to be debugged.

  ## enum Best practices ?
  We could use const before defining the enum to make the compiler generate more optimized code.
