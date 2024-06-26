# zig-exercism

## Overview
I am working through exercises found on https://exercism.org/tracks/zig/exercises. 

## Why?
The name is fun, so I decided to look into it.

## Some resources I stumbled across
- [Zig in 100 Seconds](https://www.youtube.com/watch?v=kxT8-C1vmd4)
  - Transcript:
    ```
    Zig is a high performance system programming language often labeled as a next Generation alternative to C.
    It was created by Andrew Kelly in 2016 and has quickly evolved into one of the most desired new languages in the world.
    Like C it's minimal extremely fast and allows for low-level memory control but instead of managing memory directly in the language with 
    functions like malloc and free, the zig standard library ships allocators to provide a consistent interface for memory management. 

    Zig is not a memory-safe language like Rust or Go but it doesn't have any hidden memory allocations making the code far more explicit and 
    portable because allocators can be easily swapped out in the code to target different architectures like x86, arm, webassembly and bare metal. 

    In addition, Zig has no hidden control flow. If it looks like a function and quacks like a function it's a function there's no operator 
    overloading and it doesn't even have exceptions. If a function can fail it needs to return an explicit error value.

    The language also has a unique comp time keyword that makes it trivial to run code at compile time instead of runtime. No preprocessor or 
    macros are necessary. 

    And finally, Zig can integrate well into a C or C++ codebase and supports cross-compilation out of the box with LLVM although divorce paperwork 
    has been filed to get started. Install Zig then create a new project with the zignet exe command in the main file first to import the standard 
    library then define a main function. Notice how the function returns a type of void with an exclamation point. That exclamation point means 
    that the function might return an error, declare a mutable variable with the VAR keyword followed by a type. Like you wait to represent a 
    single byte then assign and modify its value later or use cons to define an immutable variable that cannot be changed. 

    We can also bundle multiple variables together into a struct then access them on that namespace with DOT notation. Now things start to get more 
    interesting when memory management comes into play. When initializing an array of integers we can allocate it to a slice of memory in the Heap 
    using the built-in page allocator from the standard library. What's so cool about this is that we could swap it out with other allocators to 
    use different memory management strategies. Now when we're done with this memory, we need to set it free. Otherwise, we could have a memory 
    leak. 

    The defer keyword allows us to put that code right next to the allocation itself and will automatically de-initialize the list when it goes out 
    of scope. Now as we operate on the list the try keyword provides explicit error handling. If this line fails it will automatically catch and 
    return the error. You can't just ignore it and that will make your code more reliable. 

    And speaking of reliability Zig has a built-in testing framework use the test keyword to evaluate code outside of the main program then use the 
    zig test command to run it and finally build an executable with the zig build command and choose a build mode to optimize for speed size or 
    safety.
    ``` 
- [Ziglang](https://ziglang.org/)
- [Zig Official Github](https://github.com/ziglang/zig)
  - Several [proposals](https://github.com/ziglang/zig/issues?q=is%3Aopen+is%3Aissue+label%3Aproposal) have interesting discussions.
  - The bounty ["introduce labeled continue syntax inside a switch expression"](https://github.com/ziglang/zig/issues/8220) has a lot of community ideas, differing implementations, and discussions.
  - There are several other labels to explore. 
- [Zig on X (formerly known as Twitter)](https://x.com/ziglang?lang=en)
- [Reddit: What do C programmers think of the Zig language in 2023?](https://www.reddit.com/r/C_Programming/comments/14q5uhy/what_do_c_programmers_think_of_the_zig_language/)
- [Considering learning Zig but wondering about the long-term trajectory of the project](https://www.reddit.com/r/Zig/comments/1cmzhgz/considering_learning_zig_but_wondering_about_the/)
- [FreeBSD: ZIG programming language.](https://forums.freebsd.org/threads/zig-programming-language.88728/)
- [Zig subreddit](https://www.reddit.com/r/Zig)

## Calling C functions in Zig 
-  See the overview of [integration with C libraries without ffibindings](https://ziglang.org/learn/overview/#integration-with-c-libraries-without-ffibindings) for using the built-in [#cImport](https://ziglang.org/documentation/master/#cImport).


## TODO: Add podcasts and meetups known to be informative and fun!
