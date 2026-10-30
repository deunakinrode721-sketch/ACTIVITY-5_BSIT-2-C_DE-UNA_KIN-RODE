# Stacks and Queues: Array vs. Linked List

## Description
This Python program demonstrates four data structures: an array-based stack, a linked-list stack, a circular array queue, and a linked-list queue. It includes a menu-driven test program, underflow and overflow checks, a balanced-parentheses checker, and a FIFO print-queue simulation.

## Files
- `array_stack.py` — fixed-capacity stack with `push`, `pop`, `peek`, `is_empty`, and `is_full`.
- `linked_stack.py` — linked-list stack with the same stack operations and no fixed capacity.
- `array_queue.py` — circular fixed-capacity queue with `enqueue`, `dequeue`, `peek_front`, `is_empty`, and `is_full`.
- `linked_queue.py` — linked queue with head and tail references.
- `main.py` — menus, structure tests, balanced-parentheses exercise, and print-queue exercise.
- `analysis.md` — written answer to the analysis question.

## Requirements
Python 3. Run the files from the same folder. No third-party packages are required.

## How to Run
Open a terminal in this folder and enter:

```bash
python main.py
```

Choose **Use a data structure**, select one of the four implementations, and follow the operation menu. For the array implementations, enter a capacity when prompted; pressing Enter uses the default capacity of 5. Choose the balanced-parentheses or print-queue options to run the application exercises.

## Error Handling
Popping or peeking at an empty stack, or dequeuing or peeking at an empty queue, raises an underflow exception with a descriptive message. Adding to a full array structure raises an overflow exception. The menu catches these errors and displays them.

## Example Tests
- Array stack: choose capacity `2`, pop while empty to see underflow, then push three items to see overflow.
- Circular array queue: choose capacity `3`, enqueue `A`, `B`, `C`, dequeue twice, then enqueue `D` and `E` to demonstrate wrap-around.
- Balanced parentheses: try `{[()]}` (balanced) and `([)]` (not balanced).
- Print queue: enter multiple job IDs and page counts; jobs print in the same order they were enqueued.

## Complexity Notes
Stack push/pop and linked queue enqueue/dequeue take O(1) time. The array queue uses circular indexing and a size counter to distinguish full from empty.
