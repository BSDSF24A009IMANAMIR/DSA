# DATA STRUCTURES IN C++

This repository contains a **template-based data structures** implemented in C++.  
It allows basic operations using data structures and can work with any data type (int, float, string, etc.).

---

## 🌟 Day 1 Implementation – Linear Singly Linked List (LSLL)
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

```
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

```
# 🌟 Day 3 – Doubly Linked List (DLL)

## ✅ Features Implemented Today
- Insert at **head**  
- Insert at **tail**  
- Remove a node by value  
- Search for a value  
- Update a specific value  
- Count total nodes  
- Display the list  
- Proper constructor & destructor (safe memory cleanup)

---

## 📘 Example Usage
```cpp
#include <iostream>
#include "DLL.h"

int main() {
    DLL<int> list;

    list.insertAtHead(10);
    list.insertAtTail(20);
    list.insertAtTail(30);
    list.display();   // Output: 10 20 30

    list.remove(20);  // deletes 20
    list.display();   // Output: 10 30

    std::cout << "Found 30? " << list.search(30) << std::endl;

    list.update(30, 99);
    list.display();   // Output: 10 99

    std::cout << "Total nodes: " << list.countNodes() << std::endl;

    return 0;
}
```

