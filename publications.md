---
permalink: "/publications/"
layout: page
title: Publications
sidebar_link: true
order: 2
---

<style>

table {
  margin-bottom: 1rem;
  width: 100%;
  font-size: 85%;
  border: 0px solid $border-color;
  border-collapse: collapse;
}

td,
th {
  padding:  1rem .25rem;
  border: 0px solid $border-color;
}

th {
  text-align: left;
}

tbody tr:nth-child(odd) td,
tbody tr:nth-child(odd) th {
  background-color: transparent;
}

paper {
 color: #; 
 font-weight:bold;
}



</style>
#### 2024
<p>
<paper>Live Objects All The Way Down: Removing the Barriers between Applications and Virtual Machines</paper>
<br>
<b>Javier Pimás</b>, Stefan Marr, Diego Garbervetsky
<br>
Submitted to The Art, Science, and Engineering of Programming, 2024, Vol. 8, Issue 2, Article 5. Also presented at the <Programming> 2024 Conference in Lund, Sweden.
<details>
    <summary>Abstract | <a href='https://doi.org/10.22152/programming-journal.org/2024/8/5'>PDF</a>
        </summary>
    <p class='message'>
   Object-oriented languages often use virtual machines (VMs) that provide mechanisms such as just-in-time (JIT) compilation and garbage collection (GC). These VM components are typically implemented in a separate layer, isolating them from the application.

While this approach brings the software engineering benefits of clear separation and decoupling, it introduces barriers for both understanding VM behavior and evolving the VM implementation. For example, the GC and JIT compiler are typically fixed at VM build time, limiting arbitrary adaptation at run time. Furthermore, because of this separation, the implementation of the VM cannot typically be inspected and debugged in the same way as application code, enshrining a distinction in easy-to-work-with application and hard-to-work-with VM code. These characteristics pose a barrier for application developers to understand the engine on top of which their own code runs, and fosters a knowledge gap that prevents application developers to change the VM.

We propose Live Metacircular Runtimes (LMRs) to overcome this problem. LMRs are language runtime systems that seamlessly integrate the VM into the application in live programming environments. Unlike classic metacircular approaches, we propose to completely remove the separation between application and VM. By systematically applying object-oriented design to VM components, we can build live runtime systems that are small and flexible enough, where VM engineers can benefit of live programming features such as short feedback loops, and application developers with fewer VM expertise can benefit of the stronger causal connections between their programs and the VM implementation.

To evaluate our proposal, we implemented Bee/LMR, a live VM for a Smalltalk-derivative environment in 22057 lines of code. We analyze case studies on tuning the garbage collector, avoiding recompilations by the just-in-time compiler, and adding support to optimize code with vector instructions to demonstrate the trade-offs of extending exploratory programming to VM development in the context of an industrial application used in production. Based on the case studies, we illustrate how our approach facilitates the daily development work of a small team of application developers.

Our approach enables VM developers to gain access to live programming tools traditionally reserved for application developers, while application developers can interact with the VM and modify it using the high-level tools they use every day. Both application and VM developers can seamlessly inspect, debug, understand, and modify the different parts of the VM with shorter feedback loops and higher-level tools.
    </p>
</details>
</p>


#### 2022
<p>
<paper>PowerlangJS: A Quick Way to Get Your Smalltalk to the Web?</paper>
<br>
<b>Javier Pimás</b>
<br>
Submitted to the FAST Workshop 2022 on Smalltalk Related Technologies, co-located with the 14th Smalltalks Conference 2022 in Buenos Aires, Argentina
<details>
    <summary>Abstract | <a href='https://openreview.net/pdf?id=DRUVWUDX_z'>PDF</a>
        </summary>
    <p class='message'>
    Powerlang bootstrapper was designed to bring alive Smalltalk systems from specifications stored in source code files. Powerlang includes an evaluator that is able to execute initialization code of the Smalltalk being bootstrapped. Could we use that same evaluator for running that same Smalltalk on the Web? We present our work in progress towards that goal, which involves transpiling the Smalltalk evaluator, written in Smalltalk, to JavaScript, generating a Smalltalk image compatible with that evaluator, and optimizing the evaluator and the Smalltalk code of the image.
    </p>
