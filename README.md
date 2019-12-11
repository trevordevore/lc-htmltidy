# Tidy LiveCode Builder Wrapper

This repository contains LiveCode Builder code for wrapping libtidy, the library version of HTML Tidy. HTML Tiday tidies HTML and XML and you can learn more about it on [the official website](http://www.html-tidy.org). There is a good [introduction for developers page](http://www.html-tidy.org/developer/) as well.

The repository also contains the libtidy libraries for macOS and Windows.



## Building 

Instructions for building libtidy can be found here:

https://github.com/htacg/tidy-html5/blob/next/README/BUILD.md#build-the-tidy-library-and-command-line-tool

### Building on Windows

On Windows you need to make some changes to the CMakeLists.txt file so that the DLL is created using the `__cdecl` calling convention. LiveCode Builder seems to require this in the DLL. Attempting to suffix bindings with `!stdcall` with the win32 tidy.dll binaries made available for download would fail to bind in LiveCode 9.0.5. 

You will find the changes that you need to make here:

https://github.com/htacg/tidy-html5/issues/560#issuecomment-302749926
