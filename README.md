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

We force the local build of Boost because
instead of downloading prebuilt Boost binary because it is not available for Apple clang on macOS Catalina.
This is apparently because clang, at least on that platform today, does not fully support C++20
yet, which was overlooked by people who provided CGAL for Conan.
