# faust-pd
The FAUST compiler embedded in a Pd external

## Dependencies
- [faust](https://github.com/grame-cncm/faust.git)
- [pure-data](https://github.com/pure-data/pure-data.git)
- [pd.build](https://github.com/pierreguillot/pd.build.git)

## Compilation

- macos
```
- brew install pkg-config
#- port install llvm-5.0 +universal
- git submodule update --init --recursive
- mkdir faust/build/personal && cd faust/build/personal
- cmake .. -DINCLUDE_STATIC=on -DINCLUDE_OSC=off -DINCLUDE_HTTP=off -DUNIVERSAL=on -C../backends/backends.cmake
- make
- mkdir ../../../build && cd ../../../build
- cmake .. -GXcode "-DCMAKE_OSX_ARCHITECTURES=i386;x86_64"
```
- linux
