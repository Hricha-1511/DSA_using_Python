# 📚 Doubly Linked List (DLL) - Interview Questions & Answers

This repository contains the **most frequently asked Doubly Linked List (DLL) interview questions**, along with concise answers, time complexities, and real-world applications.

---

# 1. What is a Doubly Linked List (DLL)?

A **Doubly Linked List (DLL)** is a linear data structure in which each node contains:

- 📌 Data
- 📌 Pointer to the next node (`next`)
- 📌 Pointer to the previous node (`prev`)

Unlike a **Singly Linked List**, a Doubly Linked List allows traversal in **both forward and backward directions**.

---

# 2. Difference Between Singly Linked List and Doubly Linked List

| Singly Linked List | Doubly Linked List |
|--------------------|--------------------|
| Stores one pointer (`next`) | Stores two pointers (`next` and `prev`) |
| Forward traversal only | Forward & backward traversal |
| Requires less memory | Requires more memory |
| Simpler implementation | More complex implementation |
| Deleting a node requires finding its previous node | Deletion is easier when the node is known |

---

# 3. Why do we use a `prev` pointer?

The **`prev` pointer** allows us to:

- ✅ Traverse backward
- ✅ Delete a node efficiently
- ✅ Insert a node before another node
- ✅ Implement Browser History
- ✅ Implement Undo/Redo functionality
- ✅ Implement an LRU Cache

---

# 4. Why do we maintain a `tail` pointer?

The **tail pointer** stores the address of the last node.

### Without Tail Pointer

- Insert at End → **O(n)**
- Delete Last Node → **O(n)**

### With Tail Pointer

- Insert at End → **O(1)**
- Delete Last Node → **O(1)**

---

# 5. Time Complexity of Common Operations

| Operation | Time Complexity |
|-----------|-----------------|
| Insert at Beginning | **O(1)** |
| Insert at End (with tail) | **O(1)** |
| Insert at End (without tail) | **O(n)** |
| Insert at Given Position | **O(n)** |
| Delete from Beginning | **O(1)** |
| Delete from End (with tail) | **O(1)** |
| Delete from End (without tail) | **O(n)** |
| Search | **O(n)** |
| Forward Traversal | **O(n)** |
| Backward Traversal | **O(n)** |

---

# 6. Why does a Doubly Linked List require more memory?

Each node stores an extra pointer (`prev`) in addition to `next`.

Because of this extra pointer, every node occupies **more memory** than a Singly Linked List node.

---

# 7. Advantages of a Doubly Linked List

- ✅ Forward traversal
- ✅ Backward traversal
- ✅ Easy insertion and deletion
- ✅ Efficient deletion when node reference is available
- ✅ Used in Browser History, Undo/Redo, Playlists, and LRU Cache

---

# 8. Disadvantages of a Doubly Linked List

- ❌ More memory consumption
- ❌ More pointer updates during insertion/deletion
- ❌ Slightly more complex implementation

---

# 9. Why is deletion easier in a Doubly Linked List?

Every node stores references to both:

- Previous node
- Next node

Therefore, deletion only requires updating two pointers:

- Previous node's `next`
- Next node's `prev`

In a Singly Linked List, the previous node must first be found by traversal.

---

# 10. Can a Doubly Linked List be traversed backward?

**Yes.**

Since every node stores a `prev` pointer, traversal can begin from the **tail** and continue toward the **head**.

---

# 11. What happens if the `prev` pointer is not updated correctly?

The list becomes inconsistent, causing:

- ❌ Incorrect backward traversal
- ❌ Broken links
- ❌ Runtime errors
- ❌ Invalid list structure

---

# 12. Why is a Doubly Linked List used in an LRU Cache?

An **LRU Cache** performs two operations frequently:

- Remove a node
- Move a node to the front

A Doubly Linked List allows both operations in **O(1)** time when combined with a **HashMap**.

---

# 13. Why is a Doubly Linked List used for Browser History?

Browser navigation requires:

- ⬅️ Back
- ➡️ Forward

Since DLL supports traversal in both directions, it is ideal for browser history implementation.

---

# 14. Can a Doubly Linked List be implemented using only a `head` pointer?

**Yes.**

However,

- Insert at End → **O(n)**
- Delete Last Node → **O(n)**

Using both **head** and **tail** makes these operations **O(1)**.

---

# 15. What happens when the only node in the list is deleted?

Both pointers should become:

```python
head = None
tail = None
```

The list becomes empty.

---

# 16. Can a Doubly Linked List contain a cycle?

**Yes.**

Although uncommon, incorrect pointer updates can create cycles.

Cycle detection can be performed using:

- **Floyd's Cycle Detection Algorithm**
- **Tortoise and Hare Algorithm**

---

# 17. Real-World Applications of a Doubly Linked List

- 🌐 Browser History
- ↩️ Undo/Redo
- 🎵 Music Playlists
- 🖼️ Image Viewer
- ⚡ LRU Cache
- 🧭 Navigation Systems
- 📝 Text Editors

---

# 18. Why is insertion at the beginning an **O(1)** operation?

Only a constant number of pointers are updated:

- New node's `next`
- Old head's `prev`
- `head`

No traversal is required.

---

# 19. Why is searching **O(n)**?

Unlike arrays, linked lists **do not support indexing**.

Each node must be visited sequentially until:

- The element is found
- The end of the list is reached

---

# 20. Important Edge Cases

A correct DLL implementation should handle:

- ✅ Empty List
- ✅ Single Node List
- ✅ Insert at Beginning
- ✅ Insert at End
- ✅ Insert at Given Position
- ✅ Delete from Beginning
- ✅ Delete from End
- ✅ Delete at Given Position
- ✅ Invalid Positions
- ✅ Proper Head & Tail Updates
- ✅ Correct `next` and `prev` pointer updates

---

# 💻 Common Coding Questions

1. Create a Doubly Linked List
2. Insert at Beginning
3. Insert at End
4. Insert at Given Position
5. Delete from Beginning
6. Delete from End
7. Delete at Given Position
8. Traverse Forward
9. Traverse Backward
10. Reverse a Doubly Linked List
11. Search an Element
12. Find Length of the List
13. Find the Middle Node
14. Detect a Cycle
15. Remove Duplicate Nodes
16. Merge Two Sorted Doubly Linked Lists
17. Sort a Doubly Linked List
18. Flatten a Multilevel Doubly Linked List
19. Implement an LRU Cache using DLL + HashMap
20. Design Browser History using a Doubly Linked List
21. Implement Undo/Redo using a Doubly Linked List

---

# 💡 Interview Tip

> **Always update both `next` and `prev` pointers during insertion and deletion.**

Most bugs in Doubly Linked List implementations occur because one of these pointers is forgotten or updated incorrectly.

This is one of the **first things interviewers check** during coding interviews.

---

⭐ **If you found this repository helpful, consider giving it a star!**
