# BitSignificant CSharp

## 0. A History On Computer Systems

### Electronic Numerical Integrator and Computer (ENIAC)
The [_ENIAC_](https://en.wikipedia.org/wiki/ENIAC)  was the first general-purpose digital computer. Built by the University of Pennsylvania and finished in 1945, it was primarily used to calculate artillery firing tables for the US military. The importance of his machine comes from it's general-purpose nature which meant it could accomplish many different tasks by reprogramming, however, that was not a simple task.  The ENIAC was extremely large compared to today's computers, weighing 30 tons consisting of 18 000 vacuum tubes, and consuming 140 kilowatts of power. 

The number system the ENIAC used was decimal (base 10) instead of binary (base 2) like modern-day computers. It could represent numbers as large as 10 digits using 10 vacuum tubes, one per digit. 

The ENIAC was laid to rest in 1955 after helping solve complex mathematical problems of its time, including helping determine the feasibility of the hydrogen bomb (the project on which John von Neumann worked). 

### The Von Neumann Machine
The Von Neumann machine aimed to solve having reprogram a machine each time, and instead proposed a way to store a program alongside its data in some sort of memory component. Reprogramming was a timeous task as was evident on the ENIAC. This idea is attributed to the designers of the ENIAC, the most famous being the mathematician John Von Neumann. This stored-program concept was also developed by Alan Turing around the same time. 

In 1946, Von Neumann proposed this idea in a publication for a new computer called the EDVAC (Electronic Discrete Variable Computer). Which is the ancestor of all subsequent general-purpose computers.

The EDVAC had the following components:
1. A main memory - stores a program's data as well as the programs instructions
2. An arithmetic and logic unit (ALU) - processed binary data
3. A control unit - reads and inteprets the instructions from memory and executes them
4. Input/Output - a way to accept and produce data from and to the internal and outside world; controlled by the control unit

![Von Neumann Architecture](https://en.wikipedia.org/wiki/Von_Neumann_architecture#/media/File:Von_Neumann_Architecture.svg)

Some detailed information can be found at the [Von Neumann Architecture Wikipedia page](https://en.wikipedia.org/wiki/Von_Neumann_architecture).

### Transistor-based Machines


## 1. An Introduction to Computer Systems

Modern computers are fairly complex machines compared to their simple but ground-breaking ancestors starting from the 1940s. If there's one thing all these machines have in common it is that they all processed data. That's what computers are good at processing data for us. Whether it's doing mathematical calculations like crunching a block's hash in some blockchain, loading and saving a text document, or sending messages via a chat application to friends. While all these operations have varying complexities, they all involve processing some data and then doing some useful with it.

To achieve these tasks computers a simplistic internal representation of a computer may have the following components:

1. Central Processing Unit (CPU) - a general-purpose or purpose-built array of transistors that controls the operation and coordination of the computer and its components
2. Main Memory - a temporary (volatile) storage component that holds data the CPU deems the most important for the moment
3. Input/Output Components - facilitates the passing around of data both throughout the internal internal and external systems (devices)
4. System Communication Components - these combine all the necessary components that allow all components in a computer to communicate with one another

### The Central Processing Unit (CPU)
The CPU is the brain of the computer and controls the functioning of the other components. A CPU usually consists of:  
1. Control Unit - controls the operation of the CPU itself
2. Arithmetic and Logic Unit (ALU) - performs arithmetic and logical operations, ultimately where data processing occurs
3. Registers - internal storage to the CPU
4. CPU Communication - facilitates communication of the CPU's interal components
