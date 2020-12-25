Basic Usage
===========

~~~
$ mkdir build
$ cd build
$ conan install .. --build=boost --build=cgal --build=mpir --build=m4
$ cmake ..
~~~

Misc
====

We force the build of Boost because
recent Boost binary is not available for Apple clang.
This is apparently because clang on macOS Catalina does not fully support C++20
yet, which was overlooked by people who provided Boost for Conan.
