# Lin Clark

ASM.js = precursor to webassembly

WebAssembly allows you to write code that runs in the browser in a few other languages. (e.g. C/C++)
- benefit of more code reuse (e.g. react native)
- potentially runs faster than javascript


Currently no direct access to the DOM. :(

To use:
- Fetch .js, fecth .wasm
- Compiles .wasm to machine code on the fly, off the main thread
- Returns promise, giving instance of module

WebAssembly can import and interface with JavasScript functions.

JavasScript automatic GC has overhead

WebAssembly runtime environment provides helpers (like encoding/decoding)

JavaScript can allocate an ArrayBuffer to pass to WebAssembly to share memory.

Does an ArrayBounds check to make sure WebAssembly only touches the memory its been allocated (for security)