</details>
</p>

#### 2019
<p>
<paper>Powerlang: a Vehicle for Lively Implementing Programming Languages</paper>
<br>
<b>Javier Pimás</b>, Guido Chari
<br>
Submitted to the 11th International Workshop on Smalltalk Technologies (IWST-19), co-located with ESUG 2019 in Cologne, Germany
<details>
    <summary>Abstract | <a href='/assets/images/2019-IWST-Powerlang.pdf'>PDF</a>
        </summary>
    <p class='message'>
    Developing a programming language from scratch, with a stable and yet efficient runtime environment could be considered a titanic task.
To mitigate this situation, and promote the early emergence of new languages, two main alternatives have been proposed: adopt an established virtual machine or exploit meta-compilation frameworks.
In addition, micro VMs have been proposed as a foundation for developing VMs on top of a thin layer of abstraction similar to the micro kernel concept proposed for operating systems.
Each of these approaches represents a compromise solving the tensions between flexibility, correctness, efficiency, and effort when designing a language runtime.
Accordingly, each approach exposes its benefits while still suffers from limitations.

The Bee development team has been developing a complete Smalltalk system for more than a decade.
During the journey, we implemented several artifacts needed to build a virtual machine: parsers, compilers, assemblers, bootstrapping utilities, (native code) debuggers, remote execution protocols, simulation tools, and garbage collection algorithms, among others.
After weighing all the different paths followed during these years, in this paper we advocate for a novel approach for building language runtimes.
Concretely, we envision Powerlang, a framework that would enable to design, debug, inspect, compile, optimize, and test new programming languages, with a moderate effort and significant versatility.
Powerlang represents a novel point in the design space of this kind of solutions.
Finally, Powerlang is developed using a live environment like Smalltalk.
We also elaborate on why this is an excellent match to host such a framework.
    </p>
</details>
</p>

#### 2018
<p>
<paper>Self-contained development environments</paper>
<br>
Guido Chari, <b>Javier Pimás</b>, Jan Vitek, Olivier Flückiger
<br>
Submitted to the 14th Dynamic Languages Symposium (DLS-18), co-located with SPLASH 2018 in Boston, Massachusetts
<details>
    <summary>Abstract | <a href='http://janvitek.org/pubs/dls18.pdf'>PDF</a>
        </summary>
    <p class='message'>
    Operating systems are traditionally implemented in low-level, performance-oriented programming languages. These languages typically rely on minimal runtime support and provide unfettered access to the underlying hardware. Tradition has benefits: developers control the resources that the operating system manages and few performance bottlenecks cannot be overcome with clever feats of programming. On the other hand, this makes operating systems harder to understand and maintain. Furthermore, those languages have few built-in barriers against bugs. This paper is an experiment in side-stepping operating systems, and pushing functionality into the runtime of high-level programming languages. The question we try to answer is how much support is needed to run an application written in, say, Smalltalk or Python on bare metal, that is, with no underlying operating system. We present a framework named NopSys that allows this, and we validate it with the implementation of CogNos a Smalltalk virtual machine running on bare x86 hardware. Experimental results suggest that this approach is promising.
    </p>
</details>
</p>

<p>
<paper>Migrating Bee Smalltalk to a Different Instruction Set Architecture</paper>
<br>
<b>Javier Pimás</b>
<br>
Submitted to the 10th International Workshop on Smalltalk Technologies (IWST-18), co-located with ESUG 2018 in Cagliary, Italy
<details>
    <summary>Abstract | <a href='/assets/images/2018-IWST-MigratingBee.pdf'>PDF</a>
        </summary>
    <p class='message'>
    We report our experience in porting Bee Smalltalk Dynamic Metacircular Runtime (DMR) from the 32-bit Intel-x86 instruction set architecture (ISA) to AMD64,
