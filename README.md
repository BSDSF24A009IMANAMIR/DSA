# Singly Linked List (Template-Based) in C++

This repository contains a **template-based Singly Linked List (LSLL)** implemented in C++.  
It allows basic linked list operations and can work with any data type (int, float, string, etc.).

---

## 🌟 Features (First Day Implementation)

- Insert at head and tail  
- Display the linked list  
- Template-based for generic data types  

> More operations like insertBefore, insertAfter, remove, search, and update will be added gradually in future commits.

---

## 📘 Example Usage

```cpp
#include <iostream>
#include "LSLL.h" // if separated into a header

int main()
{
    LSLL<int> list;
    list.insertAtHead(10);
    list.insertAtTail(20);
    list.insertAtTail(30);
    list.display();   // Output: 10 20 30

    return 0;
}

## 🌟 Day 2 Implementation – Circular Singly Linked List (CSLL)

**Features:**
- Insert at head and tail
- Insert before a specific key
- Insert after a specific key
- Remove head, tail, or a specific node
- Search for a value
- Display the list (shows circular structure)
- Count total nodes

> Future updates: removing duplicates, reversing the list, sorting, etc.

---

### 📘 Example Usage – CSLL

```cpp
#include <iostream>
#include "CSLL.h"

int main() {
    CSLL<int> list;

    // Day 2 Operations
    list.insertAtHead(10);
    list.insertAtTail(20);
    list.insertAtTail(30);
    list.insertAtTail(40);
    list.insertAtTail(20);  // duplicate

    list.display(); // Output: 10 -> 20 -> 30 -> 40 -> 20 -> (back to head)
    std::cout << "Total nodes: " << list.countNodes() << std::endl;

    list.removeHead();
    list.removeTail();
    list.display(); // Output: 20 -> 30 -> (back to head)

    return 0;
}
