---
category: data structure
url_path: '/stack'
title: "Stack in Array"
type: 'ds'

layout: null
---

## Stack
- Stack implements a **Last-in, First-out** or **LIFO** policy.
- It's also called as **First-in, Last-out** or **FILO** policy.
- *Insert* operation → **PUSH**
- *Delete* operation → **POP**

Think of a stack of books. You only have an access to the book on the top and you need to remove(pop) it to grab the next book.
So in Stack, delete operation removes the most recently added item in the set; hence it is called last-in, first-out.

<img src="/assets/images/ds/stack-array-books.png" alt="stack of plates" width="600px" height="300px" /><br/>
<a href="https://www.vectorstock.com/royalty-free-vector/paper-sticker-on-stylish-background-stack-of-books-vector-16581812">Vector image by VectorStock / Anastasia8</a>

### empty()
```cpp
bool empty()
{
  return top == 0;
}
```

### push(x)
```cpp
void push(int val)
{
  if (top == capacity)
  {
    cout << "Overflow...";
    return;
  }

  top += 1;
  stack[top] = val;
}

```

### pop()
```cpp
int pop() 
{
  if(empty())
  {
    cout << "Underflow...";
    return -1;
  }
  else
  {
    top -= 1;
    return stack[top + 1];
  }
}
```

## Reference
- Introduction to Algorithms, 3rd Edition (CLRS)