as a first step to move forward towards a multi-platform Bee Smalltalk.

This port required subtle changes in most areas present in typical Virtual Machines (VMs): low-level object shape, JIT-compiler, garbage collector, primitives and FFI.
We present a comprehensive analysis of the migration difficulties, and the key implementation and design decisions taken during our work in the context of Bee, which is implemented in terms of a Smalltalk DMR, in contrast to VMs written in languages like C/C++.
Additionally, we depict the image-level mechanisms we deviced in order to support the transition between 32 and 64-bit images, which can also be applied to traditional-VM based Smalltalks.
    </p>
</details>
</p>

#### 2017
<p>
<paper>Garbage Collection and Efficiency in Dynamic Metacircular Runtimes: an Experience Report</paper>
<br>
<b>Javier Pimás</b>, Javier Burroni, Jean Bauptiste Arnaud, Stefan Marr
<br>
Submitted to the 13th Dynamic Languages Symposium (DLS-17), co-located with SPLASH 2017 in Vancouver, Canada
<details>
    <summary>Abstract | <a href='https://www.ssw.uni-linz.ac.at/Research/Papers/Marr/dls17-pimas-et-al-garbage-collection-and-efficiency-in-dynamic-metacircular-runtimes.pdf'>PDF</a>
        </summary>
    <p class='message'>
    In dynamic object-oriented languages, low-level mechanisms such as just-in-time compilation, object allocation, garbage collection (GC) and method dispatch are often handled by virtual machines (VMs). VMs are typically implemented using static languages, allowing only few changes at run time. In such systems, the VM is not part of the language and interfaces to memory management or method dispatch are fixed, not allowing for arbitrary adaptation. Furthermore, the implementation can typically not be inspected or debugged with standard tools used to work on application code. This paper reports on our experience building Bee, a dynamic Smalltalk runtime, written in Smalltalk. Bee is a Dynamic Metacircular Runtime (DMR) and seamlessly integrates the VM into the application and thereby overcomes many restrictions of classic VMs, for instance by allowing arbitrary code modifications of the VM at run time. Furthermore, the approach enables developers to use their standard tools for application code also for the VM, allowing them to inspect, debug, understand, and modify a DMR seamlessly. We detail our experience of implementing GC, compilation, and optimizations in a DMR. We discuss examples where we found that DMRs can improve understanding of the system, provide tighter control of the software stack, and facilitate research. We also show that the Bee DMR matches and surpass the performance of a widely used Smalltalk VM.
    </p>
</details>
</p>

<p>
<paper>Metaphysics: Towards a Robust Framework for Remotely Working with Potentially Broken Objects and Runtimes</paper>
<br>
<b>Javier Pimás</b>, Stefan Marr
<br>
Submitted to the Workshop on Meta-Programming Techniques and Reflection, co-located with SPLASH 2017 in Vancouver, Canada
<details>
    <summary>Abstract | <a href='/assets/images/2017-Meta-Metaphysics.pdf'>PDF</a>
        </summary>
    <p class='message'>
    Dynamic Metacircular Runtimes (DMRs) enable a new way of developing Virtual Machines (VMs). Instead of writing VMs by manipulating files, DMR programmers work on a running system by modifying its methods, classes and, more generally, objects. This development workflow has both advantages and disadvantages. While it allows us to more easily understand the behavior of the system by showing it alive, it is also problematic, because the system relies on itself to be constantly working.

In this work, we experiment with adapting such live programming tools to make them safer for the development of core DMR components. Furthermore, we make them robust so that they can work on crashed DMRs or systems not that are currently fully working. This paper describes Metaphysics, a framework that combines mirrors and proxies to reify different message execution semantics, allowing execution of code by mixing behavior of a remote, possibly broken system with a local fully-working one. With Metaphysics we were able to create native code debugging and profiling tools. These new tools make full use of the metacircularity of our Bee DMR and enable a dynamic, fast-paced edit-test workflow like the one we are used to when developing application-level code, instead of the classic edit-compile-get-coffee-test cycle used for state-of-the-art VMs.
    </p>
