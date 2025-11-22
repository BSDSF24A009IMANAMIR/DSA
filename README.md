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
