dining-philosopher
==================
**Theory**

In computer science, the dining philosophers problem is an example problem often used in concurrent algorithm design to illustrate synchronization issues and techniques for resolving them.

It was originally formulated in 1965 by *Edsger Dijkstra*.


Five silent philosophers sit at a table around a bowl of spaghetti. A fork is placed between each pair of adjacent philosophers. (An alternative problem formulation uses rice and chopsticks instead of spaghetti and forks.)

Each philosopher must alternately think and eat. However, a philosopher can only eat spaghetti when he has both left and right forks. Each fork can be held by only one philosopher and so a philosopher can use the fork only if it's not being used by another philosopher. After he finishes eating, he needs to put down both forks so they become available to others. A philosopher can grab the fork on his right or the one on his left as they become available, but can't start eating before getting both of them.

Eating is not limited by the amount of spaghetti left: assume an infinite supply.

The problem is how to design a discipline of behavior (a concurrent algorithm) such that each philosopher won't starve; i.e., can forever continue to alternate between eating and thinking assuming that any philosopher cannot know when others may want to eat or think.

Src: http://en.wikipedia.org/wiki/Dining_philosophers_problem See more there.

**Documentation**

For the solution I have used Java as a programming language.


```
Class:  Dine - it has a main method.

Class:  Philosopher - represent the philosopher, it contains the two objects to represent the chopistrics.
          Methods
              eat     - called when enter for eating.
              think   - called when enter for thinking.
              run     - overriden method for Thread class.
            
Class:  Chopstick - represent the chopistic available.
          Methods
              take      - called when before occupied.
              release   - called when philosopher starts thinking.
              
            Both methods are the synchronized method.
```

**Running the program**

Compile
```
                    javac Dine.java
```

Run 
```
                    java Dine
```


Enjoy Coding **:) **



