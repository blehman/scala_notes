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

# Scalding Notes
<pre>
$cd source/science
follow directions: go/scaldingrepl  
</pre>
Once scalding is running...
<pre>
import scala.io.Source  
val alice = Source.fromURL("http://www.gutenberg.org/files/11/11.txt").getLines.toIterable  
alice.take(10).foreach { line: String => println(line)}  
val alicePipe = TypedPipe.from(alice)  
alicePipe.map { line => line.length }  
alicePipe.map { line => line.length }.limit(10).dump  
alicePipe.map { line => line.length }.filter { length: Int => length > 0 }.limit(10).dump  
</pre>
...skip to tutorial: https://confluence.twitter.biz/display/ANALYTICS/Scalding+at+Twitter+Tutorial
<pre>
$cd source/science
</pre>
Now follow the instructions starting with `mkdir src/scala/com/twitter/tweetcounter/`  


