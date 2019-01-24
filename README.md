# WasmFFMpeg.js
wasm media codec based on ffmpeg

# History
2018 Nov. I'm searching a way to decode hevc data in browser. As wiki says https://en.wikipedia.org/wiki/HTML5_video, only safari/android support
hevc, thus using mse api is not capable. When in node it can be done easily by calling native lib (like ffmpeg), so port ffmepg as a wasm module
can do the same thing.

# Process
1. 
