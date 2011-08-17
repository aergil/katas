Sum Of Two Integers
===

This is a solution to this [little exercise](http://programmingpraxis.com/2011/07/19/sum-of-two-integers/). I'm not very fond of the purely algorithmic problem, so the solution i found is very naive. I may spend some time on this later, thought.
There are 2 algorithm in the files, because I wanted to compare the speed of each one. In the first one, I made a heavy use of fold and map, wich ends up in making unnecessary work. In the second one, the use of a loop allows to stop the computation as soon as the result is found.

Lessons Learned
---
* TDD is cool. I started without any thinking beforehand, and i came to the first solution quite naturally.
* My only tools when writing iterations in Scheme are recursion and map/fold functions, and it's not very good. I wasn't used to the named let syntax, it's pretty nice. I had to check the racket docs about the for form for the sake of the kata, there are nice things, but I tend to stick with portable forms when doing those exercices.
* I used [Geiser](http://www.nongnu.org/geiser/) instead of [Quack](http://www.neilvandyke.org/quack/) for Racket programming in emacs. It's a nice tool.
* Those two solutions led me to make a little benchmark, and I ran very simple benchmarks one the chicken and Racket executables. Chicken creates a real compiled executable, whereas Racket exe as it is bytecode compiled comes with the VM. The two algos are so close that it doesn't make sense to compare them. Racket exe is much faster than chicken one (like 8 times faster) and when running in REPL, chicken is like 10 times solwer than Racket. Racket team seems to have done a very good job on the performance issues they had a few years ago. But I sill have a soft spot for Chicken :)