
# Protothreads库

    Protothreads 是一种针对 C 语言封装后的轻量级的协程（宏）函数库，为 C 语言模拟了一种无堆栈的轻量线程环境，能够实现模拟线
    程的条件阻塞、信号量操作等操作系统中特有的机制，从而使程序实现多线程操作。

    每个 Protothreads 线程仅增加 10 行代码和 2 字节RAM的额外硬件资源消耗。对于资源紧缺而不能移植嵌入式操作系
    统的嵌入式系统，使用Protothreads 能够方便直观地设计多任务程序，能够实现用线性程序结构处理事件驱动型程序和
    状态机程序，简化了该类程序的设计。
    
    Protothread是专为资源有限的系统设计的一种耗费资源特别少并且不使用堆栈的线程模型，其特点是：  
    ◆ 以纯C语言实现，无硬件依赖性；  
    ◆ 极少的资源需求，每个Protothread仅需要2个额外的字节；  
    ◆ 可以用于有操作系统或无操作系统的场合；  
    ◆ 支持阻塞操作且没有栈的切换。


Protothreads are extremely lightweight stackless threads designed for
severely memory constrained systems such as small embedded systems or
sensor network nodes. Protothreads can be used with or without an
underlying operating system.

Protothreads provides a blocking context on top of an event-driven
system, without the overhead of per-thread stacks. The purpose of
protothreads is to implement sequential flow of control without
complex state machines or full multi-threading.

Main features:

    * No machine specific code - the protothreads library is pure C
    * Does not use error-prone functions such as longjmp()
    * Very small RAM overhead - only two bytes per protothread
    * Can be used with or without an OS
    * Provides blocking wait without full multi-threading or
      stack-switching
    * Freely available under a BSD-like open source license    

Example applications:

    * Memory constrained systems
    * Event-driven protocol stacks
    * Small embedded systems
    * Sensor network nodes

The protothreads library is released under an open source BSD-style
license that allows for both non-commercial and commercial usage. The
only requirement is that credit is given.

The protothreads library was written by Adam Dunkels <adam@sics.se>
with support from Oliver Schmidt <ol.sc@web.de>.

More information and new versions can be found at the protothreads
homepage:
		     http://www.sics.se/~adam/pt/

Documentation can be found in the doc/ subdirectory.

Two example programs illustrating the use of protothreads can be found
in this directory:

   example-small.c         A small example showing how to use protothreads
   example-buffer.c        The bounded buffer problem with protothreads
   example-codelock.c	   A code lock with simulated key input

To compile the examples, simply run "make".


Adam Dunkels, 3 June 2006
