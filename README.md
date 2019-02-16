# FreeArc

### **GENERAL GUIDELINES:**  
  
1) The backend part of the program (CLI) must compile with GCC or clang. Ideally, a simple `./configure && make` or `cmake . && make` should suffice. Even when a developer makes use of another toolchain or IDE of their choosing, the code on this repository must adhere to this requirement.  
2) The backend must be portable, able to compile under Linux, Windows and OSx operating systems. That means no dependencies exclusive to any platform, and preferably only standard C++ code. This item and the previous one will allow for the community to easily participate in testing and bug-hunting.
3) When possible at all, all new libraries of recompression (mp2, zstd, lz4, lzx, lzw and others are planned) must have a common API, identical or at least similar to those already in place, to simplify implementation. A developer can use packJPG or some other known library with a clear structure as a template.  
4) No idle time is the goal. The backbone of this project is efficiency, so the implementation must use all resources available by default, especially CPU, unless otherwise stated by the user. That means everything that can be parallelized, should be parallelized.  
  
I realize that some of this things will require some getting used to, and even perhaps modifications to the original code. That's OK, and I will not expect any contributor to make a complete revamp of the program just to comply with this guideline (that will come in due time), but all **new** code **must** adhere to it.
