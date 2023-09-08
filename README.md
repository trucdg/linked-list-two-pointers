# ✌️ 2 Pointers in Linked List
- Let's start with a classic problem:
> Given a linked list, determine if it has a cycle in it.

You might have come up with the solution using the `hash table`. 

But there is a more efficient solution using `the 2 pointers technique.`

Imagine there are 2 runners with different speed. If they are running on a straight path, the fast runner will first arrive at the destination. However, if they are running in a circular track, the fast runner will catch up with the slow runner if they keep running.

That's exactly what we will come across using 2 pointers with different speed in a linked list:
1. `If there is no cycle, the fast pointer will stop at the end of the linked list.`
2. `If there is a cycle, the fast pointer will eventually meet with the slow pointer.`

So the only remaining question is:
> What should be the proper speed for the 2 pointers?

It is a safe choice to move the slow pointer `one step` at the time while moving the fast pointer `2 steps` at a time. For each iteration, the fast pointer will move 1 extra step. If the length of the cycle is M, after M iterations, the fast pointer definitely move one more cycle and catch up with the slow pointer.
