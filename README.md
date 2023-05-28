# System Programming Roadmap

A roadmap to teach myself compiler dev, malware reverse engineering and kernel dev fundamentals. To be noted they are only for the fundamental knowledge and doesn't make you a master of any. I will pick one or more of the below mentioned fields for later research in some specific topics. [Low Level Programming University](https://github.com/gurugio/lowlevelprogramming-university) also has a good list of resources to follow but this is my personal roadmap.

Topics to study here may or may not be in order and can be studied according to your preference, gievn that prerequisites are getting fulfilled for each one of them.

## Prerequisites

I'm already assuming that you have basic understanding of computer architecture and experience with atleast one system programming language, some basics of how assembly works and familiar using any POSIX system. A good detailed look of how computers work at the electronics level can be found in the book [Introduction to Digital Electronics](https://agner.org/digital/digital_electronics_agner_fog.pdf) by Agner Fog.

### System Programming Languages
Learn any two of the given languages, make some basic projects to get yourself familiar with it, solve some programming exercises.
- [C](https://beej.us/guide/bgc/)
- [Rust](https://doc.rust-lang.org/stable/book/)
- [Learn C++](https://www.learncpp.com/), [C++ reference](https://en.cppreference.com/w/)
- [C++ (video)](https://www.youtube.com/playlist?list=PLlrATfBNZ98dudnM48yfGUldqGD0S4FFb)

### Learn some Computer Architecture

Learn Arm and RISCV based computer architecture to build an efficient and optimized approach towards solving the problems at hardware level 

- [David A. Patterson, John L. Hennessy "Computer Architecture: A Quantitative Approach"](http://acs.pub.ro/~cpop/SMPA/Computer%20Architecture%20A%20Quantitative%20Approach%20(5th%20edition).pdf)
- [David A. Patterson, John L. Hennessy "Computer Organization and Design ARM Edition"](http://home.ustc.edu.cn/~louwenqi/reference_books_tools/Computer%20Organization%20and%20Design%20ARM%20edition.pdf)
- [David A. Patterson, John L. Hennessy "Computer Organization and Design RISC-V Edition"](https://www.cs.sfu.ca/~ashriram/Courses/CS295/assets/books/HandP_RISCV.pdf)
- [John Paul Shen, Mikko H. Lipasti "Modern Processor Design: Fundamentals of Superscalar Processors"](https://github.com/savitham1/books/raw/master/Modern%20Processor%20Design%20-%20Fundamentals%20of%20Superscalar%20Processors.pdf)
- [CMU Computer Architecture by CMU Youtube](https://www.youtube.com/channel/UCnoYy1k6I5gLIxhlNiStrdQ) 



### Learn some x86
Prerequisites: Learn about [Digital Logic](https://agner.org/digital/digital_electronics_agner_fog.pdf)

If you are not familiar with assembly yet, I would recommend to check out some tutorials like-
- [x86 quickstart[MASM]](https://www.cs.virginia.edu/~evans/cs216/guides/x86.html)
- [x86 quickstart [NASM]](https://cs.lmu.edu/~ray/notes/nasmtutorial/)
- [Another x86 quickstart[NASM]](https://asmtutor.com/)
- [Introduction to x86 assembly language by Davy on youtube](https://www.youtube.com/playlist?list=PLmxT2pVYo5LB5EzTPZGfFN0c2GDiSXgQe)
- [OMU x86_64 lessons](https://omu.rce.so/lessons/asm-x86-64/)
- https://asmtutor.com/
- [x86 Asm](https://en.wikibooks.org/wiki/X86_Assembly)
- [The Art Of Asm](https://www.plantation-productions.com/Webster/www.artofasm.com/Linux/HTML/AoATOC.html)
- Even Manuals are great sources of learning.The manuals for processor can easily be found using a Google search ("Intel Manuals," "ARM manuals)
- [Compiler Explorer](https://godbolt.org/): Making C programs and reading the disassembly always helps to match patterns.
- [Article by 0x41 reversing for dummies](https://0x41.cf/reversing/2021/07/21/reversing-x86-and-c-code-for-beginners.html) to be able to reverse basic crackmes.

After this I would recommend to solve easy crackmes for exercise. [crackmes.one](https://crackmes.one) and tryhackme is a good place to find some of the easy ones. Hard ones still require some pwning knowledge which I'm gona discuss in the exploitation section.

### Compilers

Prerequisites include experience creating projects in a system programming language and deep understanding of memory and CPU.

- Read the [Dragon Book](https://en.wikipedia.org/wiki/Compilers:_Principles,_Techniques,_and_Tools).
- [Crafting Interpreters](https://craftinginterpreters.com/) is a good one for beginners.
- [Language Implementation Patterns](https://pragprog.com/titles/tpdsl/language-implementation-patterns/) provides some good insights on workings of compilers.
- [Stanford Notes CS143](https://web.stanford.edu/class/archive/cs/cs143/cs143.1128) Good assignments and notes related to compiler design.
- [CMU slides and Projects](https://www.cs.cmu.edu/~janh/courses/411/16/schedule.html)
- [Awesome Compilers](https://github.com/aalhour/awesome-compilers)
- [Make a Language in Rust](https://arzg.github.io/lang/)
- [Rust Parsing Basics](https://domenicquirl.github.io/blog/parsing-basics/)
- Make a tree walk interpreted programming language.
- Also try to implement a bytecode engine for your interpreter, try out some optimizations and GC.
- You can also emulate machines like [Chip8](https://www.cs.columbia.edu/~sedwards/classes/2016/4840-spring/designs/Chip8.pdf) or [Nes](https://www.nesdev.org/wiki/Nesdev_Wiki).
  - Emulation requires knowledge of [VM internals](#vm-internals) and graphics programming.
  - You can use SDL as an IO/graphics/sound engine.
- Try to make a compiled programming language targetting one architecture.
- Learn about the [LLVM toolchain](https://llvm.org/docs/)
- [LLVM tutorial in Rust](https://github.com/jauhien/iron-kaleidoscope)
- Try to follow the llvm tutorial to make your first programmging language using llvm backend.
- Try to make a Just In Time Compiler around the bytecode engine, detect hot regions and JIT them.
- My [discord server](https://discord.gg/RrDnEj6r9k) lang-dev section

### Exploitation
Prerequisites include experience with [assembly](#learn-some-x86).
- [pwn.college](https://pwn.college) is the best learning resource I got so far for exploitation. From assembly to kernel exploitation, it covers it all.
- [Introduction to exploit development](https://samsclass.info/127/ED_2020.shtml)
- [Nightmare](https://guyinatuxedo.github.io/index.html): Intro to binary exploitation based around CTFs.
- [CS6265: Reverse Engineering and Binary Exploitation Lab](https://tc.gts3.org/cs6265/2021/_static/tut.pdf)
- [OMU exploitation labs](https://omu.rce.so/gcc-2022/)
- [LiveOverflow's binexp series on youtube](https://www.youtube.com/playlist?list=PLhixgUqwRTjxglIswKp9mpkfPNfHkzyeN)
- [Tutorial by 0xinfection](https://0xinfection.github.io/reversing/)
- [Exploit dev on the infosec reference](https://github.com/rmusser01/Infosec_Reference/blob/master/Draft/Exploit_Dev.md)
- [ROP Emporium](https://ropemporium.com/index.html)
- Windows Stuff
  - [Windows x64 reversing](https://github.com/0xZ0F/Z0FCourse_ReverseEngineering)
  - [Win32 API programming](https://riptutorial.com/Download/win32-api.pdf)
  - [Windows exploit dev](https://github.com/FULLSHADE/WindowsExploitationResources)
- After learning about some exploitation, you can solve CTFs now. Some of them include:
  -  [pwnable.kr](https://pwnable.kr)
  -  [Exploit Education VMs](https://exploit.education/)
  -  [Overthewire wargames covering exploitation](https://overthewire.org/wargames)
  -  HackTheBox challenges based on binary exploitation

### Browser Hacking
Prerequisites include high level knowlegde of [VM internals](#vm-internals), and solid understanding and experience with [Compiler Engineering](#compilers----6-9-months)
- Development
  - [Create a basic html dom parser Rust](https://www.youtube.com/watch?v=brhuVn91EdY)
  - [Toy browser engine](https://limpet.net/mbrubeck/2014/08/08/toy-layout-engine-1.html), [Browser engine from scratch](https://zerox-dg.github.io/blog/2020/05/29/Browser-from-Scratch-Introduction/)
  - [JavaScript bytecode VM Andreas Kling](https://www.youtube.com/playlist?list=PLMOpZvQB55beChggmvk-sUm8X_vSezpqL)
  - [Browser Parsing & JS AST Anderas Kling](https://www.youtube.com/playlist?list=PLMOpZvQB55be0Nfytz9q2KC_drvoKtkpS)
  - [Inside look at modern browser](https://developers.google.com/web/updates/2018/09/inside-browser-part1)
  - Blogs to follow: [V8](https://v8.dev/blog), [MozHacks](https://hacks.mozilla.org/), [Webkit](https://webkit.org/blog/)
  - Docs: [Firefox](https://firefox-source-docs.mozilla.org/index.html), [Chromium](https://chromium.googlesource.com/chromium/src/+/master/docs/README.md), [Webkit Wiki](https://chromium.googlesource.com/chromium/src/+/master/docs/README.md)
  - [Compiler Compiler: A Twitch series about working on a JavaScript engine](https://hacks.mozilla.org/2020/06/compiler-compiler-working-on-a-javascript-engine/)
  - Graphics: Choose a 2d graphics lib for your language or platform.
    You can surely use [OpenGL](https://learnopengl.com) or Vulkan?!? to render your innocent CSS but trust me it is not worth it.
    - [Skia](https://skia.org/) is a good one for linux and android (chrome uses it on android)
    - [Direct2D](https://learn.microsoft.com/en-us/windows/win32/direct2d/direct2d-portal) yeah windows only.
    - [Cairo](https://www.cairographics.org/) and [Blend2D](https://blend2d.com) These are cross platform, worth looking into.
  - [High performance gc for V8](https://v8.dev/blog/high-performance-cpp-gc)
  - [Adventures in JIT compilation](https://eli.thegreenplace.net/2017/adventures-in-jit-compilation-part-1-an-interpreter/)
  - [Speculation in JavaScriptCore](https://webkit.org/blog/10308/speculation-in-javascriptcore/)
  - Network Programming [Rust Networking](https://www.rust-lang.org/what/networking), [Rust std::net](https://doc.rust-lang.org/std/net/index.html), [C](https://beej.us/guide/bgnet/)
  - After learning about parsing, rendering and JIT, you can now make your own browser with basic APIs and minimal features, following the [whatwg standards](https://whatwg.org/)
- Exploitation: A great way to understand about how a browser works is to try to hack it: (prerequisites include solid binary exploitation skills)
  - [Browser Exploition series by LiveOverflow](https://www.youtube.com/playlist?list=PLhixgUqwRTjwufDsT1ntgOY9yjZgg5H_t) | [Written](https://liveoverflow.com/topic/browser-exploitation/)
  - [Web Assembly Hacking talk Black Hat](https://www.youtube.com/watch?v=DFPD9yI-C70)
  - [Browser pwn on github](https://github.com/m1ghtym0/browser-pwn)
  - [Web Browser Exploitation- University of Florida](https://www.youtube.com/watch?v=-bfO-b5gzHc)
  - Go through writups of CVEs or CTF challenges based around browsers or runtime envs.

### Malware
Prerequisites includes high level understanding of windows and solid reverse engineering skills.
- [Practical Malware Analysis](https://www.amazon.in/Practical-Malware-Analysis-Hands-Dissecting/dp/1593272901)
- [Malware analysis bootcamp by hackersploit](https://www.youtube.com/playlist?list=PLBf0hzazHTGMSlOI2HZGc08ePwut6A2Io)
- [CS5138 Malware Analysis, UC](https://class.malware.re/)
- After learning basics of malware reversing and behaviour, you can now move to reversing some real samples of those.
- [Labs by Malware Unicorn](https://malwareunicorn.org/#/workshops)
- [VX Underground - The largest collection of malware source code, samples, and papers on the internet.](https://www.vx-underground.org/)
- [Malware section from the infosec reference](https://github.com/rmusser01/Infosec_Reference/blob/master/Draft/Malware.md)

### OS Fundamentals
I'm not quite sure that I want to get into kernel development (yet) but the concepts seem cool and its a good idea for a vacation project or assignments for my OS classes in university. Make sure to read the [requirements](https://wiki.osdev.org/Required_Knowledge) before getting started. 
- [OS Dev Wiki](https://wiki.osdev.org) is the goto place if you want to learn about OS. It's well documented and also helps eyes to bleed.
- [Linux Kernel Labs](https://linux-kernel-labs.github.io/refs/heads/master/)
- [Tutorials Section from awesome OS on github](https://github.com/jubalh/awesome-os#tutorials)
- [Broken Thorn's Tutorial](http://www.brokenthorn.com/Resources/)
- [OS in 3 pieces](https://pages.cs.wisc.edu/~remzi/OSTEP/)
- [Little OS Book](https://littleosbook.github.io/)
- [Blog OS: Writing an OS in rust](https://os.phil-opp.com/)
- [Bootlin Slides and Labs](https://bootlin.com/docs/)
- [539kernel: A Journey in Creating an OS Kernel](https://539kernel.com/book/)
- Stuff to work on:
  - [Haiku](https://www.haiku-os.org/)
  - [React OS](https://reactos.org/architecture/)
  - [The Eudyptula Challenge](http://www.eudyptula-challenge.org/)
  - [Redox](https://www.redox-os.org/)
  - [More rust projects](https://wiki.osdev.org/Rust)
- [Awesome OS on github](https://github.com/jubalh/awesome-os)
- [My discord server's OS dev channel](https://discord.gg/mAKetvg2eX) to get some more resources and books.

### VM internals
Lists of VM internals to study while making progress in compiler engineering and Browser development:
- [How to build a virtual machine](https://www.youtube.com/watch?v=OjaAToVkoTw)
- [JS internals](https://codeburst.io/node-js-v8-internals-an-illustrative-primer-83766e983bf6), [V8's bytecode](https://medium.com/dailyjs/understanding-v8s-bytecode-317d46c94775)
- [Dart VM architecture](https://mrale.ph/dartvm/)
- [JVM structure main](https://docs.oracle.com/javase/specs/jvms/se14/html/jvms-2.html), [JVM internals I](https://blog.jamesdbloom.com/JVMInternals.html), [JVM internals Beginners](https://www.freecodecamp.org/news/jvm-tutorial-java-virtual-machine-architecture-explained-for-beginners/)

### Collective Courses
Collection of resources which includes 2 or more of the topics discussed above:
- [Nand To Tetris](https://www.nand2tetris.org) A course to teach you about how to build a computer, OS and a compiler form stratch.
- [Dive Into Systems](https://diveintosystems.org/) A really good book to introduce you with systems programming.
