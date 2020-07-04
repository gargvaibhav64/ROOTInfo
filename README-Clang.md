CMake Config:
-------------

**Debug**
```
cmake -DLLVM_ENABLE_PROJECTS=clang -G "Visual Studio 16 2019" -A Win32 -Thost=x64 ..\llvm
```

**Release**
```
cmake -DLLVM_ENABLE_PROJECTS=clang -G "Visual Studio 16 2019" -A Win32 -Thost=x64 -DCMAKE_BUILD_TYPE:Release ..\llvm
```

Build Config:
-------------
**Release:**

With Tests:
```
cmake --build . --target check-clang --config Release
```
Without Tests:
```
cmake --build . --target clang --config Release
```

**Debug:**

With Tests:
```
cmake --build . --target check-clang --config Debug
```
Without Tests:
```
cmake --build . --target clang --config Debug
```

Running a Test
--------------

Release:

```
python ./build/release/bin/llvm-lit.py -sv --param build_config=Win32 --param build_mode=Release --param llvm_site_config=./build/test/lit.site.cfg path/to/test/filename
```

Debug:

```
python ./build/debug/bin/llvm-lit.py -sv --param build_config=Win32 --param build_mode=Debug --param llvm_site_config=./build/test/lit.site.cfg path/to/test/filename
```
