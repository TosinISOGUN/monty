# C - Stacks, Queues - LIFO, FIFO
## Synopsis
This is a ***ALX Holberton School*** project, it is a basic `monty` `bytecode interpreter` that executes the instructions using stacks or queues implemented with doubly linked lists. This project is to be done in teams of two people.

## Monty Interpreter
A language interpreter made in the C programming language to manage stacks and queues (LIFO and FIFO). The aim is to interpret Monty bytecodes files. [Monty](http://montyscoconut.github.io/) is a language that aims to close the gap between scripting and programming languages.

## Requirements
<img src="https://alx-apply.hbtn.io/brand_alx/share_image_2019.jpg" width="300" height="100" />

- Allowed editors: `vi`, `vim`, `emacs`.
- Compilation is done on **Ubuntu 20.04 LTS** using `gcc`, using the options `$ gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty9.`
- Coding Style;
  - Betty Style, It will be checked using [betty-style.pl](https://github.com/holbertonschool/Betty/blob/master/betty-style.pl) and [betty-doc.pl](https://github.com/holbertonschool/Betty/blob/master/betty-doc.pl).
- No more than 5 functions per file.
- A README.md file, at the root of the folder of the project is mandatory.
- No more than 5 functions per file.
- The prototypes of all functions should be included in the header file called [monty.h](https://github.com/TosinISOGUN/monty/blob/main/monty.h)
- Usage of a maximum of one global variable.
- **Here's the data structure used for this project;**
```C
/**
 * struct stack_s - doubly linked list representation of a stack (or queue)
 * @n: integer
 * @prev: points to the previous element of the stack (or queue)
 * @next: points to the next element of the stack (or queue)
 *
 * Description: doubly linked list node structure
 * for stack, queues, LIFO, FIFO
 */
typedef struct stack_s
{
        int n;
        struct stack_s *prev;
        struct stack_s *next;
} stack_t;

/**
 * struct instruction_s - opcode and its function
 * @opcode: the opcode
 * @f: function to handle the opcode
 *
 * Description: opcode and its function
 * for stack, queues, LIFO, FIFO
 */
typedef struct instruction_s
{
        char *opcode;
        void (*f)(stack_t **stack, unsigned int line_number);
} instruction_t;
```
## Compilation
To compile this project, you can use the following command:
```Shell
$ make
```

## Allowable opcodes and what they do;
| opcode | functionality |
| --- | --- |
| push	| add element to the 'top' of stack and 'end' of queue. |
| pop	| remove element from 'top' of stack and 'end' of queue. |
| pall	| print every member of the structure. |
| pint	| prints the member value at the top of stack. |
| swap	| swaps the order of the 1st and 2nd elements in stack. |
| add	| add top two member values. |
| sub	| subtract the top element from the 2nd top element. |
| div	| divide the 2nd element by the top element. |
| mul	| multiply the top two elements of the stack. |
| mod	| the remainder when the 2nd element is divided by the top element. |
| comment	| there is the ability to parse comments found in bytecode ->'#'. | 
| pchar	| print character at the top of the stack. |
| pstr	| print the character at the top of the stack. | 
| rotl	| moves element at the top to the bottom of the stack. |
| rotr	| the bottom of the stack becomes the top. |
| queue, stack	| toggles the doubly link list implementation style. |
| nop	| opcode should do nothing. |

**Examples:** **`$ cat opcodetestfile.m`**

`push 1`

`push 2`

`push 3`

`pall`

`$ ./montyfile opcodetestfile.m`

`3`

`2`

`1`

`$`

## Exit Status
Exits with status `EXIT_FAILURE`

## Authors & Credits
- [Oluwatomisin ISOGUN](https://@github.com/TosinISOGUN)
- [Adeoye Abisola](https://@github.com/Biswealth1)

> Thank you for reading through our README documentation.
