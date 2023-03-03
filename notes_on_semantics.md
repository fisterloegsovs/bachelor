# Notes on chapter 9 in Semantics with Applications: An Appetizer.

A partial correctness property of a program need not ensure that it terminates. Which is contrary to a total correctness property, which express that the program will terminate and that there will be a certain relationship between the initial and the final values of the variables.

We then have that:

partial correctness + termination = total correctness.

Implying that we only need to show partial correctness and that it terminates.

We can use the following example of proving partial correctness:
```y := 1; while not(x=1) do (y := y * x; x := x - 1)```
This example is partially correct; meaning that if the statement terminates, then the final value of y will be the factorial of the initial value of x. So how can we prove that it terminates? 

## Natural semantics

I barely understand this...

## Structural operational semantics

Also this...

## Denotional semantics

And this...

## Partial correctness assertions

An assertion is a partial correctness property. The assertion is a triple of the form:

```{P} S {Q}```

Where S is a statement and P and Q are predicates. Here P is called the precondition and Q is called the postcondition. Intuitively ```{P} S {Q}``` means that:

- if P holds in the initial state, and

- if the execution of S terminates when started in that state,

- then Q will hold in the state in which S halts.

NOTE: that for ```{P} S {Q}``` to hold we do not require that S halt when started in states satisfying P - merely that if it does halt, then Q holds in the final state.

## Logical variables

