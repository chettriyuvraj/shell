# Shell

Terminal shell in C to understand exceptional control flow. 

This shell was created to apply concepts learnt in Chapter 8 of [CS: APP](https://www.amazon.in/Computer-Systems-Programmers-Randal-Bryant/dp/013409266X)

What works and what is left:

- It has a really cute logo 🔥
- Executes commands by spawning child processes: try _sleep 30_ in this shell and quickly _ps -j -h | grep sleep_ in bash to see the child process you have created.
- Demonstrates the concept of signal handling: try _sleep 30_ and _ctrl + c_ to send a SIGINT which kills the child process, you can check using the _ps_ command previously explained.
- Operator handling: implements the _&&_ and _||_ operators as they work in bash.
- Implements the notion of a foreground process with the _&_ operator: try _sleep 30 & sleep 40 & sleep 50_, then _ctrl + c_ which sends a signal only to terminate sleep 50, since the rest are background processes.

TODO:
- builtins, implemented the _alias_ builtin which turned into a big ball of mud, so currently only _exit_ works.
- job control: things such as the bg, fg and jobs command, which will be the end of this project!

# Usage

- compile: _gcc shell.c_
- run binary: _./a.out_

# Output

A pretty wack shell

<img width="505" alt="image" src="https://github.com/chettriyuvraj/shell/assets/32122172/8a02672d-a701-4b7b-b210-86b97e18940e">



