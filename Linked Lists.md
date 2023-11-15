## array vs linked lists
**Arrays:**
- Have indices to access elements (e.g., `myArray[0]`, `myArray[1]`).
- Elements are stored contiguously in memory.
- Efficient for random access to elements.
- Fixed size in many programming languages, making resizing difficult.
- Appropriate when you need fast access to elements and the size is known in advance.

**Linked Lists:**
- Do not have indices; elements are accessed by traversing the list.
- Elements are stored non-contiguously in memory as nodes with references to the next element.
- Dynamic in size; elements can be easily added or removed.
- Not suitable for random access but efficient for insertions and deletions.
- Appropriate when the size is unknown or when frequent insertions/deletions are required.

![[Pasted image 20231105222520.png]]

- We can't go backward in the linked list
- adding and removing from the the beginning is O(1)
- removing from the end is O(1)
- adding at the end is O(n)

![[Pasted image 20231107205731.png]]

# LL under the hood
![[Pasted image 20231107210726.png]]

# Push
- insert at the end of the LL.

- create a new node
- The last node of previous LL point to it
- the tail point to it

# Pop
edge cases
- no item
- 1 item

