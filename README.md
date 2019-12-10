# tidy-html5 LiveCode Builder Wrapper

This repository contains LiveCode Builder code for wrapping libtidy. It also contains the libtidy libraries for macOS and Windows.

## Building 

Instructions for building tidy-html5 can be found here:

https://github.com/htacg/tidy-html5/blob/next/README/BUILD.md#build-the-tidy-library-and-command-line-tool

### Building on Windows

On Windows you need to make some changes to the CMakeLists.txt file so that the DLL is created using the `__cdecl` calling convention. LiveCode Builder seems to require this in the DLL. Attempting to suffix bindings with `!stdcall` with the win32 tidy.dll binaries made available for download would fail to bind in LiveCode 9.0.5. 

You will find the changes that you need to make here:

https://github.com/htacg/tidy-html5/issues/560#issuecomment-302749926
