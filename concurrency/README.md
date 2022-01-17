# Effective in Java

##  Overview (/index)
    
##  Item 78 - Synchronize access to shared mutable data

- The synchronized keyword ensures that only a single thread can execute a method or block at one time. 
- This view is correct, but it’s only half the story.
- The language specification guarantees that reading or writing a variable is
  atomic unless the variable is of type long or double
- You may hear it said that to improve performance, you should dispense with
  synchronization when reading or writing atomic data.
  - This advice is dangerously wrong.
- **Synchronization is required for reliable communication between threads as well as for mutual exclusion.**
- **Do not use Thread.stop**
- 