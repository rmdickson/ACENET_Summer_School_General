---
title:  "Introduction"
start: true
teaching: 10
exercises: 15
questions:
- "What parallel computing is and why it is important?"
- "How does a parallel program work?"
objectives:
- "Explain differences between a serial and a parallel program"
- "Introduce types of parallelism available in modern computers"

keypoints:
- "Parallel computing is much better suited for modelling, simulating and understanding complex, real-world phenomena."
- "Modern computers have several levels of parallelism"
---

Parallel computing is the science of solving problems using multiple computer processors at the same time.

### Why parallel computing?
- From the beginning of electronic computers to about 2010 or so, computer engineers were able to build faster and faster CPUs.  Clock speeds went from about 60 MHz around 5 GHz between about 1990 and 2010.  Programs could be sped up just by buying the latest chip every year.

- This growth has effectively ended due to limitations of miniaturization, power consumption, and heat dissipation.

- It is increasingly expensive to make a single processor faster. Using a larger number of moderately fast commodity processors to achieve the same (or better) performance is more practical.

### Example applications

Here are just a few examples of how parallel computing is helping to accelerate research and solve new problems.

1. Numeric weather prediction
    - Combining current observations and mathematical models to forecast the future state of the weather
2. Computational astrophysics
    -  Numerical relativity, magnetohydrodynamics, stellar and galactic magnetohydrodynamics
3. Seismic data processing
    - Analyze seismic data to find oil and gas-bearing layers
4. Commerce
    - Nearly every major aspect of today’s banking, from credit scoring to risk modelling to fraud detection, is GPU-accelerated.
5. Pharmaceutical design
    - Uses parallel computing for running simulations of molecular dynamics
6. Computational fluid dynamics, tidal wave simulations

### Benefits of parallel computing:
 - Compared to **serial** (non-parallel) computing, the number of problems you can solve practically with parallel computing is huge.
 - It allows us to solve problems in a shorter time.
 - Allows solving larger, more detailed problems.
 - Parallel computing is better suited for modelling, simulating, and understanding complex, real-world phenomena.

### Limitations and disadvantages:

- Some problems can not be broken into pieces of work that can be done independently
- Not every problem can be solved in less time with multiple compute resources than with a single computing resource. Some problems may not have enough inherent parallelism to exploit.
- Large-scale parallel computing equipment is expensive.
- Developing parallel code is not easy.
- It requires expertise, time, and effort.

#### Before you start your parallel computing project

- Select the most appropriate parallelization options for your problem.
- Estimate the effort and potential benefits.

In this course, we hope to give you the knowledge to make the right decisions on parallel computing projects.

### How does a parallel program work?

Let us start by exploring how a serial (non-parallel) program works.

### Traditional serial program
![](../fig/Serial_program.svg)

- A problem is broken into a set of instructions
- Instructions are executed in a specified order on a single CPU
- Only one instruction can be executed at a time

###  Parallel program

In parallel computing, individual instructions execute concurrently on different CPUs and/or computers.

![](../fig/Parallel_program.svg)

- A problem is broken into parts that can be done at the same time
- Each part is further broken down into a set of instructions
- Instructions from each part execute simultaneously on different processors
- Requires an overall control & coordination mechanism.

> ## Discussion exercise
> 
> Pretend it's the days before electronic computers, and you have been assigned the task
> of computing the sum of 1,000 four-digit numbers as rapidly as possible.
> You hold in your hands a stack of 1,000 index cards, each containing a single
> number, and you are in charge of 1,000 accountants, each with a pencil.
> You may choose to use the services of any number of these accountants.
> The accountants are sitting at desks in a cavernous room. The desks are organized
> into 25 rows and 40 columns. Each accountant can pass cards to the four
> accountants nearest them--- in front, in back, to the left, and to the right.
>
> Discuss with your classmates:
> - How many accountants should we use?
> - How will we get the cards to right accountants?
> - How will we turn the subtotals generated by the active accountants into a grand total?
> - What should we do differently if there were 10,000 cards (but still 1,000 accountants)?
>
> You do not need to arrive at a perfect plan. (Indeed, you don't have enough
> information to devise a perfect plan!)  But try to sketch a rough plan,
> figure out some ideas, talk about whether those ideas have merit or not, 
> and think what other information you would want to carry this out this 
> imaginary task.
> 
> (Adapted from Michael J. Quinn, ["Parallel Programming in C with MPI and OpenMP"](https://www.amazon.com/Parallel-Programming-Openmp-Michael-2008-01-01/dp/B01F81TFD8/ref=sr_1_2?ie=UTF8&qid=1496073113&sr=8-2&keywords=Michael+J.+Quinn%2C+%22Parallel+Programming+in+C+with+MPI+and+OpenMP%22))
>
{: .challenge}


{% include links.md %}
