# WebAssembly by Ben Smith

### What is WebAssembly?
- New text and binary format spec
- Designed to eb fast to load and execute
- Is a alternative to JavaScript
- Compilation target for languages like C, C++, Rust, etc.
- Safe (Can't crash)
- Portable (Running in every browsers)
- Designed by W3C Community Group that includes representatives from
all major browsers

It's a shortcut to your JavaScript engine optimizer.

--

### JavaScript Optimization
- Tiered; hotter code is optimized more
- Gather type information while executing
- Make assumptions based on type information
- Failed assumption => "Deoptimization"

### and what's NOT
- Replacement for JavaScript
- Compilation target for languages that compile to JavaScript
- Programming language (it's a compilation target)

--

### WebAssembly use cases
Long list... including games, image recognition, VPN, Encryption, CAD Apps, etc.
All of them with high CPU frequency requirements.

--

### We can compile C/C++/C++14 to JavaScript with emcc with asm.js
#### ASM.js
- Low level, optimizable subset of JavaScript
- Linear memory accessed via TypeArrays
- Import and exports functions
- Functions have type annotations on expressions, parameters and return values

#### Why not just ASM.JS?
**Pros**:
  - asm.js-aware engines can produce good code
  - *"It's just JavaScript"* = polyfill for free

**Cons**:
  - Parsing can be expensive
  - Validation failure = fallback to JavaScript
  - Hard to extend functionalty
  - No 64-bit integers

### How we can make it better?

  - Compile C using Clang via Emscripten
  - Emscripten generates asm.js
  -
  - Then to Stack Machine

--

### A lot more to mention
- Linear moemory
- Other control flow
- Funcitons calls direct and indirect
- Import/exporting memory and functions tables
- 32 and 64-bits floating point opreations
- "start" functins
- global variables

--

[Source WebAssembly](https://github.com/webassembly/)
