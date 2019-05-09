# WasmFFMpeg.js
wasm media codec based on ffmpeg

# Background
Nov 2018. I'm searching a way to decode hevc video in browser. As wiki says https://en.wikipedia.org/wiki/HTML5_video, only safari/android support
hevc, thus using mse api is not capable. In node this can be done easily by calling native lib (like ffmpeg), so port ffmepg as a wasm module
may do the same thing.

# Procedure
1. compile ffmpeg with emcripten and got "*.bc" libs. 
2. write a c/c++ wrap code to export suitable interface (c style extern) for js runtime. Compile it with emcripten linking "*.bc" libs and got wasm file (x.wasm/x.js).
3. write js wrap modules (like audioDecoder.js, audioEncoder.js...) for js use.
