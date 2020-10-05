# Program Development Guidelines

> Quality comes not from inspection, but from improvement of the production process.

\- W. Edwards Deming



---

### Design

D1 - Write code that communicate its purpose and intent (readability)

D2 - Code Refactoring

D3 - Favor object composition over class inheritance

D4 - Programming to an interface, not an implementation (but DON't overdo it)

D5 - Be SOLID (**S**ingle responsibility, **O**pen-closed, **L**iskov substitution, **I**nterface segregation, and **D**ependency inversion)

D6 - Premature optimization is the root of all evil



## Coding

C1 - Use intention-revealing names

C2 - Use enum instead of constants to define a finite set of values

C3 - Use exceptions rather than return codes

C4 - Use unchecked exceptions

C5 - Dont' return `null`

C6 - Prefer (and keep) debugging log messages to user of debuggers

C7 - Crash early



## Testing

T1 - Test everything that could possibly break (but NOT trivial accessors)

T2 - Put the test class in the same package as the class under test, in a `test` folder

T3 - Name the test methods with `[methodName]_Should[_expected_behaviour]_When[_state_under_test]`

---



## D1 - Write code that communicate its purpose and intent (readability)

Bugs sneak in when code need to be changed without a complete and clear understanding, it happens
when features were added to a piece of software by maintenance programmers (or author programmers
in their “maintenance mode”) within a tight timeframe.

**Programs must be written for people to read**

To some people who understand the craft of programming so well, programming is a way to
communicate one’s thoughts through code:

> Computer language is not just a way of getting a computer to perform operations but rather that it is a **novel formal medium for expressing ideas about methodology**. Thus, **programs must be written for people to read**, and only incidentally for machines to execute.

From The Structure and Interpretation of Computer Programs, Preface to the First Edition [^AS96]

**Good programmers write code that humans can understand**

It is fast and easy to work with readable code, that’s why Martin Fowler use the ability to write readable
code to measure the competence of a programmer:

> Any fool can write code that a computer can understand, **good programmers write code that humans can understand**.

Source: [^FBBOR99] p.15.



## D2 - Code Refactoring

To quote the original sermon on structured programming by Edsger Dijkstra:

> The extent to which the program correctness can be established is not purely a function or the program's external specifications and behavior but depends critically on its internal structure.

Source [^Dij70] p.5

**Refactor the code to make program easier to read and therefore easier to maintain**

> Refactoring is the process of changing a software system in such a way that it does not alter the external behavior of the code yet **improves its internal structure**. It is a disciplined way to clean up code that **minimizes the chances of introducing bugs**. In essence when you refactor you are **improving the design of the code after it has been written**.

> "Improving the design after it has been written." That's an odd turn of phrase. In our **current understanding of software development we believe that we design and then we code**. A good design comes first, and the coding comes second. Over time the code will be modified, and the integrity of the system, its structure according to that design, gradually fades. The code **slowly sinks from engineering to hacking**.

> Refactoring is the opposite of this practice. With refactoring you can take a bad design, chaos even, and rework it into well-designed code. Each step is simple, even simplistic. You move a field from one class to another, pull some code out of a method to make into its own method, and push some code up or down a hierarchy. Yet the cumulative effect of these small changes can radically improve the design. It is the exact **reverse of the normal notion of software decay**.

> With refactoring you find the balance of work changes. You find that design, rather than occurring all up front, occurs continuously during development. You learn from building the system how to improve the design. The resulting interaction leads to a program with a design that stays good as development
> continues.

From the preface of *Refactoring: Improving the Design of Existing Code* [^FBORR99]

**Good designs are easy to test and difficult to mess up**

Tom DeMarco et al put their insight about software design improvement in *Adrenaline Junkies and*
*Template Zombies: Understanding Patterns of Project Behavior* [^DHLMRR08]:

> …be capable and willing to look in detail at your people’s designs, and be aware enough to see quality when it’s there. Doing this for even the shortest time will quickly convince you that the gold-plating argument is a red herring; no design is made better in any way by piling on added features or glitz. Rather, **what enhances a design’s aesthetic is what is taken away**. The best designs are typically
> spare and precisely functional, **easy to test and difficult to mess up when changes are required**. Moreover, they make you feel that there could be no better way to achieve the product’s assigned functionality.



## References:

[^AS96]: Structure and Interpretation of Computer Programs (Second Edition), Harold Abelson and Gerald Jay Sussman with Julie Sussman, The MIT Press, 1996. [link](http://mitpress.mit.edu/sicp/full-text/book/book-Z-H-7.html#%_chap_Temp_4)

[^DHLMRR08]: Robertson, Adrenaline Junkies and Template Zombies: Understanding Patterns of Project Behavior, Tom DeMarco, Peter Hruschka, Tim Lister, Steve McMenamin, James Robertson, Suzanne Dorset House, 2008.

[^Dij70]: The 'premature optimization is evil' myth, Joe Duffy, 2010. [link](http://joeduffyblog.com/2010/09/06/the-premature-optimization-is-evil-myth/)

[^FBBOR99]: Refactoring: Improving the Design of Existing Code, Martin Fowler et al., Addison-Wesley, 1999