</details>
</p>

#### 2014
<p>
<paper>Design and implementation of Bee Smalltalk Runtime</paper>
<br>
<b>Javier Pimás</b>, Javier Burroni, Gerardo Richarte
<br>
Submitted to the 6th International Workshop on Smalltalk Technologies (IWST-14), co-located with ESUG 2014 in Cambridge, England
<details>
    <summary>Abstract | <a href='http://esug.org/data/ESUG2014/IWST/Papers/iwst2014_Design%20and%20implementation%20of%20Bee%20Smalltalk%20Runtime.pdf'>PDF</a>
        </summary>
    <p class='message'>
    Bee is a Smalltalk dialect. Its runtime is exceptional in that it is completely written in Smalltalk. Bee includes a minimal kernel with on-demand loaded libraries, a JIT compiler, an FFI interface, an optimizing SSA-based compiler, a garbage collector, and native threading support among other things. Despite being written in Smalltalk, Bee achieves promising performance levels.
    </p>
</details>
</p>

#### 2012
<p>
<paper>Memory snapshotting of self-modifying systems</paper>
<br>
Guido Chari, <b>Javier Pimás</b>, Gerardo Richarte, Gabriela Arévalo, Stéphane Ducasse
<br>
Submitted to the Smalltalk Directions Symposium, co-located with STIC 2012 in Biloxi, Mississippi
<details>
    <summary>Abstract | <a href='/assets/images/SqueakNOS-sigplan.pdf'>PDF</a>
        </summary>
    <p class='message'>
    Self describing (pure reflective) and meta-circular systems have many advantages, but in some low-level operations, such as memory snapshotting, self-modification brings some problems.
The problem of atomic-copy deals with object immutability and virtual machine state consistency that should be enforced when the same system is used to save itself. 
Specifically in Smalltalk environments, generating a complete snapshot of the Smalltalk object memory, using the same system that has to be persisted is a challenge since the system changes itself during the saving process.
In the context of our work, the SqueakNOS environment (an OS written in Smalltalk) lacks persistency features because of the complexity of the atomic-copy problem.
In this paper we present a page-based memory manager which can handle native page faults at language level and then a copy-on-write strategy on top of it. 
Except low-level hardware features, all the implementation is written at Smalltalk abstraction level.
Additionally to the advantage of dealing with very low-level operations using high-level languages, we introduce a mechanism that reduces memory usage up to 95%, compared to other approaches on SqueakNOS.
    </p>
</details>
</p>

<p>
<paper>GPU Computing and CUDA technology used to accelerate a mesh generator application</paper>
<br>
Adriana Gaudiani, Santiago Montiel, <b>Javier Pimás</b>
<br>
Proceedings of the International Conference on Parallel and Distributed Processing Techniques and Applications (PDPTA)
<details>
    <summary>Abstract | <a href='http://world-comp.org/p2012/PDP3610.pdf'>PDF</a>
        </summary>
    <p class='message'>
    The potential of GPU computing used in general purpose parallel programming has been amply shown. These massively parallel many-core multiprocessors are available to any users in every PCs, notebook, game console or workstation. In this work, we present the parallel version of a mesh-generating algorithm and its execution time reduction by using off-the-shelf GPU technology. We use commodities GPUs as a useful CPU co-processor to improve this kind of applications, characterized by a high level of data parallelism. Compared to the sequential algorithm, our techniques achieve 6X overall performance for GPU-CPU implementation; furthermore we achieve 50X speedup when implementing core operations of the algorithm. Results show that GPU provides a helpful platform for high performance computing to improve the execution time of these applications.
    </p>
</details>
</p>

