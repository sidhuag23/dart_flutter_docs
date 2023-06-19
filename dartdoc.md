
<h2> Dart (programming language) </h2>

Dart designed by google team 
Used for general purpose eg:- web/mobile app servers desktop app etc 

- object oriented class-based , garbage-collected c style syntax , null safe 
- type safe with dynamic type option
- asynchoronous and isolated concurrency 
-  It can compile to either machine code, JavaScript, or WebAssembly. It supports interfaces, mixins, abstract classes, reified generics and type inference

The Dart software development kit (SDK) ships with a standalone Dart runtime. This allows Dart code to run in a command-line interface environment. The SDK includes tools to compile and package Dart apps Dart ships with a complete standard library allowing users to write fully working system apps like custom web servers.

<h4>Dart Deployment Methods </h4>

- javascript (web)
- webassembly (web)
- self contained executable
- ahead of time 
- just-in-time (requires dart VM)
- portable module  (requires dart VM)


<h4>Ahead-of-time module</h4>
When compiled ahead of time, Dart code produces portable, performant, and platform-specific modules. It includes all dependent libraries and packages the app needs plus a small Dart runtime. This increases its compilation time. The compiler outputs an app specific to the architecture on which it was compiled

<h4>Just-in-time module</h4>
When compiled just in time, Dart code produces performant modules that compile fast. This module needs the Dart VM included with the SDK to run. The compiler loads all parsed classes and compiled code into memory the first time the app runs. This speeds up any subsequent run of the app. The compiler outputs an app specific to the architecture on which it was compiled.

<h4>ConCurrency</h4>
To achieve concurrency, Dart uses isolated, independent workers that do not share memory, but use message passing
Every Dart program uses at least one isolate, which is the main isolate. Since Dart 2, the Dart web platform no longer supports isolates, and suggests developers use Web Workers instead

<h4>Data storage </h4>
Snapshot files, a core part of the Dart VM, store objects and other runtime data.

- <h4>Script snapshots</h4>
    Dart programs can be compiled into snapshot files containing all of the program code and dependencies preparsed and ready to execute, allowing fast startups.

- <h4>Full snapshots</h4>
    The Dart core libraries can be compiled into a snapshot file that allows fast loading of the libraries. Most standard distributions of the main Dart VM have a prebuilt snapshot for the core libraries that is loaded at runtime.
- <h4>Object snapshots</h4>
    Dart uses snapshots to serialize messages that it passes between isolates. As a very asynchronous language, Dart uses isolates for concurrency. An object generates a snapshot, transfers it to another isolate, then the isolate deserializes it.