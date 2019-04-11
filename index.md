## Python Linked List

#### [HackerRank](www.hackerrank.com)

> Complete the insert function in your editor so that it creates a new Node (pass data as the Node constructor argument)
> and inserts it at the tail of the linked list referenced by the head parameter. Once the new node is added, return the
> reference to the head node.
> Note: If the head argument passed to the insert function is null, then the initial list is empty.

To be honest, I had no idea what they were asking so there was no preprocess. I just know from past experience of using a
Node that there is some recursion. So that is what I did. That's how it goes sometimes.

### Thoughts becacuse I was not sure of the steps
#### Because it be like that sometimes.

* I know if the head passed is empty to return a new node with data
* Else I see it has a .next instance which is what I will fill
* I know for this to be repeated I have to constantly check if the head is empty and if the head is empty than I check if next is empty.
* For repeated stuff like that, its time for recursion to come out and play.

### Code

```python
def insert(self,head,data): 
    #Complete this method
    # I know if the head is empty I simply return the data as a new Node
      if head == None:
        head = Node(data)
      else:
        # I know it has to be repeated and I am not going to replace head so the next
        # option is head.next. But how do I keep checking if head.next is empty?
        # Oh wait I have already done that in this function so lets just re-call it ;)
        head.next = self.insert(head.next, data)
        
      # Do not forget to return or you'll keep failing.
      return head
```

## Conclusion

Great warm up. I had forgotten about nodes and even though the question was ill set up (in my most hubmle opinion) it was still
very fun.
