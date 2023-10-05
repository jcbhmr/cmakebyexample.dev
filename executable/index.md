# Build an executable

Instead of running `cc main.c -o myapp`, the "hello world" for a CMake project
is a bit more involved. You need to create an additional `CMakeLists.txt` file
that tells CMake what to do.

We can use the `add_executable()` function to define a `myapp` target that CMake
knows how to build. With it defined, we can run `cmake` and it will compile and
generate the `myapp` target for us based on the `main.c` file that we gave to
the `add_executable()` function.

<<< ./CMakeLists.txt{cmake}

<<< ./main.c

```sh
cmake -B build
cmake --build build
./build/myapp
```



## What is a <dfn id="target">target</dfn>?

> Probably the most important item is targets. Targets represent executables,
> libraries, and utilities built by CMake. Every `add_library`,
> `add_executable`, and `add_custom_target` command creates a target. For
> example, the following command will create a target named “foo” that is a
> static library, with `foo1.c` and `foo2.c` as source files.
>
> ```cmake
> add_library(foo STATIC foo1.c foo2.c)
> ```

<!-- prettier-ignore -->
&mdash; [Key Concepts | CMake](https://cmake.org/cmake/help/book/mastering-cmake/chapter/Key%20Concepts.html#:~:text=Targets%20represent%20executables%2C%20libraries%2C%20and,c%20and%20foo2.)