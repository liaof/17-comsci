# Chapter 17

### Building Blocks of JS
![](./Images/400-javascript-parts.png)</br>An example of how each part plays a role in how Javascript works.

JavaScript is comprised of three data structures: a stack, a queue, and a heap.
Stack and Queue are linear data structures because they have a start and end. A heap is a 
2D structure with a hierarchical organization.
#### Call Stack
This data structure adds and removes data from only one end of the structure, like taking chips out a 
Pringles can. This type of operation is called FILO: First in, Last out
The pop() method removes items from the same end targeted by push.
#### Callback Queue
This data structure adds data at one end of the structure and removes data from the other, like water
flowing through a garden hose. This type of operation is called FIFO: First in, First out
The shift() method removes items from the front of the array queue and push adds elements to the end.</br> 

#### a Closure 
is a function that contains references to its surrounding state. Created when a function is returned.
Lets us access the outer scope containing the variable count.
</br> For Example:</br> 
 function counter() {</br>
   let count = 0;</br>
   return function() {</br>
     return count++;</br>
   }</br>
 }</br> 
the surrounding lexical environment here would belong to counter, which is { count: 0, anonymous(): f() { return count++; }. Note how in the closure function we return count, a variable not initialised in the closure.</br>

##### Benefits of Closure</br>
Prevent polluting the global namespace that can cause collisions due to name conflicts</br>

Accidental modifications of global variables</br>

Performance gains when accessing local variables vs. lookups on the global scope</br>

#### Factory Function
a function that produces objects, returns object literals</br>
const tiger = function() {
  const noise = 'roar';</br>
  return {</br>
    sound: function() {</br>
      console.log(noise);</br>
    },</br>
  }</br>
}</br>

const tigger = tiger();
tigger.sound(); //=> "roar"
### Other Definitions</br>
Thread of Execution TOE - the line of code currently being executed.

Inheritance - when you design your types based on what they are

Composition - when you design your types based on what they can do

event loop
web api
node.js core modules



