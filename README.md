# QUEUES DATA STRUCTURE

How do we use them in programming?

- Background tasks e.g Online Gaming, waiting to join the server.
- Uploading resources.
- Printing / Task processing.

### A Queue Class

```js
class Queue {
  constructor() {
    this.first = null;
    this.last = null;
    this.size = 0;
  }
}

class Node {
  constructor(value) {
    this.value = value;
    this.next = null;
  }
}
```

### enqueue() Pseudocode

- This code accepts some value.
- Create a new node using that value passed to the function.
- If there are no nodes in the queue, set this node to be the first and the last property of the queue.
- Otherwise, set the next property on the current last to be that node, and then set the last property of the queue to be that node.

### dequeue() Pseudocode

- If there is no first property, return null.
- Store the fist property in a variable.
- See if the fist is the same as the last, if so set the first property to be null.
- If there is more than 1 node, set the first property to be the next property of first.
- Decrement the size by 1.
- Return the value of the node dequeud.
