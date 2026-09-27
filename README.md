# Leetcode_Day57
# Day 57 — Merge Two Sorted Lists

## 🧩 Problem

Given the heads of two sorted linked lists, `list1` and `list2`, merge them into a single sorted linked list.

The merged list should be created by reusing the nodes from the original lists.

### Example

Input:
- List 1: `1 → 2 → 4`
- List 2: `1 → 3 → 4`

Output:
`1 → 1 → 2 → 3 → 4 → 4`

---

## 💡 Approach

I used two pointers:

- `p1` → points to the current node of `list1`
- `p2` → points to the current node of `list2`
- A dummy node is used to make building the merged list easier.

### Steps

1. Create a dummy node and keep a pointer `d` to the current end of the merged list.
2. Compare the values pointed to by `p1` and `p2`.
3. Attach the smaller node to the merged list.
4. Move the corresponding pointer forward.
5. Continue until one list becomes empty.
6. Attach the remaining nodes from the other list.
7. Return `dummy.next` as the head of the merged list.

---

## 🧠 What I Learned

Today's problem helped me understand how two sorted linked lists can be merged efficiently using pointers.

The key idea is simple: because both lists are already sorted, I don't need to compare every element with every other element. I only need to compare the current nodes and choose the smaller one.

I also got more comfortable with using a **dummy node**, which makes linked-list problems cleaner by avoiding special cases for the first node.

---

## ⏱️ Complexity

### Time Complexity
`O(n + m)`

Where:
- `n` = number of nodes in the first list
- `m` = number of nodes in the second list

Each node is visited only once.

### Space Complexity
`O(1)`

No additional data structure is required apart from a few pointers.

---

## 🎯 Takeaway

When the input already has useful structure, take advantage of it.

Instead of doing extra work, use what the problem has already given you — in this case, the fact that both linked lists are sorted.
