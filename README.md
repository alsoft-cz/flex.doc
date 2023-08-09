Programming Language Flex®
==========================

_Copyright © 2000–2004 A && L soft_

Flex is a general purpose programming language. Intended range of usage encloses virtually any type of application, starting from systems programming, through embedded systems' development, small single-purpose applications, information systems, distributed systems, mission-critical applications, up to large complex multi-platform applications.

Flex is a classic programming language supporting different programming paradigms, including object-oriented programming, formal development methods, and parallel computing. No experimental or unproven language constructs and features were included into this language.

Programming language Flex is the result of research in programming languages and programming techniques held for more than five years at [A && L soft](https://www.alsoft.cz/). Its features were tested and proven to be practically usable and helpful in real software development of large-scale multi-platform complex applications.

Contacts
--------

To contact the authors, please send email to [flex@alsoft.cz](mailto:alsoft@alsoft.cz)

A && L soft, s.r.o.  
Zahrebska 23  
120 00 Praha 2  
Czech Republic  
Phone: +420 284 862 333

License
-------

### License to the language

If you intend to write a compiler or interpreter of the Flex programming language, please contact A && L soft.

### Licence to the compiler

Non-commercial license is granted for free and entitles its holder to use the Flex compiler for creation of programs for personal use, for creation of programs distributed under the terms of the General Public License, and for educational purposes.

The non-commercial license particularly forbids usage of the Flex compiler for creation of programs, that are intended to be offered for remuneration.

Please contact A && L soft for application of the non-commercial license. A && L soft reserves the right not to grant a non-commercial license without giving any reasons.

Commercial license is necessary for any other use not covered by the non-commercial license. Please contact A && L soft about the details of the commercial license.

Warranty
--------

Flex 4.0.0 compiler is in development and there is no warranty of correctness of its functions. The Flex compiler must not be used in any occasion, where its potential incorrectness of functions could cause any damage. A && L soft is not responsible for any damage caused by incorrect use.

A && L soft reserves the rights to change any function of the program anytime, stop supporting the program, or change license policy of new versions.

Current Status
--------------

The Flex project is currently in progress.

Current version of the language is marked 4.0. A compiler for the previous version of the language (3.0) is in everyday use at A && L soft and is being used for development of the [OfficeLine](https://www.alsoft.cz/)® system.

Two compilers are being developed for the current version of the language. Flex 4.0.0 command-line compiler is intended for the Windows NT a Linux targets on the Intel platform. It implements only a subset of the language and is used for development of the 4.0.1 version, that is already written in Flex.

Available Language Reference Manual doesn't cover all topics yet.

Supported platforms
-------------------

The Flex compiler will be available for following platforms:

*   Windows NT/2000, Windows 9x
*   Linux
*   BSD
*   IBM AS/400

Download
--------

*   [Language Reference Manual](lrm/lrm40.pdf) — preliminary language description in PDF format
*   Flex 4.0.0 command-line compiler (not yet available) — currently available command-line compiler, that implements a subset of the whole language

Design Goals and Fundamental Features
-------------------------------------

### Easy to use programming language with sufficient expressiveness.
Flex is designed to allow different programmers with different programming experience level and preferred programming style (in concern with preferred methods how to solve certain problems) to cooperate on a single project. This enables less-experienced programmers to use only simpler language features and build programs from predefined components, while giving advanced programmers the freedom to use all language features.

Flex is based on the Pascal family of languages and was greatly influenced by the Ada programming language. While it is a feature-rich language that offers approximately the same functionality as Ada, it is still easy to learn and can be taught in more levels of difficulty.

Certain language features that were not straightforwardly usable, or implementable, or led to difficult semantic rules with obscure behavior in non-standard situations, were omitted from the language. All language constructs are designed to be straightforward with clear semantics.

The syntax of the language is constructed to improve readability of the program and support formal description of algorithms and coding style rather than ease of writing. All syntax rules are based on few fundamental principles that lead to syntactically consistent source code.

### Support for all levels of abstraction.
Flex can be used for system level programming as well as for formal description of algorithms on the highest level of abstraction. This is enabled by sufficient support for both data abstraction and precise machine dependent data type specifications.

Various language constructs, which need a strong run-time support system, exist in the language. These constructs are intended to ease software development on a high level of formalization. In Flex, there is no need to manipulate with objects in memory as if they had no type. Unlike in other languages, where various library routines are needed to perform certain actions (e.g. memcpy or memset in C/C++), there is always a language defined construct that is able to do such action without the need of a library routine in a straightforward manner (e.g. assignment of structured variables, aggregates, nil as a universal concept).

Flex covers multitasking, inter-task communication, synchronization, and concurrent processing as native qualities of the language. This enables programmers to use most advanced features of the underlaying operating system and hardware platform in a consistent and natural way.

### Preventing errors, maintenance cost, and reusability.
Today's main goals in software development are reusability and maintenance cost. Flex offers certain mechanisms to reach such goals with low effort.

Lot of errors in current programs arise from careless of developers, misuse of varibles, types and subprograms, and lack of support for advanced features in programming languages. Flex allows the programmer to declare a certain entity in a way, that prevents its accidental misuse in an originally unintended manner. Native support for advanced features like multi-tasking or synchronization gives the programmer the opportunity to concentrate of software engineering instead of solving trivial problems again and again.

Properties of the type system (especially inheritance, encapsulation of data structures and dynamic type information) allow creation of general modules, that can be reused in future projects with low requirements for changes.

Attributes give the programmer the ability to reference certain properties of every entity (like the size in bytes of a type) in a consistent way without the need to declare additional constants or use complex programming rules. Algorithms can be specified without the knowledge of actual values of such attributes leading to better reusability and maintainability of the source code.

### Strong type system.
The type system covers all simple and compound data types as well as special types supporting other features of the language instead of introducing new types of entities.

Strong type checking, both static and dynamic, is a fundamental concept. Flex emphasizes a type as a key entity, that forms a base for formal description of algorithms. Static type checking rules can be constrained by the programmer enabling the programmer to declare special-purpose types with restricted compatibility — this mechanism can virtually disallow compatibility with any other type.

Inheritance is a general concept, that allows the programmer to build type hierarchies of any kind. Inheritance mechanisms are defined for all data types, even simple types, arrays, and pointers. Together with dynamic type checking, inheritance allows run-time processing of polymorphic data with a common ancestor. Dynamic type information (type tags) is also the base concept used in dispatching of virtual methods — any type hierarchy based on any data type can be used for dispatching.

Encapsulation of types enables the programmer to define abstract data types together with related operations, thus leading to better control over a certain data structure, even in situations, where object-oriented programming cannot be used with sufficient effectivity.

Attributes of every type (size of the type, precision of a number, alignment of components etc.) can be either chosen by the compiler to best-fit the target machine, or specified by the programmer. This gives the programmer required control over the generated code and layout of data structures, where appropriate.

### Unification of language constructs.
Great attention has been given to possible unification of apparently disconnected language constructs. This endeavor led to a merger of inter-task communication and exception handling, leading to a powerful mechanism of synchronous and asynchronous messages.

Modules and classes share most of their functionality. Modules can be inherited one from another as well as classes. Virtual methods can be declared both in classes and modules, and were generalized to allow simultaneous dispatching on multiple arguments, not only the class's current instance.

Other example is the inheritance paradigm in the type system.

### Future extensibility.
All language constructs are designed to be simply extensible in the future, when new ideas and programming techniques evolve. This extensibility is based on an open syntax scheme, like standardized way of building declarations of new types of entities, and overall fundamental semantic concepts, like declarative regions, fundamental concepts of the type system and unification of apparently disconnected language constructs (like inter-task communication and exception handling).

### No language defined entities.
Flex contains no built-in features such as predefined types, subprograms, constants or other entities. There is a predefined environment, that is intended to enable quick start-up and easy programming of very small single-purpose applications, but it is fully specified in source code and can be modified and even completely eliminated from a certain project — it is not a compiler-built-in feature.

Similarly there is a standardized container module — module Flex — for the run-time environment support routines. As well as the predefined environment, it is not a compiler-built-in feature, and it is up to the programmer if he uses this run-time system, redefines it, or completely removes (and so effectively disabling certain language features — but it is the purpose of the run-time system to provide support for advance features of the language, like tasking, synchronization, inter-task communication, exception handling etc.).

This enables the programmer to take complete control over the application and disallow any third-party components. This is extremely important in security related and mission-critical applications that need to have certification of all components.
