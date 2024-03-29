<img src="./images/Archer2_logo.png"  width="355" height="100" align="left"> <img src="./images/epcc_logo.jpg" align="right" width="133" height="100">

<br /><br /><br /><br /><br />


# ARCHER 2 MPI course (May 2020)

[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

The world’s largest supercomputers are used almost exclusively to run
applications which are parallelised using Message Passing. The course
covers all the basic knowledge required to write parallel programs
using this programming model, and is directly applicable to almost
every parallel computer architecture.

Parallel programming by definition involves co-operation between
processes to solve a common task. The programmer has to define the
tasks that will be executed by the processors, and also how these
tasks are to synchronise and exchange data with one another. In the
message-passing model the tasks are separate processes that
communicate and synchronise by explicitly sending each other
messages. All these parallel operations are performed via calls to
some message-passing interface that is entirely responsible for
interfacing with the physical communication network linking the actual
processors together. This course uses the de facto standard for
message passing, the Message Passing Interface (MPI). It covers
point-to-point communication, non-blocking operations, derived
datatypes, virtual topologies, collective communication and general
design issues.

The course is normally delivered in an intensive three-day format
using EPCC’s dedicated training facilities. It is taught using a
variety of methods including formal lectures, practical exercises,
programming examples and informal tutorial discussions. This enables
lecture material to be supported by the tutored practical sessions in
order to reinforce the key concepts.

Intended Learning Outcomes

On completion of this course, students should be able to:

 * Understand the message-passing model in detail.

 * Implement standard message-passing algorithms in MPI.

 * Debug simple MPI codes.

 * Measure and comment on the performance of MPI codes.

 * Design and implement efficient parallel programs to solve
regular-grid problems.

Pre-requisite Programming Languages:

Fortran, C or C++. It is not possible to do the exercises in Python or Java.

<h2>Message Passing Programming with MPI</h2>

<p><strong>Dates:</strong>14th, 15th and 22nd May 2020
<p><strong>Location:</strong>Online</p>

<h3>Installing MPI locally</h3>

Note that all registered users will be given access to the Cirrus
system. Although having MPI installed on your laptop will be
convenient, do not worry if these instructions do not work for you.

<h4>Linux</h4>

Linux users need to install the GNU compilers and a couple of MPI packages,
e.g. for Ubuntu:

    user@ubuntu$ sudo apt-get install gcc
    user@ubuntu$ sudo apt-get install openmpi-bin
    user@ubuntu$ sudo apt-get install libopenmpi-dev

<h4>Mac</h4>

Mac users need to install compilers from the Xcode developer
package. It is easiest to install MPI using the Homebrew package
manager - here are [Instructions on how to install Xcode and
Homebrew](https://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/).

Now install OpenMPI:

    user@mac$ brew install open-mpi

<h4>Windows</h4>

We recommend that Windows users access the EPCC systems (e.g. Cirrus
or NEXTGenIO) using
[MobaXterm](https://www.archer2.ac.uk/training/training-software).

However, that may not be possible at present due to the ongoing
security issues affecting many supercomputers worldwide including
systems at EPCC.

One solution is to install a Linux virtual machine (e.g. Ubuntu) and
follow the Linux installation instructions above.

I know that some users have been able to install MPI natively on
Windows using the [Intel Parallel
Studio](https://software.intel.com/content/www/us/en/develop/tools/parallel-studio-xe/choose-download.html)
compilers and the [Intel MPI
library](https://software.intel.com/content/www/us/en/develop/documentation/mpi-developer-guide-windows/top.html).

<h3>Guest accounts on the NEXTGenIO system</h4>

    ssh -XY ngguestXX@hydra-vpn.epcc.ed.ac.uk
    ssh -XY nextgenio-login2

Here are the [assignments of account names to users](exercises/accounts.txt)

<h3>Lecture Slides</h3>

<p><blockquote>Unless otherwise indicated all material is Copyright
&copy; EPCC, The University of Edinburgh, and is only made available
for private study. </blockquote></p>

<h4>Wednesday</h4>

<ul>
<li><a href="slides/L00-ARCHER2-PTC-Intro.pdf">ARCHER2 and the training programme</a>
<li><a href="slides/L00-overview_3day.pdf">Overview of MPI course</a>
<li><a href="slides/L01-mpconcepts.pdf">Message-Passing Concepts</a>
<li><a href="slides/E01-traffic.pdf">Parallel Traffic Modelling</a>
<li><a href="slides/road-solution.pdf">Parallel Traffic Modelling: solution</a>
<li><a href="slides/L02-intro.pdf">MPI Programs</a>
<li><a href="slides/L03-archer-cirrus-mpi.pdf">MPI on Cirrus and ARCHER</a>
<li><a href="slides/L04-pt2pt.pdf">Point-to-Point Communication</a>
<li><a href="slides/L06-modetagcomm.pdf">Communicators, Tags and Modes</a>
</ul>

<h4>Thursday</h4>

<ul>

<li><a href="slides/L07-nonblocking.pdf">Non-Blocking Communication</a>
<li><a href="slides/L08-collective.pdf">Collective Communication</a>
<li><a href="slides/L09-topology.pdf">Virtual Topologies</a>
<li><a href="slides/L10-derivedtypes.pdf">Derived Data Types</a> 

</ul>

<h4>Friday</h4>

<ul>
<li>Screenshots of the MPI Quiz showing correct answers and explanations: 
<a href="exercises/MPP-quiz-q01-03.png">q01-03</a>, 
<a href="exercises/MPP-quiz-q04-06.png">q04-06</a>, 
<a href="exercises/MPP-quiz-q07-09.png">q07-09</a>, 
<a href="exercises/MPP-quiz-q10-11.png">q10-11</a>, 
<a href="exercises/MPP-quiz-q12.png">q12</a>, 
<a href="exercises/MPP-quiz-q13.png">q13</a>, 
<a href="exercises/MPP-quiz-q14.png">q14</a>
<li><a href="slides/L11-casestudy.pdf">Case Study</a>
<li><a href="slides/L12-tipsandtricks.pdf">MPI Tips and Tricks (includes dynamic memory allocation in C and array syntax issues in Fortran)</a>
<li><a href="slides/L13-scaling.pdf">MPI Scaling (not delivered as part of this course but included for reference)</a>
</ul>

<h3>Notes</h3>

<ul>
<li><a href="notes/MPP-notes.pdf">MPI course notes (historical)</a>
<li><a href="notes/MPP-f90issues.pdf">Issues with non-blocking calls and f90 array syntax</a>
</ul>

<h3>Exercise Material</h3>

<p><blockquote>Unless otherwise indicated all material is Copyright &copy; EPCC, The University of Edinburgh, and is only made available for private study. </blockquote></p>

<ul>
<li><a href="exercises/road.pdf">Traffic modelling exercise sheet</a></li>
<li><a href="exercises/NEXTGenIO-MPI-cribsheet.pdf">Instructions for logging on, compiling and running on NEXTGenIO</a></li>
<li><a href="exercises/Cirrus-MPI-cribsheet.pdf">Instructions for logging on, compiling and running on Cirrus</a></li>
<li><a href="exercises/MPP-templates.tar">Useful files and pieces of code: MPP-templates.tar</a></li>
<li><a href="exercises/hello.job">Example SLURM script for NEXTGenIO - all instructions included as comments</a></li>
<li><a href="exercises/MPP-exercises.pdf">MPI exercise sheet</a></li>
<li><a href="exercises/MPP-pi.tar">Detailed solutions to pi calculation example</a>
<li><a href="exercises/MPP-solutions.tar">Simple example solutions to all exercises</a>
<li><a href="exercises/MPP-casestudy.pdf">Case Study exercise sheet</a></li>
<li><a href="exercises/MPP-casestudy.tar.gz">Case Study source code</a></li>
<li><a href="exercises/MPP-caseserial.tar">Simple Case Study solutions (serial)</a></li>
<li><a href="exercises/MPP-casesolns.tar">Simple Case Study solutions (parallel)</a></li>
<li><a href="exercises/MPP-arralloc.tar">Code for dynamic array allocation in C</a>
<li><a href="exercises/MPP-traffic.tar">Serial and parallel solutions to the traffic model</a></li>
</ul>

---

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

