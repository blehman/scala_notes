# Scala Notes
Attempting to learn how to write scala code.

## Example 1: coin flip
First we define a function called `coinFlip` that returns a value of the type 'String' and does not take an input.
<pre>
scala> def coinFlip(): String = {
     | Random.nextBoolean match {
     | case true => "Heads."
     | case false => "Tails."
     | }
     | }
</pre>
When random numbers are created, we match them based on the case being `true` or `false`, in which case we return the respective string.

Try it! 
`coinFlip()`
res0: String = Heads.

scala> coinFlip()
res2: String = Tails.
