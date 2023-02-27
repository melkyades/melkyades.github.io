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
    Operating systems are traditionally implemented in low-level, performance-oriented programming languages. These languages typically rely on minimal runtime support and provide unfettered access to the underlying hardware. Tra- dition has benefits: developers control the resources that the operating system manages and few performance bottle- necks cannot be overcome with clever feats of programming. On the other hand, this makes operating systems harder to understand and maintain. Furthermore, those languages have few built-in barriers against bugs. This paper is an ex- periment in side-stepping operating systems, and pushing functionality into the runtime of high-level programming languages. The question we try to answer is how much sup- port is needed to run an application written in, say, Smalltalk or Python on bare metal, that is, with no underlying oper- ating system. We present a framework named NopSys that allows this, and we validate it with the implementation of CogNos a Smalltalk virtual machine running on bare x86 hardware. Experimental results suggest that this approach is promising.
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

