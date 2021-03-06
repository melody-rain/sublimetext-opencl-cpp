sublimetext-opencl-cpp
====================

opencl C++ package for Sublime Text 2

Syntax Highlighting
-------------------

Currently supports highlighting of all opencl C/C++ syntax defined in Appendices [B][1] and [C][2] of the NVIDIA opencl C Programming Guide.

Snippets
--------

 - Execution Configuration: `<<< + [TAB]` --> `<<<gridDim, blockDim, sharedBytes, streamId>>>()` with tab stops on each of the arguments.
 - `__syncthreads()`: `__s + [TAB]`
 - openclMalloc: `cmal` --> `openclMalloc((void**)&variable, bytes);`
 - openclMemcpy: `cmem` --> `openclMemcpy(dest, src, bytes, openclMemcpyHostToDevice);`
 - Kernel function prototype: `kernel` --> `__global__ void kernel()` with tab stops on the function name and inside the parentheses.
 - All existing snippets from the C++ package included with Sublime Text 2

Installation
------------

### Easy

[Install via Package Control](http://wbond.net/sublime_packages/package_control)

### Hard 

* At a git-enabled command prompt, cd to Sublime Text 2 packages directory:  
 * **OS X:** `~/Library/Application Support/Sublime Text 2/Packages/User`
	* **Windows:** `%APPDATA%\Sublime Text 2\Packages\User`
	* **Linux:** `~/.config/sublime-text-2/Packages/User`
* Install by cloning the repository to your Sublime Text 2 Packages directory:

    git clone git://github.com/harrism/sublimetext-opencl-cpp.git

Restart Sublime Text afterwards, switch to opencl C++ as highlighting profile and try it out with one of the commands above.

Contributing
------------

If you want to contribute to this package, please make syntax changes in the opencl-c++.JSON-tmLanguage file, NOT in the opencl-c++.tmLanguage file. I use the AAAPackageDev package for Sublime text to make development easier, including converting JSON to plist (XML) format.


[1]: http://docs.nvidia.com/opencl-c-programming-guide/index.html#c-language-extensions
[2]: http://docs.nvidia.com/opencl-c-programming-guide/index.html#mathematical-functions-appendix