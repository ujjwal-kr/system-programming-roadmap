# System Programming Roadmap

A three year long roadmap to teach myself compiler dev, malware reverse engineering and kernel dev fundamentals. To be noted they are only for the fundamental knowledge and doesn't make you a master of any. I will pick one or more of the below mentioned fields for later research in some specific topics. [Low Level Programming University](https://github.com/gurugio/lowlevelprogramming-university) is also a great resource to follow but this is my personal roadmap.

Topics to study here may or may not be in order and can be studied according to your preference, gievn that prerequisites are getting fulfilled for each one of them.

## Prerequisites

I'm already assuming that you have basic understanding of computer architecture and experience with atleast one system programming language, some basics of how assembly works and familiar using any POSIX system.

### System Programming Languages -- 4 months
Learn any two of the given languages, make some basic projects to get yourself familiar with it, solve some programming exercises.
- [C](https://beej.us/guide/bgc/)
- [Rust](https://doc.rust-lang.org/stable/book/)
- [C++](https://www.learncpp.com/)
- [C++ (video)](https://www.youtube.com/playlist?list=PLlrATfBNZ98dudnM48yfGUldqGD0S4FFb)

### Learn some x86 -- 3 months
If you are not familiar with assembly yet, I would recommend to check out some tutorials like-
- [Introduction to x86 assembly language by Davy on youtube](https://www.youtube.com/playlist?list=PLmxT2pVYo5LB5EzTPZGfFN0c2GDiSXgQe)
- [OMU x86_64 lessons](https://omu.rce.so/lessons/asm-x86-64/)
- [begin.re/](https://www.begin.re/)
- [x86 Asm](https://en.wikibooks.org/wiki/X86_Assembly)
- [The Art Of Asm](https://www.plantation-productions.com/Webster/www.artofasm.com/Linux/HTML/AoATOC.html)
- Even Manuals are great sources of learning.The manuals for processor can easily be found using a Google search ("Intel Manuals," "ARM manuals)
- After being comfortable with the concepts, [x86 instruction listings](https://en.wikipedia.org/wiki/X86_instruction_listings) on wikipedia will always be the goto guide for reference.
- And making C programs and reading the disassembly always helps to match patterns.
- [Article by 0x41 reversing for dummies](https://0x41.cf/reversing/2021/07/21/reversing-x86-and-c-code-for-beginners.html) to be able to reverse basic crackmes.

After this I would recommend to solve easy crackmes for exercise. [crackmes.one](https://crackmes.one) and tryhackme is a good place to find some of the easy ones. Hard ones still require some pwning knowledge which I'm gona discuss in the exploitation section.

### Compilers -- 6-9 months

Prerequisites include experience creating projects in a system programming language and deep understanding of memory and CPU.

- Read the [Dragon Book](https://en.wikipedia.org/wiki/Compilers:_Principles,_Techniques,_and_Tools).
- [Crafting Interpreters](https://craftinginterpreters.com/) is a good one for beginners.
- [Awesome Compilers](https://github.com/aalhour/awesome-compilers)
- [Make a Language in Rust](https://arzg.github.io/lang/)
- [Rust Parsing Basics](https://domenicquirl.github.io/blog/parsing-basics/)
- Make an interpreted programming language.
- Make a source to source compiler (or transpiler).
- Try to make a compiled programming language targetting one architecture.
- Learn about the [LLVM toolchain](https://llvm.org/docs/)
- [LLVM tutorial in Rust](https://github.com/jauhien/iron-kaleidoscope)
- Try to follow the llvm tutorial to make your first programmging language using llvm backend.
- Make a Just In Time Compiler
- Experiment with the toolchain to create custom backends as well.
- My [discord server](https://discord.gg/RrDnEj6r9k) lang-dev section

### Exploitation -- 2-4 months
Prerequisites include experience with [assembly](#learn-some-x86----3-months).
- [pwn.college](https://pwn.college) is the best learning resource I got so far for exploitation. From assembly to kernel exploitation, it covers it all.
- [Introduction to exploit development](https://samsclass.info/127/ED_2020.shtml)
- [OMU exploitation labs](https://omu.rce.so/gcc-2022/)
- [LiveOverflow's binexp series on youtube](https://www.youtube.com/playlist?list=PLhixgUqwRTjxglIswKp9mpkfPNfHkzyeN)
- [Tutorial by 0xinfection](https://0xinfection.github.io/reversing/)
- [Exploit dev on the infosec reference](https://github.com/rmusser01/Infosec_Reference/blob/master/Draft/Exploit_Dev.md)
- [Windows exploit dev](https://github.com/FULLSHADE/WindowsExploitationResources)
- After learning about some exploitation, you can solve CTFs now. Some of them include:
  -  [pwnable.kr](https://pwnable.kr)
  -  [Exploit Education VMs](https://exploit.education/)
  -  [Overthewire wargames covering exploitation](https://overthewire.org/wargames)
  -  HackTheBox challenges based on binary exploitation

### Browser Exploitation and Development -- 6-9 months
Prerequisites include high level knowlegde of [VM internals](#vm-internals), and solid understanding and experience with [Compiler Engineering](#compilers----6-9-months)
- Development
  - [Create a basic html dom parser Rust](https://www.youtube.com/watch?v=brhuVn91EdY)
  - [Toy browser engine](https://limpet.net/mbrubeck/2014/08/08/toy-layout-engine-1.html), [Browser engine from scratch](https://zerox-dg.github.io/blog/2020/05/29/Browser-from-Scratch-Introduction/)
  - [JavaScript bytecode VM Andreas Kling](https://www.youtube.com/playlist?list=PLMOpZvQB55beChggmvk-sUm8X_vSezpqL)
  - [Browser Parsing & JS AST Anderas Kling](https://www.youtube.com/playlist?list=PLMOpZvQB55be0Nfytz9q2KC_drvoKtkpS)
  - [Inside look at modern browser](https://developers.google.com/web/updates/2018/09/inside-browser-part1)
  - [Adventures in JIT compilation](https://eli.thegreenplace.net/2017/adventures-in-jit-compilation-part-1-an-interpreter/)
  - After learning about parsing, rendering and JIT, you can now make your own browser with basic APIs and minimal features, following the [whatwg standards](https://whatwg.org/)
- Exploitation: (learn some binary exploitation and workings of the browser)
  To learn more about the browser, you can learn how to exploit/reverse engineer some.
  - [Browser Exploition series by LiveOverflow](https://www.youtube.com/playlist?list=PLhixgUqwRTjwufDsT1ntgOY9yjZgg5H_t)
  - [Web Assembly Hacking talk Black Hat](https://www.youtube.com/watch?v=DFPD9yI-C70)
  - [Browser pwn on github](https://github.com/m1ghtym0/browser-pwn)
  - [Web Browser Exploitation- University of Florida](https://www.youtube.com/watch?v=-bfO-b5gzHc)

### Malware -- 4-5 months
Prerequisites includes high level understanding of windows and solid reverse engineering skills.
- [Practical Malware Analysis](https://www.amazon.in/Practical-Malware-Analysis-Hands-Dissecting/dp/1593272901)
- [Malware analysis bootcamp by hackersploit](https://www.youtube.com/playlist?list=PLBf0hzazHTGMSlOI2HZGc08ePwut6A2Io)
- [CS5138 Malware Analysis, UC](https://class.malware.re/)
- After learning basics of malware reversing and behaviour, you can now move to reversing some real samples of those.
- [Labs by Malware Unicorn](https://malwareunicorn.org/#/workshops)
- [VX Underground - The largest collection of malware source code, samples, and papers on the internet.](https://www.vx-underground.org/)
- [Malware section from the infosec reference](https://github.com/rmusser01/Infosec_Reference/blob/master/Draft/Malware.md)

### OS Fundamentals 6-10 months
I'm not quite sure that I want to get into kernel development (yet) but the concepts seem cool and its a good idea for a vacation project or assignments for my OS classes in university. Make sure to read the [requirements](https://wiki.osdev.org/Required_Knowledge) before getting started. 
- [OS Dev Wiki](https://wiki.osdev.org) is the goto place if you want to learn about OS. It's well documented and also helps eyes to bleed. 
- [Tutorials Section from awesome OS on github](https://github.com/jubalh/awesome-os#tutorials)
- [Making An OS - youtube](https://www.youtube.com/playlist?list=PLm3B56ql_akNcvH8vvJRYOc7TbYhRs19M)
- [My discord server's OS dev channel](https://discord.gg/mAKetvg2eX) to get some more resources and books.
- [Broken Thorn's Tutorial](http://www.brokenthorn.com/Resources/)
- [Little OS Book](https://littleosbook.github.io/)
- [OS in 3 pieces](https://pages.cs.wisc.edu/~remzi/OSTEP/)

### VM internals
Lists of VM internals to study while making progress in compiler engineering and Browser development.
- [How to build a virtual machine](https://www.youtube.com/watch?v=OjaAToVkoTw)
- [JS internals](https://codeburst.io/node-js-v8-internals-an-illustrative-primer-83766e983bf6), [V8's bytecode](https://medium.com/dailyjs/understanding-v8s-bytecode-317d46c94775)
- [Dart VM architecture](https://mrale.ph/dartvm/)
- [JVM structure main](https://docs.oracle.com/javase/7/docs/), [JVM internals I](https://blog.jamesdbloom.com/JVMInternals.html), [JVM internals II](https://www.freecodecamp.org/news/jvm-tutorial-java-virtual-machine-architecture-explained-for-beginners/)
