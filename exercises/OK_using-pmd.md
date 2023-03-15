# Using PMD

Pick a Java project from Github (see the [instructions](../sujet.md) for suggestions). Run PMD on its source code using any ruleset. Describe below an issue found by PMD that you think should be solved (true positive) and include below the changes you would add to the source code. Describe below an issue found by PMD that is not worth solving (false positive). Explain why you would not solve this issue.

## Answer
Here is for the **false negative error**:
In ```MillerUpdatingRegressionTest.java``` which is line 87. 
There is a return in a void method which is unnecessary. 

For the **true positive**:
In ```TravellinSalemanSolver.java``` which is line 127. 
It advice to do separate catch for this kind of expression.
```java
catch (InterruptedException | ExecutionException e) {
    if (e instanceof InterruptedException) {
        // Restore interrupted state...
        Thread.currentThread().interrupt();
    }
    throw new RuntimeException(e);
}
```
Which can be solve by divided thoses 2 exceptions:
```java
catch (InterruptedException e) {
    // Restore interrupted state...
    Thread.currentThread().interrupt();
    throw new RuntimeException(e);
}
catch (ExecutionException e) {
    throw new RuntimeException(e);
}
```