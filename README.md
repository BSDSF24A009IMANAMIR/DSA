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
# 🌟 Day 3 Implementation – Doubly Linked List (DLL)


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
## 🌟 Day 4 Implementation – Circular Doubly Linked List (CDLL)

Today’s implementation introduces a **Circular Doubly Linked List**, where each node points both forward and backward, and the last node connects back to the first node.

---

### ✅ Features Implemented

- Insert at **head**
- Insert at **tail**
- Remove a node by value
- Search for a value
- Update a value
- Count total nodes
- Display entire circular list
- Fully working **constructor & destructor** (complete cleanup of circular nodes)

---

### 📘 Example Usage – CDLL

```cpp
#include <iostream>

int main() {
    CDLL<int> list1;
    list1.insertAtHead(20);
    list1.insertAtHead(10);
    list1.insertAtTail(30);
    list1.insertAtTail(40);
    list1.insertAtTail(50);

    list1.display();  // Output: 10 20 30 40 50

    CDLL<int> list2;
    list2.insertAtHead(15);
    list2.insertAtHead(25);
    list2.insertAtTail(80);
    list2.insertAtTail(90);
    list2.insertAtTail(100);

    list2.display();  // Output: 25 15 80 90 100

    CDLL<int> list3;
    list3.merge(list1, list2);   // Will be implemented in next update
    list3.display();

    return 0;
}
```
## 🌟 Day 5 Implementation – Stack (Array-Based)

Today’s implementation introduces a **template-based Stack** using a **dynamic array**.  
It supports safe memory handling, copy semantics, and all core stack operations.

---

### ✅ Features Implemented
- Push (add element to top)
- Pop (remove top element)
- Stack Top (view last pushed element)
- Check if stack is **full**
- Check if stack is **empty**
- Copy Constructor
- Assignment Operator
- Destructor (safe cleanup)
- Get current size

---

## 📘 Example Usage
```cpp
#include <iostream>
#include "Stack.h"
using namespace std;

int main() {
    Stack<int> st(5);   // stack of size 5

    st.Push(10);
    st.Push(20);
    st.Push(30);
    st.Push(40);

    cout << "Top element: " << st.Stacktop() << endl;  
    // Output: 40

    cout << "Popped: " << st.Pop() << endl;  
    // Output: 40

    st.Push(99);
    cout << "New Top: " << st.Stacktop() << endl;  
    // Output: 99

    cout << "Current Size: " << st.getCurrentSize() << endl;  
    // Output: 4

    return 0;
}
```

